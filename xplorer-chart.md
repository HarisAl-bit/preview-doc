# 📊 Line, Bar, Area, and Scatter Chart Widgets

## Overview

These four chart types are used to visualize quantitative data across categories or time.  
- **Line Chart**: Best for showing trends over time.  
- **Bar Chart**: Ideal for comparing quantities across categories.  
- **Area Chart**: Like a Line Chart but with filled areas for emphasis.  
- **Scatter Chart**: Useful for visualizing correlations between two numeric variables.
- **Horizontal Bar** : Useful for comparing values across categories with long names. Bars go from left to right.

All these charts share the same configuration options.

---

## Axis Configuration

![Configuration Axis](/vdata/documentation/xplorer/common-chart/axis-config.webp)

| Property       | Description                                                                                     | Example                     |
|----------------|-------------------------------------------------------------------------------------------------|-----------------------------|
| **X-Axis**     | Field for the horizontal axis. Ideal for categories such as names, regions, or time periods.    | `Campus`                    |
| **Y-Axis**     | Field for the vertical axis. Typically used for numeric values to be measured.                 | `Publication Count`         |
| **Group By**   | (Optional) Allows you to split the data into multiple series based on a category.              | `Year`, `Department`        |
| **Limit**      | Sets the maximum number of items to display in the chart. Adjusted via slider.                 | –                           |
| **Sort by Value** | Determines the sorting order based on **X-Axis** values: <br> - `Unset`: Original order <br> - `Ascending`: A to Z / earliest to latest <br> - `Descending`: Z to A / latest to earliest | –         


---

## Column Configuration

![Configuration Column](/vdata/documentation/xplorer/common-chart/column-config.webp)

| Property         | Description                                                                                                                                                                                                                               | Example                        |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Data Type**     | Defines the data format of the selected field.<br>Options:<br>- `String`: Text-based categories<br>- `Integer`: Whole numbers<br>- `Float`: Decimal numbers                                                                             | `Campus`, `Publication Count` |
| **Encoding Type** | Determines how the data should be interpreted.<br>Options:<br>- `Nominal`: Categorical without order<br>- `Ordinal`: Categorical with order<br>- `Quantitative`: Numeric values<br>- `Temporal`: Time-based values                      | `Nominal`: `Campus`<br>`Quantitative`: `Total Score`<br>`Temporal`: `Year` |
| **Aggregation**   | Specifies how to summarize the field’s data.<br>Options:<br>`Unset`, `Count`, `Sum`, `Min`, `Max`, `Distinct`, `Mean`, `Average`, `Variance`, `Variancep`, `Stdev`, `Stdevp`, `Stderr`, `Median`, `Q1`, `Q3`                             | `Sum` for revenue, `Count` for entries |
| **Sort**          | Controls the sorting order of the field values.<br>Options:<br>- `Unset`: No sorting<br>- `Ascending`: A to Z / 0 to 100<br>- `Descending`: Z to A / 100 to 0                                                                            | –                              |
| **Filter**        | Applies conditions to include only specific values.<br>Options:<br>`Equal`, `Not Equal`, `Lower Than`, `Lower Than Equal`, `Greater Than`, `Greater Than Equal`, `Contain`, `Not Contain`, `Regex`                                      | `Campus = UI`, `Year > 2020`  |
| **Value**         | Input field for specifying the target value in the selected filter.                                                                                                                               | `UI`, `2022`, `>= 100`         |

---
## Chart Style

![Chart Style](/vdata/documentation/xplorer/common-chart/chart-style.webp)

| Property                  | Description                                                                                  | Example            |
|---------------------------|----------------------------------------------------------------------------------------------|--------------------|
| **Border Style**          | Visual style for the chart border. Options: `None`, `Solid`, `Dashed`, `Dotted`, `Double`.  | `Solid`            |
| **Width (Border)**        | Thickness of the chart border in pixels.                                                    | `1px`              |
| **Color (Border)**        | Color of the chart border in HEX code.                                                      | `#CCCCCC`          |
| **Horizontal Grid**       | Style of the horizontal guide lines across the chart. Options same as Border Style.         | `Dashed`           |
| **Width (Horizontal Grid)** | Thickness of horizontal lines in pixels.                                                   | `1px`              |
| **Color (Horizontal Grid)** | Color of horizontal lines.                                                                 | `#E0E0E0`          |
| **Vertical Grid**         | Style of the vertical guide lines along the X-axis. Options same as Border Style.           | `Dotted`           |
| **Width (Vertical Grid)** | Thickness of vertical grid lines.                                                           | `1px`              |
| **Color (Vertical Grid)** | Color of vertical grid lines.                                                               | `#E0E0E0`          |
| **Chart Color**           | Primary color used for chart elements such as bars, lines, or points.                       | `#5B9BD5`          |
| **Background**            | Background color of the entire chart area.                                                  | `#FFFFFF`          |

---


## Example Preview

> **Line Chart**
>
> ![Line Chart Example](/vdata/documentation/xplorer/common-chart/line-chart.webp)

> **Bar Chart**
>
> ![Bar Chart Example](/vdata/documentation/xplorer/common-chart/bar-chart.webp)

> **Area Chart**
>
> ![Area Chart Example](/vdata/documentation/xplorer/common-chart/area-chart.webp)

> **Scatter Chart**
>
> ![Scatter Chart Example](/vdata/documentation/xplorer/common-chart/scatter-chart.webp)

> **Horizontal Bar Chart**
>
> ![Horizontal Example](/vdata/documentation/xplorer/common-chart/horizontal-bar-chart.webp)

