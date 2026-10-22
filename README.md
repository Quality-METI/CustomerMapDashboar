# Customer Territory Dashboard

Static Leaflet dashboard for GitHub Pages.

## Files
- `index.html`: dashboard UI and filters.
- `data/customers.json`: customer points and public-safe attributes (phone numbers and street addresses omitted).
- `data/territories.geojson`: territory polygons, with Region/Branch enriched from Structure when TerrID matches.
- `data/audit_review.csv`: preliminary records requiring review.

## Publish
1. Create a GitHub repository.
2. Upload all files/folders in this project.
3. Repository Settings → Pages → Deploy from a branch → `main` / root.
4. Open the generated Pages URL.

## Important security note
GitHub Pages is public static hosting. Any file committed here is publicly downloadable. This prototype excludes customer phone numbers and street addresses, but still contains customer names/codes, SAP customer numbers, territories, and sales assignments. Do not publish this dataset unless company policy authorizes it. The audit panel is not an authenticated private editor area; real editor-only access requires a backend/authenticated service or separate private deployment.

## Data rules
- Structure sheet is authoritative for Region and BranchName by TerrID.
- Shape File supplies geometry and TerrName.
- Customer sheet supplies assigned TerrID, location, code/name, lists and target.
- Missing shape and name mismatch are flagged, not auto-corrected.
- `Location` is parsed as latitude, longitude based on sample rows. Verify coordinate convention before production.
