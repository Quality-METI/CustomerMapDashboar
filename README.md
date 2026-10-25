# Customer Territory Dashboard — Lite build

This build is optimized for browser performance using Leaflet Canvas rendering, debounced search, reduced customer fields, and simplified territory boundaries.

## Run locally
Serve this folder using any static web server; opening index.html directly may block JSON fetches.

## Important data warning
The customer dataset still contains customer names, SAP customer numbers, and sales assignment details. Do not publish this repository publicly unless your company has explicitly approved public disclosure. The editor audit CSV is intentionally excluded from this Lite archive. GitHub Pages is public by default; a private repository does not automatically make the published website private.


## Map appearance update
- Basemap selector: Dark, Satellite, Light, and Streets.
- Territory borders use a dark casing plus bright cyan/orange outlines for visibility.
- To update an existing GitHub repository, replace `index.html` with this version and commit the change. Keep the existing `data` folder unless replacing it with the matching optimized data package.
- Tile layers require an internet connection. Satellite tiles are provided by Esri; dark/light tiles by CARTO; street tiles by OpenStreetMap.
