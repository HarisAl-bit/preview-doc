# 🔀 Merge/Split Column – Volantis Pipeline

## Overview  
The **Merge/Split Column** feature allows you to either combine multiple columns into one (merge) or split a single column into several (split), based on your transformation goals.

You can use this to:  
- Merge columns like `Date` and `Time` into a new `Timestamp`.  
- Split values like `"2024-12-01"` into `Year`, `Month`, and `Day`.  
- Customize input, delimiter, and output columns freely.

---

## Merge Column Configuration

![Merge Column Config](/vdata/documentation/pipeline/merge-split-col/merge-con.webp)

- **Input**: Select multiple columns to be merged.  
- **Output Column Name**: Enter the name for the new merged column.  
  Example: `Timestamp`

> Values will be joined using a space or a custom delimiter (if supported).

---

## Split Column Configuration

![Split Column Config](/vdata/documentation/pipeline/merge-split-col/split-con.webp)

- **Input Column**: Select the column you want to split.  
- **Delimiter**: Define the character used to split the values (e.g., `-`).  
- **Output Columns**: Use ➕ to add custom output column names (e.g., `Year`, `Month`, `Day`).

---

## Previewing the Output

![Merge Split Column Preview](/vdata/documentation/pipeline/merge-split-col/merge-split-prev.webp)

Before saving, click **Preview** to check how your transformation will look:

- Ensure merged columns appear correctly with the delimiter.
- Confirm split columns are broken down as intended.
- Check output column names are as expected.
- Click **Save** to apply the changes.  

---