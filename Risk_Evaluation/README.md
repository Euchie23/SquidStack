# ☣️ Risk Evaluation — Translating Marine Contaminant Data into Human Health Insight

## 🧭 Problem Framing & Decision Context

Seafood contamination data are only meaningful when translated into **human exposure and health risk context**. Concentration values alone do not answer the critical question faced by regulators, public health authorities, and seafood safety professionals:

**Do measured contaminants in squid pose a potential dietary health concern under realistic consumption scenarios?**

The **Risk Evaluation Dashboard** bridges this gap by converting contaminant measurements in *Illex argentinus* into **Estimated Daily Intake (EDI)** and **Hazard Quotient (HQ)** metrics under transparent, adjustable assumptions. This enables **defensible screening-level risk evaluation** rather than raw data inspection.

---

## 📘 Executive Summary

This module allows users to:

- Translate contaminant concentrations into **dietary exposure (EDI)**
- Evaluate potential concern using **Hazard Quotients (HQ)**
- Compare **normal vs. high-exposure (95th percentile)** scenarios
- Explore sensitivity to **body weight, consumption rate, and detection limits (BLOD/BLOQ)**
- Generate **dynamic, consultancy-grade risk interpretations**

The dashboard is designed for **screening, prioritization, and communication**, not regulatory adjudication.

---

## 📚 Overview (Species & Risk Assessment Context)

*Illex argentinus* (Argentine shortfin squid) is widely consumed and occupies a central role in marine food webs, making it a relevant **sentinel species for dietary exposure assessment**.

This module focuses exclusively on:

- **Muscle tissue** (edible portion)
- **Trace metals** (essential and toxic)
- **Organic compounds** (screened where reference doses exist)

Risk metrics are calculated using **internationally accepted dietary risk assessment frameworks**, with assumptions made explicit and adjustable by the user.

---

## 🌍 Real-World Value

The Risk Evaluation dashboard supports **evidence-based decision making** by transforming complex exposure calculations into interpretable outputs.

**Stakeholders include:**

- 🏛️ Public health authorities — screening potential dietary risks
- 🧪 Environmental consultancies — rapid client-facing risk interpretation
- 🐟 Fisheries & seafood safety managers — consumption guidance context
- 🌍 ESG & sustainability teams — human health risk communication

**Why it matters:**  
This module enables **transparent, reproducible, and scenario-based risk screening**, avoiding both false reassurance and over-interpretation of raw contaminant data.

---

## 🔍 Key Validation Notes

- Biological datasets are **simulated** and structurally representative
- Absolute concentrations are **not validated for regulatory use**
- HQ and EDI calculations follow **standard methodologies**
- Results are **screening-level indicators**, not clinical risk estimates

> ⚠️ **Consultancy Note:**  
> Interpret results comparatively and contextually. Focus on **relative risk signals**, dominant contributors, and scenario sensitivity.

---

## 🧪 Risk Evaluation Workflow

1. **Parameter Definition**
   - Country label, body weight, and squid consumption rate
   - BLOD/BLOQ substitution multipliers for non-detects

2. **Scenario Selection**
   - Normal (mean exposure)
   - Extreme (95th percentile exposure)

3. **Risk Metric Calculation**
   - Estimated Daily Intake (EDI)
   - Hazard Quotient (HQ = EDI / RfD)

4. **Interactive Visualization**
   - Dumbbell plots comparing relative exposure versus relative risk
   - Color-coded safety signals to highlight potential concern

5. **Scenario-Based Interpretation & Comparison Engine**
   - Automatically identifies **pollutants of potential concern** within each country–scenario
   - Differentiates **essential, tolerated, and toxic compounds** based on exposure–risk patterns
   - Enables side-by-side comparison of multiple saved country scenarios
   - Flags scenarios that may warrant closer monitoring under specific dietary assumptions

All components are implemented in **R Shiny**, using reactive logic to ensure that visualizations and interpretations update dynamically in response to user-defined assumptions.


---

## 📊 Dashboard Access

- **Preview Screenshot:**  
![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1gx1il39MQFfgQkFV0oLrQAhquYcdzPpH)
- **Live Dashboard:** [Risk Evaluation Dashboard](https://euchie23.shinyapps.io/risk_evaluation/)  
- **Module Location:** `SquidStack/Risk_Evaluation/`

---

## 🧪 Datasets

### Biological Data (Simulated)

The Risk Evaluation module primarily utilizes the **long-format analytical dataset originally developed for the Fluctuations dashboard**. This dataset, previously titled **`Long-Format Dataset(Long_format.csv)`** (see [*Fluctuation Data Schema*](https://github.com/Euchie23/SquidStack/blob/main/Fluctuations/Data/DATA_SCHEMA.md)), was renamed to **`risk_eval`** for use in this application.

Because the dataset already integrated **both trace metal and organic compound measurements in a unified long format**, it provided a consistent and efficient foundation for dietary exposure and risk calculations. This structure enabled direct computation of Estimated Daily Intake (EDI) and Hazard Quotients (HQ) without additional reshaping of analyte-level data.

Only the **subset of variables required for risk evaluation**—including analyte identity, concentration, tissue type, year, and detection status (BLOD/BLOQ)—was extracted and processed. All biological values remain **simulated and anonymized**, while preserving realistic data structure and relationships.


### Reference Data

- Oral Reference Doses (RfDs) sourced from:
  - U.S. EPA
  - Peer-reviewed toxicological literature

> ⚠️ **Data Note:**  
> Datasets are **simulated** for confidentiality and demonstration purposes. Structural integrity mirrors real monitoring data.

---

## 📉 Limitations & Considerations

- Results are **screening-level**, not regulatory determinations
- HQ > 1 indicates **potential concern**, not confirmed harm
- Organic compounds without RfDs are **excluded from risk scoring**
- Detection limit handling (BLOD/BLOQ) introduces uncertainty

> ⚠️ Use this module to **prioritize follow-up**, not replace formal risk assessment.

---

## 📝 Recommendations

- Compare **normal vs. extreme scenarios** to assess sensitivity
- Focus on **dominant contributors to HQ**
- Flag metals with **low exposure but high toxicity**
- Contextualize essential metals separately from toxicants
- Document assumptions using the built-in **logbook system**

---

## 🧭 Role in the SquidStack Series

- **Module 1 — Foundation:** Data integrity & validation
- **Module 2 — Exploration:** Cross-sectional contamination patterns
- **Module 3 — Fluctuations:** Temporal trends & lag effects
- **Module 4 — Risk Evaluation:** Human dietary exposure & risk translation *(this module)*

---

## ⚠️ Data Confidentiality Notice

All biological datasets used in this module are **simulated** to protect sensitive research data.  
Values are anonymized but structurally representative of real-world observations.  
Interpretations should be used for **methodological demonstration and screening only**.

---

## 🤝 Invitation to Collaborators

We welcome collaboration from:

- 🧪 Ecotoxicologists & exposure scientists
- 🌊 Marine pollution researchers
- 🧑‍💻 R / Shiny developers
- 🏛️ Public health & seafood safety professionals
- 🌍 ESG and sustainability analysts

Active development takes place in a **private repository** (`squid_Fest`).  
This **public repo** hosts the interactive dashboard and simulated datasets.

📬 For questions or access to extended modules, contact **[Euchie](mailto:euchie23@gmail.com)**  
📇 Or connect via **[LinkedIn](https://www.linkedin.com/in/euchiejnpierre/)**  

> 🦑 *Module 4 of the SquidStack series — translating marine contamination data into actionable human health insight.*
> 📌 This module is the next stage in our data journey from the [**Fluctuations Dashboard**](https://github.com/Euchie23/SquidStack/edit/main/Fluctuations/).
[Click here for App](https://euchie23.shinyapps.io/fluctuation/)
