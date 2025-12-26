Both datasets share 14 columns containing metadata such as sample ID, location, date, and biological measurements like length and weight. The remaining columns report analyte concentrations specific to each dataset type.

> 📝 **Note:**  
> Columns labeled as `"int"` contain whole numbers, while `"num"` columns contain decimal (real) values. Some concentration columns are `"chr"` (character), indicating values flagged as **below the limit of quantification (BLOQ)**. These BLOQ indicators replace actual measurements. If a concentration column is `"num"`, all values were above the LOQ and are considered detected.

> ⚠️ Reminder: Metal and organic compound names (e.g., Metal_A, Organic_B) are anonymized to maintain confidentiality.

### 🔁 Shared Columns (1–14)

| Column Name       | Data Type | Description                       |
|-------------------|-----------|-----------------------------------|
| ID     | chr    | Unique identifier for the sample |
| Year              | int     | Year of capture  |
| ID_num        | int     | ID # given in fisheries science lab |
| Area   | int      | Area # given by fishing vessel   |
| Tissue             | chr     | Squid tissues analyzed  |
| Gender (0=Females, 1=Males)| int     | Squid genders analyzed  |
| dta_km (distance to Argentina in Km)| int     | Measured distance (Google Earth) from catch location to the shores of Argentina        |
|dtfl_km (distance to Falkand Islands in km)| int       | Measured distance (Google Earth) from catch location to the shores of the Falkland Islands        |
| Longitude          | chr     | longitude coordinates strings (DMS) of catch location   |
| Latitude           | chr     | latitude coordinates strings (DMS) of catch location   |
| Month_of_Capture   | int     | Month of capture for squids|
| Mantle_length_ mm  | num     | Squid Mantle Length measured in milli meters  |
|Wet Weight_g        | num     | Full squid body weight measured in lab (grams) before dissection  |
| Maturity_level     | int     | Squid maturity level assessed based on a paper by Arkhipkin et al, 1992 |


### 🧲 Trace Metals Dataset (`trace_metals.csv`)

| Column Name     | Data Type | Description                         |
|-----------------|-----------|-------------------------------------|
| DW (Dry Weight) | num       |Weight of the freeze-dried, ground tissue sample aliquot used for extraction and analysis|
| Metal_A         | num       | Metal_A concentration (mg/kg)    |
| Metal_B         | num       | Metal_B concentration (mg/kg)    |
| Metal_C         | num       | Metal_C concentration (mg/kg)    |
| Metal_D         | num       | Metal_D concentration (mg/kg)    |
| Metal_E         | num       | Metal_E concentration (mg/kg)    |
| Metal_F         | chr       | Metal_F concentration (mg/kg)    |
| Metal_G         | num       | Metal_G concentration (mg/kg)    |
| Metal_H         | chr       | Metal_H concentration (mg/kg)    |
| Metal_I         | chr      | Metal_I concentration (mg/kg)    |
| Metal_J         | chr       | Metal_J concentration (mg/kg)    |

### 🌱 Organic Compounds Dataset (`organic_compounds.csv`)

| Column Name       | Data Type | Description                             |
|-------------------|-----------|-----------------------------------------|
| DW (Dry Weight) | num     | Weight of the freeze-dried, ground tissue sample aliquot used for extraction and analysis |
| Organic_A       | chr     | Organic_A concentration (mg/kg)            |
| Organic_B       | chr     | Organic_B concentration (mg/kg)            |
| Organic_C       | chr     | Organic_C concentration (mg/kg)            |
| Organic_D       | chr     | Organic_D concentration (mg/kg)            |


## 📊 Analytical Approaches

The dashboard is structured across 8 interactive tabs — each representing a stage in the data dive:
> 📌 To download datasets: Right-click the link → "Save link as..." → If your browser tries to save it as a `.txt` file, simply rename the extension to `.csv` before saving.

| Stage | Tab Title                | Description                                     |Dataset
|-------|--------------------------|-------------------------------------------------|----------------------------| 
| 1     | ⛴️ Dockside Briefing     | Intro, roadmap, and dataset context             |         Not Needed     |
| 2     | 🐙 Diving In              | Analyte concentration summaries by tissue      | [`Diving In Organics.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Org_Diving_In.csv) and [`Diving In Metals.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Met_Diving_in.csv)                   |
| 3     | 🧍‍♂️ Buddy Diving         | Sex-based pollutant comparisons                  |      [`Long_Dataset.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Long_Dataset.csv)                    |
| 4     | 📏 Tiddlers among Titans | Size-based bioaccumulation patterns             |      `Long_Dataset.csv`           |
| 5     | 🌊 Riding the Current     | Year-to-year pollutant flows by tissue          |     `Long_Dataset.csv`              |
| 6     | 📚 Echoes in the Deep     | PCA & K-Means cluster analysis                  |     [`Wide_Dataset.csv`](https://raw.githubusercontent.com/Euchie23/SquidStack/main/Exploration/data/Wide_Dataset.csv)             |
| 7     | ⚗️ Shipwrecks and Shadows | Correlation networks (Spearman)                 |     `Long_Dataset.csv`          |
| 8     | 🧠 Resurfacing            | Summary of patterns and takeaways               |          Not Needed         |
