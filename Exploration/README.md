# 🧭 Exploration Dashboard

## 📋 Executive Summary

This dashboard continues the investigation into marine pollution in *Illex argentinus* by transitioning from method validation (Foundation Module) to exploratory data analysis. It focuses on uncovering patterns in contaminant concentrations across tissues, years, and biological traits — while maintaining transparency about data limitations and simulation use.

Using simulated datasets resembling real observations (to preserve confidentiality), this dashboard applies dimensionality reduction, clustering, pollutant interaction analysis, and statistical testing to investigate pollutant behavior across 2019–2021.

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


📌 *Screenshot of the dashboard interface*  
 **Insert a screenshot of your main dashboard view here.**  
Recommended name: `exploration_dashboard_interface.png`

![Dashboard Overview](./README_assets/exploration_dashboard_interface.png)
📌 Include a visual schematic of the data journey (e.g. diver metaphor or EDA pipeline)

## 💾 Datasets and Access

- **Trace Metals Dataset** — `321 observations × 27 variables`
- Recommended name: dataset_schema.png
![Dataset Schema](./README_assets/dataset_schema.png
- **Organic Compounds Dataset** — `324 observations × 24 variables`
Recommended name: dataset_schema.png
![Dataset Schema](./README_assets/dataset_schema.png

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
- `shinyjs`, `shinyWidgets` — UI extensions and interactivity

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

📬 For full access to the development history or extended modules, please reach out via **[Email](mailto:euchie23@gmail.com)** or connect on **[LinkedIn](https://www.linkedin.com/)**.
