# Documentación del archivo `JOIN.ipynb`

## Archivos Requeridos

1. **Entradas Base:**
   - `temperaturaMax_mensual_distrital.csv`
   - `Temp_min-mensual-distritos.csv`
   - `Precipitacion_mensual_distrital_noAnual.csv`
   - `nevada_distrital_mensual_noAnual.csv`
   - `erosion_distrital_noMensual_NoAnual.csv`
   - `tizon_distrital_noMensual_noAnual.csv`
   - `ClasificacionClimatica_distrital.csv`
   - `6variedades_distrital_mensual_anual.csv`

2. **Tablas Transformadas Temporalmente:**
   - Tablas expandidas y normalizadas en formato largo para cada variable.

---

## Flujo Interno

### **1. Carga de Archivos**
   - Lectura de cada archivo `.csv` usando `pandas`, manejando problemas de codificación (`latin1`).
   - Inspección de valores nulos y corrección de nombres de columnas inconsistentes.

### **2. Transformaciones**
   - **Normalización Temporal:**
     - Conversión al formato largo (`melt`) para columnas de meses.
     - Replicación de datos anuales a nivel mensual.
   - **Corrección de Clasificaciones:**
     - Unificación de nombres en `Clasificacion_Climatica`.
     - Agrupación y asignación de códigos numéricos.
   - **Escalado Numérico:**
     - Normalización de variables como `TEMP_MAX`, `PRECIPITACION`, `NEVADA`, entre otras, con `MinMaxScaler`.

### **3. Unión de Tablas**
   - **Paso 1:** Fusión de tablas por `NOMBDEP`, `NOMBPROV`, `NOMBDIST` y `MES`.
   - **Paso 2:** Inclusión de `tizon_distrital` y variables extendidas como `PRECIPITACION`, `NEVADA`, y `EROSION_PROMEDIO`.
   - **Paso 3:** Integración de datos de variedades (`6variedades_distrital_mensual_anual.csv`).

### **4. Preparación Final**
   - Limpieza de columnas no necesarias y normalización de datos faltantes.
   - Codificación de etiquetas (`PRODUCTO`, `Clasificacion_Climatica`) como variables categóricas.

---

## Exportaciones Finales

1. **Tablas Consolidadas:**
   - `tabla_consolidada_v2.csv`: Tablas unificadas y normalizadas.
   - `DistrToVectorNormal.csv`: Tabla con características numéricas normalizadas.
   - `tabla_preparada_modelo.csv`: Tabla lista para modelos predictivos.

2. **Detección de Problemas:**
   - `duplicados.csv`: Registros duplicados para inspección manual.

---

## Uso Posterior

- **`tabla_preparada_modelo.csv`:** Lista para uso en modelos de clasificación o regresión.
- **`DistrToVectorNormal.csv`:** Entrada estándar para modelos basados en vectores de características.
