# 📈 Linear Regression – Volantis Pipeline

## Overview
The **Linear Regression** tool in Volantis Pipeline helps you build predictive models by analyzing relationships between a target column and feature columns.

This module allows you to:
- Choose from multiple regression algorithms (Linear, Ridge, Lasso, etc.). See [Model Algorithms](/vdata/documentation?page=model-algorithms) for more detail.
- Select a target variable and relevant features
- Fine-tune model behavior with advanced options
- Instantly preview predictions
- Save configuration and train your model for future predictions

---

## Configuration

![Regression Config](/vdata/documentation/pipeline/regression/regression-config.webp)

| Section               | Property            | Description                                                                 | Example                          |
|------------------------|---------------------|-----------------------------------------------------------------------------|-----------------------------------|
| **Model Name**         | Text input          | Define a name for your regression model.                                    | `Harga Rumah`                     |
| **Algorithm**          | Dropdown            | Select a regression algorithm: Linear, Ridge, Lasso, SGD, or Elastic Net.   | `Linear Regression`               |
| **Column to Predict**  | Dropdown            | Choose the target variable you want to predict.                             | `Harga_Rumah`                     |
| **Features Columns**   | Multi-select        | Select the independent variables (features) that influence the target.      | `Luas_Tanah`, `Jumlah_Kamar`      |

---

## Advanced Configuration

![Advanced Settings](/vdata/documentation/pipeline/regression/regression-advance.webp)

| Section             | Property       | Description                                                                 | Example       |
|---------------------|----------------|-----------------------------------------------------------------------------|---------------|
| **Model Config**    | Copy X         | Whether to copy the input data before training.                             | `true`        |
|                     | Fit Intercept  | Whether to calculate the intercept (bias).                                  | `true`        |
|                     | N Jobs         | Number of CPU cores to use for training. `-1` uses all available cores.     | `-1`          |
|                     | Positive       | Forces all model coefficients to be positive.                               | `false`       |

---

## Previewing the Output

![Regression Preview](/vdata/documentation/pipeline/regression/regression-preview.webp)

- Use the **Preview** button to visualize a sample of predicted values based on your selected features.
- This helps ensure the model is configured correctly before training.

---

## Saving & Running the Model

To finalize your regression setup:
1. Click **Save Config** to store all selected options.
2. Run the **Job** to train the model with your data.
3. After training, the model is accessible for prediction tasks in the [Model Library](/vdata/documentation?page=model-library).
