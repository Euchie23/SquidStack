# 🌊 Fluctuations - Temporal Analysis of Marine Pollution for Early-Stage Risk Assessment

## 🧭 Problem Framing & Decision Context

Marine pollution in *Illex argentinus* can reflect **ecosystem stress driven by industrial and agricultural activity**, and may also respond to **temporary changes in human activity**, such as those seen during the COVID-19 pandemic.

The **Fluctuations Dashboard** explores **temporal patterns** in pollutant concentrations, with special attention to potential **lag effects** between economic activity and bioaccumulation, including the possible **COVID-19 “reprieve”** period in 2020–2021.

This module supports **early-stage monitoring, risk screening, and hypothesis generation**.

---

## 📘 Executive Summary

This dashboard enables stakeholders to explore:

- Year-to-year pollutant trends (2019–2021)  
- Tissue-specific bioaccumulation  
- Potential lag effects between industrial/agricultural activity and contaminant levels  
- Possible environmental “reprieve” during COVID-19 restrictions  

Simulated datasets (reflecting real marine data but anonymized) and public economic indicators allow **interactive temporal analysis** in R Shiny. Insights guide **prioritization for monitoring, assessment, and early warning**, without making causal claims.

---

## 📚 Overview (Species & Analytical Context)

*Illex argentinus* (Argentine shortfin squid) is a key bioindicator for marine contamination. Data include:

- **Trace metals** (cadmium, mercury, copper, etc.)  
- **Organic compounds** (pesticides, industrial chemicals)  
- **Economic indicators**: Manufacturing output and agricultural GDP per country  

Sampling occurred Feb–Apr 2019–2021. The dashboard integrates biological and economic data to allow exploration of **lag effects** and **COVID-related changes** in contamination patterns.

---

## 🌍 Real-World Value

The dashboard translates temporal pollution data into actionable early-stage insights:

**Stakeholders:**  
- Regulators: identify **critical monitoring windows**, including COVID-related shifts  
- Environmental consultancies: **prioritize pollutants and regions** for assessment  
- Fisheries managers: anticipate **ecosystem stress periods**  
- ESG and sustainability teams: contextualize **temporal risk signals**  

**Why It Matters:**  
Temporal analysis, including COVID-19 reprieve effects, helps organizations **plan sampling, evaluate risk, and monitor environmental trends proactively**.

---

## 🔍 Key Validation Findings

- Biological datasets are **simulated**; absolute concentrations are not validated.  
- Temporal associations with economic indicators are **hypothesis-generating**, not causal.  
- COVID-19 “reprieve” signals are exploratory and require **confirmatory follow-up**.

> ⚠️ Consultancy Note: Focus on **relative trends and patterns**, not absolute levels. Lag analysis and reprieve effects are **screening tools** for further investigation.

---

## 🧪 Analytical Workflow

1. **Dockside Briefing:** Overview and dataset context  
2. **Temporal Trends:** Time series of pollutant levels by tissue  
3. **Lag Exploration:** Sliding correlation with industrial/agricultural activity  
4. **Comparative Panels:** Tissue-specific and year-specific comparisons  
5. **Dynamic Insights:** Summary of temporal patterns and potential COVID-19 effects  

All implemented in **R Shiny** with interactive plots, lag sliders, and tooltips.

---

## 📊 Dashboard Access

- **Live Dashboard:** [Fluctuations Dashboard](https://euchie23.shinyapps.io/fluctuations/)  
- **Preview Screenshot:**  
![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1dAi2br9mE_u49_kc97j5pyhvW1qevMag)

---

## 🧪 Datasets

### Biological Datasets (Simulated)

- [`trace_metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/trace_metals.csv)  
- [`organic_compounds.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/organic_compounds.csv)  
- [`Long-Format.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/Data/temp_fluct.csv)

### Economic Datasets (Public)

- [`manufacturing_output.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/Data/manufacturing_output.csv)  
- [`agri_GDP.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Fluctuations/Data/agri_gdp.csv)

> ⚠️ Note: Biological datasets are **simulated** to protect confidentiality; economic datasets are publicly sourced.
> Full column descriptions and data types are in DATA_SCHEMA.md.

---

## 📉 Limitations & Considerations

- Data are **simulated**; do not use absolute values for regulatory purposes.  
- Temporal alignment with economic indicators **does not imply causation**.  
- Lag analysis and COVID-19 reprieve observations are **exploratory**.  
- Focus on **relative patterns** across tissues, years, and pollutants.

> ⚠️ Consultancy framing: This module is designed for **risk screening and early-stage hypothesis generation**, not definitive regulatory assessment.

---

## 📝 Recommendations

- Use the dashboard to identify periods of **elevated risk or potential reprieve**.  
- Prioritize unusual pollutant patterns for **confirmatory assessment**.  
- Compare trends with external environmental or policy events (e.g., COVID-19 lockdowns).  
- Integrate insights into **early-warning or ESG reporting**, highlighting temporal context.

---

## 🧭 Role in the SquidStack Series

- **Module 1 — Foundation:** Exposure data validation  
- **Module 2 — Exploration:** Cross-sectional exploratory analysis  
- **Module 3 — Fluctuations:** Temporal trends, lag effects, and COVID-19 reprieve hypothesis exploration

---

### ⚠️ Data Confidentiality Notice

> The biological datasets (`trace_metals.csv` and `organic_compounds.csv`) are **simulated** to protect sensitive research data. Values are anonymized or modified but structurally mimic real-world observations.  
> The economic datasets are **publicly sourced** and lightly processed for time alignment with biological sampling periods.

---

## 🤝 Invitation to Collaborators

We welcome contributions, feedback, or collaboration from:

- 🌊 Marine biologists & environmental scientists
- 🧪 Ecotoxicologists & pollution analysts
- 🧑‍💻 Shiny developers & R data scientists
- 🏛️ Institutions studying seafood safety or policy impacts
- 🌍 ESG professionals focused on ocean health

Active development takes place in a **private repository** (`squid_Fest`).  
This **public repo** hosts the interactive dashboard and simulated datasets.

📬 For questions or access to extended modules, contact **[Euchie](mailto:euchie23@gmail.com)**  
📇 Or connect via **[LinkedIn](https://www.linkedin.com/in/euchiejnpierre/)**  

> 🦑 *Module 3 of the [SquidStack](https://github.com/Euchie23/SquidStack) series —  focused on marine Pollution, industrial emissions assessments & risk analysis.* <br>
> 📌 This module is the next stage in our data journey from the [**Exploration Dashboard**](https://github.com/Euchie23/SquidStack/edit/main/Exploration/).
[Click here for App](https://euchie23.shinyapps.io/exploration/)
