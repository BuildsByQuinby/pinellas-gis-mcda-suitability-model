# 🧭 Spatial Analysis Workflow  
**Project:** Residential Suitability Modeling – Pinellas County, FL  
**Method:** Raster-Based Multi-Criteria Decision Analysis (MCDA)  
**Software:** ArcGIS Pro  

---

# 🔍 Overview

This workflow documents the full geospatial processing pipeline used to generate a composite residential suitability index for Pinellas County, Florida.

The model integrates three spatial criteria:

1. Flood Risk (Environmental Hazard)
2. Land Use Classification (Policy Constraint)
3. Social Vulnerability Index (Socioeconomic Risk)

All variables were standardized and combined using raster-based overlay analysis.

---

# 🗂️ Step 1 — Data Acquisition

Datasets were collected from authoritative government sources:

- FEMA Special Flood Hazard Areas (SFHA)
- Pinellas County eGIS Land Use
- CDC/ATSDR Social Vulnerability Index (SVI)
- U.S. Census TIGER County Boundaries

All source metadata is documented in `/data_sources/data_sources.md`.

---

# 📐 Step 2 — Coordinate System Standardization

All layers were:

- Reprojected to:  
  **NAD 1983 StatePlane Florida West (FIPS 0902 Feet)**
- Clipped to Pinellas County boundary
- Verified for spatial alignment

This ensured consistent spatial reference prior to raster conversion.

---

# 🧱 Step 3 — Raster Conversion

All vector datasets were converted to raster format using:

- Polygon to Raster tool
- Consistent cell size
- Defined snap raster
- Uniform spatial extent

This standardization ensured pixel-level alignment across all inputs.

---

# 🎚️ Step 4 — Reclassification

Each raster layer was reclassified onto a standardized 1–5 suitability scale:

| Suitability Score | Interpretation |
|------------------|----------------|
| 1 | Very Low Suitability |
| 2 | Low Suitability |
| 3 | Moderate Suitability |
| 4 | High Suitability |
| 5 | Very High Suitability |

### Reclassification Logic

**Flood Risk**
- Floodplain areas → Lower suitability
- Non-flood zones → Higher suitability

**Land Use**
- Conservation/Restricted → Lower suitability
- Residential zoning → Higher suitability

**Social Vulnerability**
- High SVI → Lower suitability
- Low SVI → Higher suitability

---

# 🧮 Step 5 — Raster Overlay (Composite Index Calculation)

Raster Calculator was used to generate the Final Suitability Index:

Final_Suitability_Index =
(Flood_Risk + Land_Use + Social_Vulnerability) / 3

All variables were equally weighted.

Output values ranged approximately from **0.6 to 4.7**.

---

# 🗺️ Step 6 — Classification & Symbolization

The final composite raster was:

- Classified into 5 categories
- Symbolized using a sequential color ramp
- Exported as final suitability map

Categories:

- Very Low
- Low
- Moderate
- High
- Very High

---

# 📊 Step 7 — Interpretation & Spatial Pattern Analysis

Spatial clustering patterns were evaluated:

- Coastal zones showed lower suitability due to flood exposure.
- Inland mid-county areas showed higher development potential.
- High SVI tracts reduced composite suitability scores.

This analysis demonstrates the interaction between environmental hazard exposure and socioeconomic resilience.

---

# ⚙️ Model Design Considerations

- Equal weighting applied across all variables.
- No dynamic weighting or scenario testing.
- No temporal modeling (static data snapshot).
- No sea level rise projection integration.

Future iterations could incorporate:

- Weighted overlay sensitivity testing
- Sea level rise scenarios
- Transit accessibility layers
- Housing cost metrics
- Multi-year hazard frequency analysis

---

# 🔁 Reproducibility Summary

The model can be reproduced using:

1. Standardized CRS
2. Uniform raster cell size
3. Reclassification to common scale
4. Raster Calculator composite formula
5. Final classification and symbology

All processing performed in ArcGIS Pro.

---
