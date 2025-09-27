# 🧱 Foundation 🧱📚🦑 

### 📋 Executive Summary

This dashboard is not about patterns or conclusions, it’s about **building trust in the data** through transparent methods and reproducible validation steps.  
It presents the **analytical method validation efforts** that form the backbone of a broader investigation into marine pollution, using *Illex argentinus* as a bioindicator species.

It focuses on the reliability of data obtained from two key instrumental techniques:

- **ICP-MS** for trace metals  
- **LC-MS/MS** for organic compounds  

---

### 🔍 Key Findings

**🧲 Trace Metals**  
- Most metals showed acceptable recovery rates  
- **Metal H** and **Metal J** displayed elevated values, suggesting possible matrix effects or contamination  
- **Metal I** could not be validated due to its absence from the certified reference material (CRM)  
- Further validation is recommended through **spike recovery** or alternate CRMs  

**💊 Organic Compounds**  
- Due to the absence of a compound-specific CRM for squid, a **modified literature-based approach** was adopted  
- The approach is effective as a preliminary method, but requires **further refinement** for consistent use  

---

This foundational work is **critical for ensuring the accuracy and reproducibility** of downstream analyses presented in future dashboards.  
It also supports broader goals in:

- 🐟 Marine pollution monitoring  
- 🧫 Seafood safety  
- ⚖️ Ecotoxicological research and regulation  

By prioritizing high-quality, transparent data, this work strengthens the evidence base for informed **policy, public health, and environmental decision-making**.
.<br><br>

## Overview 📚🦑

*Illex argentinus*, the Argentine shortfin squid, is a crucial species in marine ecosystems and fisheries. Its ability to bioaccumulate pollutants makes it a useful bioindicator for assessing marine pollution levels, particularly in regions with high seafood consumption.
This dashboard presents the analytical workflow and validation protocols used to ensure the accuracy and reliability of contaminant data in *Illex argentinus* (Argentine shortfin squid). It focuses on validating methods for detecting trace metals using ICP-MS and organic compounds using LC-MS/MS, with recovery rates evaluated against certified reference materials (CRMs). While a standard CRM was used for trace metals, organic compound validation relied on adapted literature-based methods due to the lack of a squid-specific CRM — a challenge acknowledged and addressed within the dashboard.<br>

<img src="../docs/Analytical_flowchart.svg" alt="Analytical Workflow">
<sub><i>Notesℹ️ and limitations⚠️ are embedded at key stages to guide interpretation, highlight potential sources of bias, and support informed decision-making during analysis.</i></sub><br><br>

The above flowchart outlines the analytical workflow used to validate methods for detecting trace metals and organic contaminants in *Illex argentinus*. Each stage—sample processing, instrumental analysis, quantification and data preprocessing, and analytical method validation—comprises key steps that together produce two well-structured datasets for statistical analyses. 


![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1wlEd0oB_0hlqFj3MaKRL7xSZT4bFdS5f)
*Note: The screenshot above shows a partial view of the dashboard.*
[(Click here for dashboard)](https://euchie23.shinyapps.io/foundation/)
<br><br>


### 🧪 Analytical Method Validation<br>

####  Method Validation Summary:

- **Trace Metals**: To ensure data reliability, trace metals were quantified using ICP-MS [(Instrument Parameters)](Methodology/Metals/Instrumnt_Param.pdf) with validation performed against Certified Reference Material (NIST CRM 1566b, Oyster Tissue) [(More information provided here)](https://tsapps.nist.gov/srmext/certificates/1566b.pdf). Average recovery rates for metals were calculated, and two metals (Metal H and Metal J) showed recovery rates above the expected average, suggesting the presence of matrix effects or potential contamination in those results. External calibration [(See Calibration Ranges)](Methodology/Metals/Calib_Stand_Rangs.png) and recovery assessments confirmed method accuracy [(View CRM Results CSV)](https://github.com/Euchie23/SquidStack/blob/main/docs/Metals/recovery_rate.csv)  . Metal I, however, could not be validated for accuracy using the selected CRM as it is not included in the cerificate of measurement.<br>

- **Organic Compounds**: Organic contaminants were analyzed by LC-MS/MS [(Instrument Parameters)](Methodology/Organics/Instrumnt_Params.pdf). Due to the complexity of analyzing organic compounds in squid tissue, there is no compound-specific CRM available for organic compounds in squid tissue, validation was based on adapted literature methods (Feo et al., 2020) [(More information provided here)](Methodology/Organics/Anlyt_Method_Valid_Organics.md) with proposed modifications to handle the unique challenges of analyzing organic compounds in marine species.<br><br>


#### Key Insights from Validation:
- **Trace Metals**: Metals H and J showed unusual recovery rates, indicating potential interference or matrix effects. This is an important observation that calls for further investigation to ensure accurate readings. Since Metal I could not be validated using the current CRM, additional validation through spike recovery or alternative reference materials could be used. <br>
  ![Metals_Screenshot](https://drive.google.com/uc?export=view&id=1qaBRQPlTE93RwNKcS_GHjDqk5YU252wp)
  *Note: The screenshot above shows the recovery rate % table for 9 trace metals.* <br><br>
  
- **Organic Compounds**: Since no CRM exists for these compounds, the proposed modified approach (Feo et al., 2020) could improve validation processes, but further refinement is necessary.<br>
 ![Organics_Screenshot](https://drive.google.com/uc?export=view&id=1-1Lcn3j4kFZKxzO1R5HT6lU6Ir_MxhIR)
*Note: The screenshot above is a snippet of the full markdown, linked to the dashboard, which explains the validation status and proposed validation technique for the organic compounds.*
<br><br>

### 📝 Recommendations:

- **Further Investigation**: The unusual recovery rates for Metals H and J need to be explored further to identify the cause of the matrix effects or contamination. Additional studies should focus on refining the analysis for these metals to improve the accuracy of future readings. Future validation efforts by using spike recovery techniques or alternative reference materials may be required, especially for Metal I, due to its abscence in the current CRM and possibly for Metals H and J.

- **Improved Methodology for Organic Compounds**: The proposed method validation approach for organic contaminants, based on Feo et al. (2020), should be tested and refined, possibly with the development of new CRMs for organic compounds in marine species to ensure more accurate results.

- **Future Data Collection**: While the dashboard primarily focuses on method validation, future data collection should prioritize the inclusion of metals not included in current CRMs (such as Metal I), and organic compounds, which currently lack specific CRMs. Expanding the dataset to assess these factors across different tissues and years could increase the chances of these metals and compounds being included in future CRMs. Additionally, this could facilitate the development of more robust methods for validating organic compounds, improving the accuracy of contamination assessments and enhancing future method validation efforts.<br><br>


### 🤝 💬 Invitation to Collaborators and Reviewers 💬 🤝

We welcome contributions to refine methodologies, expand contaminant scopes, and integrate ecological or socioeconomic analyses to deepen understanding and impact. <br>
🛂This repository hosts the public-facing dashboards only. Active development and version control take place in a private repository (Squid_fest) to allow for faster iteration and maintainability. The private repo (squid_Fest) includes additional modules and in-progress work that may not yet be stable or documented, so if you would like access to the development history or full codebase please dont hesitate to contact me 🙂. 🛂.
