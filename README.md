# Water Quality Management Using Machine Learning

## 🌊 Project Overview

This project focuses on classifying water quality using machine learning techniques. It uses water-quality parameters as input features to predict a water-quality category, helping support data-driven assessment and monitoring.

The project compares multiple classification algorithms, evaluates their predictive performance, and uses model explainability techniques to understand which parameters contribute most to the predictions.

## 🎯 Objectives

- Analyze water-quality data using Python.
- Train and compare different machine learning classification models.
- Classify water samples into quality categories.
- Evaluate models using cross-validation and test-set metrics.
- Interpret model predictions using feature-importance and SHAP analysis.
- Explore the relationship between water-quality measurements and water-quality assessment indices.

## 📊 Dataset

The dataset contains **4,300 records and 15 columns**, including water-quality parameters and a target label.

### Input Features

- Temperature
- Turbidity
- Dissolved Oxygen (DO)
- Biochemical Oxygen Demand (BOD)
- CO₂
- pH
- Alkalinity
- Hardness
- Calcium
- Ammonia
- Nitrite
- Phosphorus
- Hydrogen Sulfide (H₂S)
- Plankton

### Target

The target column is `Water Quality`, with three classes:

- **Excellent**
- **Good**
- **Poor**

The exact dataset source and measurement units should be documented alongside the dataset file when available.

## 🧰 Technologies Used

- **Language:** Python
- **Data processing:** pandas, NumPy
- **Machine learning:** scikit-learn
- **Gradient boosting:** XGBoost, LightGBM
- **Model explainability:** SHAP
- **Visualization:** Matplotlib, Seaborn (if used)
- **Environment:** Jupyter Notebook

## 🤖 Machine Learning Models

The project evaluates multiple classification algorithms:

- Decision Tree
- Random Forest
- XGBoost
- LightGBM
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- AdaBoost

Hyperparameter tuning and cross-validation are used to identify suitable model configurations.

## 📈 Model Evaluation

Models are assessed using metrics such as:

- Accuracy
- Classification report (precision, recall, and F1-score)
- Confusion matrix
- Cross-validation score

### Reported Test Accuracy

| Model | Test Accuracy |
|---|---:|
| Random Forest | 99.51% |
| Decision Tree | 99.44% |
| XGBoost | 99.37% |
| LightGBM | 99.37% |
| SVM | 95.42% |
| K-Nearest Neighbors | 87.17% |
| AdaBoost | 84.64% |

*These values reflect the evaluated configuration of this project. Results can vary with dataset versions, preprocessing, and train/test splits. Very high scores should be checked for data leakage and validated on independent data before real-world use.*

## 🔍 Model Explainability

SHAP (SHapley Additive exPlanations) is used to examine how input features influence model predictions. In the evaluated Random Forest model, the leading features by mean absolute SHAP value included:

1. BOD
2. Dissolved Oxygen
3. H₂S
4. Nitrite
5. Ammonia
6. Turbidity

Feature importance indicates how the model uses the available data; it does not establish that a feature causes a change in water quality.

## ⚙️ Workflow

1. Load and inspect the dataset.
2. Clean the data and prepare the input features and target.
3. Split the data into training and testing sets.
4. Train classification models.
5. Tune hyperparameters using cross-validation.
6. Evaluate the selected models on the test set.
7. Compare model performance.
8. Use SHAP to interpret model predictions.
9. Explore water-quality indices and relationships where appropriate.

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or a compatible Python version
- Jupyter Notebook or JupyterLab
- The dataset used by the notebooks

### Installation

Clone the repository:

```bash
git clone https://github.com/k-raghu24/Water-Quality-Management.git
cd Water-Quality-Management
```

Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

Install the libraries used by the project:

```bash
pip install pandas numpy scikit-learn xgboost lightgbm shap matplotlib seaborn jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the relevant notebook, update the dataset path if necessary, and run the cells in order.

## 📁 Repository Contents

The repository contains the notebooks, data, or supporting files used for the water-quality machine learning workflow. Open the repository file list to identify the main notebook and the dataset filename before running the project.

## 🌱 Applications

- Preliminary water-quality classification
- Comparing machine learning algorithms for environmental data
- Identifying influential water-quality parameters
- Supporting exploratory analysis and decision-making
- Educational research in environmental data science and machine learning

## ⚠️ Limitations

- Predictions depend on the quality, representativeness, and labeling of the dataset.
- A high test score does not by itself guarantee performance on new locations or future samples.
- Model predictions are not a substitute for certified laboratory testing or regulatory assessment.
- Water-quality indices require clearly defined formulas, units, and validated thresholds.

## 🔮 Future Enhancements

- Validate models using independent datasets from different locations and seasons.
- Build a dashboard for interactive water-quality predictions.
- Add model comparison charts and downloadable reports.
- Integrate real-time sensor readings where suitable hardware is available.
- Improve explainability and calibration of model predictions.
- Document the data source, preprocessing steps, and reproducible experiment settings.

## 👨‍💻 Author

**Raghu Raman K.**

GitHub: [@k-raghu24](https://github.com/k-raghu24)

## 📄 License

No license is specified here. Add a `LICENSE` file to define how others may use, modify, and distribute this project.
