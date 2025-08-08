# 🧱 Foundation 🧱📚🦑

## Overview 📚🦑

Illex argentinus, the Argentine shortfin squid, is a crucial species in marine ecosystems and fisheries. Its ability to bioaccumulate pollutants makes it a useful bioindicator for assessing marine pollution levels, particularly in regions with high seafood consumption. The dashboard presents an analysis of method validation for trace metal analysis and organic compound contamination, which aims to ensure the reliability and accuracy of the analytical methods used in this study.<br>

### Summary
This project primarily focuses on validating analytical methods used to detect trace metals and organic contaminants in squid tissues. The dashboard displays average recovery rates for trace metals and details the approach taken to validate the detection of organic compounds, acknowledging the complexity of the method and the lack of a specific Certified Reference Material (CRM) for organic compounds in squid tissues. <br><br>


### 🧪 Analytical Method Validation<br>


####  Method Validation Summary:

- **Trace Metals**: To ensure data reliability, trace metals were quantified using ICP-MS [(Instrument Parameters)](Methodology/Metals/Instrumnt_Param.pdf) with validation performed against Certified Reference Material (NIST CRM 1566b, Oyster Tissue) [(More information provided here)](https://tsapps.nist.gov/srmext/certificates/1566b.pdf). Average recovery rates for metals were calculated, and two metals (Metal H and Metal J) showed recovery rates above the expected average, suggesting the presence of matrix effects or potential contamination in those results. External calibration [(See Calibration Ranges)](Methodology/Metals/Calib_Stand_Rangs.png) and recovery assessments confirmed method accuracy [(View CRM Results CSV)](https://github.com/Euchie23/SquidStack/blob/main/docs/Metals/recovery_rate.csv)  . Metal I, however, could not be validated for accuracy using the selected CRM as it is not included in the cerificate of measurement.<br>

- **Organic Compounds**: Organic contaminants were analyzed by LC-MS/MS [(Instrument Parameters)](Methodology/Organics/Instrumnt_Params.pdf). Due to the complexity of analyzing organic compounds in squid tissue, there is no compound-specific CRM available for organic compounds in squid tissue, validation was based on adapted literature methods (Feo et al., 2020) [(More information provided here)](Methodology/Organics/Anlyt_Method_Valid_Organics.md) with proposed modifications to handle the unique challenges of analyzing organic compounds in marine species.<br><br>


#### Key Insights from Validation:
- **Trace Metals**: Metals H and J showed unusual recovery rates, indicating potential interference or matrix effects. This is an important observation that calls for further investigation to ensure accurate readings. Since Metal I could not be validated using the current CRM, additional validation through spike recovery or alternative reference materials could be used.

- **Organic Compounds**: Since no CRM exists for these compounds, the proposed modified approach (Feo et al., 2020) could improve validation processes, but further refinement is necessary.

### Executive Summary:
This dashboard provides an overview of method validation efforts for trace metals and organic contaminants in squid tissues. A primary concern is the elevated recovery rates for certain metals (Metal H and Metal J), which may indicate matrix effects or contamination. Additionally, Metal I could not be validated for accuracy due to its absence in the certificate of measurement for the current CRM. To address this, future validation efforts may require the use of spike recovery techniques or alternative reference materials for Metal I and possibly Metals H and J.

For organic compounds, the lack of an appropriate CRM led to a modified validation approach. While promising, this approach requires further refinement. This study is vital for ensuring the reliability of contamination data, which will guide future research and policy decisions regarding marine pollution and public health.

### Recommendations:

- **Further Investigation**: The unusual recovery rates for Metals I and J need to be explored further to identify the cause of the matrix effects or contamination. Additional studies should focus on refining the analysis for these metals to improve the accuracy of future readings.

- **Improved Methodology for Organic Compounds**: The proposed method validation approach for organic contaminants, based on Feo et al. (2020), should be tested and refined, possibly with the development of new CRMs for organic compounds in marine species to ensure more accurate results.

- **Future Data Collection**: While the dashboard focuses on validation, future projects could expand to include a larger dataset to assess actual contamination levels in various tissues and years, which could then be used for further analytical insights.<br><br>


### 🤝 💬 Invitation to Collaborators and Reviewers 💬 🤝

We welcome contributions to refine methodologies, expand contaminant scopes, and integrate ecological or socioeconomic analyses to deepen understanding and impact.
