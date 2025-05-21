# 🪢 Clustering – Volantis Pipeline

## Overview  
The **Clustering** feature in Volantis Pipeline helps uncover natural groupings in your dataset using unsupervised learning algorithms. The currently supported method is **KMeans**, which partitions data points into distinct clusters based on similarity.

This module is ideal for use cases such as:

- Choose from multiple clustering algorithms. See [Model Algorithms](/vdata/documentation?page=model-algorithms) for more detail.
- Student performance segmentation  
- Customer segmentation  
- Market basket analysis  
- Behavioral grouping  

---

## Configuration

![Clustering Config](/vdata/documentation/pipeline/clustering/clustering_config.webp)

| Field                       | Description                                                                 | Example                      |
|----------------------------|-----------------------------------------------------------------------------|------------------------------|
| **Model Name**             | A custom name to identify your clustering model.                            | `kluster`                    |
| **Algorithm**              | Select the clustering algorithm. Currently supports `KMeans`.               | `KMeans`                     |
| **Column to Predict (Target)** | The column used for reference or evaluation. Not required for training in KMeans, but useful for post-analysis. | `semester_6`                 |
| **Features Columns**       | The feature columns used to form clusters.                                  | `semester_4`, `semester_5`   |

---

## Preview

![Clustering Preview](/vdata/documentation/pipeline/clustering/clustering_preview.webp)

- Use the **Preview** button to display generated clusters.
- Each data point is assigned to a cluster based on feature similarity.

---

## Saving & Running the Model

To finalize your clustering setup:
1. Click **Save Config** to store your configuration.
2. Run the **Job** to train the clustering model.
3. After training, the model will be available in the [Model Library](/vdata/documentation?page=model-library) and ready for segmentation tasks.
