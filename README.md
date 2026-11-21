# Defus · דפוס

A prototype portal for discovering open scans of printed Hebrew books and Judaica,
1469–1920, gathered from the libraries that hold them.

**Site:** https://ezrabrand.github.io/defus/

Each entry is an *edition*. It lists every known scanned copy (HathiTrust, Internet
Archive, Bavarian State Library / MDZ, UB Frankfurt, National Library of Israel),
with pages, resolution and rights, and marks the best copy: open IIIF images, open
rights, highest resolution.

## What is here

| Path | What |
|---|---|
| `index.html` | The whole site: search, filters, timeline, edition panel (plain HTML/CSS/JS) |
| `data/editions.json` | The sample of editions shown on the site |

Cover images load directly from the Internet Archive and the Bavarian State
Library. The **Viewer** link opens a copy in Universal Viewer where the library
allows outside viewers to load its IIIF manifests (Internet Archive, MDZ).

## Status

A prototype with a sample of 11,150 editions from an inventory of over 100,000
records. The inventory, its harvesters and the build scripts are in a separate
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
