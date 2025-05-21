# 🎨 Widget Style Configuration

This section provides customization options for the appearance of your chart widgets.  
Use these settings to adjust titles, footers, axis appearance, borders, background, and more.

## Table of Contents

- [Chart Title](#chart-title)  
  Customize the main title's text, position, size, and color.

- [Chart Footer](#chart-footer)  
  Add annotations, data source info, and control text styling.

- [Chart Style](#chart-style)  
  Configure the chart's border, gridlines, background, and primary colors.

- [Axis Style (X and Y Axis)](#axis-style-x-and-y-axis-)  
  Adjust axis label fonts, colors, alignment, and padding.

---

## Chart Title

![Chart Title](/vdata/documentation/xplorer/common-chart/chart-title.webp)

| Property        | Description                                                                                                       | Example                               |
|----------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| **Chart Title** | Enter the title text to be displayed at the top or bottom of the chart.                                           | `Publication Trends by University`   |
| **Position**    | Defines the alignment of the title. Options:<br>- `Top Left`<br>- `Top Center`<br>- `Top Right`<br>- `Bottom Left`<br>- `Bottom Center`<br>- `Bottom Right` | `Top Center`                          |
| **Size**        | Sets the font size of the chart title in pixels.                                                                | `12px`, `16px`                        |
| **Color**       | Defines the color of the title text using HEX code.                                                             | `#000000` (black), `#FF0000` (red)    |

---

## Chart Footer

![Chart Footer](/vdata/documentation/xplorer/common-chart/chart-footer.webp)

| Property             | Description                                                                                               | Example                                                      |
|----------------------|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| **Notes**            | A short annotation or remark that provides additional context to the chart.                              | `* Data includes publications from 2020 to 2024`             |
| **Font Weight**      | Determines the thickness of the footer text. Options: `Normal`, `Bold`, `Lighter`.                        | `Normal`                                                     |
| **Size**             | Font size of the footer text in pixels.                                                                   | `12px`                                                       |
| **Color**            | Text color of the footer section in hexadecimal format.                                                   | `#4A4A4A` (dark gray)                                        |
| **Data Source**      | Name of the institution or platform where the data originated.                                            | `Ministry of Research and Technology`                       |
| **Data Source Link** | A direct hyperlink to the dataset or its source for transparency and verification purposes.               | `https://data.ristekbrin.go.id/publications`                |

---

## Chart Style

The **Chart Style** configuration is available on each individual chart’s documentation page. Since each chart type (e.g., Line, Bar, Pie, Bubble) may have different styling options and behaviors, the style settings are provided within their respective pages to ensure clarity and relevance. Please refer to the specific chart documentation for detailed and accurate style configurations.

---

## Axis Style (X and Y Axis)

![Axis Style](/vdata/documentation/xplorer/common-chart/xy-axis-style.webp)

| Property        | Description                                                                                      | Example                             |
|-----------------|--------------------------------------------------------------------------------------------------|-------------------------------------|
| **Title**        | Label describing what the axis represents.                                                      | `Campus`, `Publication Count`       |
| **Title Size**   | Font size of the axis title in pixels.                                                          | `12px`                              |
| **Title Color**  | HEX code representing the color of the title.                                                   | `#000000`                           |
| **Label Align**  | Alignment of axis labels. Options: `Left`, `Center`, `Right`.                                   | `Right`                             |
| **Label Size**   | Font size of axis tick labels.                                                                  | `10px`                              |
| **Label Color**  | Color of axis labels.                                                                            | `#333333`                           |
| **Angle (X-Axis only)** | Rotation angle of X-axis labels to prevent text overlapping.                             | `45°`                               |
| **Padding**      | Spacing between axis content and the chart area (in pixels).                                    | `10px`                              |

## Legend Style

![Legend Style](/vdata/documentation/xplorer/pie-bubble/pie-chart-legend.webp)

This section allows you to customize the appearance of the legend in pie charts.

| Property          | Description                                                                 | Example              |
|-------------------|-----------------------------------------------------------------------------|----------------------|
| **Title**         | Optional label to describe the legend section.                              | `Department Type`    |
| **Size (Title)**  | Font size of the legend title in pixels.                                    | `14px`               |
| **Color (Title)** | Color of the legend title text in HEX format.                               | `#000000` (black)    |
| **Item Position** | Position of the legend relative to the chart. Options: `Top`, `Bottom`, `Left`, `Right`. | `Right`              |
| **Size (Item)**   | Font size of each legend item.                                               | `10px`               |
| **Color (Item)**  | Text color of legend items.                                                  | `#333333`            |
