CREARMODELOSPARCADAVARIEDAD.IPYNB

#### Archivos Necesarios

- demanda.csv (Dataset con columnas: Fecha, VariedadPapa, PMax, PMin, PProm, Volumen)
- Archivos .pkl generados para cada modelo SARIMA

#### Estructura y Funcionalidad

1. Preparación de Datos
    
    - Carga y limpieza del dataset
    - Formateo de fechas
    - Cálculo de demanda (Volumen × PProm)
    - Manejo de valores nulos
2. Análisis Inicial
    
    - Visualización de series temporales
    - Estadísticas descriptivas
    - Identificación de patrones estacionales
    - Evaluación de valores atípicos
3. Modelado SARIMA por Variedad
    
    - Normalización de datos
    - Auto ARIMA para selección de parámetros
    - Entrenamiento individual por variedad
    - Almacenamiento de modelos en .pkl
4. Evaluación y Predicción
    
    - Cálculo de métricas MAE/RMSE
    - Validación de residuos
    - Predicciones para 2025
    - Visualización de pronósticos

#### Output Principal

- Modelos SARIMA guardados (.pkl)
- Métricas de evaluación por variedad
- Gráficos de predicción
- Pronósticos mensuales 2025
- Reportes de precisión

















