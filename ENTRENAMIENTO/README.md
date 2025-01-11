Resumen del Notebook: ENTRENAMIENTO.IPYNB

#### Archivos Necesarios

- tabla_preparada_modelo.csv (Dataset principal)
- Variedad_a_Caracteristicas_28.csv (Características de 28 variedades)

#### Estructura y Funcionalidad

1. Análisis Exploratorio
    
    - Visualización de distribuciones
    - Detección de outliers
    - Análisis de correlaciones
    - Estadísticas descriptivas
2. Preparación de Datos
    
    - Eliminación de variedades Yungay y Huayro
    - Encoding de variables categóricas
    - Normalización de variables numéricas
    - División train/test (80/20)
3. Modelado Neural
    
    - Red neuronal secuencial
    - 3 capas densas con dropout
    - Activación ReLU
    - Optimizador Adam
    - Early stopping
4. Evaluación y Métricas
    
    - MAE por característica
    - MSE global
    - Curvas de aprendizaje
    - Matrices de confusión

#### Output Principal

- Modelo guardado (.keras)
- Gráficas:
    - Pérdida vs épocas
    - Precisión vs épocas
    - Distribuciones de características
- Métricas de evaluación en CSV
- Predicciones sobre conjunto test
