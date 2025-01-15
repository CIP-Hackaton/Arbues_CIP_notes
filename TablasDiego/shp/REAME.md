# Documentación del archivo `BrutoaConsiso.ipynb`

## Archivos Requeridos
1. **Temperatura mínima:** Carpeta `T_MIN_NEW` con archivos `.shp` (mensuales).
2. **Temperatura máxima:** Carpeta `T_MAX_NEW` con archivos `.shp` (mensuales).
3. **Precipitación:** Carpeta `PRECIPI` con archivos `.shp` (mensuales).
4. **Clasificación climática:** Archivo `CLAS_CLIMA/clasificacion_climatica.shp`.
5. **Erosión:** Carpeta `EROSION` con subcarpetas por año y archivos `.shp`.

---

## Flujo Interno

### Procesamiento General
1. Leer datos `.shp` con `GeoPandas`.
2. Limpiar datos eliminando valores nulos o inconsistentes.
3. Calcular promedio ponderado (por área) de la variable de interés.
4. Consolidar resultados en tablas.

### Variables Específicas
- **Temperatura mínima/máxima y precipitación:**
  - Promedios calculados por mes/distrito.
  - Generación de tablas por meses.
  - Mapas temáticos de Perú por distritos.
  
- **Clasificación climática:**
  - Identificación de la clasificación climática dominante en cada distrito.
  - Generación de mapas temáticos.

- **Erosión:**
  - Procesamiento anual por distrito.
  - Cálculo de promedio ponderado de erosión entre años.

---

## Exportaciones Finales
1. **Temperatura mínima:** `temperaturas_promedio_todos_meses.csv`
2. **Temperatura máxima:** `temperaturas_maximas_promedio_todos_meses.csv`
3. **Precipitación:** `Precipitacion_promedio_todos_meses.csv`
4. **Clasificación climática:**
   - `clasificacion_climatica_distritos.csv`
   - Mapas: `mapa_sin_leyenda.png`, `leyenda_clasificacion_climatica.png`
5. **Erosión:**
   - `erosion_por_anos.csv`
   - `erosion_promedio.csv`
