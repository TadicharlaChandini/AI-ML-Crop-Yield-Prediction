# Crop Yield Prediction using Machine Learning

## Problem Statement
Agriculture plays a crucial role in economic stability and food security.
Accurate prediction of crop yield helps farmers and policymakers make informed
decisions related to irrigation, pesticide usage, and crop planning.

This project aims to build a machine learning model that predicts crop yield
based on climatic and agricultural factors such as rainfall, temperature,
and pesticide usage.

---

## Dataset Description
The dataset was collected from multiple real-world sources, where each
agricultural factor was stored separately:

- Crop Yield data
- Rainfall data
- Temperature data
- Pesticide usage data

These datasets were merged using common spatial and temporal attributes
(`Area` and `Year`) to form a unified dataset for modeling.

---

## Data Preprocessing
The following preprocessing steps were performed:

- Filtered yield-specific records from raw data
- Merged multiple datasets using `Area` and `Year`
- Handled non-numeric placeholder values (`..`)
- Converted categorical variables (`Area`, `Item`) using label encoding
- Ensured no missing values remained in the final dataset

---

## Model Selection & Training
A **Decision Tree Regressor** was chosen for this task due to its ability to:

- Capture non-linear relationships
- Provide interpretability
- Work well with mixed feature types

The dataset was split into training (80%) and testing (20%) sets before
training the model.

---

## Evaluation Metrics
The model was evaluated using standard regression metrics:

- **Mean Absolute Error (MAE):** ~3883
- **Root Mean Squared Error (RMSE):** ~13534
- **R² Score:** ~0.97

The high R² score indicates that the model explains approximately 97% of
the variance in crop yield.

---

## Feature Importance
Feature importance analysis revealed that climatic factors such as rainfall
and temperature, along with pesticide usage, significantly influence crop yield.
This improves model explainability and trust.

---

## Inference Explanation (Sample Prediction)
A sample from the test dataset was used to demonstrate model inference.
Encoded categorical features were decoded back to their original labels
for human-readable explanation.

The predicted crop yield closely matched the actual value, showing that
the model generalizes well to unseen data.

---

## Conclusion
This project demonstrates an end-to-end machine learning pipeline involving
real-world data integration, preprocessing, model training, evaluation,
and explainable inference. The focus was placed on reasoning and data handling
rather than accuracy alone.

---

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
