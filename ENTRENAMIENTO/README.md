# Documentación del archivo `ENTRENAMIENTO.ipynb`

## Archivos Requeridos

1. **Datos de Entrenamiento y Características:**
   - `tabla_preparada_modelo.csv`: Datos principales con características y etiquetas.
   - `Variedad_a_Caracteristicas.csv`: Información de variedades y sus características.
   - `Variedad_a_Caracteristicas_28.csv`: Extensión de datos con características adicionales.

2. **Salida de Datos Transformados:**
   - `Variedad_a_Caracteristicas_28_numeric.csv`: Versión numérica y codificada de las características.
   - `df_modelo_transformed.csv`: Datos principales transformados y listos para entrenamiento.

---

## Flujo Interno

### **1. Exploración de Datos**
   - Lectura de datos desde `tabla_preparada_modelo.csv`.
   - Limpieza de valores nulos, verificación de tipos y distribución.
   - Exploración de características categóricas y numéricas.

### **2. Transformaciones**
   - **One-Hot Encoding:** Variables categóricas como `Clasificacion_Climatica` y características nominales.
   - **Mapeo Ordinal:** Columnas como `Late blight (LB)` y `Growing period highland`.
   - **Normalización:** Escalado de valores numéricos con `MinMaxScaler`.
   - **Filtrado:** Eliminación de variedades con datos incompletos (e.g., Yungay, Huayro).

### **3. Entrenamiento**
   - **Modelo Vector a Vector:**
     - Características (`X`): Variables como `TEMP_MAX`, `PRECIPITACION`, etc.
     - Etiquetas (`y`): Características relacionadas como `Dry matter (%)`, `Growing period highland`.
   - **Red Neuronal:**
     - Capas: 128, 64, 32 neuronas con funciones `relu` y capa de salida `linear`.
     - Optimización: `adam` con pérdida de regresión (`mean_squared_error`).
   - **Validación y Ajuste:** División de datos en conjuntos de entrenamiento, prueba y validación.

### **4. Evaluación**
   - Métricas para cada característica:
     - **MSE:** Error Cuadrático Medio.
     - **MAE:** Error Absoluto Medio.
   - Evaluación global:
     - MSE y MAE combinados para todas las predicciones.

### **5. Guardado del Modelo**
   - Exportación del modelo entrenado en formato Keras: `Trained_model_VectorToVector.keras`.

---

## Exportaciones Finales

1. **Tablas de Datos:**
   - `Variedad_a_Caracteristicas_28_numeric.csv`
   - `df_modelo_transformed.csv`

2. **Modelo Entrenado:**
   - `Trained_model_VectorToVector.keras`

3. **Gráficas:**
   - Distribución de características.
   - Métricas de entrenamiento (precisión y pérdida por época).
   - Variación y cuartiles de las columnas.

