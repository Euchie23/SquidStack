# 🦑📚 SquidStack — Interactive Dashboards for Marine Pollution & Risk Analysis

## Overview 📚🃏

**SquidStack** is a collection of interactive dashboards built from my master's thesis at **National Taiwan University (2021–2024)**, which investigated chemical contamination in *Illex argentinus* (Argentine shortfin squid) in the Southwest Atlantic Ocean.

This work translates field and lab research into engaging, modular dashboards that help **non-technical users, researchers, and environmental advocates** explore patterns in marine pollution and assess potential human health risks. 

> 🛂 **Note:** This repository hosts the **public-facing dashboards only.** > Active development, full code history, and extended modules are maintained in a private repository: Squid_Fest. > To request access to the full codebase or development version history, [please contact me](mailto:euchiejnpierre@gmail.com). 🙂

---

## 📦 Repository Overview Each SquidStack module represents a stage in the journey — from setting sail to navigating deep patterns and surfacing human risks. 

| Module | Nickname | Description | Status | Link | 
|--------|----------|-------------|--------|------| 
| 🧱 [**Foundation**](https://euchie23.shinyapps.io/foundation/) | *The Chart Room* 🧭 | Preparing for the journey — study design, lab protocols, and data validation workflows | ✅ Complete | [View README](https://github.com/Euchie23/SquidStack/tree/main/Foundation) | 
| 🧪 [**Exploration**](https://euchie23.shinyapps.io/exploration/) | *The Deep Dive* 🤿 | Visualizing chemical detections and surfacing early patterns | ✅ Complete | [View README](https://github.com/Euchie23/SquidStack/tree/main/Exploration) | 
| 📈 **Fluctuation** | *Currents & Tides* 🌊 | Temporal analysis and regression lag modeling based on industrial/agricultural activity | [**Fluctuations**](https://euchie23.shinyapps.io/fluctuation/) | [View README](https://github.com/Euchie23/SquidStack/tree/main/Fluctuations) | 
| ⚠️ **Risk Evaluation** | *The Surface Impact* ☣️ | Estimating human health risks using EDI and HQ models | 🔄 In progress | Coming soon |

🕹️ **Click here to see the [SquidStack Changelog](CHANGELOG.md)** — All updates to modules, dashboards, and workflows are tracked here for transparency and version control.

--- 

## 🎯 Project Objectives 
- 🧪 Evaluate marine ecosystem health using short-lived bioindicator species (*Illex argentinus*)
- 📊 Identify spatial and temporal patterns of pollutant contamination, including during the COVID-19 era
- ⚖️ Estimate human health risks associated with seafood consumption (Argentina & Taiwan focus)
- 💡 Build accessible dashboards to engage non-technical stakeholders in environmental science
  
---

## 🛠️ Tools & Techniques Used in SquidStack

Each module reflects a different set of tools and analytical approaches. Below are the methods **specifically used in this public repository**:

- **Dashboard Development:** R, Shiny, BS4Dash (`All Modules`)
- **Data Cleaning & Wrangling:** R (tidyverse, `qs` for efficient file I/O), Excel (`All Modules`)
- **Statistical Analysis:**  
  - ANOVA, Kruskal-Wallis, Mann-Whitney U, Dunn’s test, Tukey HSD (`Exploration`)  
  - Spearman’s correlation (`Exploration`, `Fluctuation`)
- **Time Series Modeling:**  
  - Regression lag effect modeling to analyze pollutant bioaccumulation delay relative to emissions (`Fluctuation`)
- **Human Health Risk Assessment:**  
  - Estimated Daily Intake (EDI) (`Risk Evaluation`)  
  - Hazard Quotient (HQ) modeling (`Risk Evaluation`)
- **Visualization:** ggplot2, plotly, DT tables (`All Modules`)

---

## ⚠️ Data Confidentiality & Ethics

To protect research integrity and comply with ethical standards:

- All datasets are **simulated**, based on the structure of real laboratory and field data.
- **Pollutant names and sensitive variables were anonymized**.
- Interpretations should be seen as methodological demonstrations, not actual marine condition assessments.

---

## 🎓 Research Background

This repository reflects part of a larger thesis project conducted at **National Taiwan University** in collaboration with:

- Analytical chemists
- Oceanographers
- Fisheries scientists
- Environmental data specialists

The work included:
- Lab-based dissection, sample prep, and mass spectrometry analysis
- Manual and automated data cleaning
- Development of dashboards for exploratory and communicative analysis

---

## 👥 Who Should Explore This Repo?

This project is for:

- 🧪 Researchers in marine science, food safety, or toxicology
- 🧠 Students exploring environmental data workflows
- 📈 Data scientists interested in ecological and health risk modeling
- 🌍 Policymakers, NGOs, and the curious public

Whether you're here to visualize pollutant patterns, refine risk models, suggest improvements, or just vibe with ocean data — you're welcome aboard.

---

## 🧭 Get Involved

Got feedback, ideas, or questions?

- 🐛 [Open an issue](https://github.com/Euchie23/SquidStack/issues) — Report bugs, suggest new dashboard features, or ask a question
- ✉️ [Email me](mailto:euchiejnpierre@gmail.com) — For private collaboration or access to the full `Squid_Fest` repo
- 💼 [Connect on LinkedIn](https://www.linkedin.com/in/euchiejnpierre/) — Let’s discuss data, environment, or research

---

## 🔒 Related Project

- 🔒 `Squid_Fest` *(Private Repository)* — The full version-controlled research project including:
  - Geospatial and temporal modeling
  - Early-stage and experimental modules
  - Complete data pipelines and codebase

---

> Thanks for exploring SquidStack. Let’s make marine science more open, interactive, and impactful — one dashboard at a time. 🌊🦑📊
