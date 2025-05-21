# 🗂️ Create Table – Volantis Pipeline

## Overview  
The **Create Table** feature in Volantis Pipeline allows you to generate a new table based on the result of a transformation or selection process.

With **Create Table**, you can:  
- Name and create a new table from transformed data.  
- Choose which columns to include or exclude from the final output.  
- Automatically save the result into your model library.  
- Proceed with further analysis or visualization using the new table.

---

## Configuration

![Create Table Configuration](/vdata/documentation/pipeline/create-table/table-config.webp)

| Section         | Property           | Description                                                                 | Example               |
|------------------|--------------------|-----------------------------------------------------------------------------|------------------------|
| **Table Name**    | Output Table Name  | The name for the new table that will be saved into your model library.     | `table_income_q1`     |
| **Columns**       | Exclude Columns    | Select columns to exclude from the final result. Unchecked columns will be included. | Uncheck `Tahun`, `Triwulan I` |

> Use the **Reset** button to revert to default column selections.

---

## Previewing the Output

![Create Table Preview](/vdata/documentation/pipeline/create-table/table-preview.webp)

Click the **Preview** button to review how your table will look after creation. This allows you to verify the table name and column selection before saving.

> Preview is especially useful for confirming excluded columns are correct.

---

## Saving the Table

Once you've configured and previewed your table:

1. Enter a suitable **Table Name**.  
2. Select the columns you want to exclude.  
3. Click **Save** to create the new table.  
4. The resulting table will be saved and accessible via your model library.

---

## Example Output

If your original dataset looks like this:

| Tahun | Triwulan I | Triwulan II | Triwulan III | Triwulan IV | Total |
|-------|------------|-------------|--------------|-------------|-------|
| 2023  | 100        | 120         | 130          | 140         | 490   |

And you exclude:
- `Tahun`  
- `Triwulan I`  
- `Triwulan II`

Then your **Create Table** output will be:

| Triwulan III | Triwulan IV | Total |
|--------------|-------------|-------|
| 130          | 140         | 490   |
