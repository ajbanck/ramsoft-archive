# Verifying this archive

`mirror/` was rebuilt from Internet Archive captures. Nothing below requires
trusting this repository: each check re-derives the archive's claims from the
files themselves, or from the Internet Archive directly.

Run from the repository root.

None of the following requires trusting this repository. Run from the repo root.

**Every file matches its recorded hash** — offline, no network:

```sh
awk -F'\t' '!/^#/{print $2"  mirror/"$1}' PROVENANCE.tsv | shasum -a 256 -c
```

**Every archive is structurally intact:**

```sh
find mirror -name '*.zip' -print0 | xargs -0 -n1 unzip -tqq
find mirror -name '*.tgz' -exec sh -c 'tar tzf "$1" >/dev/null || echo "FAIL $1"' _ {} \;
```

**Every file's origin `ETag` agrees with the bytes on disk.** Apache 1.3 encodes
`inode-size-mtime`, so each ETag independently carries the size and modification
time the origin server reported — two fields that would have to be forged in
agreement:

```sh
awk -F'\t' '!/^#/{split($7,e,"-"); print e[2], e[3], $5, $3, $1}' PROVENANCE.tsv |
python3 -c '
import sys, datetime
bad = 0
for line in sys.stdin:
    sz, mt, size, mtime, path = line.split(None, 4)
    if int(sz, 16) != int(size):
        print("size", path.strip()); bad += 1
    t = datetime.datetime.fromtimestamp(int(mt,16), datetime.timezone.utc)
    if t.strftime("%Y-%m-%dT%H:%M:%SZ") != mtime:
        print("mtime", path.strip()); bad += 1
print(f"{bad} mismatches")'
```

**Any file can be re-fetched from the Internet Archive and compared.**
`wayback_capture` is the exact capture this copy came from, usable directly in a
replay URL:

```sh
f=www.ramsoft.bbk.org/software/mtzx233.zip
read -r cap sha < <(awk -F'\t' -v p="$f" '$1==p{print $4, $2}' PROVENANCE.tsv)
curl -s "https://web.archive.org/web/${cap}id_/http://$f" | shasum -a 256
echo "$sha  (recorded)"
```

Expected results: 192 of 192 hashes match; no archive fails; 0 ETag mismatches;
re-fetches reproduce the recorded hash. The one known exception is recorded in
the `cdx_digest_check` column — `emul/rspec-b6-{i686,k6,pent}.zip` do not match
the digest the CDX *index* holds, though they are valid, complete, distinct
archives whose ETag size matches the bytes on disk, placing the discrepancy in
the index rather than the content. They are flagged, not silently accepted.
