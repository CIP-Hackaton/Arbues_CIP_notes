Resumen del Notebook [Prueba.ipynb](vscode-file://vscode-app/c:/Users/kikhe/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html)

Este notebook realiza el análisis y procesamiento de datos de cultivos de papa, enfocándose en:
#### Archivos de Entrada Requeridos

- `SISAGRI.csv` - Datos del sistema agrícola
- `TEM_BIOLO_AGROBIODIVERSIDAD.dbf` - Datos de agrobiodiversidad
- `bd_prospeccion_papa.dbf` - Datos de prospección
- `parcelas_papa.dbf` - Datos de parcelas

#### Funcionalidad Principal

1. **Filtrado inicial de datos**
    
    - Filtra datos específicos de papa del dataset SISAGRI
    - Calcula rendimientos (cosecha/siembra)
    - Elimina registros con valores nulos o cero
2. **Procesamiento de datos de rendimiento**
    
    - Se enfoca en 6 variedades específicas de papa
    - Calcula métricas de rendimiento
    - Elimina datos ambiguos o incompletos
3. **Análisis estadístico**
    
    - Genera estadísticas descriptivas
    - Analiza distribución por departamentos
    - Identifica patrones de cultivo

#### Outputs Generados

- `filtrado_papa.csv` - Datos filtrados de papa
- `papas_filtradas.csv` - Dataset final procesado
- Visualizaciones y estadísticas descriptivas

