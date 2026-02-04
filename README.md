# nyc-rainy-day-crash-hotspot-analysis
Comparative analysis of NYC collision hotspots: Rainy vs. Clear weather. Identifying weather-conditioned accident patterns and road safety insights for 2021-2022.

# NYC Crash Hotspots in Rain vs Clear Weather (2021–2022)

## Overview
This repo analyzes **NYC motor vehicle collision records** to check whether crash locations differ between **rainy** and **clear** days. The focus is on identifying **locations where crash rates increase during rain** and summarizing practical, location-specific mitigation ideas.

* **Author:** Changwoo Kim (University of Michigan, Master of Data Science)
* **Project Context:** Explorer Transportation Data Science Project (Northeast Big Data Innovation Hub / NSDC)

## Research Question
**Do crash locations in NYC differ meaningfully between rainy and clear conditions?**
If so, which locations show the largest increases during rain, and what characteristics might explain them?

## Key Findings
* **Top contributing factor (overall):** "Driver Inattention/Distraction" appears most frequently in both years.
* **Location-specific rain impact:** Some locations show substantially higher crash rates on rainy days; in selected areas, this increase is **as high as ~10×** compared to clear conditions.
* **Year-to-year differences:** The set of high-increase locations is **not identical** between 2021 and 2022, suggesting variability across years.

<img width="569" height="414" alt="image" src="https://github.com/user-attachments/assets/f6ba8126-c9ce-41dd-8a21-80228c97f651" />
<img width="566" height="422" alt="image" src="https://github.com/user-attachments/assets/1e9e0c11-53b8-4383-9e5f-fc010e8bb0f7" />
<img width="536" height="521" alt="image" src="https://github.com/user-attachments/assets/0a957018-308e-436b-aed4-5e2e360d2e4d" />






## Recommendations (from high-incident locations)
Detailed inspection of accident hotspots using **Google Earth satellite imagery** highlighted specific structural flaws. The following recommendations address the observed friction points regarding traffic congestion, parking zones, and transit infrastructure:

* **Adjust bus stop placement near intersections**
    * Bus stops immediately before intersections can narrow lanes and disrupt flow.
* **Enforce illegal parking near intersections**
    * Parked vehicles can block sightlines for turning vehicles and contribute to conflict points.
* **Reconsider curbside parking near parks / expand lanes where feasible**
    * Reducing curbside friction can improve throughput for buses/shuttles and reduce merging conflicts.

## Limitations & Next Steps
* **No traffic volume normalization:** Results are based on crash counts/rates without detailed exposure data (traffic volume by weather). Adding volume would improve risk estimation.
* **Statistical testing not fully implemented:** Future work can add hypothesis testing and trend analysis (e.g., by month/season) to validate stability of observed differences.

## Data
**Total records analyzed:** 196,099

### A. NYC Motor Vehicle Collisions (Open Data)
* **2021:** 110,557 records
* **2022:** 85,542 records
* **Key fields used:** Date/time, latitude/longitude, injuries/fatalities, contributing factors, vehicle type

### B. Weather data (precipitation)
* Used to label crash dates as **Rainy** vs **Clear** for comparison.

## Tech Stack & Tools
This project was executed in a **Python** environment (Google Colab) utilizing the following libraries:

| Category | Libraries Used |
| :--- | :--- |
| **Data Manipulation** | Pandas, NumPy |
| **Statistical Analysis** | Statsmodels |
| **Visualization** | Matplotlib, Seaborn |
| **Geospatial Analysis** | Folium (Interactive maps) |

## Approach

### Phase 1: Data Preparation
* Loaded large-scale CSV datasets into the environment.
* Conducted **Exploratory Data Analysis (EDA)** using methods such as `head()`, `describe()`, and `isnull()` to understand data structure and distribution.

### Phase 2: Data Pre-processing
* **Missing Values:** Handled missing data in key columns (e.g., `OFF STREET NAME`, `CONTRIBUTING FACTOR`).
* **Data Ethics:** Reviewed potential regional or demographic biases in the data collection process to ensure ethical analysis standards.

### Phase 3: Detailed Analysis
* Identified the **Top 10 causes** of accidents (e.g., Driver Inattention, Following Too Closely).
* Compared accident frequencies by location under different weather conditions (Rainy vs. Clear).
* Investigated specific intersections and road structures correlated with high accident rates.


---
*This project was completed in collaboration with the Northeast Big Data Innovation Hub.*
