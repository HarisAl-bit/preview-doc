# 📊 Table Widget

## Overview

The Table Widget displays data in a tabular format based on configured metrics and segments. Users can define value columns, segmentation on X and Y axes, and perform row/column calculations.

---

## Configuration

![Table Config](/vdata/documentation/xplorer/table/table-config.webp)
![Table Calculate Row](/vdata/documentation/xplorer/table/table-config-calculaterow.webp)
![Table Calculate Column](/vdata/documentation/xplorer/table/table-config-calculatecolumns-limit.webp)


| Property              | Description                                                                 | Example             |
|-----------------------|-----------------------------------------------------------------------------|---------------------|
| **Columns**           | Numeric fields to display as table values.                                 | `Sales`, `Profit`   |
| **Segment X**         | Field used as table rows (horizontal grouping).                            | `Region`            |
| **Segment Y**         | Field used as additional column segments (vertical grouping).              | `Product`           |
| **Calculate Rows**    | Add calculations (Sum, Avg, etc.) per row.                                 | `Sum of Sales`      |
| **Calculate Columns** | Add calculations (Sum, Avg, etc.) per column.                              | `Unset`             |
| **Limit**             | Limit the number of displayed records.                                     | All / Custom        |

---

## Style

![Table Style](/vdata/documentation/xplorer/table/table-style.webp)

| Section           | Property          | Description                                                    | Example              |
|------------------|-------------------|----------------------------------------------------------------|----------------------|
| **Table Title**   | Position          | Chart title alignment.                                         | `Top Center`         |
|                  | Size              | Font size of the title.                                        | `1px`                |
|                  | Color             | Title text color.                                              | `#000000`            |
| **Table Style**   | Border Style      | Table border style (`None`, `Solid`, etc.).                    | `None`               |
|                  | Width             | Border thickness.                                              | `0px`                |
|                  | Color             | Border color.                                                  | `#000000`            |
|                  | Background         | Table background color.                                        | `#FFFFFF`            |
| **Header Style**  | Weight            | Header font weight.                                            | `Normal`             |
|                  | Size              | Header font size.                                              | `10px`               |
|                  | Color             | Header font color.                                             | `#888888`            |
|                  | Background Color  | Header background color.                                       | `#F5F5F5`            |
|                  | Border Color      | Header border color.                                           | `#CCCCCC`            |
|                  | Text Align        | Text alignment in the header.                                  | `Auto`               |
| **Body Style**    | Weight            | Body font weight.                                              | `Normal`             |
|                  | Size              | Body font size.                                                | `10px`               |
|                  | Color             | Body font color.                                               | `#888888`            |
|                  | Background Color  | Body background color.                                         | `#FFFFFF`            |
|                  | Border Color      | Body border color.                                             | `#CCCCCC`            |
|                  | Text Align        | Text alignment in the body.                                    | `Auto`               |
