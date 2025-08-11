# 🧱 Foundation 🧱📚🦑

## Overview 📚🦑

Illex argentinus, the Argentine shortfin squid, is a crucial species in marine ecosystems and fisheries. Its ability to bioaccumulate pollutants makes it a useful bioindicator for assessing marine pollution levels, particularly in regions with high seafood consumption. The dashboard presents our analytical workflow for trace metal analysis and organic compound contamination, which aims to ensure the reliability and accuracy of the analytical methods used in this study.<br>

![Analytical Flowchart](../docs/Analytical_flowchart.svg)
*This flowchart outlines the analytical workflow used to validate methods for detecting trace metals and organic contaminants in Illex argentinus. Each step represents a key stage in sample preparation, instrumental analysis, and data quality assessment, including checks against established validity ranges. Deviations—such as higher-than-range results for two metals. Notes and limitations are embedded at key stages to guide interpretation, highlight potential sources of bias, and support informed decision-making during analysis.*

### Summary
This project primarily focuses on validating analytical methods used to detect trace metals and organic contaminants in squid tissues. The dashboard displays average recovery rates for trace metals and details the approach taken to validate the detection of organic compounds, acknowledging the complexity of the method and the lack of a specific Certified Reference Material (CRM) for organic compounds in squid tissues. 

![Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1PD2BbKdcjNXCILbI2lW43rVXJX92xunH)
*Note: The screenshot above shows a partial view of the dashboard.*
<br><br>


### 🧪 Analytical Method Validation<br>


####  Method Validation Summary:

- **Trace Metals**: To ensure data reliability, trace metals were quantified using ICP-MS [(Instrument Parameters)](Methodology/Metals/Instrumnt_Param.pdf) with validation performed against Certified Reference Material (NIST CRM 1566b, Oyster Tissue) [(More information provided here)](https://tsapps.nist.gov/srmext/certificates/1566b.pdf). Average recovery rates for metals were calculated, and two metals (Metal H and Metal J) showed recovery rates above the expected average, suggesting the presence of matrix effects or potential contamination in those results. External calibration [(See Calibration Ranges)](Methodology/Metals/Calib_Stand_Rangs.png) and recovery assessments confirmed method accuracy [(View CRM Results CSV)](https://github.com/Euchie23/SquidStack/blob/main/docs/Metals/recovery_rate.csv)  . Metal I, however, could not be validated for accuracy using the selected CRM as it is not included in the cerificate of measurement.<br>

- **Organic Compounds**: Organic contaminants were analyzed by LC-MS/MS [(Instrument Parameters)](Methodology/Organics/Instrumnt_Params.pdf). Due to the complexity of analyzing organic compounds in squid tissue, there is no compound-specific CRM available for organic compounds in squid tissue, validation was based on adapted literature methods (Feo et al., 2020) [(More information provided here)](Methodology/Organics/Anlyt_Method_Valid_Organics.md) with proposed modifications to handle the unique challenges of analyzing organic compounds in marine species.<br><br>


#### Key Insights from Validation:
- **Trace Metals**: Metals H and J showed unusual recovery rates, indicating potential interference or matrix effects. This is an important observation that calls for further investigation to ensure accurate readings. Since Metal I could not be validated using the current CRM, additional validation through spike recovery or alternative reference materials could be used. <br>
  ![Metals_Screenshot](https://drive.google.com/uc?export=view&id=1lm4IUYNWdwMEkOOJQAaUIYPSUNJRmfzI)
  *Note: The screenshot above shows the recovery rate % table for 9 trace metals.* <br><br>
  
- **Organic Compounds**: Since no CRM exists for these compounds, the proposed modified approach (Feo et al., 2020) could improve validation processes, but further refinement is necessary.<br>
 ![Organics_Screenshot](https://drive.google.com/uc?export=view&id=1-1Lcn3j4kFZKxzO1R5HT6lU6Ir_MxhIR)
*Note: The screenshot above is a snippet of the full markdown, linked to the dashboard, which explains the validation status and proposed validation technique for the organic compounds.*
<br><br>

### 📋 Executive Summary:
This dashboard provides an overview of method validation efforts for trace metals and organic contaminants in squid tissues. A primary concern is the elevated recovery rates for certain metals (Metal H and Metal J), which may indicate matrix effects or contamination. Additionally, Metal I could not be validated for accuracy due to its absence in the certificate of measurement for the current CRM. To address this, future validation efforts may require the use of spike recovery techniques or alternative reference materials for Metal I and possibly Metals H and J.

For organic compounds, the lack of an appropriate CRM led to a modified validation approach. While promising, this approach requires further refinement. This study is vital for ensuring the reliability of contamination data, which will guide future research and policy decisions regarding marine pollution and public health.<br><br>

### 📝 Recommendations:

- **Further Investigation**: The unusual recovery rates for Metals H and J need to be explored further to identify the cause of the matrix effects or contamination. Additional studies should focus on refining the analysis for these metals to improve the accuracy of future readings. Future validation efforts by using spike recovery techniques or alternative reference materials may be required, especially for Metal I, due to its abscence in the current CRM and possibly for Metals H and J.

- **Improved Methodology for Organic Compounds**: The proposed method validation approach for organic contaminants, based on Feo et al. (2020), should be tested and refined, possibly with the development of new CRMs for organic compounds in marine species to ensure more accurate results.

- **Future Data Collection**: While the dashboard primarily focuses on method validation, future data collection should prioritize the inclusion of metals not included in current CRMs (such as Metal I), and organic compounds, which currently lack specific CRMs. Expanding the dataset to assess these factors across different tissues and years could increase the chances of these metals and compounds being included in future CRMs. Additionally, this could facilitate the development of more robust methods for validating organic compounds, improving the accuracy of contamination assessments and enhancing future method validation efforts.<br><br>


### 🤝 💬 Invitation to Collaborators and Reviewers 💬 🤝

We welcome contributions to refine methodologies, expand contaminant scopes, and integrate ecological or socioeconomic analyses to deepen understanding and impact.
