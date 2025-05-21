# ✍️ Text To Column – Volantis Pipeline

## Overview  
The **Text To Column** feature in Volantis Pipeline allows you to split a single column containing combined text into multiple columns based on a specified delimiter (e.g., commas).  

With **Text To Column**, you can:  
- Split values like `"Kota, Provinsi, Negara"` into separate columns.  
- Define custom column names for the results.  
- Preview the output instantly before saving changes.  
- Save the result as a transformed table for further use.

---

## Configuration Options

![Text To Column Config](/vdata/documentation/pipeline/text-to-column/text-to-column-config.webp)

### 1. **Input Column**  
Select the column that contains the combined values you want to split.

- **Field:** `Location`  
  *(In this example, the column contains values like `"Kota1, Provinsi1, Negara1"`)*

- **Delimiter:** `,`  
  *(The character that separates values in the column)*

---

### 2. **Output Columns**  
Define the new column names that will hold the separated values.

- **Column 1 Name:** `kota`  
- **Column 2 Name:** `provinsi`  
- **Column 3 Name:** `negara`  

You can add or remove column fields based on how many values you're splitting from the original string.

---

## Previewing the Output  
To check if the column was split correctly, click the **Preview** button. This will show you a live preview of the transformed data.

![Text To Column Preview](/vdata/documentation/pipeline/text-to-column/text-to-column-preview.webp)

---

## Saving the Transformation  
Once satisfied with the configuration:

1. Click the **Save** button to save your setup.  
2. This will schedule a [**Job**](/vdata/documentation?page=jobs) to process the transformation.  
3. After the job completes, the updated table will be available in your model library.
