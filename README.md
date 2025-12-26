# 🦑📚 SquidStack — Interactive Dashboards for Marine Pollution & Risk Analysis

## 🌍 Real-World Value

SquidStack converts multi-year lab and field research into **actionable marine pollution intelligence**.  
These dashboards provide **decision-ready insights** on contamination patterns, ecological risks, and seafood safety in the Southwest Atlantic Ocean.

### Problem Statement
Marine ecosystems in the Southwest Atlantic are increasingly impacted by industrial and agricultural activity. Bioaccumulation of contaminants in *Illex argentinus* signals ecosystem stress and potential human health risk, yet stakeholders often lack tools to quickly identify trends, temporal patterns, or early warning signals.

### Decision Context
SquidStack dashboards enable **regulators, environmental agencies, fisheries managers, and public health teams** to:  
- Detect changes in contaminant levels over time  
- Assess ecological and human health implications  
- Prioritize monitoring, compliance, and mitigation efforts  
- Communicate insights clearly to non-technical stakeholders  

---

## Overview 📚🃏

**SquidStack** is a modular collection of interactive dashboards built from my master's thesis at **National Taiwan University (2021–2024)**, focused on chemical contamination in *Illex argentinus* (Argentine shortfin squid).  

These dashboards translate field and lab research into **explorable insights**, supporting early detection of environmental stress and aiding evidence-based decision-making. 

> 🛂 **Note:** This repository hosts **public-facing dashboards only.** Full code history and extended modules are maintained in a private repository: `Squid_Fest`. To request access, [contact me](mailto:euchiejnpierre@gmail.com).

---

## 📦 Repository Overview

Each SquidStack module represents a stage in the analytical journey — from validating data to surfacing actionable insights.  

| Module | Nickname | Value | Status | Link | 
|--------|----------|-------|--------|------| 
| 🧱 [**Foundation**](https://euchie23.shinyapps.io/foundation/) | *The Chart Room* 🧭 | Validates data and prepares stakeholders for reliable insights | ✅ Complete | [View README](https://github.com/Euchie23/SquidStack/tree/main/Foundation) | 
| 🧪 [**Exploration**](https://euchie23.shinyapps.io/exploration/) | *The Deep Dive* 🤿 | Reveals statistical patterns in pollutant data to guide analysis priorities | ✅ Complete | [View README](https://github.com/Euchie23/SquidStack/tree/main/Exploration) | 
| 📈 [**Fluctuations**](https://euchie23.shinyapps.io/fluctuation/) | *Currents & Tides* 🌊 | Detects temporal trends and lag effects for proactive environmental monitoring | ✅ Complete | [View README](https://github.com/Euchie23/SquidStack/tree/main/Fluctuations) | 
| ⚠️ **Risk Evaluation** | *The Surface Impact* ☣️ | Estimates human health risks to inform seafood safety decisions | 🔄 In progress | Coming soon |

🕹️ **Click here to see the [SquidStack Changelog](CHANGELOG.md)** — All updates to modules, dashboards, and workflows are tracked for transparency.

---

## 🎯 Project Objectives
- 🧪 Evaluate ecosystem health using bioindicator species (*Illex argentinus*)  
- 📊 Detect temporal patterns and correlations in contaminant data, including COVID-19 effects  
- ⚖️ Support human health risk estimation for seafood consumption (Argentina & Taiwan)  
- 💡 Provide accessible dashboards for non-technical stakeholders to explore marine pollution trends  

---

## 🛠️ Tools & Techniques

**Public modules use the following techniques for actionable insights:**

- **Dashboard Development:** R, Shiny, BS4Dash  
- **Data Cleaning & Wrangling:** R (tidyverse, `qs`), Excel  
- **Statistical Analysis:**  
  - ANOVA, Kruskal-Wallis, Mann-Whitney U, Dunn’s test, Tukey HSD (`Exploration`)  
  - Spearman’s correlation (`Exploration`, `Fluctuation`)  
- **Time Series Modeling:** Regression lag analysis to detect bioaccumulation delays (`Fluctuation`)  
- **Human Health Risk Assessment:** Estimated Daily Intake (EDI) and Hazard Quotient (HQ) (`Risk Evaluation`)  
- **Visualization:** ggplot2, plotly, DT tables  

> Each tool is applied to **generate insights that support evidence-based decisions**.

---

## ⚠️ Data Confidentiality & Ethics

- All datasets are **simulated**, preserving real data structure.  
- **Pollutant names and sensitive variables are anonymized.**  
- Interpretations serve as **methodological demonstrations** rather than actual marine condition assessments.

---

## 🎓 Research Background

This project reflects a broader thesis at **National Taiwan University**, in collaboration with:

- Analytical chemists  
- Oceanographers  
- Fisheries scientists  
- Environmental data specialists  

Key activities included:

- Lab-based dissection, sample prep, and mass spectrometry  
- Automated and manual data cleaning  
- Development of **interactive dashboards for insight generation**  

---

## 👥 Who Should Explore SquidStack

- 🧪 Researchers in marine science, toxicology, and food safety  
- 🧠 Students learning environmental data workflows  
- 📈 Data scientists focused on ecological and health risk modeling  
- 🌍 Policymakers, NGOs, and stakeholders needing **evidence-driven insights**  

---

## 🧭 Get Involved

- 🐛 [Open an issue](https://github.com/Euchie23/SquidStack/issues) — Report bugs or suggest features  
- ✉️ [Email me](mailto:euchiejnpierre@gmail.com) — Private collaboration or access to `Squid_Fest`  
- 💼 [Connect on LinkedIn](https://www.linkedin.com/in/euchiejnpierre/) — Discuss data, environment, or research  

---

## 🔒 Related Project

- 🔒 `Squid_Fest` *(Private Repository)* — Full version-controlled research including:  
  - Geospatial and temporal modeling  
  - Experimental modules  
  - Complete data pipelines and codebase  

---

**Key Takeaways:**  
1. Quickly identify temporal trends and statistical patterns in contamination data  
2. Prioritize monitoring and mitigation efforts based on dashboard insights  
3. Evaluate lagged bioaccumulation to anticipate ecological and health risks  
4. Export insights for reporting, policy, or environmental management  

> Thanks for exploring SquidStack — making marine science interactive, insightful, and actionable. 🌊🦑📊
