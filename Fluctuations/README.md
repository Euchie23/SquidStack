# 🌊 Fluctuations Dashboard

## 📋 Executive Summary

The **Fluctuations Dashboard** extends the *Illex argentinus* marine pollution investigation by shifting focus from static comparisons to **temporal patterns** — especially in relation to industrial emissions. This module explores how pollution fluctuates **over time** and how **lag effects** between emission and bioaccumulation might emerge.

Using **simulated datasets** modeled after real marine data (with all sensitive information anonymized), this dashboard pairs pollutant concentration data with economic activity indicators (e.g., manufacturing output, agricultural GDP) to help users explore possible cause–effect relationships.

This dashboard is not inferentially conclusive but provides a scalable, interactive tool for exploring marine contamination trends in the Southwest Atlantic Ocean using **R Shiny**.

---

## 🧭 Overview

The Argentine shortfin squid (*Illex argentinus*) serves as a vital bioindicator species in marine pollution studies. Between 2019–2021, simulated data approximating real tissue samples were collected during summer months (Feb–Apr) and analyzed for concentrations of:

🧲 **Trace metals** (e.g., cadmium, mercury, copper)  
💊 **Organic compounds** (e.g., pesticides, industrial chemicals)

This dashboard introduces a unique integration of environmental and economic data. Alongside pollutant concentrations, it incorporates:

- 📉 **Manufacturing Output (% change YoY)** for Argentina, Brazil, and Uruguay (monthly; late 2018–2021)
- 🌾 **Agricultural GDP (Inflation-adjusted Index)** for Argentina, Brazil, and Uruguay — capturing quarterly shifts in agro-industrial activity (Q4 2018–Q1 2022)

These supporting datasets allow users to explore potential **lag effects** — where spikes in industrial or agricultural activity may result in delayed pollutant accumulation in marine organisms like squid.


## 🧪 Dataset Schema

This dashboard draws from the **four datasets** mentioned above. You can find downloadable links below for exploration and reproducibility.

> 📌 To download: Right-click the link → "Save link as..."  
> If your browser tries to save it as a `.txt` file, simply rename the extension to `.csv` before saving.


> 📌 To download: Right-click the link → "Save link as..." → If your browser tries to save it as a `.txt` file, simply rename the extension to `.csv` before saving.

---

### 🎣 Marine Pollution Datasets

These share 14 metadata columns (sample ID, sex, size, tissue, capture location, etc.) and contain pollutant values as either `"num"` or `"chr"` (if BLOQ flagged).

- [`trace_metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/trace_metals.csv)  
- [`organic_compounds.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/organic_compounds.csv)

---

### 📈 Supporting Industrial Activity Datasets

These help users **compare pollution patterns with regional economic activity**.

- [`manufacturing_output.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/Data/manufacturing_output.csv)  
Contains quarterly manufacturing output estimates by country from 2018 to 2023.

- [`agri_GDP.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/Data/agri_gdp.csv)  
Reports agriculture’s contribution to GDP by quarter over time.

---

### 🐙 1. Trace Metals Dataset (`trace_metals.csv`)

Simulated concentrations of trace metal pollutants in squid tissues.

| Column Name         | Type | Description |
|---------------------|------|-------------|
| ID                  | chr  | Unique identifier for each sample |
| Year                | int  | Sampling year (2019–2021) |
| ID_num              | int  | Lab-generated numeric sample ID |
| Area                | int  | Capture area number |
| Tissue              | chr  | Tissue type analyzed (e.g., mantle, digestive gland) |
| Gender              | int  | 0 = Female, 1 = Male |
| dta_km              | int  | Distance (km) to Argentina shoreline |
| dtfl_km             | int  | Distance (km) to Falkland Islands |
| Longitude           | chr  | Longitude in DMS format |
| Latitude            | chr  | Latitude in DMS format |
| Month_of_Capture    | int  | Month the sample was caught |
| Mantle_length_mm    | num  | Squid mantle length (mm) |
| Wet_Weight_g        | num  | Squid weight before dissection (grams) |
| Maturity_level      | int  | Maturity stage (per Arkhipkin et al., 1992) |
| DW (Dry Weight)     | num  | Dry weight of tissue used for analysis |
| Metal_A to Metal_J  | num/chr | Simulated metal concentrations (mg/kg), some BLOQ values stored as character strings |

---

### 💊 2. Organic Compounds Dataset (`organic_compounds.csv`)

Simulated organic pollutant data from squid tissues.

| Column Name         | Type | Description |
|---------------------|------|-------------|
| (Same first 14 columns as `trace_metals.csv`) |
| DW (Dry Weight)     | num  | Dry weight of extracted tissue |
| Organic_A to Organic_D | chr | Simulated organic compound concentrations (mg/kg); some values BLOQ |

---

### 🏭 3. Manufacturing Output Dataset (`manufacturing_output.csv`)

Year-on-year monthly % change in manufacturing output for 3 SWAO-bordering countries.

| Column Name   | Type | Description |
|---------------|------|-------------|
| Month         | int  | Month of % change |
| Country       | chr  | Argentina, Brazil, or Uruguay |
| Year          | int  | Year of % change |
| YoY_%_Change  | num  | % change in manufacturing output compared to same month previous year |

> 📆 Coverage: Nov 2018 – Dec 2021  
> 📍 Source: Trading Economics Website
---

### 🌾 4. Agricultural GDP Dataset (`agri_gdp.csv`)

Quarterly agricultural GDP index values, inflation-adjusted.

| Column Name   | Type | Description |
|---------------|------|-------------|
| Quarter       | chr  | Reporting quarter (e.g.,2018_Oct-Dec) |
| Country       | chr  | Argentina, Brazil, or Uruguay |
| GDP           | num  | Inflation-adjusted index (using index values starting at 100 in the last quarter of 2018) |

> 📆 Coverage: Q4 2018 – Q1 2022  
> 📍 Source: Trading Economics Website

---

### ⚠️ Data Confidentiality Notice

> The biological datasets (`trace_metals.csv` and `organic_compounds.csv`) are **simulated** to protect sensitive research data. Values are anonymized or modified but structurally mimic real-world observations.  
> The economic datasets are **publicly sourced** and lightly processed for time alignment with biological sampling periods.

---

## 🖼️ Dashboard Preview
![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1dAi2br9mE_u49_kc97j5pyhvW1qevMag)
*Note: This image shows a cropped view of the full dashboard.*

[🔗 Click here to open the live dashboard](https://euchie23.shinyapps.io/fluctuations/)

---

## 🧠 Dashboard Highlights

In the **Fluctuations module**, we explore:

📅 **Year-to-Year Trends** in contaminant levels  
🧬 **Tissue-Specific Uptake** of metals and organics  
📈 **Disruption Patterns** during and after COVID-19  
⏳ **Lag Effects** between emissions and bioaccumulation  
> 🧭 Users can slide between 0–12 months to simulate the delay between economic surges and pollutant detection in squid tissues.

## 🎯 Exploratory Objectives

- 📅 Reveal temporal shifts in pollutant levels (2019–2021)
- 🧪 Track how contamination changes across squid tissues
- 📊 Compare patterns with industrial/agricultural surges
- ⏳ Investigate time lags between emissions and detection
- 🔍 Provide contextual understanding of ecosystem stress

## 📊 Core Analytical Components

The Fluctuations dashboard includes:

- **Time Series Plots** of pollutant levels across quarters  
- **Comparative Panels** linking squid contamination with regional manufacturing/agriculture data  
- **Lag Correlation Sliders** allowing users to shift timelines and test for delayed effects  
- **Dynamic Tooltips & Caveat Sections** that clarify dataset limitations, validation levels, and guidance for interpreting simulated data

## 🛠️ Built With

This dashboard was developed in **R (Version 2023.06.0+421)** using **Shiny** and includes several custom features and visualization techniques to enhance exploration of temporal pollution dynamics.

### 📦 Core Frameworks
- `shiny`, `bs4Dash`, `shinyWidgets`, `shinyjs`, `shinydashboard` — for responsive UI and interactivity
- `qs`, `memoise` — for efficient data loading and caching

### 📈 Visualization & Layout
- `ggplot2`, `plotly`, `ggnewscale`, `grid`, `gridExtra` — for multi-layered and interactive visualizations

### 🧪 Statistical Testing & Post-Hoc Comparisons
- `FSA`, `agricolae`, `rcompanion`, `MASS` — for ANOVA, Tukey HSD, Dunn's test, and compact letter displays (CLDs)

### 📆 Temporal & Correlation Analysis
- `lubridate`, `zoo` — for date handling, rolling averages, and time-based transformations
- **Cross-correlation analysis** — used to detect **lag effects** between industrial output and squid pollutant concentrations

### 🌐 Data Import
- `googlesheets4`, `tidyverse` — for reading online economic indicators (manufacturing and agriculture data) and general data wrangling

### ✨ Custom Features
- 🧭 **Lag Slider** — allows users to adjust and visualize temporal lag effects between industrial activity and bioaccumulation
- 📚 **Tooltip Citations** — hoverable in-app references for scholarly transparency
- 📊 **Dynamic Cross-Correlation Visuals** — highlight potential cause-effect timing between emissions and marine contamination


---

## 🛂 Repository Notes

This dashboard is part of a larger marine pollution research project using *Illex argentinus* as a bioindicator of ecological health in the South West Atlantic Ocean. It builds on the foundational work conducted in the **[Foundation](https://github.com/Euchie23/SquidStack/tree/main/Foundation)** and **[Exploration](https://github.com/Euchie23/SquidStack/tree/main/Exploration)** modules.

> 📎 For more background, visit the [SquidStack GitHub Repository](https://github.com/Euchie23/SquidStack)


## 🤝 Invitation to Collaborators

We welcome contributions, feedback, or collaboration from:

- 🌊 Marine biologists & environmental scientists
- 🧪 Ecotoxicologists & pollution analysts
- 🧑‍💻 Shiny developers & R data scientists
- 🏛️ Institutions studying seafood safety or policy impacts
- 🌍 ESG professionals focused on ocean health

📬 For questions or access to extended modules, contact **[Euchie](mailto:euchie23@gmail.com)**  
📇 Or connect via **[LinkedIn](www.linkedin.com/in/euchiejnpierre/)**  

