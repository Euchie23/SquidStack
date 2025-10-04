# 🌊 Fluctuations Dashboard

## 📋 Executive Summary

The **Fluctuations Dashboard** extends the *Illex argentinus* marine pollution investigation by shifting focus from static comparisons to **temporal patterns** — especially in relation to industrial emissions. This module explores how pollution fluctuates **over time** and how **lag effects** between emission and bioaccumulation might emerge.

Using **simulated datasets** modeled after real marine data (with all sensitive information anonymized), this dashboard pairs pollutant concentration data with economic activity indicators (e.g., manufacturing output, agricultural GDP) to help users explore possible cause–effect relationships.

This dashboard is not inferentially conclusive but provides a scalable, interactive tool for exploring marine contamination trends in the Southwest Atlantic Ocean using **R Shiny**.

---

## 🧭 Overview

The **Argentine shortfin squid (*Illex argentinus*)** serves as a vital bioindicator species in marine pollution studies. Between 2019–2021, simulated data approximating real tissue samples were collected during summer months (Feb–Apr) and analyzed for concentrations of:

- 🧲 **Trace metals** (e.g., cadmium, mercury, copper)
- 💊 **Organic compounds** (e.g., pesticides, industrial chemicals)

This dashboard links **pollutant concentrations** to **economic activity metrics** to allow exploration of potential **lag effects** — when contaminants enter marine food webs **months after** spikes in industrial activity.

⚠️ **Data Disclaimer:**  
To comply with research confidentiality protocols, all datasets in this dashboard are **simulated approximations** of original research data. Names, units, and categories have been anonymized, though the overall structure reflects real data collected and analyzed at National Taiwan University.

## 🖼️ Dashboard Preview

![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=YOUR_SCREENSHOT_IMAGE_ID)
*Note: This image shows a cropped view of the full dashboard.*

[🔗 Click here to open the live dashboard](https://euchie23.shinyapps.io/fluctuations/)

## 🧪 Dataset Schema

This dashboard integrates **four main datasets** — two pollutant datasets and two contextual economic datasets to support lag effect analysis.

> 📌 To download: Right-click the links → “Save link as…”  
> If your browser saves the file as `.txt`, rename it to `.csv` after download.

---

### 🎣 Marine Pollution Datasets

These contain biological and environmental metadata along with pollutant concentrations.

- [`trace_metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/data/trace_metals.csv)  
- [`organic_compounds.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/data/organic_compounds.csv)

These share 14 metadata columns (sample ID, sex, size, tissue, capture location, etc.) and contain pollutant values as either `"num"` or `"chr"` (if BLOQ flagged).

---

### 📈 Supporting Industrial Activity Datasets

These help users **compare pollution patterns with regional economic activity**.

- [`manufacturing_output.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/data/manufacturing_output.csv)  
Contains quarterly manufacturing output estimates by country from 2018 to 2023.

- [`agri_GDP.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/data/agri_GDP.csv)  
Reports agriculture’s contribution to GDP by quarter over time.

These datasets are primarily used to investigate **lag effects** between industrial emissions (cause) and bioaccumulated pollutants in squid (effect).

> 💡 A lag effect means there’s a **delay** between an environmental pressure (e.g., spike in manufacturing) and its biological impact (e.g., contaminant uptake in squid).

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
📇 Or connect via **[LinkedIn](https://www.linkedin.com/in/YOUR-LINKEDIN)**  

