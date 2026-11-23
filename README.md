# Defus · דפוס

Cite as: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24458153.svg)](https://doi.org/10.5281/zenodo.24458153) (Zenodo; this DOI always points to the newest release)

A prototype portal for discovering open scans of printed Hebrew books and Judaica,
1469–1920, gathered from the libraries that hold them.

**Site:** https://openseforim.org/defus/

Each entry is an *edition*. It lists every known scanned copy (HathiTrust, Internet
Archive, Bavarian State Library / MDZ, UB Frankfurt, National Library of Israel),
with pages, resolution and rights, and marks the best copy: open IIIF images, open
rights, highest resolution.

## What is here

| Path | What |
|---|---|
| `index.html` | The whole site: search, filters, timeline, edition panel (plain HTML/CSS/JS) |
| `data/editions.json` | Works, editions and copies shown on the site (compact format v3) |

Cover images load directly from the Internet Archive and the Bavarian State
Library. The **Viewer** link opens a copy in Universal Viewer where the library
allows outside viewers to load its IIIF manifests (Internet Archive, MDZ).

## Status

A prototype with all in-scope records of the inventory so far (22-Nov-2026): 31,656 works in
41,506 editions (67,632 scanned copies; single periodical issues and known
manuscripts left out). Volumes of one set are one edition; editions are grouped
into works by uniform titles, a list of canonical works and matching title and
author in Hebrew or Latin letters, ignoring plene/defective spelling
(נופת = נפת). Works or editions, cards or list. The inventory, its harvesters and the build scripts are in a separate
(private) repository, `hebrew-print-inventory`: `portal/export_sample.py`
writes the data, `portal/build_site.py` writes this site.

Known limits: copies of one edition are grouped by catalogue numbers and by
matching title, place and year, so some groups are wrong or incomplete; about
half of the printing places are not yet normalized; HathiTrust-only editions
have no cover (HathiTrust images are behind a bot check).

## Data and rights

The catalogue data comes from the holding libraries' open metadata (CC0 for MDZ,
UB Frankfurt and HathiTrust; Internet Archive item metadata; NLI Open Library API).
The scans stay with the libraries; rights are per copy and shown on the site.

## Licence

The catalogue data as compiled here (works, editions, grouping) and the site: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) (see `LICENSE`), © 2026 Ezra Brand. The source metadata is open (CC0 for MDZ, UB Frankfurt and HathiTrust; Internet Archive item metadata; NLI Open Library API). The scans stay with the libraries; rights are per copy.
