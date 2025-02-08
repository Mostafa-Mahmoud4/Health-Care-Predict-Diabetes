# Health-Care-Predict-Diabetes

## Overview

This project utilizes the National Health and Nutrition Examination Survey (NHANES) dataset to predict diabetes status using demographic data and body measurements. The study involves data preprocessing, feature selection, and multiple machine learning models to assess predictive performance.

## Dataset

The dataset is derived from NHANES 2013-2014 and includes the following components:

1. **Demographics** - Gender, family income, years in the US, etc.
2. **Examinations** - Blood pressure, body measures, grip strength, etc.
3. **Dietary Data** - Total nutrient intake.
4. **Laboratory Tests** - Glycohemoglobin, fasting glucose, cholesterol levels, etc.
5. **Questionnaire Responses** - Health conditions, medical history, and lifestyle factors.
6. **Medications** - Prescription drug usage.

## Data Preprocessing

- **Data Loading:** Merging datasets from NHANES.
- **Handling Missing Values:**
  - Replacing missing values using median imputation.
  - Forward fill for categorical variables.
  - Default values for categorical indicators (e.g., breastfed status).
- **Feature Selection:**
  - Variance thresholding to remove low-variance features.
  - Selecting relevant features: `GlycoHemoglobin`, `ArmCircum`, `SaggitalAbdominal`, `GripStrength`, etc.
- **Diabetes Classification:**
  - **0**: Normal (`GlycoHemoglobin` < 6.0)
  - **1**: High-risk (`6.0 <= GlycoHemoglobin <= 6.4`)
  - **2**: Diabetic (`GlycoHemoglobin` >= 6.5)

## Model Training & Evaluation

### Models Implemented:

1. **Linear Regression**
2. **K-Means Clustering**
3. **AdaBoost Classifier (Decision Tree-based)**
4. **Bagging Classifier**
   - Decision Tree-based
   - K-Nearest Neighbors (KNN)-based
5. **Multi-Layer Perceptron (MLP) Classifier**

### Model Performance

Each model was evaluated using accuracy scores:

| Model                        | Accuracy      |
| ---------------------------- | ------------- |
| Linear Regression            | 0.120948      |
| AdaBoost Classifier          | 0.704170      |
| Bagging (Decision Tree)      | 0.874902      |
| Bagging (KNN)                | 0.880671      |
| Multi-Layer Perceptron (MLP) | 0.880671&#xD; |

### Visualization

- **Correlation Heatmap**: Visualizes relationships between features.
- **Pairplot**: Examines feature distributions and clustering.
- **Model Performance Bar Chart**: Compares accuracy scores.

## Conclusion

- Machine learning models can effectively predict diabetes risk using demographic and body measurement data.
- Ensemble methods (AdaBoost, Bagging) showed strong predictive performance.
- Future improvements include incorporating additional clinical variables and optimizing hyperparameters.

---

### References

- NHANES: [CDC NHANES Website](https://www.cdc.gov/nchs/nhanes/index.htm)
- Machine Learning Libraries: Scikit-learn, Seaborn, Matplotlib, Pandas


