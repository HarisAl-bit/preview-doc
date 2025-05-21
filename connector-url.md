# 🌐 Connecting File from URL to My Data

## Overview  
This tutorial explains how to upload a **file-based dataset from a URL** into **My Data**. With this method, you can quickly connect remote files without manually downloading them first. This is especially useful when your data source is hosted on the web or in a public cloud service.

---

## 1. Navigate to My Data  
Go to **My Data**: [My Data](/my-data)

---

## 2. Upload from URL  

![MyData Page](/documentation/mydata/url-1.webp)
![Upload from URL](/documentation/mydata/url-2.webp)

1. Click the **"+ New Data"** button on the right panel.  
2. Switch to the **Upload from URL** tab.  
3. Paste the **URL of your file** into the input field.  
   > Format URL :  
   > `https://your-server.com/files/your-data.xlsx`

4. Click **"Upload Data"** to start the import.

**Supported file formats:**  
- `.csv` (Comma-Separated Values)  
- `.xlsx`, `.xls` (Excel files)  
- `.json` (Structured JSON)  
- `.sqlite`, `.db` (SQLite Database)  
- `.txt`
- `.pdf`, `.docx`, `.pptx` *(limited preview for unstructured types)*

---

## 3. Mapping Tabular Data (If Applicable)  
If the uploaded file is tabular (CSV, Excel, etc.), the system will automatically analyze its structure and present you with **mapping options**.

You can:  
- Skip empty rows or metadata rows.  
- Set the number of header rows.  
- Choose which column to use as a timestamp (if available).  
- Preview data before saving.

Click **"Save"** to confirm and import your file.

---

## 4. View & Manage the Imported File  
Once uploaded successfully, the file will appear in the **My Data** list.

- Click on the dataset name to preview its content.  
- Use the **Statistics** tab for automatic insights.  
- You can rename, share, or enrich the dataset using the platform tools.

---

## Example Public File URLs  
Here are some sample URLs you can try with this feature:

```text
https://people.sc.fsu.edu/~jburkardt/data/csv/airtravel.csv
