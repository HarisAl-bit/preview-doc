# 🔽 Filter Widget

## Overview

The **Filter Widget** allows users to apply dynamic filters to one or more widgets that use the same data source (table). It helps users interactively narrow down the data displayed on charts, tables, or other visual components.

---

## User Flow

1. **Add the Filter Widget to the dashboard**  
   ![Step 1 - Add Filter Widget](/vdata/documentation/xplorer/filter/filter-add.webp)

2. **Configure the filter**  
   - Select the column you want to use as a filter  
   - Choose the appropriate condition (e.g., Equal, Not Equal, Greater Than)  
   ![Step 2 - Configure Filter](/vdata/documentation/xplorer/filter/filter-add-col.webp)

> The Filter Widget will affect any chart or widget that shares the same data table.

---

## Filter Configuration

![Filter Configuration](/vdata/documentation/xplorer/filter/filter-config.webp)

| Section   | Property        | Description                                                                 | Example               |
|-----------|------------------|-----------------------------------------------------------------------------|------------------------|
| **Columns** | Add Column       | Select one or more columns to use as filters.                               | `Date`                |
| **Filter**  | Equal            | Filters data where the column value is equal to a specific value.           | `Equal to "2025-01-01"`|
|             | Not Equal       | Filters data that do not match the specified value.                         | `Not equal to "X"`     |
|             | Lower Than      | Filters values less than a specified threshold.                             | `< 100`                |
|             | Lower Than Equal| Filters values less than or equal to a value.                               | `<= 100`               |
|             | Greater Than    | Filters values greater than a specified threshold.                          | `> 100`                |
|             | Greater Than Equal | Filters values greater than or equal to a value.                         | `>= 100`               |

---

> *Use the Filter Widget to control the visibility of data across your dashboard and improve data exploration experience.*
