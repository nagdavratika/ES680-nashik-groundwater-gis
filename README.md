# Spatiotemporal Assessment of Groundwater Level Fluctuations in Nashik District (2005–2019)

Course project for **ES 680: GIS for Environmental Planning and Management**, Centre of Studies in Resources Engineering (CSRE), IIT Bombay — under the guidance of Prof. Anil Kumar Dikshit.

## Overview

An integrated GIS and remote sensing analysis of how land-cover change (urbanisation vs. vegetation) affects groundwater recharge in Nashik District's fractured basaltic aquifers, comparing 2005 and 2019.

## Key findings

- **Dense-vegetation zones recharge ~48% more effectively per monsoon season than built-up zones** (mean seasonal recharge shift: 7.74 m vs. 5.22 m) — even though 2019 received ~25% less monsoon rainfall than 2005, showing surface permeability, not just rainfall, drives recharge efficiency.
- **The recharge disparity between the best- and worst-performing land-cover classes widened ~4x** over the 14-year period (0.51 m → 2.03 m).
- **All land-cover classes show a net decadal water-table drop exceeding 5 m**, confirming a district-wide sustainability deficit — even the most efficient (vegetated) recharge zones aren't keeping pace with cumulative abstraction.

## Data sources

- **Landsat 8 OLI/TIRS** (2019, 30m) — USGS EarthExplorer
- **MODIS/Aqua MOD09GQ** (2005, 250m) — NASA LP DAAC / AppEEARS
- **CGWB groundwater well records** (80 monitoring stations, pre/post-monsoon 2005 & 2019) — India-WRIS
- **Administrative boundary** — Survey of India / LGD

## Methods

NDVI derived from both sensors (harmonised via zonal-mean analysis to avoid cross-resolution pixel-count bias); groundwater recharge (Δh) computed from seasonal well-level differences and interpolated to continuous surfaces using **Empirical Bayesian Kriging (EBK)**; recharge surfaces intersected with NDVI-derived land-cover zones via Zonal Statistics. Full technical workflow in the report, Section 7–8.

Processed in **ArcGIS Pro**.

## Repo contents

```
report/
  ES680_Project_Report_25M0333.pdf   Full report with methodology, maps, tables, references
data/                                  (not included — see note below)
maps/                                  (exported map figures, if included)
```

**Note on data:** raw CGWB well records, satellite imagery, and ArcGIS project files are not included in this repo (large file sizes, and satellite data redistribution terms). See the report's Data Sources section (5) for direct links to obtain them.

## Citation

Nagda, V. (2026). *Spatiotemporal Assessment of Groundwater Level Fluctuations and its Impact on Agricultural Patterns in Nashik District (2005–2019)*. ES 680 Course Project, Centre of Studies in Resources Engineering, Indian Institute of Technology Bombay.
