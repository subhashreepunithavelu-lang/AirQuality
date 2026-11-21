# Air Quality Analysis (UCI Air Quality Dataset)

## About
This project analyses the **Air Quality UCI dataset** using Python in a Jupyter Notebook. It covers data cleaning, exploration, and visualisation to understand how air pollutants and weather conditions change over time.

## Dataset
- **File:** `AirQualityUCI.csv`
- **Source:** UCI Machine Learning Repository (Air Quality dataset)
- **Records:** 9,357 hourly readings
- **Period:** 10 March 2004 to 4 April 2005
- **Data source:** Readings from a gas multisensor device placed in an Italian city, compared with reference analyser values
- **Format:** Semicolon-separated (`;`) with a decimal comma (`,`)

### Columns
| Column | Description |
|---|---|
| `Date`, `Time` | Date (DD/MM/YYYY) and hour of the reading |
| `CO(GT)` | True hourly average of carbon monoxide (mg/m³) |
| `PT08.S1(CO)` | Tin oxide sensor response (CO) |
| `NMHC(GT)` | True hourly average of non-methane hydrocarbons (µg/m³) |
| `C6H6(GT)` | True hourly average of benzene (µg/m³) |
| `PT08.S2(NMHC)` | Titania sensor response (NMHC) |
| `NOx(GT)` | True hourly average of nitrogen oxides (ppb) |
| `PT08.S3(NOx)` | Tungsten oxide sensor response (NOx) |
| `NO2(GT)` | True hourly average of nitrogen dioxide (µg/m³) |
| `PT08.S4(NO2)` | Tungsten oxide sensor response (NO2) |
| `PT08.S5(O3)` | Indium oxide sensor response (O3) |
| `T` | Temperature (°C) |
| `RH` | Relative humidity (%) |
| `AH` | Absolute humidity |

### Data notes
- Missing values are recorded as **-200** in the dataset and must be replaced with `NaN` during cleaning.
- `NMHC(GT)` has the most missing values (about 90%), so it is usually dropped.
- The file has 114 empty rows and 2 empty trailing columns that need to be removed.

## Notebook
- **File:** `AirQuality.ipynb`
- **What it does:**
  - Loads the CSV with the correct separator and decimal format
  - Cleans the data (removes empty rows/columns, handles -200 values)
  - Explores trends and correlations between pollutants and weather
  - Visualises the results with charts

## How to Run
1. Download or clone this repository
   ```
   git clone https://github.com/subhashreepunithavelu-lang/AirQuality.git
   ```
2. Install the required libraries
   ```
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open the notebook in Jupyter Notebook or Google Colab
4. Load the data using:
   ```python
   import pandas as pd
   df = pd.read_csv("AirQualityUCI.csv", sep=";", decimal=",")
   ```
5. Run all cells

## Tools Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## Author
**Subhashree**
MOP Vaishnav College

## Acknowledgement
Dataset: S. De Vito et al., *Air Quality* dataset, UCI Machine Learning Repository.
