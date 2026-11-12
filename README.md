# namastevis.in

Amit Jena's personal website. Plain HTML and one stylesheet: no framework, no build step, no trackers.

## Pages
- `index.html`: home, with the India population density map
- `work.html`, `open-source.html`, `teach.html`, `work-with-me.html`, `about.html`, `now.html`, `404.html`
- `styles.css`: all colours and type. Light values at the top, dark-mode values under `prefers-color-scheme`.

To edit a page, edit its HTML file directly. The header and footer are repeated in every page.

## The map
India as a 40 × 40 km grid (Albers equal-area), coloured above or below India's 2020 average of 447 people per km².
- Population: `ind_pd_2020_1km.tif` from namastevis/population-density-maps-india (TODO: confirm and credit the original source)
- Boundary: Survey of India outline from DataMeet (`india-soi.geojson`)
- Small crosses in the far north: cells with no population data

## Deploy on Hostinger
1. Back up the current site (hPanel → File Manager → public_html → download).
2. Upload everything here into `public_html` for namastevis.in, including the hidden `.htaccess`.
3. Keep the existing `/khel/` folder; the site links to it. `press.namastevis.in` is a subdomain and is not affected.
   Or connect this repo with hPanel's Git deployment so a push updates the site.

## Redirect namastevis.com to namastevis.in
In hPanel, open namastevis.com → Redirects, and add a permanent (301) redirect to `https://namastevis.in`,
keeping the path, so namastevis.com/about.html goes to namastevis.in/about.html.

## Later
- Writing: add Ghost (writing.namastevis.in) or Decap, then add "Writing" to the menu.
- Case studies: fill in the `<!-- Add here -->` comments in `work.html`.
