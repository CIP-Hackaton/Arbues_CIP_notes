### Resumen del Notebook: ZONAS DE RIESGO DEL TIZON TARDIO.ipynb

Este notebook procesa y analiza datos geoespaciales relacionados con el riesgo de tizón tardío en Perú para los años 2014-2016.

#### Archivos Necesarios

- `S_2014.asc`, `S_2015.asc`, `S_2016.asc` - Archivos raster con datos de presencial del Tizon Tardio
- `distritos-peru@bogota-laburbano.geojson` - Archivo con límites de distritos
- `consolidado_tizon_distritos.csv` - Archivo de presencia del tizon por distrito

#### Estructura y Funcionalidad

1. **Carga y Visualización de Datos**
    
    - Carga archivos ASC para cada año
    - Visualiza mapas de riesgo usando matplotlib
    - Procesa datos raster a nivel de distrito
2. **Procesamiento Geoespacial**
    
    - Convierte coordenadas raster a geográficas
    - Intersecta datos raster con límites distritales
    - Calcula estadísticas por distrito y año
3. **Generación de Resultados**
    
    - Calcula porcentajes de riesgo por distrito
    - Genera mapas de calor por año
    - Exporta resultados consolidados a CSV

#### Output Principal

- DataFrame con porcentajes de riesgo por distrito para cada año
- Mapas de calor mostrando la distribución espacial del riesgo
- Estadísticas comparativas entre años
