# 🤿 Exploration Dashboard

## 📋 Executive Summary

This dashboard continues the investigation into marine pollution in *Illex argentinus* by transitioning from method validation (Foundation Module) to exploratory data analysis. It focuses on uncovering patterns in contaminant concentrations across tissues, years, and biological traits — while maintaining transparency about data limitations and simulation use.

Using simulated datasets resembling real observations (to preserve confidentiality), this dashboard applies correlation, dimensionality reduction, clustering, pollutant interaction analysis, and statistical testing to investigate pollutant behavior across 2019–2021.

Although the results are exploratory and not inferentially conclusive, this tool plays a key role in identifying leads for future hypothesis testing and risk assessment, while showcasing scalable analytical workflows in R Shiny.

---

## 📚 Overview

*Illex argentinus*, the Argentine shortfin squid, serves as a bioindicator for marine pollution in the Southwest Atlantic Ocean. Between February and April (2019–2021), squid samples were analyzed for trace metals and organic contaminants. This dashboard serves as an interactive front-end to examine how these pollutants vary across:

- **Biological traits** (e.g., sex, size, maturity)
- **Environmental features** (e.g., capture month, distance to land)
- **Time** (e.g., pre-, mid-, and post-COVID sampling years)

⚠️ **Data Disclaimer:** Due to confidentiality agreements, all data shown in this dashboard are simulated. Variable names, values, and categories were anonymized or altered, but the structure mimics real datasets used in the original study.

---

## 🖼️ Dashboard Preview
![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1FWCFLVcbpxVV6sybB56DgOCKAxhsM_xI)
*Note: The screenshot above shows a partial view of the dashboard.*
[(Click here for dashboard)](https://euchie23.shinyapps.io/exploration/)
<br><br>


## 🧪 Dataset Schema

The project uses two datasets collected for exploratory data analysis (EDA) in R:

- [`trace_metals.csv`](./data/trace_metals.csv): Contains measurements of trace metal pollutants
- [`organic_compounds.csv`](./data/organic_compounds.csv): Contains measurements of organic compound pollutants

Both datasets share 14 columns, which include metadata such as ID, length, weight, location, distance and date. The remaining columns contain concentrations of different analytes specific to each dataset type. <br>
*📝 Note:
Columns labeled as "int" (integer) contain whole numbers, while "num" (number) columns contain decimal (real) values. Some concentration columns are "chr" (character), indicating that certain values are flagged as below the limit of quantification (BLOQ). In those cases, the reported value is not the true concentration but a BLOQ indicator. If a concentration column is "num", all values were above the LOQ and considered detected.*

### 🔁 Shared Columns (1–15)

| Column Name       | Data Type | Description                       |
|-------------------|-----------|-----------------------------------|
| ID (sample ID)    | chr    | Unique identifier for the sample |
| Year              | int     | Latitude of the sample location  |
| ID_num        | int     | Longitude of the sample location |
| Area   | int      | Date when sample was collected   |
| Tissue             | chr     | Depth of sample (if applicable)  |
| Gender (0=Females, 1=Males)| int     | Temperature at collection site   |
| dta_km (distance to Argentina in Km)| int     | Measured pH of the sample        |
|dtfl_km (diustance to Falkand Islands in km)| int       | Additional shared fields         |
| Longitude          | chr     | Temperature at collection site   |
| Latitude           | chr     | Temperature at collection site   |
| Month_of_Capture   | int     | Temperature at collection site   |
| Mantle_length_ mm  | num     | Temperature at collection site   |
|Wet Weight_g        | num     | Temperature at collection site   |
| Maturity_level     | int     | Temperature at collection site   |


### 🧲 Trace Metals Dataset (`trace_metals.csv`)

| Column Name     | Data Type | Description                         |
|-----------------|-----------|-------------------------------------|
| DW (Dry Weight) | num       | Sampling location name or code   |
| Metal_A         | num       | Metal_A concentration (mg/kg)    |
| Metal_B         | num       | Metal_B concentration (mg/kg)    |
| Metal_C         | num       | Metal_C concentration (mg/kg)    |
| Metal_D         | num       | Metal_D concentration (mg/kg)    |
| Metal_E         | num       | Metal_E concentration (mg/kg)    |
| Metal_F         | chr       | Metal_F concentration (mg/kg)    |
| Metal_G         | num       | Metal_G concentration (mg/kg)    |
| Metal_H         | chr       | Metal_H concentration (mg/kg)    |
| Metal_I         | chr      | Metal_I concentration (mg/kg)    |
| Metal_J         | chr       | Metal_J concentration (mg/kg)    |

### 🌱 Organic Compounds Dataset (`organic_compounds.csv`)

| Column Name       | Data Type | Description                             |
|-------------------|-----------|-----------------------------------------|
| DW (Dry Weight) | num     | Sampling location name or code   |
| Organic_A       | chr     | Organic_A concentration (mg/kg)            |
| Organic_B       | chr     | Organic_B concentration (mg/kg)            |
| Organic_C       | chr     | Organic_C concentration (mg/kg)            |
| Organic_D       | chr     | Organic_D concentration (mg/kg)            |


## 📊 Analytical Approaches

The dashboard is structured across 8 interactive tabs — each representing a stage in the data dive:

| Stage | Tab Title                | Description                                     |
|-------|--------------------------|-------------------------------------------------|
| 1     | ⛴️ Dockside Briefing     | Intro, roadmap, and dataset context             |
| 2     | 🐙 Diving In              | Analyte concentration summaries by tissue       |
| 3     | 🧍‍♂️ Buddy Diving         | Sex-based pollutant comparisons                 |
| 4     | 📏 Tiddlers among Titans | Size-based bioaccumulation patterns             |
| 5     | 🌊 Riding the Current     | Year-to-year pollutant flows by tissue          |
| 6     | 📚 Echoes in the Deep     | PCA & K-Means cluster analysis                  |
| 7     | ⚗️ Shipwrecks and Shadows | Correlation networks (Spearman)                 |
| 8     | 🧠 Resurfacing            | Summary of patterns and takeaways               |

---

## 🎯 Exploratory Objectives

- 📅 Examine temporal trends in pollutant concentrations (2019–2021)  
- ⚥ Compare pollutant loads by sex and maturity status  
- 📏 Investigate body size relationships with contaminant levels  
- 🧪 Assess tissue-specific differences in accumulation  
- 📚 Apply unsupervised learning (PCA & clustering) to identify hidden patterns  
- 🌐 Analyze pollutant co-occurrence via correlation matrices  

---

## 🧠 Key Takeaways

> 🔎 *These insights are exploratory only — not definitive conclusions.*

- Seasonal and size-based differences may be present across pollutant types  
- Cluster analysis reveals meaningful groupings by tissue and year  
- Certain pollutants appear to co-occur, suggesting shared sources or accumulation behavior  
- Organic compound variability is higher, likely due to matrix effects or validation limitations  

---

## 🤝 Invitation to Collaborators

We welcome collaboration and feedback from:

- 🧪 Environmental scientists and toxicologists  
- 📊 Data scientists and Shiny developers  
- 🌊 Marine biologists and ecologists  
- 🏛️ Organizations focused on seafood safety and sustainability  
- 🌍 ESG and compliance professionals working in marine environments  

---

## 🛂 Repository Notes

This dashboard is part of a broader marine pollution research project using *Illex argentinus* as a bioindicator.

## 🛠️ Built With

This dashboard was developed in **R Shiny** using the following packages:

### 📦 Core Frameworks
- `shiny` — App framework for interactive dashboards  
- `bs4Dash` — Bootstrap 4 dashboard theme  
- `shinydashboard`,`shinyjs`, `shinyWidgets` — UI extensions and interactivity

### 📊 Data Manipulation & Wrangling
- `dplyr`, `tidyr`, `tibble`, `forcats`, `purrr` — Tidyverse tools for data wrangling  
- `FSA`, `MASS`, `dunn.test` — Statistical analysis  
- `googlesheets4`, `qs`, `openxlsx` — Data I/O (Google Sheets, fast read/write, Excel export)

### 📈 Visualization & Reporting
- `ggplot2`, `plotly`, `GGally`, `ggcorrplot`, `ggtext`, `ellipse`, `RColorBrewer` — Data visualization  
- `knitr`, `kableExtra`, `flextable` — Table rendering and report formatting

---

Active development takes place in a **private repository** (`squid_Fest`).  
This **public repo** hosts the interactive dashboard and simulated datasets.

📬 For full access to the development history or extended modules, please reach out via **[Email](mailto:euchie23@gmail.com)** or connect on **[LinkedIn](https://www.linkedin.com/)** 😃.
