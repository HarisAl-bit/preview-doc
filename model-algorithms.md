# 🤖 Model Algorithms – Volantis ML Tool Pipeline

## Overview

When using our Machine Learning tool ([AutoML](/vdata/documentation?page=pipeline-automl), [Regression](/vdata/documentation?page=pipeline-regression), [Classification](/vdata/documentation?page=pipeline-classification), [Clustering](/vdata/documentation?page=pipeline-clustering), [Time Series](/vdata/documentation?page=pipeline-timeseries)) in **[Volantis Pipeline](/vdata/documentation?page=pipeline)**, you have a wide range of model algorithms to choose from—each designed to suit different needs and deliver the best possible results. Below, we explain these model algorithms in more detail to help you get the most value from your data.

## Regression

### 1. Linear Regression

Linear Regression is the **simplest regression method**. It fits a **straight line** (or plane in multiple dimensions) through the data to make predictions.

- **When to use**: When the relationship between features and target is roughly linear and your dataset is clean.
- **Benefit**: Easy to understand and interpret.
- **Regularization**:  None. This means it doesn’t control for overfitting, so it might not work well on complex datasets.
- **Highlight**: Best for getting started or when interpretability is a priority.

### 2. Ridge Regression

Ridge Regression is like **Linear Regression** but adds **L2 regularization**.

- **L2 Regularization**: Penalizes large weights by squaring them, encouraging the model to spread influence across features instead of relying on a few.
- **When to use**: When you have many features and want to avoid overfitting without removing any features.
- **Benefit**: Makes the model more stable and generalizable.
- **Regularization**:  L2
- **Highlight**: Ideal when you want to keep all features but prevent any from dominating.

### 3. Lasso Regression

Lasso stands for **Least Absolute Shrinkage and Selection Operator**. It adds **L1 regularization**.

- **L1 Regularization**: Shrinks some weights to exactly zero, which means it can eliminate unimportant features completely.
- **When to use**: When you want automatic feature selection and a simpler model.
- **Benefit**: Can make the model easier to understand and more efficient.
- **Regularization**: L1
- **Highlight**: Great for simplifying models by ignoring irrelevant inputs.

### 4. SGDRegressor (Stochastic Gradient Descent)

SGDRegressor trains the model by **updating it one example at a time**, rather than using all data at once. It’s great for large datasets or online learning.

- **Regularization**: Supports L1, L2, or both (Elastic Net) — you can configure it.
- **L1** helps ignore irrelevant features.
- **L2** keeps the model smooth and stable.
- **Elastic Net** gives a balanced effect.
- **When to use**: For huge datasets or streaming data where traditional regression is too slow.
- **Benefit**: Very efficient and flexible.
- **Highlight**: Best choice when working with massive datasets or live/real-time data.

### 5. Elastic Net

Elastic Net **combines L1 and L2 regularization**, giving you the best of both worlds.

- **L1** helps remove unimportant features (by setting their coefficients to zero).
- **L2** keeps the model stable by shrinking large coefficients.
- **When to use**: When you have many features, especially if some are correlated or not useful.
- **Benefit**: Handles complex, high-dimensional data better than Lasso or Ridge alone.
- **Regularization**: L1 + L2 (controlled by `l1_ratio`)
- **Highlight**: A perfect balance for large, noisy, or messy datasets.

---

## Classification

### 1. Logistic Regression

Logistic Regression is a simple and widely used **classification** model. It predicts the probability of a class using a **curve (sigmoid function)** instead of a straight line.

- **When to use**: When the output should be a **binary or multi-class label**.
- **Regularization**: Supports **L1, L2, or both (Elastic Net)** — configurable.
- **Benefit**: Easy to interpret and fast to train.
- **Highlight**: Great for problems where **understanding why** the model made a decision is important.

### 2. Ridge Classifier

The Ridge Classifier works like Logistic Regression but uses Ridge (L2) regularization directly on the decision boundary.

- **When to use**: When you want a fast and simple classifier that avoids overfitting.
- **Regularization**: L2 only.
- **Benefit**: Stable even with correlated features.
- **Highlight**: Best when you want simplicity with automatic overfitting protection.

### 3. SGDClassifier (Stochastic Gradient Descent)

This model trains a linear classifier using a very efficient online approach, updating its weights with each example.

- **Regularization**: L1, L2, or Elastic Net.
- **When to use**: When you have huge datasets or need fast training.
- **Benefit**: Very customizable and memory-efficient.
- **Highlight**: Perfect for real-time or large-scale classification problems.

### 4. Passive Aggressive Classifier

This is an online learning algorithm that stays “passive” when predictions are correct but becomes “aggressive” on errors by updating heavily.

- **When to use**: For online learning—when data arrives continuously or in streaming.
- **Regularization**: L1 or L2.
- **Benefit**: Extremely fast and effective in changing environments.
- **Highlight**: Best when you need to react quickly to new incoming data.

### 5. Perceptron

The Perceptron is one of the earliest and simplest binary classifiers. It learns by adjusting weights whenever it makes errors.

- **When to use**: Simple binary classification tasks with **linearly separable** data.
- **Regularization**: Supports **optional L2 regularization**.
- **Benefit**: Fast, easy to implement, and good for educational purposes.
- **Highlight**: Great for understanding the foundations of machine learning.

---

## Clustering

### 1. KMeans

KMeans partitions data into a specified number of clusters (K) by minimizing the distance between data points and their cluster centers.

- **When to use**: When you have an idea of how many clusters you want.
- **Strength**: Fast and efficient, especially on large datasets.
- **Weakness**: Requires you to specify the number of clusters (K) beforehand; sensitive to outliers.
- **Highlight**: Works best when clusters are roughly spherical and similar in size.

### 2. Agglomerative Clustering

A type of hierarchical clustering that builds a tree of clusters by step-by-step merging the closest pairs.

- **When to use**: When you want a visual hierarchy or don’t know the number of clusters in advance.
- **Strength**: No need to specify the number of clusters upfront.
- **Weakness**: Can be slow on large datasets.
- **Highlight**: Great for understanding nested cluster structures (like a tree).

### 3. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

Finds clusters based on areas of high density, ignoring noise and outliers.

- **When to use**: When clusters have irregular shapes and noise is present.
- **Strength**: Can find non-spherical clusters and handle outliers well.
- **Weakness**: Struggles if densities vary too much across clusters.
- **Highlight**: Great for real-world messy data with noise.

### 4. Mean Shift

A centroid-based algorithm that shifts data points toward the **mode** (peak) of the data distribution.

- **When to use**: When you don’t want to specify the number of clusters.
- **Strength**: Automatically finds the number of clusters based on data density.
- **Weakness**: Can be slow on large datasets.
- **Highlight**: Best for discovering clusters with **unknown** and **uneven densities**.

### 5. Spectral Clustering

Uses graph theory and the eigenvalues of a similarity matrix to divide data into clusters.

- **When to use**: When clusters are non-convex or intertwined.
- **Strength**: Finds clusters with complex or irregular shapes.
- **Weakness**: Slower and requires tuning the similarity graph.
- **Highlight**: Great for separating complex, overlapping patterns that other algorithms struggle with.

## Time Series

### 1. ARIMA (AutoRegressive Integrated Moving Average)

ARIMA is a classic model used for forecasting time series data by combining three key elements:

- **AutoRegression (AR)** – uses past values.
- **Integration (I)** – makes data stationary by differencing.
- **Moving Average (MA)** – uses past forecast errors.
- **When to use**: When data shows trends but not strong seasonal patterns.
- **Strength**: Works well for stable and trend-based time series.
- **Weakness**: Doesn’t handle seasonality well by itself.
- **Highlight**: Great for capturing trends and autocorrelations in time-based data.

### 2. SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous variables)

SARIMAX extends ARIMA by adding seasonality and external factors (called exogenous variables) into the model.

- **When to use**: When your data has seasonal patterns (like monthly cycles) or is affected by outside variables (like holidays or weather).
- **Strength**: Can model seasonality and external influences.
- **Weakness**: Can be complex to tune (many parameters).
- **Highlight**: Ideal for time series with seasonal spikes and outside influences.

