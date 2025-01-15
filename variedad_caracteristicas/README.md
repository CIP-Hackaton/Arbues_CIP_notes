# README para Archivos de Datos

## Archivos Requeridos

1. **`Variedad_a_Caracteristicas_28.csv`**
   - Contiene características cualitativas y cuantitativas de variedades de papa.
   - Columnas principales:
     - Variety: Nombre de la variedad.
     - Late blight (LB): Resistencia a tizón tardío.
     - Predominant tuber flesh color: Color predominante de la carne del tubérculo.
     - Tuber shape depth of eyes: Profundidad de los ojos del tubérculo.
     - Dry matter (%): Porcentaje de materia seca.
     - Growing period highland: Periodo de crecimiento en tierras altas.

2. **`caracteristicas.csv`**
   - Contiene datos extendidos de variedades de papa, con características adicionales.
   - Columnas principales:
     - Similar a las de `Variedad_a_Caracteristicas_28.csv`, con la adición de:
       - Predominant tuber skin color: Color predominante de la piel del tubérculo.
       - General tuber shape: Forma general del tubérculo.

3. **`Variedad_a_Caracteristicas_28_numeric (1).csv`**
   - Versión numérica de `Variedad_a_Caracteristicas_28.csv`.
   - Columnas categóricas convertidas a variables binarias o codificadas numéricamente:
     - Late blight (LB): Codificado como 0, 1, 2, 3.
     - Predominant tuber flesh color y Tuber shape depth of eyes: Codificadas como variables dummy.

## Flujos Internos

1. **Limpieza y Conversión:**
   - Limpieza básica de datos en columnas.
   - Conversión de valores categóricos a numéricos para análisis cuantitativo.
   
2. **Agrupación y Filtrado:**
   - Agrupación por variedad para consolidar características comunes.
   - Inclusión de columnas adicionales en `caracteristicas.csv` para análisis más detallado.

3. **Salida:**
   - Datos cualitativos y cuantitativos procesados y exportados en CSV.

## Exportaciones Finales

- **Archivos finales generados:**
  1. `Variedad_a_Caracteristicas_28.csv`: Datos crudos de características.
  2. `caracteristicas.csv`: Datos extendidos con características adicionales.
  3. `Variedad_a_Caracteristicas_28_numeric (1).csv`: Versión numérica para análisis cuantitativo.
