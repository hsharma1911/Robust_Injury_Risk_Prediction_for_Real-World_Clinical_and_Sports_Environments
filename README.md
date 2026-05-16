# Sports Injury Prediction & Performance Analytics

[![Status](https://img.shields.io/badge/status-Proof%20of%20Concept-green)](https://github.com/)
[![Python](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-None-lightgrey)](LICENSE)

## Overview

This capstone project explores multimodal sports injury prediction and athlete performance analytics using machine learning. It combines physiological, biomechanical, environmental, and training load data to predict injury occurrence and validate regression-based performance models.

## Short Description

A data-driven sports injury analytics project focused on using a multimodal dataset to train and compare classification and regression models for injury risk assessment and athlete monitoring.

## Long Description

The repository contains an end-to-end experimental workflow for a sports injury prediction problem. It includes a Jupyter notebook for exploratory analysis, a multimodal injury dataset, pre-trained model artifacts, and evaluation results for classification and regression approaches.

Key outcomes include:
- injury occurrence classification with multiple model families
- regression analysis for performance and recovery metrics
- pre-trained model artifacts for CatBoost, LightGBM, XGBoost, Random Forest, stacking, and deep learning
- evaluation output saved in CSV files for easy review

## Key Features

- ✅ Multimodal athlete dataset with physiological, biomechanical, and contextual features
- ✅ Injury classification and performance regression modeling
- ✅ Pre-trained models in `models/`
- ✅ Evaluation results for both classification and regression tasks
- ✅ Notebook-driven exploratory analysis and model workflow
- ✅ Reproducible project structure with dataset and results tracking

## Tech Stack

- Python
- Jupyter Notebook
- pandas, numpy
- scikit-learn
- CatBoost, LightGBM, XGBoost
- TensorFlow / Keras
- joblib

## Prerequisites

- Python 3.10 or later
- pip
- A virtual environment is strongly recommended

## Installation & Setup

1. Clone the repository:

```bash
git clone <repository-url> "Sports-Injury-Analytics"
cd "Sports-Injury-Analytics"
```

2. Create and activate a virtual environment:

```bash
python -m venv .venv
# Windows
.venv\Scriptsctivate
# macOS / Linux
source .venv/bin/activate
```

3. Install required packages:

```bash
pip install pandas numpy scikit-learn catboost lightgbm xgboost tensorflow keras matplotlib seaborn
```

> Note: This repository does not include a dedicated `requirements.txt` file. If one is added later, use `pip install -r requirements.txt`.

## Usage / Quick Start

### Open the analysis notebook

The main workflow is implemented in `Code_File.ipynb`. Open it in Jupyter Notebook or JupyterLab to run the analysis end-to-end.

```bash
jupyter notebook Code_File.ipynb
```

### Load the dataset

```python
import pandas as pd

path = "multimodal_sports_injury_dataset.csv"
df = pd.read_csv(path)
print(df.head())
```

### Example: Inspect dataset shape

```python
print(df.shape)
print(df.columns.tolist())
```

### Load a saved model artifact

```python
import joblib
model = joblib.load("models/model_CatBoost.joblib")
```

### Review evaluation results

The `results/` directory includes CSV summaries for classification and regression metrics.

## Configuration

- `multimodal_sports_injury_dataset.csv` is the primary dataset.
- Pre-trained model artifacts are stored in `models/`.
- Evaluation CSV files are stored in `results/`.
- `catboost_info/` contains CatBoost training logs and monitoring data.

If you want to customize paths or parameters, update the notebook or add a small configuration script to manage paths and options.

## Project Structure

```text
.
├── Code_File.ipynb                  # Main Jupyter notebook for data exploration and modeling
├── multimodal_sports_injury_dataset.csv  # Dataset used for modeling
├── models/                          # Trained model artifacts
│   ├── autoencoder_model.keras
│   ├── encoder_model.keras
│   ├── model_CatBoost.joblib
│   ├── model_LightGBM.joblib
│   ├── model_RandomForest.joblib
│   ├── model_Stacking_Regressor.joblib
│   ├── model_XGBoost.joblib
│   ├── wide_deep_best.h5
│   ├── X_test_latent.npy
│   └── X_train_latent.npy
├── results/                         # Model evaluation results
│   ├── all_regression_results.csv
│   ├── classification_results.csv
│   ├── classification_summary.csv
│   ├── improved_classification_results.csv
│   ├── improved_regression_results.csv
│   └── regression_model_results.csv
├── catboost_info/                   # CatBoost training logs and info
└── README.md                        # Project documentation
```

## Testing

This repository does not include a dedicated automated test suite. To verify the project workflow:

1. Run `Code_File.ipynb` in Jupyter Notebook.
2. Confirm the dataset loads successfully.
3. Validate that the evaluation CSV files in `results/` contain model metric summaries.

## Contributing

Contributions are welcome. You can help by:

- improving documentation
- adding a `requirements.txt`
- organizing model training and evaluation code into reusable scripts
- creating automated tests

Please open issues or submit pull requests for enhancements.

## License

No license file is included in this repository. Add a `LICENSE` file to define the reuse policy for this project.

## Acknowledgements

- Open-source machine learning libraries and frameworks
- The dataset and evaluation workflow for sports injury prediction
- Capstone project mentors and collaborators

## Screenshots

![Project overview](screenshots/placeholder.png)

> Add screenshots or visualizations here once available.
