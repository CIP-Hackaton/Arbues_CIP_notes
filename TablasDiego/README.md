Resumen del Notebook [DATOS_DIEGO.ipynb](vscode-file://vscode-app/c:/Users/kikhe/AppData/Local/Programs/Microsoft%20VS%20Code/resources/app/out/vs/code/electron-sandbox/workbench/workbench.html)

Este notebook procesa y analiza tres conjuntos principales de datos relacionados con la agricultura en Perú.

#### Archivos de Entrada Necesarios

1. **Agrobiodiversidad**
    
    - `AGROBIODIVERSIDAD_cleaned.csv`
2. **Concentración de Especies**
    
    - `Concentracion_espcies_SHP.csv`
3. **Nevadas**
    
    - `[Enero-Diciembre].csv` (12 archivos, uno por mes)

#### Funcionalidad Principal

1. **Análisis de Agrobiodiversidad**
    
    - Procesamiento de datos de variedades de papa
    - Ubicación geográfica (lat/lon)
    - 6012 registros con información de cultivos
    - No lo usaremso al final
2. **Análisis de Concentración de Especies**
    
    - Datos por distrito/provincia/departamento
    - Categorización de zonas agrícolas
    - Análisis de fuentes de Sentinel 2B
    - No lo usaremso al final
3. **Procesamiento de Nevadas**
    
    - Consolidación de datos mensuales
    - Análisis de frecuencias por UBIGEO
    - Generación de tabla consolidada anual

#### Output Principal

- `consolidado_frecuencia_mensual.csv` - Dataset final con frecuencias mensuales de nevadas por distrito

