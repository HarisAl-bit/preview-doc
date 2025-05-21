# 🗺️ GeoMap Widget

### Overview

The GeoMap Chart displays geographic data by mapping numeric values onto cities or regions on a map. It’s particularly useful for visualizing spatial trends, comparing regional performance, and identifying geographic patterns.

This chart type is commonly used to highlight data like population, sales, or user engagement across cities, provinces, or countries. The color intensity on the map reflects the magnitude of the values — darker or more vibrant areas represent higher values.

GeoMap Charts are ideal for:

- Showing sales distribution by city or region
- Highlighting high-performance vs. low-performance areas
- Visualizing population or demographic metrics across regions

---

### Map Configuration

![GeoMap Config](/vdata/documentation/xplorer/geomap/geomap-config.webp)

| Field            | Description                                                                 | Example           |
|------------------|-----------------------------------------------------------------------------|-------------------|
| **Map**          | The base map used to plot data. Options: `Indonesia (cities)`, `Indonesia (regions)`, `World regions`. | `Indonesia (cities)` |
| **Matching Key** | Method used to match region names from your data with the map layer. See full list below. | `Local Name`      |
| **Column**       | The column that contains geographic names (city or province).               | `Provinsi`        |
| **Value**        | The metric that will be visualized via color intensity on the map.          | `Nilai`           |

#### **Available Matching Keys:**

| Name             | Value        |
|------------------|--------------|
| Country          | `country`    |
| Name             | `name`       |
| Local Name       | `locname`    |
| Wikidata         | `wikidata`   |
| Wikimedia        | `wikimedia`  |
| rpath            | `rpath`      |
| ISO3166_2        | `ISO3166_2`  |
| ISO Name         | `iso_name`   |
| HASC             | `hasc`       |
| FIPS             | `fips`       |
| Longitude Latitude | `longlat`  |

---

### Chart Style

![GeoMap Style](/vdata/documentation/xplorer/geomap/geomap-chart-style.webp)

| Property             | Description                                                                 | Example     |
|----------------------|-----------------------------------------------------------------------------|-------------|
| **Color Scheme**     | Color palette applied to the map regions.                                   | `Viridis`   |
| **Border Style**     | Visual style for region borders: `None`, `Solid`, `Dashed`, `Dotted`, `Double`. | `Solid`     |
| **Border Width**     | Thickness of region borders.                                                | `1px`       |
| **Border Color**     | Color of region borders in HEX.                                             | `#D9D9D9`   |
