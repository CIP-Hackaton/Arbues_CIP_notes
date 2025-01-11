Plan de Análisis del Notebook Clima.ipynb

#### Archivos Necesarios

- `distritos-peru@bogota-laburbano.geojson` - Archivo con datos geoespaciales de distritos
- `Clima.ipynb` - Notebook principal
#### Estructura y Funcionalidad

1. **Configuración Inicial**
    
    - Carga de librerías geoespaciales
    - Configuración de Selenium para scraping
2. **Procesamiento de Datos**
    
    - Lee datos GeoJSON de distritos
    - Extrae coordenadas para cada distrito
    - Visualiza datos en mapas
3.  **Intento de Web Scraping**
    
    - Función principal: `clima_scraper_lat_lon_fecha()`
    - Extrae datos meteorológicos de Ventusky
    - Genera DataFrame con resultados

#### Output

- DataFrame con datos meteorológicos:
    - Fecha
    - Coordenadas (lat/lon)
    - Variables meteorológicas (temperatura min/max)
    - Información del distrito

