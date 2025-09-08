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

Both datasets share 14 columns containing metadata such as sample ID, location, date, and biological measurements like length and weight. The remaining columns report analyte concentrations specific to each dataset type.

> 📝 **Note:**  
> Columns labeled as `"int"` contain whole numbers, while `"num"` columns contain decimal (real) values. Some concentration columns are `"chr"` (character), indicating values flagged as **below the limit of quantification (BLOQ)**. These BLOQ indicators replace actual measurements. If a concentration column is `"num"`, all values were above the LOQ and are considered detected.

> ⚠️ Reminder: Metal and organic compound names (e.g., Metal_A, Organic_B) are anonymized to maintain confidentiality.

### 🔁 Shared Columns (1–14)

| Column Name       | Data Type | Description                       |
|-------------------|-----------|-----------------------------------|
| ID     | chr    | Unique identifier for the sample |
| Year              | int     | Year of capture  |
| ID_num        | int     | ID # given in fisheries science lab |
| Area   | int      | Area # given by fishing vessel   |
| Tissue             | chr     | Squid tissues analyzed  |
| Gender (0=Females, 1=Males)| int     | Squid genders analyzed  |
| dta_km (distance to Argentina in Km)| int     | Measured distance (Google Earth) from catch location to the shores of Argentina        |
|dtfl_km (distance to Falkand Islands in km)| int       | Measured distance (Google Earth) from catch location to the shores of the Falkland Islands        |
| Longitude          | chr     | longitude coordinates strings (DMS) of catch location   |
| Latitude           | chr     | latitude coordinates strings (DMS) of catch location   |
| Month_of_Capture   | int     | Month of capture for squids|
| Mantle_length_ mm  | num     | Squid Mantle Length measured in milli meters  |
|Wet Weight_g        | num     | Full squid body weight measured in lab (grams) before dissection  |
| Maturity_level     | int     | Squid maturity level assessed based on a paper by Arkhipkin et al, 1992 |


### 🧲 Trace Metals Dataset (`trace_metals.csv`)

| Column Name     | Data Type | Description                         |
|-----------------|-----------|-------------------------------------|
| DW (Dry Weight) | num       |Weight of the freeze-dried, ground tissue sample aliquot used for extraction and analysis|
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
| DW (Dry Weight) | num     | Weight of the freeze-dried, ground tissue sample aliquot used for extraction and analysis |
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
