# 🦑📚 SquidStack 📚🦑🃏📊📈

## Objective 🎯

SquidStack is a curated version of a larger private repository **(Squid_Fest)** where the full version control and raw development occur. Updates are copied here once polished. **Version control and history exists in the private repo and is available upon request for collaborators or reviewers**.

**What is the Squid_Fest repository about?**
____________________________________________

Squid Fest is a data science portfolio that represents an extension and refinement of my graduate thesis work and interdisciplinary research conducted as a Master's student and Research Assistant at National Taiwan University (2021–2024). It presents a snapshot of applied research involving marine resource sustainability, ecosystem health, and data-driven fisheries science. <br>

This repository includes a few projects that define three core topics developed using a combination of ecological, biological, chemical, remote sensing, and industrial activity datasets, focused on Illex argentinus (Argentine shortfin squid) in the Southwest Atlantic Ocean. The projects demonstrate proficiency across a wide range of techniques including data engineering, statistical and machine learning modeling, and geospatial data fusion — with practical applications in marine ecology, environmental monitoring, and resource management. <br>

The overarching goals were to: <br>
 - Evaluate regional marine ecosystem health and the human health risk of major consumers
 - Analyze spatial and temporal squid catch patterns
 - Build predictive models to support sustainable fishery management <br>

## **⚠️Data Confidentiality Notice⚠️** 
**To comply with research confidentiality and ethical standards, the datasets used in this repository have been simulated to closely resemble real-world data. Pollutant names and other sensitive variables were anonymized. The primary goal of these projects is to demonstrate analytical workflows, modeling techniques, and geospatial methodologies used during real research conducted at the National Taiwan University. As such, any interpretations or conclusions drawn from this repository should not be considered accurate representations of actual marine conditions in the study region.** <br> <br>


### 🧠 Learning Note <br>
This Squid_Fest portfolio reflects skills developed and applied over several months of focused, self-directed study and hands-on practice. While these tools and techniques are still being refined, the work demonstrates a solid and growing proficiency in applying data science to complex ecological problems with real-world relevance. <br> <br>


## 👩‍💻 Key Skills and Technical Proficiencies <br>
### 🧩 Data Engineering
 - Designed and implemented ETL pipelines to ingest, clean, and merge biological, environmental, and chemical datasets using R and Python
 - Structured data for modeling and analysis with reproducible, version-controlled code using Jupyter, RStudio, and PostgreSQL <br>
### 📈 Statistical & Predictive Modeling
 - Applied Generalized Additive Models (GAMs), Tweedie GLMs, and Bayesian techniques to standardize and predict Catch Per Unit Effort (CPUE)
 - Built models to forecast squid biomass under different future ocean warming scenarios using Environmental Surplus Dependent Models (EDSPMs) <br>
### ⚙️ Machine Learning & AutoML
 - Developed a lightweight AutoML pipeline to compare model strategies (e.g., ensemble, linear, and tree-based)
 - Created a Streamlit dashboard for interactive CPUE prediction using model inference and user-defined environmental parameters <br>
### 🔍 Feature Engineering
 - Conducted exploratory feature creation, transformation, and reduction using BorutaPy for variable importance ranking and interpretability
 - Performed domain-aware feature selection to improve model performance and clarity <br>
### 📊 Programming & Visualization
 - Built dynamic, publication-ready visualizations using ggplot2, Seaborn, and Matplotlib
 - Developed interactive dashboards with Shiny (R) and Streamlit (Python) for result presentation and stakeholder communication
 - Refined string handling and data manipulation skills using tidyverse and base R <br>
### 🛰️ Geospatial Data Analytics
 - Integrated NASA and Copernicus NetCDF remote sensing data (Chlorophyll-A, Sea Surface Height) into CPUE models as spatio-environmental features
 - Developed spatial data pipelines for missing value imputation using nearest-neighbor querying across raster layers (temperature, depth)
### 🌍 Spatial Analysis & GIS
 - Leveraged PostgreSQL with PostGIS, along with QGIS, for advanced geospatial querying, spatial joins, and mapping
 - Produced multi-layer environmental visualizations to communicate habitat dynamics and fishing pressure zones <br> <br>

## 🛠️ Tools & Technologies
 - Analytical Chemistry: ICP-MS, LC-MS
 - Programming: R, Python, SQL (PostgreSQL), Bash
 - Geospatial Tools: QGIS, PostGIS, NetCDF, Raster/Vector GIS analysis
 - Modeling Libraries: PyCaret, pyGAM, scikit-learn, BorutaPy, streamlit
 - Data Processing: pandas, dplyr, tidyr, data.table
 - Visualization: ggplot2, seaborn, matplotlib, plotly
 - Dashboards: Shiny (R), Streamlit (Python)
 - Productivity: Git, GitHub, Excel (VBA), Word <br> <br>

### Squid_Concentrations_Analysis ⏳📈📊 [Open Folder](./Squid_Conc_Anly) <br>
    Task-0-CRM (Analytical Method validation)
    Task-1-Data_Preprocessing
    Task-2-Detectiion_summary
    Task-3-Data_mining
    Task-4-Temporal_variations_in_Chemical Concentrations
    Task-5-Human_Health_Risk
    Appendix
    shiny_dashboard

### Squid_Stock_Assessment_and_Forecasting 📈 📊 🦑 [Open Folder](./Squid_Stock_Assmnt_Forecast) <br>
    data
    notebooks
    outputs
    results
    scripts
    streamlit_apps

### Squid_SQL 🛠️ 📈 🦑 [Open Folder](./Squid_SQL) <br>
    squid_spatial_analysis_postGIS
    more to come....
