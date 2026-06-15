# California Housing Price Prediction with MLflow

## Project Overview

This project demonstrates an end-to-end Machine Learning workflow using MLflow for experiment tracking, model registry, versioning, and model management.

The California Housing dataset from Scikit-Learn is used to predict housing prices using multiple machine learning models.

---

## Features

- MLflow Experiment Tracking
- Multiple Model Comparison
- Hyperparameter Tuning using GridSearchCV
- Model Signature Inference
- Model Registry
- Model Versioning
- Staging and Production Deployment
- Prediction Analysis
- Actual vs Predicted Visualization

---

## Dataset

California Housing Dataset

Source:

```python
from sklearn.datasets import fetch_california_housing
```

Features:

- MedInc
- HouseAge
- AveRooms
- AveBedrms
- Population
- AveOccup
- Latitude
- Longitude

Target:

- Median House Value

---

## Models Used

### Decision Tree Regressor

Performance:

- R² Score ≈ 0.60
- RMSE ≈ 0.72

### Random Forest Regressor

Performance:

- R² Score ≈ 0.77
- RMSE ≈ 0.54

### Tuned Random Forest (Best Model)

Performance:

- R² Score ≈ 0.81
- RMSE ≈ 0.50

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- MLflow
- Matplotlib

---

## MLflow Workflow

1. Create Experiment
2. Train Multiple Models
3. Log Parameters
4. Log Metrics
5. Infer Model Signature
6. Register Model
7. Create Model Versions
8. Promote Model to Staging
9. Promote Model to Production
10. Load Model from Registry
11. Make Predictions

---

## Project Structure

```
mlflow_california_housing/

│
├── notebooks/
│   └── housepriceprediction.ipynb
│
├── mlartifacts/
│
├── mlflow.db
│
├── requirements.txt
│
├── README.md
│
└── .gitignore
```

---

## Starting MLflow Server

```bash
mlflow server ^
--backend-store-uri sqlite:///mlflow.db ^
--default-artifact-root ./mlartifacts ^
--host 127.0.0.1 ^
--port 5000
```

Open:

http://127.0.0.1:5000

---

## Example Results

### Best Model

Random Forest Regressor

Metrics:

- R² Score = 0.806
- RMSE = 0.504

---

## Actual vs Predicted Analysis

The scatter plot below compares actual housing prices against predicted values.

- Red dashed line indicates perfect predictions.
- Color intensity represents prediction error.
- Most points cluster around the diagonal line, indicating good predictive performance.

---

## Future Improvements

- XGBoost
- LightGBM
- CatBoost
- Feature Engineering
- Model Deployment using FastAPI
- Docker Integration
- CI/CD Pipeline

---

## Author

Nitesh Kumar

MCA
NIT Jamshedpur