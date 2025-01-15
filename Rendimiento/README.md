# Summary of the Notebook [Prueba.ipynb](vscode-file://vscode-app/c:/Users/kikhe/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html)

This notebook performs data analysis and processing for potato crops, focusing on the following:

#### Required Input Files

- `SISAGRI.csv` - Agricultural system data
- `TEM_BIOLO_AGROBIODIVERSIDAD.dbf` - Agrobiodiversity data
- `bd_prospeccion_papa.dbf` - Prospection data
- `parcelas_papa.dbf` - Plot data

---

#### Main Functionality

1. **Initial Data Filtering**
   - Filters potato-specific data from the SISAGRI dataset
   - Calculates yields (harvest/planting ratio)
   - Removes records with null or zero values

2. **Yield Data Processing**
   - Focuses on six specific potato varieties
   - Calculates yield metrics
   - Eliminates ambiguous or incomplete data

3. **Statistical Analysis**
   - Generates descriptive statistics
   - Analyzes distribution by departments
   - Identifies cultivation patterns

---

#### Generated Outputs

- `filtrado_papa.csv` - Filtered potato data
- `papas_filtradas.csv` - Final processed dataset for the six selected potato varieties
- Visualizations and descriptive statistics
