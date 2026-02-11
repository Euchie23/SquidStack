### 🐙 1. Trace Metals Dataset (`trace_metals.csv`)

Simulated concentrations of trace metal pollutants in squid tissues.

| Column Name         | Type | Description |
|---------------------|------|-------------|
| ID                  | chr  | Unique identifier for each sample |
| Year                | int  | Sampling year (2019–2021) |
| ID_num              | int  | Lab-generated numeric sample ID |
| Area                | int  | Capture area number |
| Tissue              | chr  | Tissue type analyzed (e.g., mantle, digestive gland) |
| Gender              | int  | 0 = Female, 1 = Male |
|dta_km | int     | Distance from squid catch location to a representative reference point on the Argentine shelf (Patagonian shelf) |
|dtfl_km | int       | Distance from squid catch location to a reference point along the north-western Falkland Islands shelf  |
| dtu_km | int     | Distance from squid catch location to the Río de la Plata estuarine reference point  |
|dtb_km | int       | Distance from squid catch location to the Lagoa dos Patos shelf-influenced reference point    |
| Longitude           | chr  | Longitude in DMS format |
| Latitude            | chr  | Latitude in DMS format |
| Month_of_Capture    | int  | Month the sample was caught |
| Mantle_length_mm    | num  | Squid mantle length (mm) |
| Wet_Weight_g        | num  | Squid weight before dissection (grams) |
| Maturity_level      | int  | Maturity stage (per Arkhipkin et al., 1992) |
| DW (Dry Weight)     | num  | Dry weight of tissue used for analysis |
| Metal_A to Metal_J  | num/chr | Simulated metal concentrations (mg/kg), some BLOQ values stored as character strings |

---

### 💊 2. Organic Compounds Dataset (`organic_compounds.csv`)

Simulated organic pollutant data from squid tissues.

| Column Name         | Type | Description |
|---------------------|------|-------------|
| (Same first 14 columns as `trace_metals.csv`) |
| DW (Dry Weight)     | num  | Dry weight of extracted tissue |
| Organic_A to Organic_D | chr | Simulated organic compound concentrations (mg/kg); some values BLOQ |

---

### 🧪 3. Long-Format Dataset (`Long_format.csv`)

Long-format dataset used for analyzing time lags between environmental emissions and bioaccumulated pollutant levels in squid.

| Column Name         | Type  | Description                                                                 |
|---------------------|-------|-----------------------------------------------------------------------------|
| ID                  | chr   | Unique identifier for each sample-tissue combination (e.g., "49_14_muscle") |
| Year                | int   | Year of sample collection (2019–2021)                                       |
| Gender              | int   | 0 = Female, 1 = Male                                                        |
|dta_km | int     | Distance from squid catch location to a representative reference point on the Argentine shelf (Patagonian shelf) |
|dtfl_km | int       | Distance from squid catch location to a reference point along the north-western Falkland Islands shelf  |
| dtu_km | int     | Distance from squid catch location to the Río de la Plata estuarine reference point  |
|dtb_km | int       | Distance from squid catch location to the Lagoa dos Patos shelf-influenced reference point    |
| Longitude           | chr   | Longitude in DMS format                                                     |
| Latitude            | chr   | Latitude in DMS format                                                      |
| Month_of_Capture    | int   | Month sample was captured                                                   |
| Mantle_length_mm    | num   | Squid mantle length (mm)                                                    |
| Wet_Weight_g        | num   | Squid weight before dissection (g)                                          |
| Maturity_level      | int   | Maturity stage (per Arkhipkin et al., 1992)                                 |
| size                | chr   | Size class bin (e.g., "small (181 mm – 237.3 mm)")                          |
| Tissue              | chr   | Tissue type (e.g., muscle, digestive gland)                                 |
| pollutant           | chr   | Pollutant name (e.g., Metal_A, Organic_B)                                   |
| concentration       | num   | Measured concentration (mg/kg); BLOQ values handled separately              |
| status              | chr   | Indicates whether value was "Detected", "BLOQ", or "BLOD"                   |
| outlier             | chr   | "yes" or "no" flag based on outlier detection                               |

---

### 🏭 3. Manufacturing Output Dataset (`manufacturing_output.csv`)

Year-on-year monthly % change in manufacturing output for 3 SWAO-bordering countries.

| Column Name   | Type | Description |
|---------------|------|-------------|
| Month         | int  | Month of % change |
| Country       | chr  | Argentina, Brazil, or Uruguay |
| Year          | int  | Year of % change |
| YoY_%_Change  | num  | % change in manufacturing output compared to same month previous year |

> 📆 Coverage: Nov 2018 – Dec 2021  
> 📍 Source: Trading Economics Website
---

### 🌾 4. Agricultural GDP Dataset (`agri_gdp.csv`)

Quarterly agricultural GDP index values, inflation-adjusted.

| Column Name   | Type | Description |
|---------------|------|-------------|
| Quarter       | chr  | Reporting quarter (e.g.,2018_Oct-Dec) |
| Country       | chr  | Argentina, Brazil, or Uruguay |
| GDP           | num  | Inflation-adjusted index (using index values starting at 100 in the last quarter of 2018) |

> 📆 Coverage: Q4 2018 – Q1 2022  
> 📍 Source: Trading Economics Website
