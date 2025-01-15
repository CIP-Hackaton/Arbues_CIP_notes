# Summary of the Notebook [DATOS_DIEGO.ipynb](vscode-file://vscode-app/c:/Users/kikhe/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html)

This notebook processes and analyzes three main datasets related to agriculture in Peru.

---

#### Required Input Files

1. **Agrobiodiversity**
   - `AGROBIODIVERSIDAD_cleaned.csv`

2. **Species Concentration**
   - `Concentracion_espcies_SHP.csv`

3. **Snowfall**
   - `[Enero-Diciembre].csv` (12 files, one for each month)

---

#### Main Functionality

1. **Agrobiodiversity Analysis**
   - Processes data on potato varieties
   - Includes geographic location (lat/lon)
   - 6,012 records with crop information
   - **Note:** Will not be used in the final analysis

2. **Species Concentration Analysis**
   - Data by district/province/department
   - Categorizes agricultural zones
   - Analyzes sources from Sentinel 2B
   - **Note:** Will not be used in the final analysis

3. **Snowfall Processing**
   - Consolidates monthly data
   - Analyzes snowfall frequencies by UBIGEO
   - Generates an annual consolidated table

---

#### Primary Output

- `consolidado_frecuencia_mensual.csv` - Final dataset with monthly snowfall frequencies by district
