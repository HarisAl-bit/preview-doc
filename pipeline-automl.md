# 🤖 AutoML – Volantis Pipeline

## Overview  
The **AutoML** feature in Volantis Pipeline enables users to automatically build predictive models by simply describing their objectives in natural language. This tool handles algorithm selection, preprocessing, and model training with minimal input required.

With **AutoML**, you can:  
- Describe your goal using plain language  
- Let the system choose the best-fit model automatically  
- Select a target column to predict (optional)  
- Instantly preview model suggestions and configurations  
- Save and train the model without coding

---

## Configuration

![AutoML Config](/vdata/documentation/pipeline/automl/automl-config.webp)

| Section               | Property             | Description                                                                 | Example                          |
|------------------------|----------------------|-----------------------------------------------------------------------------|-----------------------------------|
| **Model Name**         | Text input           | Define a name to identify your AutoML model.                                | `Customer Churn Predictor`        |
| **Objective**          | Prompt text area     | Describe your goal using natural language.                                  | `Predict if a customer will churn`|
| **Column to Predict**  | Dropdown (optional)  | Specify the target column to predict. Leave empty to let system decide.     | `churn_status`                    |

Once you've completed this form, click the **Generate** button to proceed.

---

## Model Suggestion Step

After clicking **Generate**, Volantis will analyze your objective and suggest the most suitable algorithm(s) for your task.

![AutoML Suggestion](/vdata/documentation/pipeline/automl/automl-config2.webp)

- **Model Card**: Displays the recommended model (e.g., `Fit`) along with actions.
- **Select**: Choose this model for training. See [Model Algorithms](/vdata/documentation?page=model-algorithms) for more detail.
- **Config**: Open advanced configuration options if needed.

> 💡 *The number of algorithms shown depends on your objective and dataset structure.*

---

## 🔍 Preview

Before committing to training, you can explore a **preview** of how your data will be processed and how the model is expected to perform.

![AutoML Preview](/vdata/documentation/pipeline/automl/automl-preview.webp)

In this step, you'll see:
- Sample rows from the dataset
- The selected target column (if specified)
- Basic feature analysis (e.g., missing values, distributions)
- A short summary of the model configuration (algorithm, cross-validation, etc.)

---

## Saving & Running the Model

Once you've selected your model:
1. Finalize settings through **Config** (if needed).
2. Click **Save** to store the model configuration.
3. Execute the **Job** to begin training.
4. After completion, the trained model will be available in your [Model Library](/vdata/documentation?page=model-library).
