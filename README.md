# RAMSOFT archive

Preservation mirror of **`www.ramsoft.bbk.org`**, the site of **RAMSOFT**
(*World Wide Ramsoft* / *WWR*), an Italian ZX Spectrum demogroup. The site is
offline; the domain now resolves to an unrelated parking page.

192 files, recovered from the Internet Archive as the bytes the origin server
sent, plus one later release found elsewhere. Notable contents: the **TZX**,
**CSW** and **RZX** format specifications, **MakeTZX** (tape-audio to `.tzx`
converter), **RealSpectrum** (RAMSOFT's Spectrum emulator), demoscene
productions and hardware notes.

## Layout

```
mirror/www.ramsoft.bbk.org/   the site as captured, 192 files
extra/                        RAMSOFT material from a different source
MANIFEST.timestamps           origin-server mtimes (git does not keep them)
PROVENANCE.tsv                per file: sha256, dates, origin headers
NOTICE.md                     copyright and distribution terms, quoted
VERIFY.md                     commands to re-derive every claim made here
.provenance/                  the CDX index and selection list used to rebuild
```

Nothing under `mirror/` has been added, renamed, reformatted or corrected. Its
faults are preserved too: of the 192 internal references in the mirrored pages,
12 point at files no Internet Archive capture contains. A further 3 point at
the RZX recordings, which *were* captured but are deliberately not hosted here —
`NOTICE.md` gives their Internet Archive URLs. Commentary lives outside it.

## Contents of `mirror/`

| | |
|---|---|
| 28 HTML pages | including the format specifications |
| `software/` (13) | MakeTZX and CSW releases |
| `emul/` (25) | RealSpectrum builds, ROMs, utilities |
| `demos/` (66) | demoscene productions and party releases |
| `images/` (47) | site graphics and screenshots |
| `tech/` (9) | hardware and format notes |

### Releases, labelled as the site's own download table labels them

| File | Site label | Dated |
|---|---|---|
| `software/mtzx233.zip` | MakeTZX v2.33, MSDOS | 01/08/03 |
| `software/mtzx233w.zip` | MakeTZX v2.33, Windows | 01/08/03 |
| `software/mtzx231.tgz` | MakeTZX v2.31, Linux x86 | 02/07/01 |
| `software/ami-mtzx231.zip` | MakeTZX v2.31, Amiga (68000) | 04/07/01 |
| `software/mtzx1021b.tgz` | "OLD MakeTZX" v1.02.1, Linux | 18/03/98 |
| `software/mtzx1021s.zip` | Source code v1.02.1 | 10/12/98 |
| `software/mtzxwgui050beta.zip` | WinGUI v0.50 beta | 04/07/01 |
| `software/gui012.zip` | DOS GUI v0.12 | 23/01/99 |
| `software/csw200.zip` | CSW v2.00 | 01/08/03 |
| `software/csw130.tgz` | CSW v1.30 | 05/07/99 |
| `software/ami-csw130.zip` | CSW v1.30, Amiga | 13/07/99 |
| `emul/csdpmi5b.zip` | cwsdpmi r5 | undated |

Source is present for v1.02.1 only. The manual (`mtzxman.htm`) records v2.00 as
a "totally rewritten C++ engine"; no v2.xx source appears in this archive.

`software/mtzx230.tgz` and `software/csdpmi4b.zip` are present in the mirror but
not linked from `maketzx.html` — superseded files still sitting on the server
when it was crawled. Their version numbers are inferred from their filenames;
unlike the table above, nothing on the site labels them.

`emul/` holds RealSpectrum builds `r14b`, `b13`, `b10` and `b6` across
CPU-specific variants (AMD, i686, Pentium) in both DOS and Win32 lines, plus
`rspec-roms.zip`, HDF and network utilities.

### Format specifications

| Page | Specifies |
|---|---|
| `tzxform.html` | TZX, the standard ZX Spectrum tape-image format |
| `csw.html` | CSW (Compressed Square Wave) tape audio |
| `rzxform.html` | RZX input-recording format |
| `tech.html` | "Tech notebook" — hardware findings |

## `extra/`

`mtzx240b1w.zip` — MakeTZX v2.40 beta 1 for Windows. Its `maketzx.exe` contains
the string `2.40-B1` and is dated 2010-02-20.

**No `mtzx240*` URL appears in any of the 2,214 captures** the mirror was built
from, so it was not reachable on the site during the period the Internet Archive
sampled it. That is not the same as never having been published there. This copy
came from a [Spectrum Computing forum
thread](https://spectrumcomputing.co.uk/forums/viewtopic.php?t=869); it is kept
outside `mirror/` because it did not come from the site.

## How the mirror was built

Fetched with the Wayback Machine's **`id_` replay modifier**, which returns the
archived response body unaltered. Ordinary replay URLs return a processed copy
with Wayback's JavaScript injected into every page and all links rewritten; an
earlier version of this archive was built that way and was discarded.

2,214 captures were enumerated through the CDX API and one chosen per URL by
grouping captures into runs of identical content digest, which separates a file
being replaced from a file decaying at the end of the site's life. A second,
independent selection algorithm chose the same capture for every URL.

## Two dates per file

- **`origin_mtime`** — `Last-Modified` from RAMSOFT's server: when the file was
  written. Range 2000-07-28 to 2007-04-07.
- **`wayback_capture`** — when the Internet Archive crawled it: an upper bound
  on existence, driven by crawl scheduling. Range 2000-08-18 to 2008-10-28.

The mtimes carry the site's editorial history — the MakeTZX v2.33 release of
1 August 2003:

```
12:17:31Z  software/mtzx233.zip     DOS build
12:17:44Z  software/mtzx233w.zip    Windows build, 13 seconds later
12:18:46Z  mtzxman.htm              manual
12:36:55Z  maketzx.html             download page updated
```

Git does not preserve mtimes, so `MANIFEST.timestamps` records them. Dates
inside the `.zip` and `.tgz` archives survive regardless.

To restore them:

```sh
awk '$1!~/^#/{print $1, $2}' MANIFEST.timestamps |
  while read -r t p; do touch -d "$t" "mirror/$p"; done
```

## Licensing

**See [`NOTICE.md`](NOTICE.md).** This is third-party material and no licence is
granted over it here; the absence of a `LICENSE` file is intentional. MakeTZX
and RealSpectrum both permit redistribution of unmodified archives, which is
what this repository does. The CSW specification carries no terms at all.
`NOTICE.md` quotes each statement from its primary source and marks where the
reasoning rests on RAMSOFT's own characterisation rather than an independent
grant.

This archive's own files — this README, `NOTICE.md`, `PROVENANCE.tsv`,
`MANIFEST.timestamps` — are offered under CC BY 4.0.

## Takedown

If you hold rights in any material here and want it removed, open an issue.
Requests are honoured without argument.
