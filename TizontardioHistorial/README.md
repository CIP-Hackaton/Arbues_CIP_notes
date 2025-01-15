### Summary of the Notebook: ZONAS DE RIESGO DEL TIZÓN TARDÍO.ipynb

This notebook processes and analyzes geospatial data related to the risk of late blight in Peru for the years 2014-2016.

---

#### Required Files

- `S_2014.asc`, `S_2015.asc`, `S_2016.asc` - Raster files with late blight presence data
- `distritos-peru@bogota-laburbano.geojson` - File with district boundaries
- `consolidado_tizon_distritos.csv` - File with late blight presence by district

---

#### Structure and Functionality

1. **Data Loading and Visualization**
   - Loads ASC files for each year
   - Visualizes risk maps using Matplotlib
   - Processes raster data at the district level

2. **Geospatial Processing**
   - Converts raster coordinates to geographic coordinates
   - Intersects raster data with district boundaries
   - Calculates statistics by district and year

3. **Result Generation**
   - Calculates risk percentages by district
   - Generates heat maps for each year
   - Exports consolidated results to a CSV file

---

#### Main Output

- DataFrame with risk percentages by district for each year
- Heat maps showing the spatial distribution of risk
- Comparative statistics between years
