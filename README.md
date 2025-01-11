Sistema de Análisis y Predicción para Cultivos de Papa en Perú
📋 Descripción General
Este proyecto implementa un sistema integral para el análisis y predicción de cultivos de papa en Perú, combinando datos geoespaciales, climáticos y agrícolas. El sistema utiliza modelos de aprendizaje profundo y series temporales para predecir rendimientos y demanda de diferentes variedades de papa.
🏗️ Estructura del Proyecto
/ArchivosForBackend
Contiene los modelos entrenados y tablas de relación listos para usar en producción:

Modelo neural principal para predicción de características de cultivo
Modelos SARIMA para predicción de demanda por variedad
Tablas de mapeo y normalización

/TablasDiego
Repositorio central de datos geográficos y climáticos:

Datos de agrobiodiversidad
Mapas de concentración de especies
Datos climatológicos procesados (temperatura, precipitación, etc.)
Archivos SHP para procesamiento geoespacial

/ENTRENAMIENTO
Notebooks y datos para el entrenamiento del modelo principal:

Modelo neural para mapeo vector-a-vector
Tablas de características de variedades de papa
Datasets preparados para entrenamiento

/Demanda
Análisis y modelado de demanda de papa:

Modelos SARIMA por variedad
Datos históricos de precios y volumen
Scripts de procesamiento y preparación de datos

/Rendimiento
Análisis de rendimiento de cultivos:

Datos de SISAGRI procesados
Análisis de rendimiento por variedad y región
Datasets filtrados para modelado

/TizontardioHistorial
Análisis de riesgo de tizón tardío:

Datos históricos 2014-2016
Mapas de riesgo por distrito
Procesamiento de datos geoespaciales

🔧 Tecnologías Principales

Python para procesamiento de datos y modelado
TensorFlow/Keras para redes neuronales
Statsmodels para modelos SARIMA
GeoPandas para procesamiento geoespacial
Selenium para web scraping de datos climáticos

📊 Modelos Implementados
Modelo Principal (Vector-a-Vector)

Red neuronal que mapea características geográficas/climáticas a características de cultivo
Entrenado con datos históricos y validación cruzada
Implementado en TensorFlow/Keras

Modelos de Demanda

Modelos SARIMA individuales por variedad de papa
Predicción de demanda basada en datos históricos
Incluye análisis de estacionalidad y tendencias

📁 Datos Utilizados

Datos geoespaciales de distritos peruanos
Registros históricos de cultivo (SISAGRI)
Datos climáticos y meteorológicos
Características de variedades de papa (basado en investigación científica)
Datos históricos de precios y volumen de mercado

💡 Características Principales

Predicción de rendimiento por distrito y variedad
Análisis de riesgo de tizón tardío
Pronóstico de demanda y precios
Mapeo de zonas óptimas para cultivo
Análisis de factores climáticos y geográficos

🔄 Flujo de Datos

Procesamiento de datos geográficos y climáticos
Análisis y limpieza de datos históricos
Entrenamiento de modelos predictivos
Generación de predicciones y recomendaciones
Integración con backend para servicio en producción

📚 Investigación Base

Características de variedades basadas en papers científicos
Metodología de análisis de riesgo validada
Modelos de predicción fundamentados en literatura agrícola

🛠️ Mantenimiento
Los siguientes componentes requieren actualización periódica:

Datos climáticos (actualización mensual)
Precios y volúmenes de mercado (actualización semanal)
Modelos SARIMA (reentrenamiento trimestral)
Modelo principal (reentrenamiento anual)

👥 Contribuciones
El proyecto es resultado de investigación extensiva y colaboración entre expertos en:

Ciencia de datos
Agronomía
Climatología
Análisis geoespacial

Para más información sobre componentes específicos, consultar la documentación en cada subcarpeta del proyecto.