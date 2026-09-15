# Flip-Pins pages from oshchip.org (archival mirror)

Live copy: **<https://mith.ro/oshchip-flip-pins/>** (also reachable as
<https://mithro.github.io/oshchip-flip-pins/>, which redirects there)

This repository is an archival mirror of the **Flip-Pins** pages from
[oshchip.org](http://oshchip.org/), Philip Freidin's OSHChip site. The site
has been intermittently unavailable and its domain registration lapses on
2026-11-07, so this copy exists to keep the product documentation reachable.

Flip-Pins were invented by **Philip Freidin** (Fliptronics / OSHChip).
**All content here is his copyright** and is mirrored with attribution; it is
not relicensed and no open-source licence applies to it.
[wafer.space](https://wafer.space/) now manufactures Flip-Pins under licence
from him.

## Mirror dates

- Original site fetch: **2026-09-14**.
- Re-fetched on **2026-09-15**: the FontAwesome web fonts under
  `assets/fonts/` (referenced only from the stylesheet and missed by the
  original crawl). All Flip-Pins downloads (datasheet, STEP models, ECAD
  library archives) and the product pages were re-checked against the live
  site on 2026-09-15 and matched byte for byte.

## What is here

| Path | Contents |
|---|---|
| [`products/Flip-Pins_Product.html`](https://mithro.github.io/oshchip-flip-pins/products/Flip-Pins_Product.html) | Main Flip-Pins product page |
| [`products/Soldering_Flip-Pins.html`](https://mithro.github.io/oshchip-flip-pins/products/Soldering_Flip-Pins.html) | Illustrated soldering guide |
| [`products/Flip-Pins_Altium.html`](https://mithro.github.io/oshchip-flip-pins/products/Flip-Pins_Altium.html), [`Flip-Pins_Kicad.html`](https://mithro.github.io/oshchip-flip-pins/products/Flip-Pins_Kicad.html), [`Flip-Pins_Eagle.html`](https://mithro.github.io/oshchip-flip-pins/products/Flip-Pins_Eagle.html) | ECAD symbol and footprint pages |
| [`docs/Flip-Pins-XX_REV_A.pdf`](https://mithro.github.io/oshchip-flip-pins/docs/Flip-Pins-XX_REV_A.pdf) | Datasheet (mechanical drawing, recommended footprint) |
| `docs/Flip-Pins_one_pin.step`, `docs/Flip-Pins_one_pin_with_aligner.step` | STEP models |
| `products/Flip-Pins_*_Symbols_and_Footprints_2016_09_12.zip` | Altium, KiCad and Eagle library archives |
| `images/` | All product and assembly photos |

The rest of the site (OSHChip product pages, docs, FAQ, about) is included
as captured, so that navigation links keep working. The original site home
page is at `home.html`; the repository root `index.html` redirects to the
Flip-Pins product page.

## Changes from the original

- Absolute `http://oshchip.org/...` and root-relative links in the HTML were
  rewritten to relative paths so the pages work when served from a subpath.
  The HTML is otherwise unchanged.
- The site's `assets/js/*` files (jQuery, Modernizr, html5shiv, respond,
  scripts.min.js) were already 404 on the origin and are not included; the
  pages render fine without them.
- `oshchip.org` DNS round-robins five addresses, one of which is a parked
  host that answers 404. Pin a GitHub Pages address when fetching from it:
  `curl --resolve oshchip.org:80:185.199.110.153 http://oshchip.org/...`
