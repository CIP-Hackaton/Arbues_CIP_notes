# Documentation of the `BrutoaConsiso.ipynb` File

## Required Files

1. **Minimum Temperature:** Folder `T_MIN_NEW` with `.shp` files (monthly).
2. **Maximum Temperature:** Folder `T_MAX_NEW` with `.shp` files (monthly).
3. **Precipitation:** Folder `PRECIPI` with `.shp` files (monthly).
4. **Climate Classification:** File `CLAS_CLIMA/clasificacion_climatica.shp`.
5. **Erosion:** Folder `EROSION` with subfolders by year and `.shp` files.

---

## Internal Workflow

### General Processing
1. Read `.shp` files using `GeoPandas`.
2. Clean data by removing null or inconsistent values.
3. Calculate area-weighted averages for the variable of interest.
4. Consolidate results into tables.

### Specific Variables
- **Minimum/Maximum Temperature and Precipitation:**
  - Calculate monthly/district averages.
  - Generate tables by months.
  - Create thematic maps of Peru by districts.

- **Climate Classification:**
  - Identify the dominant climate classification for each district.
  - Generate thematic maps.

- **Erosion:**
  - Process data annually by district.
  - Calculate area-weighted erosion averages across years.

---

## Final Exports

1. **Minimum Temperature:** `temperaturas_promedio_todos_meses.csv`
2. **Maximum Temperature:** `temperaturas_maximas_promedio_todos_meses.csv`
3. **Precipitation:** `Precipitacion_promedio_todos_meses.csv`
4. **Climate Classification:**
   - `clasificacion_climatica_distritos.csv`
   - Maps: `mapa_sin_leyenda.png`, `leyenda_clasificacion_climatica.png`
5. **Erosion:**
   - `erosion_por_anos.csv`
   - `erosion_promedio.csv`
