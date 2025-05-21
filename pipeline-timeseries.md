# ⏳ Time Series – Volantis Pipeline

## Overview  
The **Time Series** feature in Volantis Pipeline enables forecasting of sequential data using time-dependent models. This module supports advanced forecasting algorithms such as **[ARIMA](/vdata/documentation?page=model-algorithms)** and **[SARIMAX](/vdata/documentation?page=model-algorithms)** to capture trends, seasonality, and external regressors (features).  

---

## Configuration

![Time Series Config](/vdata/documentation/pipeline/time-series/time_series_config.webp)

| Field                       | Description                                                                 | Example                          |
|----------------------------|-----------------------------------------------------------------------------|----------------------------------|
| **Model Name**             | A custom name for your time series model.                                   | `Forecast Penjualan 2025`       |
| **Algorithm**              | Choose between `ARIMA` or `SARIMAX`.                                        | `ARIMA` or `SARIMAX`            |
| **Column to Predict (Target)** | The column that contains the values to forecast (must be time-indexed).     | `Jumlah_Penjualan`              |
| **Features Columns**       | Optional regressors used in **SARIMAX** to improve accuracy.                | `Promo_Aktivitas`, `Hari_Libur` |

---

## Advanced Settings (Optional)

![Time Series advance](/vdata/documentation/pipeline/time-series/time_series_advance.webp)


| Field                  | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Maxiter**            | Maximum number of iterations during model fitting.                         |
| **Method**             | Optimization method used to fit the model. Common options: `lbfgs`, `bfgs`. |
| **Order**              | ARIMA (p,d,q) configuration: Autoregressive (p), Differencing (d), MA (q). Example: `12,1,1` |
| **Out Of Sample Size** | Number of steps at the end of the dataset to exclude from training (for testing). |
| **Seasonal Order**     | Seasonal ARIMA order (P,D,Q,s). Use `0,0,0,0` for no seasonality.           |
| **Suppress Warnings**  | Suppress warnings during model fitting. Accepts `true` or `false`.          |
| **With Intercept**     | Include constant/intercept in the model. Accepts `true` or `false`.         |


---

## Preview  

![Time Series Preview](/vdata/documentation/pipeline/time-series/![Time Series advance](/vdata/documentation/pipeline/time-series/time_series_preview.webp)
.webp)

- Use the **Preview** button to visualize a sample of predicted values based on your selected features.
- This helps ensure the model is configured correctly before training.


## Saving & Running the Model

To finalize your regression setup:
1. Click **Save Config** to store all selected options.
2. Run the **Job** to train the model with your data.
3. After training, the model is accessible for prediction tasks in the [Model Library](/vdata/documentation?page=model-library).
