# Documentation of the `JOIN.ipynb` File

## Required Files

1. **Base Inputs:**
   - `temperaturaMax_mensual_distrital.csv`
   - `Temp_min-mensual-distritos.csv`
   - `Precipitacion_mensual_distrital_noAnual.csv`
   - `nevada_distrital_mensual_noAnual.csv`
   - `erosion_distrital_noMensual_NoAnual.csv`
   - `tizon_distrital_noMensual_noAnual.csv`
   - `ClasificacionClimatica_distrital.csv`
   - `6variedades_distrital_mensual_anual.csv`

2. **Temporarily Transformed Tables:**
   - Expanded and normalized tables in long format for each variable.

---

## Internal Workflow

### **1. File Loading**
   - Read each `.csv` file using `pandas`, handling encoding issues (`latin1`).
   - Inspect null values and correct inconsistent column names.

### **2. Transformations**
   - **Temporal Normalization:**
     - Convert to long format (`melt`) for monthly columns.
     - Replicate annual data to monthly levels.
   - **Classification Corrections:**
     - Unify names in `Clasificacion_Climatica`.
     - Group and assign numeric codes.
   - **Numeric Scaling:**
     - Normalize variables like `TEMP_MAX`, `PRECIPITACION`, `NEVADA`, among others, using `MinMaxScaler`.

### **3. Table Joining**
   - **Step 1:** Merge tables by `NOMBDEP`, `NOMBPROV`, `NOMBDIST`, and `MES`.
   - **Step 2:** Include `tizon_distrital` and extended variables such as `PRECIPITACION`, `NEVADA`, and `EROSION_PROMEDIO`.
   - **Step 3:** Integrate variety data (`6variedades_distrital_mensual_anual.csv`).

### **4. Final Preparation**
   - Clean unnecessary columns and normalize missing data.
   - Encode labels (`PRODUCTO`, `Clasificacion_Climatica`) as categorical variables.

---

## Final Exports

1. **Consolidated Tables:**
   - `tabla_consolidada_v2.csv`: Unified and normalized tables.
   - `DistrToVectorNormal.csv`: Table with normalized numerical features.
   - `tabla_preparada_modelo.csv`: Table ready for predictive modeling.

2. **Problem Detection:**
   - `duplicados.csv`: Duplicate records for manual inspection.

---

## Future Use

- **`tabla_preparada_modelo.csv`:** Ready for use in classification or regression models.
- **`DistrToVectorNormal.csv`:** Standard input for models based on feature vectors.
