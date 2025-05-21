# 🏷️ Classification – Volantis Pipeline

## Overview  
The **Classification** feature enables the creation of supervised machine learning models that categorize data into discrete classes. Use this when your prediction target is **categorical**, such as classifying emails as spam or not spam, or predicting customer churn.

This module helps you:

- Train models using classification algorithms. See [Model Algorithms](/vdata/documentation?page=model-algorithms) for more detail.
- Select target columns and feature columns  
- Customize model parameters (Advanced options)  
- Generate predictions for categorical labels  

---

## Configuration

![Classification Config](/vdata/documentation/pipeline/classification/clasification_config.webp)

| Section               | Property                   | Description                                                                 | Example                         |
|------------------------|----------------------------|-----------------------------------------------------------------------------|----------------------------------|
| **Model Name**         | Text input                 | Define a name for your classification model.                                | `Churn_Predictor`                |
| **Algorithm**          | Dropdown                   | Select a classification algorithm to train the model.                       | `Logistic Regression`, `Random Forest`, `Decision Tree`, etc. |
| **Column to Predict**  | Dropdown (select column)   | Choose the target column (label) that the model will learn to predict.      | `is_churned`                     |
| **Features Columns**   | Dropdown (multi-select)    | Choose one or more feature columns that influence the prediction.           | `age`, `monthly_usage`, `plan_type` |

<!-- ---

## Advanced Configuration (Optional)

![Advanced Config](/vdata/documentation/pipeline/classification/advanced-config.webp)

| Section             | Property         | Description                                                                 | Example       |
|---------------------|------------------|-----------------------------------------------------------------------------|---------------|
| **Model Config**    | C                | Inverse of regularization strength. Smaller values mean stronger regularization. | `1`           |
|                     | Dual             | Dual or primal formulation. Usually `False` for small datasets.             | `false`       |
|                     | Fit Intercept    | Whether to calculate the intercept for this model.                         | `true`        |
|                     | Intercept Scaling| Useful only when `solver=liblinear` and `fit_intercept=True`.              | `1`           |
|                     | L1 Ratio         | Elastic-net mixing parameter (only used if `penalty='elasticnet'`).        | `0.5`         |
|                     | Max Iter         | Maximum number of iterations taken for the solvers to converge.            | `100`         |
|                     | N Jobs           | Number of CPU cores to use. `-1` uses all processors.                      | `-1`          |
|                     | Penalty          | Used to specify the norm used in the penalization.                         | `l2`          |
|                     | Random State     | Seed used by the random number generator.                                  | `42`          |
|                     | Solver           | Algorithm to use in the optimization problem.                              | `lbfgs`       |
|                     | Tol              | Tolerance for stopping criteria.                                           | `0.0001`      |
|                     | Verbose          | Enable verbose output (useful for debugging).                              | `1`           |
|                     | Warm Start       | Reuse the solution of the previous call to fit as initialization.          | `false`       |

> 🛠️ You can switch between **Preprocessing** and **Model Config** tabs to manage both data preparation and model parameters. -->

---

## Previewing the Output

![Classification Preview](/vdata/documentation/pipeline/classification/clasification_preview.webp)

Use the **Preview** button to:

- See how the model interprets selected target and features  
- Check sample predictions before finalizing the config  
- Ensure appropriate setup before training  
- Spot any misconfigurations early  

Previewing ensures you're applying the model effectively to the dataset.


