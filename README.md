# Credit Scoring Model

## Project Overview

This project implements a Machine Learning classification model using Python and Random Forest to predict credit application outcomes based on the UCI Credit Approval Dataset.

The project demonstrates data preprocessing, feature engineering, model training, evaluation, and prediction.

## Dataset

- **Source:** [UCI Machine Learning Repository – Credit Approval Dataset](https://archive.ics.uci.edu/dataset/27/credit+approval)
- **Records:** 690
- **Features:** 15 input features
- **Target:** 1 classification column (`+` and `-`)

The dataset contains anonymized numerical and categorical attributes.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Methodology

1. Loaded and inspected the dataset.
2. Identified and handled missing values.
3. Converted appropriate numerical columns to numeric data types.
4. Separated input features and target variable.
5. Handled missing numerical values using median imputation.
6. Handled missing categorical values using most-frequent imputation.
7. Encoded categorical features using One-Hot Encoding.
8. Standardized numerical features.
9. Split the dataset into 80% training and 20% testing data.
10. Trained a Random Forest Classifier.
11. Evaluated the model using accuracy, precision, recall, F1-score, confusion matrix, and cross-validation.
12. Examined feature importance.

## Model Performance

| Evaluation Metric | Result |
|---|---:|
| Test Accuracy | 85.51% |
| 5-Fold Cross-Validation Accuracy | 87.50% |

### Classification Report

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| + | 0.82 | 0.87 | 0.84 |
| - | 0.89 | 0.84 | 0.87 |

### Confusion Matrix

```text
[[53  8]
 [12 65]]
```

The class order is `+` followed by `-`.

## Feature Importance

The Random Forest model identified the following as its most influential features:

- `cat__x8_f`
- `cat__x8_t`
- `num__x10`
- `num__x1`
- `num__x2`

## Project Structure

```text
CodeAlpha_CreditScoringModel/
│
├── main.ipynb
├── credit_scoring_model.pkl
├── README.md
└── requirements.txt
```

## How to Run

1. Clone or download this repository.
2. Install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

3. Open the project notebook:

```bash
jupyter notebook
```

4. Run the notebook cells in order.

The notebook downloads the dataset directly from the UCI repository.

## Model Usage

The trained model is saved as:

`credit_scoring_model.pkl`

It can be loaded using Joblib:

```python
import joblib

model = joblib.load("credit_scoring_model.pkl")
```

## Disclaimer

This project is an educational Machine Learning exercise. Its predictions should not be used as the sole basis for real-world credit or financial decisions.

## Author

**Dexter**

Computer Engineering Student | Machine Learning Enthusiast

GitHub: [Desmond-01-coder](https://github.com/Desmond-01-coder)