# Documentation of the `Demanda` Folder

## Required Files

1. **Base Data:**
   - `volumen.csv`: Monthly volume for each variety of potato.
   - `precio_max_papas_por_mes.csv`: Monthly maximum prices for each potato variety.
   - `precio_min_papas_por_mes.csv`: Monthly minimum prices for each potato variety.
   - `precio_prom_papas_por_mes.csv`: Monthly average prices for each potato variety.

2. **Generated Files:**
   - `demanda.csv`: Consolidation of prices and volume by variety.
   - SARIMA models (saved in `MODELOS ENTRENADOS`).

---

## Internal Workflow

### **1. Data Consolidation (`CrearDataSetDemanda.ipynb`)**
   - **Inputs:**
     - Price files (`precio_max_papas_por_mes.csv`, `precio_min_papas_por_mes.csv`, `precio_prom_papas_por_mes.csv`).
     - Volume file (`volumen.csv`).
   - **Processes:**
     - Transformation to long format (`melt`) to unify month columns into rows.
     - Data merging by `Fecha` and `VariedadPapa` using `merge`.
   - **Output:**
     - `demanda.csv`: Consolidated file with the following columns:
       - `Fecha`, `VariedadPapa`, `PMax`, `PMin`, `PProm`, `Volumen`.

### **2. Demand Analysis and Modeling (`DEMANDA.ipynb`)**
   - **Data Loading and Cleaning:**
     - Reading `demanda.csv` and validating for null or inconsistent data.
     - Normalizing dates (`YYYY-MM-DD`) and filtering by time range.
   - **Exploratory Analysis:**
     - Visualization of time series (volume and average price).
     - Inspection of unique values and descriptive statistics.
   - **SARIMA Modeling:**
     - Training a SARIMA model for each potato variety.
     - Automatic hyperparameter optimization using `pmdarima.auto_arima`.
     - Forecasting future demand until December 2025.
   - **Performance Metrics:**
     - Model evaluation using MAE and RMSE (normalized and original scale).
   - **Saving Models:**
     - Trained models saved in the `MODELOS ENTRENADOS` folder as `.pkl` files.

---

## Final Exports

1. **Consolidated Data:**
   - `demanda.csv`: Base file for demand analysis.

2. **Trained Models:**
   - `.pkl` files in the `MODELOS ENTRENADOS` folder:
     - `sarima_model_Papa_Amarilla.pkl`, `sarima_model_Papa_Blanca.pkl`, etc.

3. **Predictions and Visualizations:**
   - Time series of historical demand and future projections by variety.
   - Performance charts (residuals, metrics, and projected demand).

---

## Future Use

- **`demanda.csv`:** Base file for analysis and prediction generation.
- **SARIMA Models:** Forecast future demand for each potato variety.
- **Visualizations:** Inspect historical and projected trends.
