# 🌱 AgroWater Prediction Pipeline

A machine learning pipeline for preprocessing agronomic datasets and predicting crop water requirements using Python, Pandas, and Scikit-learn.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-green)](https://www.python.org/)

## 📖 Overview

This project focuses on building a robust data ingestion and preprocessing pipeline for agricultural datasets, followed by training machine learning models to predict water requirements for crops. Key steps include:
- **Data cleaning** (handling missing values, structural inconsistencies, and categorical encoding).
- **Feature engineering** (seasonality, climatic ratios).
- **Model training** (Random Forest, MLPRegressor, and Deep Neural Networks).
- **Performance comparison** of models.

## 🚀 Features

- **Datasets Processed**: 6 agricultural datasets with diverse features (weather, soil, crop types).
- **Preprocessing**:
  - Merging malformed rows.
  - Handling missing values and standardizing formats.
  - Normalization (`MinMaxScaler`, `StandardScaler`) and encoding (`LabelEncoder`).
- **Models**:
  - Random Forest Regressor
  - Scikit-learn MLPRegressor (Best performance: **R² = 0.9992**)
  - TensorFlow Deep Neural Network

## 📂 Datasets

| Dataset | Description                                                                 |
|---------|-----------------------------------------------------------------------------|
| 1       | Crop water needs with weather, soil, and location data.                    |
| 2       | Tomato plant water consumption over time.                                  |
| 3       | Crop growth periods and water needs (FAO data).                            |
| 4       | Irrigation records for paddy and groundnuts.                               |
| 6       | Combined data for wheat, rice, maize, and potato.                          |

## 🔧 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/aachraf94/AgroWater-Prediction-Pipeline.git
   cd AgroWater-Prediction-Pipeline
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🛠 Usage

### Preprocess Data:
Run the Jupyter notebooks in the order:
- `notebook.ipynb` (covers all datasets).
- Outputs are saved to the `Output/` directory.

### Train Models:
The final modeling section in `notebook.ipynb` trains and compares models.

### Results:
Preprocessed datasets and model results are stored in `Output/`.

## 📊 Results

| Model                      | MSE    | RMSE   | MAE    | R²     |
|----------------------------|--------|--------|--------|--------|
| Random Forest             | 0.0037 | 0.0612 | 0.0098 | 0.9962 |
| MLPRegressor (Scikit)     | 0.0008 | 0.0287 | 0.0159 | 0.9992 |
| Deep Neural Network       | 0.0155 | 0.1246 | 0.0871 | 0.9843 |

**Best Model:** Scikit-learn's MLPRegressor achieved the highest R² score (**0.9992**).

## 🙏 Acknowledgments

- **Proposed by:** Mme Karima Amrouche.
- **Tools Used:** Pandas, Scikit-learn, TensorFlow, Jupyter Notebook.

## 📜 License

This project is licensed under the MIT License. See `LICENSE` for details.

