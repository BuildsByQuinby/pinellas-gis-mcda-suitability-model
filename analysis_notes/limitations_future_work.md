# ⚠️ Limitations & Future Work  
**Project:** Residential Suitability Modeling – Pinellas County, FL  

This document outlines modeling constraints, data limitations, and opportunities for methodological refinement.

---

# 📉 Model Limitations

## 1️⃣ Equal Weighting Assumption

All variables (Flood Risk, Land Use, Social Vulnerability) were assigned equal weight in the composite index:

(Flood_Risk + Land_Use + Social_Vulnerability) / 3

This assumes each factor contributes equally to residential suitability.  
In reality, policy priorities or risk tolerance may justify differential weighting.

---

## 2️⃣ Static Snapshot Analysis

The model represents a single temporal snapshot based on:

- FEMA flood maps (2023)
- Land use zoning (2022)
- CDC SVI (2020)

It does not account for:

- Future zoning changes
- Climate-driven flood expansion
- Demographic shifts
- Infrastructure investment changes

---

## 3️⃣ Flood Risk Scope

Flood risk modeling was limited to FEMA Special Flood Hazard Areas (SFHA).  
The model does not incorporate:

- Sea level rise projections
- Storm surge modeling
- Rainfall-driven pluvial flooding
- Tidal nuisance flooding

As a result, long-term coastal vulnerability may be underestimated.

---

## 4️⃣ Spatial Resolution Constraints

Social Vulnerability Index (SVI) data is aggregated at the census tract level.  
This generalization may obscure:

- Block-level variation
- Neighborhood-level inequities
- Micro-scale resilience differences

Raster cell size standardization may also smooth localized variability.

---

## 5️⃣ Land Use Simplification

Land use classifications were grouped into broad suitability categories.  
The model does not evaluate:

- Parcel-level development constraints
- Building codes
- Environmental contamination
- Utility access
- Infrastructure capacity

---

## 6️⃣ No Infrastructure Accessibility Variables

The model does not include:

- Transit proximity
- Road network access
- School districts
- Healthcare access
- Employment density

These factors influence real-world residential development feasibility.

---

# 🔬 Future Model Enhancements

## 🌊 Integrate Sea Level Rise Projections

Incorporate NOAA or regional sea level rise scenario data to simulate long-term flood exposure and refine coastal suitability zones.

---

## ⚖ Weighted Overlay Sensitivity Testing

Conduct sensitivity analysis using variable weight scenarios:

- Flood risk priority model
- Equity-centered model (SVI weighted higher)
- Market-driven model (land use weighted higher)

This would reveal how suitability zones shift under different policy objectives.

---

## 📈 Dynamic Hazard Modeling

Incorporate:

- Storm surge frequency models
- Rainfall intensity projections
- Historical flood event data

This would strengthen hazard exposure realism.

---

## 🏘️ Infrastructure & Accessibility Layers

Add variables such as:

- Road network density
- Transit access buffers
- Utility service coverage
- Public facility proximity

This would shift the model from hazard avoidance to true development feasibility modeling.

---

## 🧠 Machine Learning Integration

Future iterations could test:

- Logistic regression suitability modeling
- Random forest classification
- Supervised learning using historical development patterns

This would transition from rule-based MCDA to predictive spatial modeling.

---

## 🗺️ Scenario-Based Planning

Develop interactive scenario models for:

- Climate resilience planning
- Affordable housing prioritization
- Strategic zoning reform analysis

---

# 🎯 Strategic Insight

This model demonstrates a structured, reproducible spatial decision-support framework.  

While simplified for instructional purposes, the architecture supports expansion into advanced resilience planning and policy-driven geospatial modeling systems.


