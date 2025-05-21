# 🧩 JSON To Column – Volantis Pipeline

## Overview  
The **JSON To Column** feature in Volantis Pipeline allows you to extract structured data from a JSON-formatted column and convert selected fields into separate columns. This is useful when dealing with columns that contain nested JSON objects, such as metadata or API responses.

With **JSON To Column**, you can:
- Parse a JSON object from a single column.
- Select specific keys (fields) from the JSON to extract.
- Define custom output column names and data types.
- Preview the extracted structure before saving.

---

## Configuration Options

![JSON To Column Config](/vdata/documentation/pipeline/json-to-column/json-to-column-config.webp)

### 1. **Input Settings**

- **Column:** `metadata`  
  *(This is the column containing JSON objects like `{"id": 123, "first_name": "John", "last_name": "Doe"}`)*

- **JSON View:**  
  Select the keys you want to extract from the JSON:
  - ✅ `id`
  - ✅ `first_name`
  - ✅ `last_name`

---

### 2. **Output Columns**  
Configure the name and data type for each extracted field:

| Output Column Name | Type     |
|--------------------|----------|
| `id`               | Auto     |
| `first_name`       | Auto     |
| `last_name`        | Auto     |

The data type is auto-detected but can be customized based on your needs (e.g., `string`, `number`).

---

## Previewing the Output  
Click the **Preview** button to see a live sample of the extracted columns. This helps verify that the JSON keys were correctly parsed and mapped.

![JSON To Column Preview](/vdata/documentation/pipeline/json-to-column/json-to-column-preview.webp)

---

## Saving the Transformation  
Once you're satisfied with the configuration:

1. Click the **Save** button to store the transformation setup.  
2. This will initiate a [**Job**](/vdata/documentation?page=jobs) to extract and generate the new columns.  
3. After completion, the resulting dataset will be available in the model library or for further processing in your pipeline.

---

## Example Output  
Given an input like:

| metadata                                      |
|----------------------------------------------|
| {"id": 1, "first_name": "John", "last_name": "Doe"} |
| {"id": 2, "first_name": "Jane", "last_name": "Smith"} |

The output after transformation will be:

| id | first_name | last_name |
|----|------------|-----------|
| 1  | John       | Doe       |
| 2  | Jane       | Smith     |
