# 🎯 Gauge Chart Widget

### Overview

The Gauge Chart is a circular meter that shows how a single value compares to a target or a scale. It's highly effective for tracking performance metrics or thresholds in a visually appealing way.

This chart type is commonly used in dashboards to monitor KPIs, such as sales targets, system utilization, or progress completion. The needle indicates the current value, while the gauge arcs represent predefined ranges.

Gauge Charts are ideal for:

- Visualizing KPI progress (e.g., sales vs. goal)
- Highlighting performance ranges (e.g., low, medium, high)
- Monitoring real-time values like system load or user count

---

### Axis Configuration

![Axis Config](/vdata/documentation/xplorer/gauge/gauge-config.webp)

| Field        | Description                                                                 | Example            |
|--------------|-----------------------------------------------------------------------------|--------------------|
| **Category** | The label used to identify the category displayed on the gauge.             | `Produk`           |
| **Value**    | The numeric metric that determines the needle position on the gauge.        | `Jumlah_Terjual`   |
| **Highlight**| Highlights a specific category on the gauge with a custom color or emphasis.| `Kopi`             |


---

### Gauge Style

![Gauge Style](/vdata/documentation/xplorer/gauge/gauge-style.webp)

| Property          | Description                                                              | Example         |
|-------------------|--------------------------------------------------------------------------|-----------------|
| **Base Color**     | Background color of the gauge arc when no value is present.              | `#E0E0E0` (light grey) |
| **Highlight Color**| The color used to highlight selected or emphasized segments.             | `#FFEB3B` (yellow)     |
| **Needle Color**   | Color of the pointer/needle.                                             | `#FFA500` (orange)     |
| **Label Size**     | Font size for the category label.                                        | `20px`          |
| **Label Color**    | Color of the category label text.                                        | `#000000` (black)|
| **Value Size**     | Font size for the numeric value displayed inside the gauge.              | `30px`          |
| **Value Color**    | Color of the numeric value text.                                         | `#000000` (black)|
