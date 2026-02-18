# Sample data — Chile COD-AB 2021

Boundaries downloaded from [HDX Chile COD-AB](https://data.humdata.org/dataset/cod-ab-chl).

| Level | Count | Use |
|-------|-------|-----|
| Admin 1 | 16 regions | Region boundaries |
| Admin 2 | 56 provinces | Province boundaries |
| Admin 3 | 345 comunas | City/comuna boundaries for spatial joins |

**Formats:** SHP, GeoJSON (HDX source). Sample: GeoPackage.

| File | Description |
|------|-------------|
| chl_admin3.gpkg | Admin 3 (comuna) boundaries from HDX |
| locode_mapping.gpkg | Comuna → UNLOCODE mapping with geometry (one row per comuna). Spatial format for joins. |

**Comuna ↔ locode matching:** Spatial join (point-in-polygon) + nearest fallback (~25 km). Only assignments with an exact or partial name match are kept; prefer no match over incorrect. Source: `notebook/exploration.ipynb`.
