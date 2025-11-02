# **Population Density and Car Dependency in Calgary**

*GEOG 587*
**Author:** Ghasan Almahdhori
**Institution:** University of Calgary | Fall 2025

---

##  Project Overview and Purpose

This repository presents a data package for the indicator ***Population Density and Car Dependency in Calgary***.
The project investigates how land-use form affects mobility and sustainability in Calgary, emphasizing the spatial relationship between **community-level population density** and **public-transit usage**.
By integrating census and open-data layers in ArcGIS Online, this project visualizes Calgary’s dependence on private automobiles and the sustainability benefits of compact urban growth.
All data are open-access and documented following **FAIR** (Findable, Accessible, Interoperable, Reusable) and **CARE** (Collective Benefit, Authority to Control, Responsibility, Ethics) principles.

---

##  Folder Structure Guide

| Folder               | Description                                                             |
| :------------------- | :---------------------------------------------------------------------- |
| **`data/`**          | Contains `.txt` files referencing datasets used in the indicator.       |
| **`data/metadata/`** | ISO-style metadata files describing source, CRS, and field information. |
| **`maps/`**          | GeoTIFF export (`.tif`) visualizing density + transit mode share.       |
| **`analysis/`**      | Notes documenting GIS workflow and analytical methods.                  |
| **`license/`**       | Repository-level license and supporting notice files.                   |
| **`README.md`**      | This main documentation file summarizing the project.                   |

---

##  Coordinate Reference System (CRS) and Data Formats

* **CRS:** NAD 1983 CSRS Alberta 10-TM (EPSG: 3403)
* **Spatial Format:** ESRI Feature Service (ArcGIS Online)
* **Map Export:** GeoTIFF (`.tif`)
* **Tabular and Metadata Format:** UTF-8 plain text (`.txt`)
* **Spatial Extent:** City of Calgary municipal boundary

---

##  Data Sources and Methods Summary

1. **2019 Calgary Community Population**
   *Source:* City of Calgary Open Data (2019 Census)
   [ArcGIS Service URL](https://services2.arcgis.com/XSv3KNGfmrd1txPN/arcgis/rest/services/2019_Census_by_Community_Calgary/FeatureServer)
   Provides total population by community, used to calculate density (population ÷ area).

2. **2021 Federal Census – Mode of Transportation to Work by Community**
   *Source:* City of Calgary Open Data (Statistics Canada 2021)
   [ArcGIS Service URL](https://services1.arcgis.com/AVP60cs0Q9PEA8rH/arcgis/rest/services/2021%20Federal%20Census%20Transportation%20to%20Work%20by%20Community/FeatureServer)
   Provides commute-mode shares (public transit %, drive %, employment counts).

**Workflow Summary:**
Population data were joined to community polygons to calculate density per km².
Transportation data were then joined by community name to derive mode-share statistics.
A **choropleth map** (blue density gradient) with **proportional green circles** for transit share was created in ArcGIS Online and exported as GeoTIFF.

---

##  Visualization

**Figure 1:** Population Density and Transit Mode Share in Calgary (2021)
*File: `maps/density_transit_choropleth_calgary.tif`*

This GeoTIFF map shows population density (blue choropleth) overlaid with proportional green circles for transit mode share.
It illustrates that Calgary’s outer low-density suburbs have very low transit usage, whereas inner-city communities show higher transit adoption and lower car dependency.

---

##  License and Citation Information

This repository and accompanying documentation are licensed under the
**Creative Commons Attribution 4.0 International (CC BY 4.0)**
[https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)

**Citation:**
Almahdhori, G. (2025). *Population Density and Car Dependency in Calgary [Data Package].* University of Calgary.
Data sourced from City of Calgary Open Data (2019, 2021) and Statistics Canada.

---

##  Contact and Acknowledgements

**Author:** Ghassan Saleh Almahdhori

Acknowledgement to Dr. Victoria Fast and the Department of Geography, University of Calgary, for guidance in spatial data management and open science practice.
