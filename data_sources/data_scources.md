Data Sources Documentation

Residential Suitability Modeling – Pinellas County, FL

This document describes all spatial datasets used in the raster-based suitability analysis, including source agency, data format, spatial characteristics, and preprocessing steps.

1. Flood Risk Data

Dataset: FEMA Special Flood Hazard Areas (SFHA)
Source: Federal Emergency Management Agency (FEMA)
Year: 2023
Format: Polygon (Vector)
Projection: Reprojected to match project CRS (NAD 1983 StatePlane Florida West FIPS 0902 Feet)

Description

Special Flood Hazard Areas (SFHA) identify zones with a 1% annual chance of flooding (100-year floodplain). Flood exposure was used as a primary environmental risk variable.

Preprocessing Steps
Clipped to Pinellas County boundary
Converted to raster
Reclassified to 1–5 suitability scale
High flood risk → 1 (Very Low Suitability)
Low/no flood risk → 5 (Very High Suitability)

2. Land Use Classification

Dataset: Pinellas County Land Use (eGIS)
Source: Pinellas County GIS Department
Year: 2022
Format: Polygon (Vector)

Description
Parcel-level land use designations used to determine zoning compatibility for residential development.

Preprocessing Steps
Clipped to county boundary
Converted to raster
Reclassified based on development compatibility:
Restricted / Non-developable → Low suitability
Residential / Mixed Use → Higher suitability

3. Social Vulnerability Index (SVI)

Dataset: CDC/ATSDR Social Vulnerability Index
Source: Centers for Disease Control and Prevention
Year: 2020
Format: Census Tract (Polygon)

Description
The Social Vulnerability Index measures community resilience using socioeconomic and demographic indicators. Higher SVI values indicate greater vulnerability.

Preprocessing Steps
Joined SVI attributes to census tract polygons
Clipped to Pinellas County
Converted to raster
Reclassified:
Higher vulnerability → Lower suitability
Lower vulnerability → Higher suitability

4. Administrative Boundary

Dataset: TIGER/Line County Boundaries
Source: U.S. Census Bureau
Year: 2023
Purpose: Spatial clipping and mask layer

Spatial Standardization

All raster layers were:

Aligned using a common snap raster
Standardized to consistent cell size
Reprojected to a uniform coordinate reference system
Processed in ArcGIS Pro

Data Limitations
Flood maps represent current conditions only
SVI data generalized at census tract level
Land use does not reflect future zoning changes
No incorporation of sea level rise or climate projection layers
