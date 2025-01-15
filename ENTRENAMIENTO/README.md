# Documentation of the `ENTRENAMIENTO.ipynb` File

## Required Files

1. **Training Data and Features:**
   - `tabla_preparada_modelo.csv`: Main dataset with features and labels.
   - `Variedad_a_Caracteristicas.csv`: Information on varieties and their features.
   - `Variedad_a_Caracteristicas_28.csv`: Extended dataset with additional features.

2. **Transformed Data Outputs:**
   - `Variedad_a_Caracteristicas_28_numeric.csv`: Numeric and encoded version of features.
   - `df_modelo_transformed.csv`: Main dataset transformed and ready for training.

---

## Internal Workflow

### **1. Data Exploration**
   - Load data from `tabla_preparada_modelo.csv`.
   - Clean null values, verify data types, and analyze distributions.
   - Explore categorical and numerical features.

### **2. Transformations**
   - **One-Hot Encoding:** For categorical variables like `Clasificacion_Climatica` and nominal features.
   - **Ordinal Mapping:** For columns like `Late blight (LB)` and `Growing period highland`.
   - **Normalization:** Scale numerical values using `MinMaxScaler`.
   - **Filtering:** Remove varieties with incomplete data (e.g., Yungay, Huayro).

### **3. Training**
   - **Vector-to-Vector Model:**
     - Features (`X`): Variables such as `TEMP_MAX`, `PRECIPITACION`, etc.
     - Labels (`y`): Related features like `Dry matter (%)`, `Growing period highland`.
   - **Neural Network:**
     - Layers: 128, 64, 32 neurons with `relu` activation functions and an output layer with `linear` activation.
     - Optimization: `adam` optimizer with regression loss (`mean_squared_error`).
   - **Validation and Fine-Tuning:** Split data into training, testing, and validation sets.

### **4. Evaluation**
   - Metrics for each feature:
     - **MSE:** Mean Squared Error.
     - **MAE:** Mean Absolute Error.
   - Global evaluation:
     - Combined MSE and MAE for all predictions.

### **5. Model Saving**
   - Export the trained model in Keras format: `Trained_model_VectorToVector.keras`.

---

## Final Exports

1. **Data Tables:**
   - `Variedad_a_Caracteristicas_28_numeric.csv`
   - `df_modelo_transformed.csv`

2. **Trained Model:**
   - `Trained_model_VectorToVector.keras`

3. **Graphs:**
   - Feature distribution.
   - Training metrics (accuracy and loss per epoch).
   - Column variation and quartiles.
