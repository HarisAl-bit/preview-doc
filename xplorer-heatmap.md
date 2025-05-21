# 🚦 Heatmap Chart Widgets

### Overview

The Heatmap Chart provides a visual representation of data intensity across two categorical dimensions using color gradients. It’s especially effective for identifying patterns, trends, and anomalies in large datasets.

This chart type is commonly used to display activity over time (e.g., interactions by hour and day), allowing users to quickly spot peak usage periods or lulls in engagement. Each cell’s color represents the magnitude of the corresponding value, with darker or more saturated shades indicating higher values.

Heatmap Charts are ideal for:

- Time-based behavior analysis (e.g., user interactions by day and hour)
- Highlighting dense vs sparse areas in a dataset
- Comparing values across multiple categories simultaneously

---

### Axis Configuration

![Axis Config](/vdata/documentation/xplorer/heatmap/heatmap-config.webp)

| Field     | Description                                               | Example    |
|-----------|-----------------------------------------------------------|------------|
| **X-Axis**| The horizontal category (e.g. Day, Category, Location).   | `Day`      |
| **Y-Axis**| The vertical category (e.g. Hour, User, Status).          | `Hour`     |
| **Value** | The metric/value that determines the color intensity.     | `Interactions` |


## Chart Style

![Chart Style](/vdata/documentation/xplorer/heatmap/heatmap-chart-style.webp)

| Property           | Description                                                                                      | Example         |
|--------------------|--------------------------------------------------------------------------------------------------|-----------------|
| **Border Style**          | Visual style for the chart border. Options: `None`, `Solid`, `Dashed`, `Dotted`, `Double`.  | `Solid`            |
| **Width (Border)**        | Thickness of the chart border in pixels.                                                    | `1px`              |
| **Color (Border)**        | Color of the chart border in HEX code.                                                      | `#CCCCCC`          |
| **Color Scheme**   | Color palette applied to the bubbles and chart elements.                                          | `darkblue`      |