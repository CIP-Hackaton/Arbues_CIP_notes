# Documentación de la Carpeta `Demanda`

## Archivos Requeridos

1. **Datos Base:**
   - `volumen.csv`: Volumen mensual de cada variedad de papa.
   - `precio_max_papas_por_mes.csv`: Precios máximos mensuales por variedad de papa.
   - `precio_min_papas_por_mes.csv`: Precios mínimos mensuales por variedad de papa.
   - `precio_prom_papas_por_mes.csv`: Precios promedio mensuales por variedad de papa.

2. **Archivos Generados:**
   - `demanda.csv`: Consolidación de precios y volumen por variedad.
   - Modelos SARIMA (guardados en `MODELOS ENTRENADOS`).

---

## Flujo Interno

### **1. Consolidación de Datos (`CrearDataSetDemanda.ipynb`)**
   - **Entradas:**
     - Archivos de precios (`precio_max_papas_por_mes.csv`, `precio_min_papas_por_mes.csv`, `precio_prom_papas_por_mes.csv`).
     - Archivo de volumen (`volumen.csv`).
   - **Procesos:**
     - Transformación al formato largo (`melt`) para unificar columnas de meses en filas.
     - Unión de datos por `Fecha` y `VariedadPapa` mediante `merge`.
   - **Salida:**
     - `demanda.csv`: Archivo consolidado con las columnas:
       - `Fecha`, `VariedadPapa`, `PMax`, `PMin`, `PProm`, `Volumen`.

### **2. Análisis y Modelado de Demanda (`DEMANDA.ipynb`)**
   - **Carga y Limpieza:**
     - Lectura de `demanda.csv` y validación de datos nulos o inconsistentes.
     - Normalización de fechas (`YYYY-MM-DD`) y filtrado por rango temporal.
   - **Análisis Exploratorio:**
     - Visualización de series temporales (volumen y precio promedio).
     - Inspección de valores únicos y estadísticas descriptivas.
   - **Modelado SARIMA:**
     - Entrenamiento de un modelo SARIMA por cada variedad de papa.
     - Optimización automática de hiperparámetros con `pmdarima.auto_arima`.
     - Predicción de demanda futura hasta diciembre de 2025.
   - **Métricas de Desempeño:**
     - Evaluación de los modelos con MAE y RMSE (normalizados y en escala original).
   - **Guardado de Modelos:**
     - Modelos entrenados guardados en la carpeta `MODELOS ENTRENADOS` como archivos `.pkl`.

---

## Exportaciones Finales

1. **Datos Consolidado:**
   - `demanda.csv`: Archivo base para análisis de demanda.

2. **Modelos Entrenados:**
   - Archivos `.pkl` en la carpeta `MODELOS ENTRENADOS`:
     - `sarima_model_Papa_Amarilla.pkl`, `sarima_model_Papa_Blanca.pkl`, etc.

3. **Predicciones y Visualizaciones:**
   - Series temporales de demanda histórica y predicción futura por variedad.
   - Gráficas de desempeño (residuos, métricas, y demanda proyectada).

---

## Uso Posterior

- **`demanda.csv`:** Base para análisis y generación de predicciones.
- **Modelos SARIMA:** Predicción de demanda futura por variedad de papa.
- **Visualizaciones:** Inspección de tendencias históricas y proyectadas.
