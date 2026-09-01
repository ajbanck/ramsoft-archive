# Notice — copyright, distribution terms, and what this archive claims

This repository is a **preservation mirror**. Nothing in `mirror/` is the work
of the person publishing it, and no licence is granted over it here. This file
records what the material itself says about its own distribution, quoted from
the mirrored documents, so you can judge for yourself rather than take an
archivist's summary on trust.

**There is deliberately no `LICENSE` file.** Adding one would assert ownership
that does not exist. GitHub reporting "no license" for this repository is
correct and intentional.

## Who made this material

**RAMSOFT** — also styled *World Wide Ramsoft* / *WWR* — an Italian ZX Spectrum
demogroup active roughly 1998–2010, whose site `www.ramsoft.bbk.org` went
offline and whose domain now resolves to an unrelated parking page. The group
is defunct and the contact addresses in these documents are dead.

## MakeTZX

From the manual (`mirror/www.ramsoft.bbk.org/mtzxman.htm`, §17 "Credits and
contact info"), quoted verbatim:

> MakeTZX is a program © 1998-2003 RAMSOFT. It comes with ABSOLUTELY NO
> WARRANTY of any kind; the authors are not liable for any damage or
> information loss caused directly or indirectly by the use of this program.
> MakeTZX can be freely distributed at the conditions that no money is required
> and the original archive and its contents are not modified. If you want to
> include MakeTZX into any software collection distributed on CDROM or any
> other electronic media, you are allowed to do it at the above conditions, but
> please inform us.

**How this archive complies.** The release archives are mirrored as unmodified
`.zip` / `.tgz` files, byte-for-byte as distributed. No money is charged. The
"please inform us" request cannot be honoured — RAMSOFT is defunct and the
contact addresses no longer function; this notice stands in its place.

Note the condition attaches to *the original archive and its contents*. Anyone
repackaging, converting or recompressing these files is outside the permission
granted above, even though mirroring them is inside it.

## The CSW specification

`mirror/www.ramsoft.bbk.org/csw.html` ("WWR - CSW technical specifications")
carries **no copyright notice, no licence, and no permission statement of any
kind**. This was verified by search, not assumed: the document contains no
occurrence of "copyright", "licence/license", "permission" or "all rights".

What it does contain is an invitation:

> Here is the CSW implementation chart for anyone who wants to use it in some
> utility or emulator (if so, please let us know).

A format specification published to encourage implementation is about as
permissive in intent as an unlicensed document gets. That is an observation
about intent, not a grant of rights.

The same page is also shipped inside `csw200.zip`. Note that the archived copy
references `wave.gif` in lowercase while the zip contains `WAVE.GIF`; DOS did
not distinguish, case-sensitive web servers do.

## RealSpectrum

From the manual (`mirror/www.ramsoft.bbk.org/rspecman.html`, §16 "License,
credits and contact info"), quoted verbatim:

> RealSpectrum is freeware. It can be freely used and distributed as long as no
> money is charged for it and the original packages, program and documentation
> are not altered in any way. If you host copies of RealSpectrum on your
> website, please keep them up to date with the most recent release and provide
> a link to the original homepage; we don't like to see obsolete releases lying
> around for ages. Before including RealSpectrum into a commercially sold media
> (such as a magazine CDROM), you must contact us first. You are not allowed to
> distribute this program together with ZX Spectrum commercial software and
> other copyright-protected material (such as games snapshots, copyrighted
> roms, etc) in any form. Disassembly, hacking and any other forms of reverse
> engineering of the program files are strictly prohibited.

**How this archive complies.** Packages are mirrored unaltered, no money is
charged, and nothing is sold. Two clauses need comment:

- *"keep them up to date … and provide a link to the original homepage"* — the
  request cannot be satisfied as written. There is no more recent release; the
  final ones are here. The original homepage is the site this repository
  mirrors, and it is gone. Preserving the last released versions is the closest
  available reading of the intent.
- *"not … together with … copyrighted roms"* — see below. RAMSOFT's own
  download page classifies the ROM bundle it shipped as *freely distributable*,
  distinguishing it from the copyrighted ROMs this clause targets.

## The system ROMs (`emul/rspec-roms.zip`)

The bundle contains ten ZX Spectrum and clone system ROMs: `48.ROM`, `128.ROM`,
`plus2.rom`, `plus3.rom`, `if1.rom`, `trdos.rom`, `pentagon.rom`,
`scorpion.rom`, `gdos.rom`, `gdos-pd.rom`.

RAMSOFT offered this file from the RealSpectrum download table on
`mirror/www.ramsoft.bbk.org/realspec.html`, described as:

> **Standard ROM files** — Freely distributable ROMs required by the emulator

So RAMSOFT drew the same distinction their licence draws — freely distributable
ROMs as against copyrighted ones — and shipped these deliberately, from the same
table as the emulator binaries.

**Stated plainly: that is RAMSOFT's characterisation, not a licence grant from
the rights holders, and this archive has not independently verified it.** For
the Sinclair ROMs it is well founded — Amstrad, which holds the Sinclair
copyrights, has long permitted their circulation with emulators. The MGT
(`gdos.rom`) and Russian-clone ROMs (`trdos.rom`, `pentagon.rom`,
`scorpion.rom`) rest on weaker footing, though `gdos-pd.rom` reads as a
public-domain variant.

The file is mirrored as RAMSOFT distributed it, together with the page stating
their claim about it. If you hold rights in any of these ROMs and disagree, see
*Takedown* below.

## The RZX recordings — withheld, and where to get them

RAMSOFT's site carried three RZX input recordings at `rzx/`, described on
`rzx.html` as demonstrations of the RZX format they designed. Each embeds a
snapshot of the game being played, so that the recording can replay:

| File | Game | Publisher |
|---|---|---|
| `myth.zip` | Myth: History in the Making | System 3 |
| `rtype.zip` | R-Type | Irem / Electric Dreams |
| `starquake.zip` | Starquake | Bubble Bus |

**These three files are not hosted in this repository.** They are the only
material from the site deliberately omitted. Everything else the site served is
here.

They remain retrievable in their original bytes from the Internet Archive
captures this mirror was built from:

```
https://web.archive.org/web/20070106083836id_/http://www.ramsoft.bbk.org/rzx/myth.zip
https://web.archive.org/web/20070106082932id_/http://www.ramsoft.bbk.org/rzx/rtype.zip
https://web.archive.org/web/20070106082900id_/http://www.ramsoft.bbk.org/rzx/starquake.zip
```

Their capture records also remain in `.provenance/cdx-all.txt`, so the omission
is documented and reversible rather than a silent gap. Three of the unresolved
internal links in the mirrored pages point at them; that is why.

**Why they are withheld.** The recordings are RAMSOFT's own work, but the
embedded snapshots are not: they are commercial games whose rights sit with
third parties. RealSpectrum's own licence, quoted above, names "games
snapshots" as material it may not be distributed alongside. Rather than argue
the point file by file — two of the three games are freely downloadable from
World of Spectrum, which lists them as "Available"; R-Type is not — this
archive applies one rule: **it does not host third-party game content.** A
uniform rule needs no per-title justification and leaves nothing to revisit.

## Other third-party material

Listed openly on RAMSOFT's own pages and mirrored as they distributed it:

| Path | As the site describes it |
|---|---|
| `emul/softcrack9.zip` | "Softcrack software (v9.2 and v9.4) and original documentation" |
| `emul/hdfutils.zip` | "Tools to read/write HDF files to/from real hard-disks (by G. Lancaster)" |
| `emul/csdpmi5b.zip` | CWSDPMI DPMI extender — see below, the one item here with an explicit redistribution grant |
| `demos/` (~78 files) | Demoscene productions by various groups, hosted by RAMSOFT as event participants and organisers |

None of these carries a distribution statement from RAMSOFT beyond the act of
hosting them. Copyright rests with the respective authors.

**CWSDPMI is the exception, and it is unambiguous.** `BIN/CWSDPMI.DOC` inside
`csdpmi5b.zip` states:

> CWSDPMI is Copyright (C) 1995-2000  Charles W Sandmann
> (sandmann@clio.rice.edu)
>
> This is release 5.  The files in this binary distribution may be
> redistributed under the GPL (with source) or without the source code
> provided: "CWSDPMI V0.90+ (r5) Copyright (C) 2000 CW Sandmann  ABSOLUTELY NO
> WARRANTY"

Mirroring the binary distribution unmodified, with that notice intact inside the
archive, satisfies the second option exactly.

## What the archivist adds, and under what terms

Everything outside `mirror/` is original work by the repository owner:
`README.md`, this notice, `PROVENANCE.tsv`, `MANIFEST.timestamps`, and anything
under `docs/`. Those files are offered under
**CC BY 4.0** (<https://creativecommons.org/licenses/by/4.0/>).

This split is why the licence question has no single answer: the mirror carries
its authors' terms, the scaffolding around it carries the archivist's.

## Provenance and integrity

`mirror/` was rebuilt from the Internet Archive Wayback Machine using the `id_`
replay modifier, which returns the archived response body **verbatim** — no
injected toolbar, no rewritten links. An earlier version of this archive used
ordinary replay URLs and consequently carried Wayback's JavaScript in every
page; that material has been discarded.

`PROVENANCE.tsv` records, per file: path, SHA-256, **origin mtime**, Wayback
capture date, size, CDX digest check, origin ETag and origin server string.

The two dates answer different questions and both are kept. The capture date is
when the Internet Archive crawled the URL — an upper bound on the file's
existence, and an artefact of crawl scheduling. The origin mtime is the
`Last-Modified` RAMSOFT's own server reported: when the file was actually
written. Origin mtimes here span 2000-07-28 to 2007-04-07 and reconstruct the
site's editorial history — for instance the MakeTZX v2.33 release of 1 August
2003, where the DOS build (12:17:31Z), the Windows build (12:17:44Z), the manual
(12:18:46Z) and the updated download page (12:36:55Z) fall in sequence across
twenty minutes.

Those mtimes are not taken on trust. The origin ran Apache 1.3, whose ETag is an
`inode-size-mtime` triple, so each response independently encodes both the
modification time and the byte count. **For all 198 URLs the ETag's mtime
matches the `Last-Modified` header exactly, and the ETag's size matches the
bytes on disk exactly.** Two header fields that would have to be forged in
agreement both confirm the stored bytes.

Three files (`emul/rspec-b6-{i686,k6,pent}.zip`) are flagged
`cdx-digest-differs`: their content hash does not match the digest the Wayback
CDX index records. They are nonetheless valid, complete, distinct zip archives,
and their origin ETag size matches the bytes on disk — so the discrepancy is in
the CDX index, not in the content. They are flagged rather than silently
accepted.

Verification performed: every archive passes `unzip -t` / `tar tzf`; every
binary's magic bytes match its extension; no file is a soft-404 error page; and
capture selection was cross-checked by a second, independent algorithm.

Git does not preserve modification times. `MANIFEST.timestamps` records the
original mtimes of the mirrored files, which span 2000 to 2008. Dates *inside*
the `.zip` / `.tgz` archives are stored byte-for-byte and survive regardless.

## No legal advice

Nothing here has been reviewed by a lawyer. The terms above are quoted from
primary sources and the compliance reasoning is the archivist's own. If you
need a legal opinion, obtain one.

## Takedown

If you hold rights in any material here and want it removed, open an issue or
contact the repository owner through their GitHub profile. Requests will be
honoured without argument — this archive exists to keep the material from
disappearing, not to contest anyone's ownership of it.
