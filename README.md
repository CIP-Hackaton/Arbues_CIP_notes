# Analysis and Prediction System for Potato Crops in Peru

## 📋 Overview
This project implements a comprehensive system for the analysis and prediction of potato crops in Peru, integrating geospatial, climatic, and agricultural data. The system uses deep learning models and time series analysis to forecast yields and demand for various potato varieties.

## 🏗️ Project Structure

### /ArchivosForBackend
Contains trained models and relationship tables ready for production use:
- Main neural model for crop characteristic prediction
- SARIMA models for demand forecasting by variety
- Mapping and normalization tables

### /TablasDiego
Central repository for geographic and climatic data:
- Agrobiodiversity data (Not used)
- Species concentration maps (Not used)
- Processed climatological data (temperature, precipitation, snowfall, erosion, climate classification)
- SHP files for geospatial processing

### /ENTRENAMIENTO
Notebooks and data for training the main model:
- Neural model for vector-to-vector mapping (from spatiotemporal feature vectors to potato characteristics)
- Tables of potato variety characteristics
- Prepared datasets for training

### /Demanda
Potato demand analysis and modeling:
- SARIMA models by variety
- Historical price and volume data
- Data processing and preparation scripts

### /Rendimiento
Crop yield analysis:
- Processed SISAGRI data
- Yield analysis by variety and region
- Filtered datasets for modeling

### /TizontardioHistorial
Late blight risk analysis:
- Historical data from 2014-2016
- District-level risk maps
- Geospatial data processing

## 🔧 Key Technologies

- Python for data processing and modeling
- TensorFlow/Keras for neural networks
- Statsmodels for SARIMA models
- GeoPandas for geospatial processing
- Selenium for web scraping climatic data (not used)

## 📊 Implemented Models

### Main Model (Vector-to-Vector)

- Neural network mapping geographic/climatic features to variety characteristics
- Trained on historical data with cross-validation
- Implemented using TensorFlow/Keras

### Demand Models

- Individual SARIMA models for each potato variety
- Demand forecasting based on historical data
- Includes seasonal and trend analysis

## 📁 Data Used

- Geospatial data for Peruvian districts
- Historical crop records (SISAGRI)
- Climatic and meteorological data
- Potato variety characteristics (based on scientific research)
- Historical price and market volume data

## 💡 Key Features

- Yield prediction by district and variety
- Late blight risk analysis
- Demand and price forecasting
- Mapping of optimal cultivation zones
- Analysis of climatic and geographic factors

## 🔄 Data Workflow

1. Processing of geographic and climatic data
2. Analysis and cleaning of historical variety data based on project needs
3. Joining variety histories with climatological and other factors, such as late blight
4. Training predictive models
5. Generating predictions and recommendations
6. Integration with backend for production service

## 📚 Research Base

- Variety characteristics based on scientific papers
- Validated risk analysis methodology
- Prediction models grounded in agricultural literature

## 🛠️ Maintenance
The following components require periodic updates:

- Climatic data (monthly updates)
- Market prices and volumes (weekly updates)
- SARIMA models (quarterly retraining)
- Main model (annual retraining)

## 👥 Contributions
This project is the result of extensive research and collaboration between experts in:

- Data Science
- Agronomy
- Climatology
- Geospatial Analysis

For more information on specific components, refer to the documentation in each subfolder of the project.
