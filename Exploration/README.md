# 🤿 Exploration Dashboard

## 📋 Executive Summary

This dashboard continues the investigation into marine pollution in *Illex argentinus* by transitioning from method validation (Foundation Module) to exploratory data analysis. It focuses on uncovering patterns in contaminant concentrations across tissues, years, and biological traits — while maintaining transparency about data limitations and simulation use.

Using simulated datasets resembling real observations (to preserve confidentiality), this dashboard applies correlation, dimensionality reduction, clustering, pollutant interaction analysis, and statistical testing to investigate pollutant behavior across 2019–2021.

Although the results are exploratory and not inferentially conclusive, this tool plays a key role in identifying leads for future hypothesis testing and risk assessment, while showcasing scalable analytical workflows in R Shiny.

---

## 🌍 Real-World Value

The Exploration dashboard transforms raw marine chemistry data into **actionable environmental insights**.  
It helps users quickly spot patterns in contamination across tissues, seasons, and biological traits — informing early decisions before formal modeling.

### Who This Helps
- **Environmental agencies:** identify potential pollution hotspots or emerging contaminants  
- **Fisheries managers:** monitor tissue-specific bioaccumulation patterns  
- **Food safety teams:** flag risk-relevant pollutants for deeper testing  
- **ESG & sustainability analysts:** track ecological indicators for reporting  

### Why It Matters
This module highlights **where and when pollution patterns change**, so organizations can prioritize sampling, regulation, and monitoring efforts based on evidence — not guesswork.

---

🎯 Applied Use Cases

The Exploration Dashboard is designed for **early-stage environmental insight generation**, helping stakeholders identify where deeper analysis, validation, or intervention may be needed before formal modeling or regulation.

**Example Use Cases:**

**1. Pollution Signal Screening**
Environmental agencies can quickly explore which contaminants:
- Appear consistently elevated across tissues
- Show unusual patterns across years or seasons
- Vary strongly by biological traits (size, sex, maturity)

This supports rapid screening before committing resources to confirmatory studies.

**2. Targeted Monitoring & Sampling Design**
Fisheries and monitoring programs can use observed patterns to:
- Prioritize specific tissues for routine testing
- Adjust sampling timing based on seasonal variability
- Identify species subgroups that may be more vulnerable to bioaccumulation

**3. Food Safety Risk Prioritization**
Food safety teams can use exploratory summaries to flag compounds that:
- Concentrate in edible tissues
- Show increasing trends over time
- Cluster with other known risk-relevant contaminants

These insights help guide which compounds warrant deeper toxicological assessment.

**4. ESG & Environmental Reporting**
ESG and sustainability analysts can use the dashboard to:
- Contextualize contamination signals across time
- Support narrative reporting on environmental pressure
- Identify emerging issues without overstating causality

⚠️ **Important Note:**  
This dashboard is exploratory by design. Patterns observed here are intended to guide hypothesis generation, monitoring priorities, and follow-up analysis — not to support causal inference or regulatory thresholds on their own.

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
> 📌 To download: Right-click the link → "Save link as..." → If your browser tries to save it as a `.txt` file, simply rename the extension to `.csv` before saving.

- [`trace_metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/trace_metals.csv): Contains measurements of trace metal pollutants.
- [`organic_compounds.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/organic_compounds.csv): Contains measurements of organic compound pollutants.

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
> 📌 To download datasets: Right-click the link → "Save link as..." → If your browser tries to save it as a `.txt` file, simply rename the extension to `.csv` before saving.

| Stage | Tab Title                | Description                                     |Dataset
|-------|--------------------------|-------------------------------------------------|----------------------------| 
| 1     | ⛴️ Dockside Briefing     | Intro, roadmap, and dataset context             |         Not Needed     |
| 2     | 🐙 Diving In              | Analyte concentration summaries by tissue      | [`Diving In Organics.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Org_Diving_In.csv) and [`Diving In Metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Met_Diving_in.csv)                   |
| 3     | 🧍‍♂️ Buddy Diving         | Sex-based pollutant comparisons                  |      [`Long_Dataset.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Long_Dataset.csv)                    |
| 4     | 📏 Tiddlers among Titans | Size-based bioaccumulation patterns             |      `Long_Dataset.csv`           |
| 5     | 🌊 Riding the Current     | Year-to-year pollutant flows by tissue          |     `Long_Dataset.csv`              |
| 6     | 📚 Echoes in the Deep     | PCA & K-Means cluster analysis                  |     [`Wide_Dataset.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Wide_Dataset.csv)             |
| 7     | ⚗️ Shipwrecks and Shadows | Correlation networks (Spearman)                 |     `Long_Dataset.csv`          |
| 8     | 🧠 Resurfacing            | Summary of patterns and takeaways               |          Not Needed         |

---

## 🎯 Exploratory Objectives

- 📅 Examine temporal trends in pollutant concentrations (2019–2021)  
- ⚥ Compare pollutant loads by sex and maturity status  
- 📏 Investigate body size relationships with contaminant levels  
- 🧪 Assess tissue-specific differences in accumulation  
- 📚 Apply unsupervised learning (PCA & clustering) to identify hidden patterns  
- 🌐 Analyze pollutant co-occurrence via correlation matrices  

---

## 🧠 Potential Insights to Explore

> 🔎 *These are exploratory hypotheses based on initial observations or existing literature. The dashboard allows users to investigate patterns interactively — these are not confirmed conclusions.*

- Seasonal and size-based differences may be present across pollutant types  
- Cluster analysis could reveal meaningful groupings by tissue and year  
- Certain pollutants may appear to co-occur, suggesting shared sources or accumulation behavior  
- Organic compound variability might be higher, likely due to matrix effects or validation limitations  

> ⚠️ Reminder: Only 7 out of 10 trace metals were validated, and none of the organic pollutants underwent full validation.
As such, caution is strongly advised when interpreting absolute concentration values, especially for organic compounds.
For more meaningful insights, consider focusing on relative differences or patterns (e.g., by tissue, season, or location) rather than direct numerical comparisons across analytes. <br>
> 📎 For more information on this issue, see the [Foundations README](https://github.com/Euchie23/SquidStack/tree/main/Foundation)
 or visit the [Dashboard](https://euchie23.shinyapps.io/foundation/)
 for guided exploration.
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

This dashboard was developed in  **R(Version 2023.06.0+421)** using **R Shiny** and the following packages:

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

### ✨ Custom Features
- 📚 **Tooltip Citations** — hoverable in-app references for scholarly transparency
  
---

Active development takes place in a **private repository** (`squid_Fest`).  
This **public repo** hosts the interactive dashboard and simulated datasets.

📬 For full access to the development history or extended modules, please reach out via **[Email](mailto:euchie23@gmail.com)** or connect on **[LinkedIn](https://www.linkedin.com/in/euchiejnpierre/)** 😃.

> 🦑 *Module 2 of the [SquidStack](https://github.com/Euchie23/SquidStack) series —  focused on marine Pollution, industrial emissions assessments & risk analysis.* <br>
> 📌 This module is the next stage in our data journey from the [**Foundation Dashboard**](https://github.com/Euchie23/SquidStack/edit/main/Foundation/README.md).
[Click here for App](https://euchie23.shinyapps.io/foundation/)
