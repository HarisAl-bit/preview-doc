# 🥧 Pie Chart & Bubble Chart Widgets

## Overview

These two chart types provide visual representation for different data relationships:

- **Pie Chart**: Ideal for showing proportions or parts of a whole.  
- **Bubble Chart**: Useful for displaying relationships between three numeric dimensions using position and bubble size.

---

## Axis Configuration

![Axis Config for Pie & Bubble Chart](/vdata/documentation/xplorer/pie-bubble/axis-config.webp)

| Property        | Description                                                                 | Example              |
|----------------|-----------------------------------------------------------------------------|----------------------|
| **Category**    | Field that defines grouping, labels, or X-axis position.                   | `Kampus`             |
| **Value**       | Numeric field used to calculate size (Pie slice size or Bubble size).      | `Jumlah Publikasi`   |
| **Limit**       | Maximum number of items to display. Adjusted using a slider.               | –                    |

> 💡 *In Bubble Charts, `Category` maps to the X-axis and `Value` defines bubble size. In Pie Charts, `Category` defines the slice label, and `Value` defines the slice size.*

---

## Chart Style

![Pie Chart Style](/vdata/documentation/xplorer/pie-bubble/pie-chart-style.webp)
![Bubble Chart Style](/vdata/documentation/xplorer/pie-bubble/bubble-chart-style.webp)

| Property           | Description                                                                                      | Example         |
|--------------------|--------------------------------------------------------------------------------------------------|-----------------|
| **Font Weight**    | Thickness of the text labels displayed on each bubble. Options: `Light`, `Medium`, `Bold`.       | `Medium`        |
| **Font Size**      | Size of the text labels inside the bubbles, in pixels.                                            | `10px`          |
| **Font Color**     | HEX color used for text labels in the bubble chart.                                               | `#000000`       |
| **Color Scheme**   | Color palette applied to the bubbles and chart elements.                                          | `darkblue`      |
| **Gravity X**      | Adjusts the horizontal position of the bubble chart within its container. Range: 0%–100%.         | `50%`           |
| **Gravity Y**      | Adjusts the vertical position of the bubble chart within its container. Range: 0%–100%.           | `50%`           |
| **Bubble Size**    | Controls the relative size of the bubbles. Range: 0%–100%.                                        | `100%`          |
