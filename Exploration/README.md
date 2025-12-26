# 🤿 Exploration - Exploratory Data Insights for Marine Pollution Risk Assessment

## 🧭 Problem Framing & Decision Context

Following the **Foundation module**, where analytical methods and data credibility were established, the next decision-facing challenge is:

> **Where do potential contamination patterns exist, and which signals are strong enough to justify deeper analysis, monitoring, or risk evaluation?**

At this stage, stakeholders are *not* asking for causal explanations or regulatory thresholds.  
They need **directional insight** to guide:
- sampling priorities,
- analytical focus,
- and downstream risk assessment.

The Exploration module addresses this need by transforming validated (but still complex) contaminant datasets into **interpretable patterns and signals**.

---

## 📘 Executive Summary

The Exploration Dashboard applies exploratory data analysis to simulated contaminant datasets for *Illex argentinus* collected between 2019–2021.

Using correlation analysis, dimensionality reduction (PCA), clustering, and non-parametric statistics, the dashboard investigates how trace metals and organic compounds vary across tissues, biological traits, and years.

This module is **explicitly exploratory**.  
Its role is to **identify patterns, anomalies, and candidate signals** that inform hypothesis development, monitoring design, and the subsequent **Fluctuation** and **Risk Evaluation** stages of SquidStack.

---

## 📚 Overview (Species & Analytical Context)

*Illex argentinus* (Argentine shortfin squid) is a fast-growing, commercially important species in the Southwest Atlantic Ocean and a well-established bioindicator of marine pollution.

Between February and April of 2019–2021, squid tissues were analyzed for:
- **Trace metals**
- **Organic (emerging) contaminants**

This dashboard provides an interactive front-end to explore how contaminant concentrations vary across:
- **Tissues** (e.g., liver, muscle, stomach, ink sac)
- **Biological traits** (sex, size, maturity)
- **Time** (pre-, mid-, and post-COVID sampling years)

> ⚠️ **Data Transparency Note**  
> All data shown are simulated to preserve confidentiality. Variable names and values were anonymized, but the structure reflects real datasets used in the original thesis.

---

## 🌍 Real-World Value

The Exploration module supports **early-stage environmental decision-making** by revealing *where patterns exist* before formal modeling or regulation.

### Practical Value
- **Environmental agencies:** Rapid screening of potential contamination signals  
- **Fisheries managers:** Identification of tissue- or size-specific accumulation trends  
- **Food safety teams:** Prioritization of compounds for further validation  
- **ESG & sustainability analysts:** Evidence-based narrative development without overstating causality  

### Why This Matters
Exploratory insight reduces uncertainty **upstream**, ensuring that resources for validation, monitoring, and risk assessment are deployed strategically rather than reactively.

---


## 🔍 Key Validation Findings

- Tissue-specific accumulation patterns are evident  
- Some biological traits (size, sex, maturity) show differentiated contaminant loads  
- Multivariate analysis (PCA & clustering) identifies grouping trends by tissue and year  
- Organic compounds display higher variability, consistent with known analytical challenges  

> These are **pattern signals**, not confirmed conclusions.

---

## 🧪 Analytical Workflow

### Datasets
Two main datasets drive this dashboard:  
- [`trace_metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/trace_metals.csv) – Measurements of trace metal pollutants across tissues and years  
- [`organic_compounds.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/organic_compounds.csv) – Measurements of organic compounds  

> Full column descriptions and data types are in [DATA_SCHEMA.md](https://github.com/Euchie23/SquidStack/blob/main/Exploration/Data/DATA_SCHEMA.md).

### Workflow Steps
The dashboard follows a staged exploratory workflow:

1. **Dockside Briefing:** Dataset context and roadmap  
2. **Diving In:** Concentration summaries by tissue  
3. **Buddy Diving:** Sex-based pollutant comparisons  
4. **Tiddlers among Titans:** Size-based bioaccumulation patterns  
5. **Riding the Current:** Year-to-year pollutant flows  
6. **Echoes in the Deep:** PCA & K-means clustering  
7. **Shipwrecks and Shadows:** Spearman correlation networks  
8. **Resurfacing:** Summary of patterns and takeaways  

> All implemented in **R Shiny**, enabling interactive exploration and reproducibility.

---

## 📊 Dashboard Access

- **Live Dashboard:** [Exploration Dashboard](https://euchie23.shinyapps.io/exploration/)  
- Screenshot:

![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1FWCFLVcbpxVV6sybB56DgOCKAxhsM_xI)

- Interactive tabs allow exploration by tissue, year, biological trait, and pollutant group.

---

## 📉 Limitations & Considerations 

- **Exploratory Only:** Patterns are intended to guide hypothesis generation, monitoring, and decision-making — not to define regulatory thresholds.  
- **Simulated Data:** All datasets are anonymized or simulated to preserve confidentiality; values do not reflect actual measurements.  
- **Validation Gaps:** Only 7 of 10 trace metals are validated; organic compounds lack full validation.  
- **Relative, Not Absolute:** Focus on patterns (e.g., by tissue, year, or trait) rather than direct numerical comparisons across analytes.  
- **Interpretive Caution:** Results should be treated as **consultancy-grade guidance** for early decision-making, not as conclusive scientific evidence.

> ⚠️ Using this dashboard as a **decision-support tool** is appropriate for exploratory guidance, monitoring prioritization, and early risk assessment.


## 📝 Recommendations

- Prioritize compounds/tissues for **further validation**  
- Refine **sampling design** based on observed patterns  
- Feed candidate signals into the next module, e.g **Fluctuation module** for temporal assessment  
- Reserve regulatory interpretation for the **Risk Evaluation module**

---

## 🧭 Role in the SquidStack Series

- **Foundation Module:** Data credibility and analytical trust  
- **Exploration Module (this):** Pattern discovery and candidate signal identification  
- **Fluctuation Module:** Temporal variation assessment from Exploration Module 
- **Risk Evaluation Module:** Human and ecological impact translation  

> Acts as the **bridge from validated data to actionable insight**.

---

## 🤝 Invitation to Collaborators

We welcome collaboration and feedback from:

- 🧪 Environmental scientists and toxicologists  
- 📊 Data scientists and Shiny developers  
- 🌊 Marine biologists and ecologists  
- 🏛️ Organizations focused on seafood safety and sustainability  
- 🌍 ESG and compliance professionals working in marine environments  

Active development takes place in a **private repository** (`squid_Fest`).  
This **public repo** hosts the interactive dashboard and simulated datasets.

📬 For questions or access to extended modules, contact **[Euchie](mailto:euchie23@gmail.com)**  
📇 Or connect via **[LinkedIn](https://www.linkedin.com/in/euchiejnpierre/)**  

---

> 🦑 *Module 2 of the [SquidStack](https://github.com/Euchie23/SquidStack) series —  focused on marine Pollution, industrial emissions assessments & risk analysis.* <br>
> 📌 This module is the next stage in our data journey from the [**Foundation Dashboard**](https://github.com/Euchie23/SquidStack/edit/main/Foundation/).
[Click here for App](https://euchie23.shinyapps.io/foundation/)
