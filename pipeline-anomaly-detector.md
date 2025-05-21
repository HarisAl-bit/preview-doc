# 🚨 Anomaly Detector – Volantis Pipeline

## Overview  
The **Anomaly Detector** feature helps identify unusual or rare patterns in data, signaling potential issues, outliers, or behaviors that deviate from the norm. It's especially useful for:

- Sensor readings  
- Financial transactions  
- Log monitoring  
- Any numeric or time-series datasets

With **Anomaly Detector**, you can:

- Automatically flag outliers or anomalies  
- Choose between multiple detection algorithms (e.g., **ECOD**, **PCA**)  
- Focus analysis on a single numeric column

---

## Configuration

![Anomaly Detector Config](/vdata/documentation/pipeline/anomaly-detect/anomaly-detect-config.webp)

| Section        | Property       | Description                                                                 | Example             |
|----------------|----------------|-----------------------------------------------------------------------------|---------------------|
| **Column**     | Numeric Field  | Column to be analyzed for anomalies.                                        | `Sensor_Value`      |
| **Algorithm**  | Selector       | Detection method used: ECOD or PCA.                                         | `ECOD`, `PCA`       |

> 💡 Use **ECOD** for general-purpose detection.  
> Use **PCA** for datasets with multiple correlated features.

---

## Previewing the Output

![Anomaly Detector Preview](/vdata/documentation/pipeline/anomaly-detect/anomaly-detect-preview.webp)

Use the **Preview** button to validate:

- The anomaly detection works correctly on your sample data  
- The generated column (e.g., `Sensor_Value_Anomaly`) flags data points accurately  
- You can visually assess which data points are labeled as anomalies

