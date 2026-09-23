# NYC Crash Data Cleaning

This repository contains a reproducible Quarto analysis for cleaning New York City motor-vehicle crash records from June 30 through July 6, 2024.

## Repository layout

- `homework4.qmd` - source analysis
- `homework4.pdf` - rendered report
- `data/nyc_crashes_2024-06-30_to_2024-07-06.csv` - crash records
- `data/nyc_modified_zip_codes.csv` - valid NYC modified ZIP codes
- `data/nyc_modified_zip_boundaries.geojson` - ZIP boundary geometry used for reverse lookup
- `data/nyc_borough_boundaries.geojson` - borough boundary geometry used for reverse lookup

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
quarto render homework4.qmd
```

Quarto and a PDF engine such as Tectonic must be installed separately.

## Data sources

The files were downloaded on September 23, 2026 from official NYC Open Data datasets:

- [Motor Vehicle Collisions - Crashes](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95)
- [Modified ZIP Code Tabulation Areas](https://data.cityofnewyork.us/Health/Modified-Zip-Code-Tabulation-Areas-MODZCTA-/pri4-ifjk)
- [Borough Boundaries](https://data.cityofnewyork.us/City-Government/Borough-Boundaries/gthc-hcne)

The crash dataset is revised over time, so row counts can differ from older rendered reports.

