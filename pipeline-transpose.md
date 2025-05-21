# 🔀 Transpose – Volantis Pipeline

## Overview  
The **Transpose** feature in Volantis Pipeline allows you to pivot your data by transforming multiple rows into columns based on a stub column.

With **Transpose**, you can:  
- Pivot rows into columns using a stub (key) column.  
- Customize the name and format of the resulting column.  
- Standardize the column name casing (e.g., lowercase, UPPERCASE, Proper Case).  
- Preview results before saving.  
- Save the transformed data as a new table for further use.

---

## Configuration Options

![Transpose Config](/vdata/documentation/pipeline/transpose/transpose-config.webp)

### 1. **Stub Column**  
This column will be used as the reference for transposing rows into columns.

- **Column Name:** `Transpose`  
  *(This will serve as the new header or column identifier in the transposed table)*

- **Format Column Name:**  
  Choose how the column names will be formatted after transposition:

  - `Lower Case` → e.g., `city`, `province`, `country`  
  - `Upper Case` → e.g., `CITY`, `PROVINCE`, `COUNTRY`  
  - `Proper Case` → e.g., `City`, `Province`, `Country`

---

## Previewing the Output  

![Transpose Preview](/vdata/documentation/pipeline/transpose/transpose-preview.webp)

Click the **Preview** button to see a visual representation of the transposed table before finalizing the transformation. This helps ensure that the stub column and formatting are correctly applied.

---

## Saving the Transformation  
Once you're satisfied with the configuration:

1. Click **Save** to apply your transpose settings.  
2. A new [**Job**](/vdata/documentation?page=jobs) will be created to process the transformation.  
3. After completion, the transposed dataset will be available in your model library.
