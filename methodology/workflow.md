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

Each raster layer was reclassified onto a standardized
