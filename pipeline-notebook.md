# 📓 Notebook – Volantis Pipeline

## Overview

The **Notebook** feature allows you to run interactive Python code directly inside the Volantis Pipeline. It’s perfect for data exploration, model building, evaluation, and even saving machine learning models.

Volantis Notebook works just like Jupyter Notebook but is seamlessly connected to the pipeline nodes and available canvas data.

---

## How to Access

![Notebook Config](/vdata/documentation/pipeline/notebook/notebook-config.webp)

To open the **Notebook**, simply select it as a tool:

1. Click the data node you want to use
2. Choose **Notebook**
3. After clicking, the Notebook configuration will appear in the right panel

You can now write and run code just like in Jupyter Notebook — from data analysis to full machine learning workflows.

---

## Input Types for Notebook

The Notebook supports multiple types of input data, enabling flexible data processing and experimentation.

### Supported Input Types:

- **Tabular Data** (CSV, Excel, SQL tables, etc.)
- **PDF Documents**
- **Audio Files**

These inputs are automatically connected to your notebook session when the pipeline runs. You can access them directly within the notebook using predefined import statements.

### How to Access Inputs in Notebook:

Depending on the input type, use the following methods to load the data inside your code:

```python
# Load file daftar_booking_pasien
file_0 = load_file("565495795353138121")

# Load model Linear Regression
model_1, encoder_1 = load_model("566670563297342409")

# Load model Random Forest Classifier
model_2, encoder_2 = load_model("566667494878622665")
```
---

## Open Notebook in New Tab

![Notebook New Tab](/vdata/documentation/pipeline/notebook/notebook-open-tab.webp)

If you prefer a larger workspace, you can open the Notebook in a new browser tab:

- Click the **↗** icon in the top-right corner of the notebook panel
- The notebook will open in a separate tab
- All code, outputs, and results remain synced with your current pipeline

---

## Save Pipeline & Create Jobs
![Button Save](/vdata/documentation/pipeline/btn-save.webp)
![Job Create](/vdata/documentation/pipeline/save-create-job.webp)
![Button Save](/vdata/documentation/pipeline/config-job.webp)
Once you're done working in the Notebook, you can save your pipeline and turn it into a job for scheduled execution.

1. Click **Save Pipeline** to store your current pipeline setup, including all notebook code and configurations.
2. Then, go to the **Jobs** section and click **Run Job** to execute the pipeline.
3. The output of the job will automatically be stored as:
   - A **data table** in **My Data**
   - A **trained model** in the **Model Library** (if your pipeline includes a training process)
4. If you need to access the resulting data table or trained model programmatically, you can use the [Volantis API](/vdata/documentation?page=api-doc)




