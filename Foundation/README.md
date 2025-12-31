# 🧱 Foundation — Exposure Data Validation for Marine Pollution Risk Assessment

## 🧭 Problem Framing & Decision Context
Environmental and human health risk assessments depend on the credibility of underlying exposure data.  
Before trends, spatial patterns, or risk metrics can be interpreted, analytical methods must be shown to be **fit-for-purpose, transparent, and reproducible**.

This module establishes the **data credibility baseline** for the SquidStack series by validating analytical methods used to quantify contaminants in *Illex argentinus*, a widely consumed and ecologically relevant species. It addresses a critical decision question:

> *Can these contaminant measurements be trusted for downstream ecological interpretation and human exposure risk evaluation?*

---

## 📘 Executive Summary
This dashboard focuses on **method validation rather than interpretation**, providing transparent QA/QC evidence for contaminant data used throughout the SquidStack pipeline.

Two instrumental techniques are evaluated:
- **ICP-MS** for trace metals  
- **LC-MS/MS** for organic compounds  

Validation results identify which analytes are robust, which require caution, and where additional verification is needed before results can inform risk assessment or policy-relevant conclusions.

---


## 📚 Overview — Species & Analytical Context

*Illex argentinus* (Argentine shortfin squid) is a commercially important species and a useful bioindicator due to its capacity to bioaccumulate environmental contaminants.  
Given high seafood consumption in parts of the South West Atlantic, reliable contaminant measurements are critical for both **ecological assessment** and **human exposure evaluation**.

This module presents the analytical workflow and validation protocols used to ensure data reliability before any interpretation of pollution patterns or risk metrics is attempted.

---

## 🌍 Real-World Value
The Foundation module provides the **analytical assurance layer** required for defensible environmental and food safety decision-making.

### Who This Helps
- **Regulators & agencies:** confirm data suitability before compliance or advisory use  
- **Food safety authorities:** validate inputs for EDI and hazard quotient models  
- **Environmental consultancies:** demonstrate due diligence and uncertainty transparency  
- **Researchers:** understand method limits prior to inference  

### Why It Matters
Without validated methods, downstream dashboards and risk indicators may be misleading.  
This module reduces **false confidence risk** by clearly defining where data are reliable, uncertain, or unsuitable for interpretation.

---

## 🔍 Key Validation Findings (Decision-Relevant)

### 🧲 Trace Metals (ICP-MS)
- Most metals showed acceptable recovery against CRM benchmarks  
- **Metal H and Metal J:** elevated recovery rates → potential matrix effects or contamination  
- **Metal I:** could not be validated due to absence from CRM  
- **Implication:** Metals H, I, and J require caution or additional validation before use in risk metrics  

### 💊 Organic Compounds (LC-MS/MS)
- No squid-specific CRM available  
- Validation based on adapted literature methodology  
- **Implication:** Suitable for exploratory screening, not regulatory thresholds  

> 🔬 Detailed recovery tables, instrument parameters, and calibration ranges are available via linked documentation for users requiring full technical review.

---

## 🧪 Analytical Workflow (Overview)
The workflow below summarizes the analytical pipeline from sample processing to validated datasets.  
Notes and limitations are embedded at each stage to guide interpretation and prevent misuse.

<img src="../docs/Analytical_flowchart.svg" alt="Analytical Workflow">

---

## 🧭 Implications for Risk Assessment & Next Steps
- Metals showing matrix effects require secondary validation (e.g. spike recovery)  
- Organic compound results should be interpreted as **screening-level evidence**  
- Expansion of reference materials would materially reduce uncertainty  
- These findings define **where downstream risk analyses are robust vs exploratory**

---

## 📊 Dashboard Access
![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1bWfy7A7wf4PUSUG3hI8052f2CNQkX5Wr)

🔗 **[Launch the Foundation Dashboard](https://euchie23.shinyapps.io/foundation/)**  
*Dashboard supports interactive review of recovery rates, validation status, and analytical assumptions.*

---

## 📉 Limitations & Considerations

From a consultancy and risk-assessment perspective, the following limitations define **how the data should be used**, not whether it is usable.

- Some analytes lack squid-specific Certified Reference Materials  
- Elevated recoveries for certain metals indicate potential matrix effects  
- Organic compound validation remains screening-level  
- Results are suitable for trend exploration and risk modeling inputs, not direct regulatory enforcement  

These constraints reflect analytical chemistry realities rather than study design flaws and are explicitly documented to support responsible interpretation.

---

## 📝 Recommendations

- Conduct spike recovery or alternative CRM validation for Metals H, I, and J prior to regulatory or threshold-based use  
- Treat organic compound concentrations as semi-quantitative until further validation is completed  
- Maintain uncertainty flags when integrating these data into exposure or risk dashboards  
- Expand validation across tissues and sampling years to strengthen future assessments  

---

## 🧭 Role in the SquidStack Series

This module represents the **Foundation** stage of the SquidStack thesis-to-application workflow:

1. **Foundation** — Analytical validation *(this module)*  
2. **Exploration** — Data structure and exploratory analysis  
3. **Fluctuation** — Temporal variability in contaminant loads  
4. **Risk Evaluation** — Human exposure and impact assessment *(in progress)*  

All subsequent modules rely on the validation boundaries established here.

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

---

> 🦑 *Module 1 of the [SquidStack](https://github.com/Euchie23/SquidStack) series — focused on marine Pollution, industrial emissions assessments & risk analysis.* 
