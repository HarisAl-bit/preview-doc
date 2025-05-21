# 📊 Volantis Xplorer User Guide

## Overview  
This guide helps you get started with **Volantis Xplorer**, a powerful tool to build interactive and visually rich dashboards using your data.

With Volantis Xplorer, you can:  
- Create custom dashboards with multiple pages and widgets.  
- Visualize your data using charts, tables, texts, and more.  
- Customize layout, themes, and publish dashboards for sharing and collaboration.

---

## 1. Access Volantis Xplorer
- Navigate to the **Volantis Xplorer** page: [Volantis Xplorer](/vdata/xplorer)

## 2. View All Dashboards
- Go to the **All Dashboard** page to see the list of available dashboards.

![All Dashboard](/vdata/documentation/xplorer/xplorer-1.webp)

## 3. Create a New Dashboard
- To create a new dashboard, click the **+** button or **+ New Xplorer**.

![New Dashboard](/vdata/documentation/xplorer/xplorer-2.webp)

## 4. Configure Dashboard Details
Set up the dashboard details as follows:

- **Dashboard Name**: Enter the name of the dashboard.  
- **Pages**: Define the number of pages for the dashboard.  
- **Title**: Set the title for each page.  
- **Dashboard Color**: Choose a color for the dashboard.  
- **Dashboard Pattern**: Select a pattern for the dashboard.  
- **Pattern Color**: Choose the color for the pattern.  
- **Page Size**: The dashboard size is adjusted based on the device being used and configured in **Page Size**.  
- **Save Settings**: Click **"Save"** to apply and store the new dashboard settings.

![Dashboard Settings](/vdata/documentation/xplorer/xplorer-3.webp)

## 5. Add a Widget
- To add a widget to your dashboard, click **New Widget** and select the type of widget (chart, table, image, etc.) from the available options.

![Dashboard Settings](/vdata/documentation/xplorer/xplorer-4.webp)

## 6. Select a Widget to Use
- Choose the widget you want to add from the list of available options.

![Dashboard Settings](/vdata/documentation/xplorer/xplorer-5.webp)

## 7. Widget Configuration
- Each widget has its own unique configuration options based on its type and functionality. For a complete guide on how to configure a specific widget, please refer to the detailed instructions available on the corresponding widget documentation page.

## 8. Column Configuration

![Configuration Column](/vdata/documentation/xplorer/common-chart/column-config.webp)

| Property         | Description                                                                                                                                                                                                                               | Example                        |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| **Data Type**     | Defines the data format of the selected field.<br>Options:<br>- `String`: Text-based categories<br>- `Integer`: Whole numbers<br>- `Float`: Decimal numbers                                                                             | `Campus`, `Publication Count` |
| **Encoding Type** | Determines how the data should be interpreted.<br>Options:<br>- `Nominal`: Categorical without order<br>- `Ordinal`: Categorical with order<br>- `Quantitative`: Numeric values<br>- `Temporal`: Time-based values                      | `Nominal`: `Campus`<br>`Quantitative`: `Total Score`<br>`Temporal`: `Year` |
| **Aggregation**   | Specifies how to summarize the field’s data.<br>Options:<br>`Unset`, `Count`, `Sum`, `Min`, `Max`, `Distinct`, `Mean`, `Average`, `Variance`, `Variancep`, `Stdev`, `Stdevp`, `Stderr`, `Median`, `Q1`, `Q3`                             | `Sum` for revenue, `Count` for entries |
| **Sort**          | Controls the sorting order of the field values.<br>Options:<br>- `Unset`: No sorting<br>- `Ascending`: A to Z / 0 to 100<br>- `Descending`: Z to A / 100 to 0                                                                            | –                              |
| **Filter**        | Applies conditions to include only specific values.<br>Options:<br>`Equal`, `Not Equal`, `Lower Than`, `Lower Than Equal`, `Greater Than`, `Greater Than Equal`, `Contain`, `Not Contain`, `Regex`                                      | `Campus = UI`, `Year > 2020`  |
| **Value**         | Input field for specifying the target value in the selected filter.                                                                                                                               | `UI`, `2022`, `>= 100`         |

## 9. Publish Dashboard
- Once your dashboard is set up with the desired widgets, click **Publish** to share and make the dashboard accessible to others.

![Dashboard Settings](/vdata/documentation/xplorer/xplorer-6.webp)

To start using Volantis Model Xplorer, go here.: [Volantis Xplorer](/vdata/xplorer)

---

## Available Widget Types

Volantis Xplorer offers a wide range of widget types that can be added to your dashboard to display various forms of data visualizations and information. Below is a list of available widget types with links to their detailed usage sections.

1. [Line Chart](/vdata/documentation?page=xplorer-chart)
2. [Bar Chart](/vdata/documentation?page=xplorer-chart)
3. [Area Chart](/vdata/documentation?page=xplorer-chart)
4. [Pie Chart](/vdata/documentation?page=xplorer-pie-bubble)
5. [Scatter Chart](/vdata/documentation?page=xplorer-chart)
6. [Heatmap Chart](/vdata/documentation?page=xplorer-heatmap)
7. [Bubble Chart](/vdata/documentation?page=xplorer-pie-bubble)
8. [Geomap](/vdata/documentation?page=xplorer-geomap)
9. [Horizontal Bar](/vdata/documentation?page=xplorer-chart)
10. [Gauge Chart](/vdata/documentation?page=xplorer-gauge)
11. [Score Card](/vdata/documentation?page=xplorer-scorecard)
12. [Table](/vdata/documentation?page=xplorer-table)
13. [Text](/vdata/documentation?page=xplorer-text)
14. [Prompt](/vdata/documentation?page=xplorer-prompt)

For more information on using these tools, refer to the specific tool sections in this documentation.