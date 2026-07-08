# Mapping Infrastructure Disparities in Douala and Yaoundé: A Geospatial Analysis of Electricity, Water, and Road Access

Satellite- and open-data-based analysis of residential infrastructure quality gaps across districts in Douala and Yaoundé, Cameroon — covering electricity, water, and road accessibility.

## Overview

Rapid, unplanned urbanization in Cameroon's two largest cities has produced uneven infrastructure access at the district level. National statistics report electricity and water access at the country level only, masking significant intra-city disparities. This project combines satellite imagery and open geospatial data to estimate infrastructure access at a finer spatial resolution (13 districts / *arrondissements*) and identify distinct district typologies based on multidimensional infrastructure profiles.

**Status:** In progress | Mid-project presentation: University of Orléans DeepLearn Summer School, July 2026

## Study Area

| City | Districts (Arrondissement) | Admin Level |
|---|---|---|
| Douala (Wouri) | 6 | ADM3 |
| Yaoundé (Mfoundi) | 7 | ADM3 |

## Data Sources

| Domain | Source | Description |
|---|---|---|
| Electricity proxy | NASA VIIRS-DNB (via Google Earth Engine) | Nighttime light intensity as a proxy for electrification |
| Roads | OpenStreetMap (via UN OCHA HDX) | Road network density, surface type |
| Water | OpenStreetMap (via UN OCHA HDX) | Water point and waterway proximity |
| Administrative boundaries | UN OCHA HDX (COD-AB, sourced from Institut National de Cartographie) | District-level boundaries |

All sources are open and freely accessible.

## Methodology

1. **Spatial preprocessing** — extract and standardize district boundaries; compute zonal statistics (nighttime light, road density, water proximity) per district
2. **Dimensionality reduction (PCA)** — combine electricity, water, and road indicators into a composite infrastructure index
3. **Clustering (K-Means)** — group districts into infrastructure typologies (e.g., "well-served", "moderate", "underserved")
4. **Visualization** — interactive dashboard (Tableau Public)

## Repository Structure

```
├── data/
│   ├── raw/          # Source downloads (not tracked in git)
│   └── processed/    # Cleaned, analysis-ready datasets
├── notebooks/        # Analysis notebooks
├── scripts/          # Reusable processing scripts
├── outputs/
│   └── figures/      # Maps and charts
└── docs/
    └── project_plan.md
```

## Tech Stack

`Python` (geopandas, rasterio, scikit-learn) · `Google Earth Engine` · `Tableau Public`

## About

Dongju — M.Sc. Data Science candidate, background in international development (incl. UNFPA)

---
*This project is part of an ongoing portfolio combining geospatial data science with international development applications.*
