# 🌊 Residential Suitability Modeling  
## Pinellas County, Florida  
**Raster-Based Multi-Criteria Spatial Decision Model**

William E. Quinby  
GIS | Environmental Risk | Spatial Analytics  

---

# 🚀 Project Summary

This project develops a raster-based spatial decision-support model to evaluate residential development suitability in Pinellas County, Florida — a high-risk coastal region facing flood exposure, dense urbanization, and socioeconomic vulnerability challenges.

Using ArcGIS Pro, three independent spatial risk layers were standardized, reclassified, and integrated into a composite suitability index:

- 🌊 Flood Risk (FEMA SFHA)
- 🏘️ Land Use Compatibility
- 🧭 Social Vulnerability Index (CDC SVI)

The result is a reproducible geospatial framework that supports data-driven coastal planning and resilience analysis.

---

# 🧠 Problem Context

Pinellas County presents a complex development landscape:

- Coastal floodplain exposure
- Urban density constraints
- Vulnerable population distribution
- Zoning and land-use policy limitations

Traditional site evaluation often isolates these variables.

This model integrates them.

The objective:  
**Identify spatially suitable zones that balance environmental safety, policy feasibility, and community resilience.**

---

# ⚙️ Methodology Overview

### 1️⃣ Data Standardization
- Reprojected all layers to common CRS  
- Clipped to county boundary  
- Converted vector data to raster format  
- Aligned cell size and snap raster  

### 2️⃣ Reclassification
Each variable was normalized to a 1–5 suitability scale:

| Score | Suitability |
|-------|------------|
| 1 | Very Low |
| 5 | Very High |

### 3️⃣ Composite Index Calculation

Final_Suitability_Index =
(Flood_Risk + Land_Use + Social_Vulnerability) / 3

All factors were equally weighted.

### 4️⃣ Classification & Interpretation
The output raster was classified into five development suitability categories and symbolized for spatial interpretation.

---

# 📊 Key Findings

- Coastal zones exhibit lowest suitability due to flood exposure.
- High-SVI census tracts reduce composite suitability inland.
- Mid-county regions demonstrate strongest development balance.
- Suitability values ranged approximately from 0.6 to 4.7.

The model reveals how environmental hazard exposure and social vulnerability interact spatially across an urban coastal system.

---

# 🛠️ Technical Stack

- ArcGIS Pro (Raster Analysis)
- Multi-Criteria Decision Analysis (MCDA)
- Raster Calculator
- Spatial Reclassification
- FEMA Floodplain Data
- CDC Social Vulnerability Index
- Spatial Data Harmonization

---

# 🧩 Repository Structure
```
pinellas-residential-suitability-model/
│
├── README.md
├── poster/
│   └── Residential_Suitability_Model_Pinellas_WEQuinby.pdf
├── data_sources/
│   └── data_sources.md
├── methodology/
│   └── workflow.md
└── analysis_notes/
    └── limitations_future_work.md
```

Supporting documentation:

- `/data_sources/data_sources.md`
- `/methodology/workflow.md`
- `/analysis_notes/limitations_future_work.md`

---

# 📎 Final Output

Full project poster:

[View Poster PDF](poster/Final_Project_Poster_WEQuinby.pdf)

---

# 🔬 Model Limitations & Future Expansion

This model represents a static, equally weighted framework.

Future enhancements could include:

- Sea level rise projections
- Weighted overlay sensitivity testing
- Infrastructure accessibility modeling
- Scenario-based climate resilience planning
- Machine learning-based suitability modeling

See full discussion in:
`/analysis_notes/limitations_future_work.md`

---

# 🎯 Strategic Significance

This project demonstrates the design and documentation of a reproducible geospatial decision-support system integrating environmental risk, land policy, and socioeconomic resilience.

The modeling architecture supports expansion into advanced coastal resilience analytics and infrastructure planning applications.

---

# 📌 Author

William E. Quinby  
St. Petersburg, FL  
GIS | Environmental Data | Spatial Risk Modeling  

