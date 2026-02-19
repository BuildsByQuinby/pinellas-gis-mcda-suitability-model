# 📊 Data Sources & Metadata  
**Project:** Residential Suitability Modeling – Pinellas County, FL  
**Author:** William E. Quinby  
**Analysis Type:** Raster-Based Multi-Criteria Decision Analysis (MCDA)  
**Software:** ArcGIS Pro  

---

## 🗺️ 1. Flood Risk Data

**Dataset:** FEMA Special Flood Hazard Areas (SFHA)  
**Source Agency:** Federal Emergency Management Agency (FEMA)  
**Year:** 2023  
**Original Format:** Polygon (Vector)  
**Final Format:** Raster  
**Projection:** NAD 1983 StatePlane Florida West (FIPS 0902 Feet)

### 📌 Description
Special Flood Hazard Areas (SFHA) represent zones with a 1% annual chance flood risk (100-year floodplain). This dataset served as the primary environmental risk variable.

### ⚙️ Preprocessing Workflow
- Clipped to Pinellas County boundary  
- Reprojected to match project CRS  
- Converted from polygon to raster  
- Reclassified to 1–5 suitability scale  

**Reclassification Logic:**  
- High flood exposure → 1 (Very Low Suitability)  
- Moderate flood exposure → 2–3  
- Minimal / No flood exposure → 5 (Very High Suitability)

---

## 🏘️ 2. Land Use Classification

**Dataset:** Pinellas County Land Use (eGIS)  
**Source Agency:** Pinellas County GIS Department  
**Year:** 2022  
**Original Format:** Polygon  
**Final Format:** Raster  

### 📌 Description
Parcel-level land use designations used to evaluate development compatibility for residential expansion.

### ⚙️ Preprocessing Workflow
- Clipped to county boundary  
- Reprojected to project CRS  
- Converted to raster  
- Reclassified based on development suitability  

**Reclassification Logic:**  
- Restricted / Industrial / Conservation → Low suitability  
- Mixed Use / Transitional → Moderate suitability  
- Residential zoning → High suitability  

---

## 🧭 3. Social Vulnerability Index (SVI)

**Dataset:** CDC/ATSDR Social Vulnerability Index  
**Source Agency:** Centers for Disease Control and Prevention (CDC)  
**Year:** 2020  
**Original Format:** Census Tract Polygon  
**Final Format:** Raster  

### 📌 Description
The Social Vulnerability Index (SVI) quantifies community resilience using socioeconomic and demographic indicators. Higher SVI values indicate greater vulnerability.

### ⚙️ Preprocessing Workflow
- Joined SVI attribute table to census tract geometry  
- Clipped to Pinellas County  
- Reprojected  
- Converted to raster  
- Reclassified to suitability scale  

**Reclassification Logic:**  
- High vulnerability → 1 (Low suitability)  
- Moderate vulnerability → 3  
- Low vulnerability → 5 (High suitability)

---

## 🧱 4. Administrative Boundary

**Dataset:** TIGER/Line County Boundaries  
**Source Agency:** U.S. Census Bureau  
**Year:** 2023  
**Purpose:** Spatial mask and clipping boundary  

---

# 🔧 Spatial Standardization

All raster layers were standardized prior to analysis:

- ✔ Common coordinate reference system  
- ✔ Consistent cell size  
- ✔ Snap raster alignment  
- ✔ Clipped to county extent  
- ✔ Processed within ArcGIS Pro raster environment  

This ensured spatial consistency for overlay operations and Raster Calculator modeling.

---

# 📉 Data Limitations

- Flood risk reflects current FEMA maps only (no sea-level rise projections).  
- Social Vulnerability Index is generalized at census tract level.  
- Land use layer does not reflect future zoning changes.  
- Equal weighting applied across all variables.  

---

