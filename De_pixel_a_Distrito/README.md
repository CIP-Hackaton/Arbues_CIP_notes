# Analysis Plan for Notebook Clima.ipynb

#### Required Files

- `distritos-peru@bogota-laburbano.geojson` - File with geospatial data of districts
- `Clima.ipynb` - Main notebook

#### Structure and Functionality

1. **Initial Setup**
    - Load geospatial libraries
    - Configure Selenium for web scraping

2. **Data Processing**
    - Read GeoJSON data of districts
    - Extract coordinates for each district
    - Visualize data on maps

3. **Web Scraping Attempt**
    - Main function: `clima_scraper_lat_lon_fecha()`
    - Extract meteorological data from Ventusky
    - Generate DataFrame with results

#### Output

- DataFrame with meteorological data:
    - Date
    - Coordinates (lat/lon)
    - Meteorological variables (min/max temperature)
    - District information
