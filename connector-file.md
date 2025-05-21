# 📄 Connecting File to My Data  

## Overview
This tutorial explains how to connect and upload file-based data sources—such as CSV, PDF, Excel (XLSX), and more—into **My Data**. Using the file connectors, you can upload both structured and unstructured data, automatically extract and map relevant information, and prepare the data for further processing, analysis, or visualization within the platform.

---

## 1. Navigate to My Data  
Go to **My Data**: [My Data](/vdata/my-data)  

![MyData Homepage](/vdata/documentation/mydata/mydata-1.webp)

---

## 2. Upload a File  
1. Click the **"Upload Data"** button.  
2. Select a file from your local storage.  
3. Supported formats:  
   - **CSV (`.csv`)** – Tabular data in plain text format.  
   - **Excel (`.xls`, `.xlsx`)** – Spreadsheet files with support for multiple sheets.  
   - **PDF (`.pdf`)** – Documents that may contain text or tables.  
   - **Word (`.doc`, `.docx`)** – Text documents.  
   - **PowerPoint (`.ppt`, `.pptx`)** – Presentation files.  
   - **Images (`.jpeg`, `.jpg`, `.png`, `.webp`)** – Common image formats.

![Upload File](/vdata/documentation/mydata/mydata-2.webp)

---

## 3. Mapping Data from Tabular Files
After uploading, the system will **automatically detect** the table structure.  
Navigate to **Data Mapping Configuration** to adjust the settings.

![Mapping Data](/vdata/documentation/mydata/mapping-data.webp)

### **Table Range**  
- **Skip Columns**: Ignore unnecessary columns.  
- **Skip Rows**: Remove unwanted rows (e.g., empty or metadata rows).  
- **Number of Columns & Rows**: Specify exact dimensions if needed.  

### **Table Header**  
- **Number of Header Rows**: Define how many rows contain column names.  

### **Timestamp Column**  
- Select the column that contains **timestamps** (e.g., dates or time values).  

Click **Preview** to review and apply the existing settings if they are correct, then click **Save** to finalize the mapping.

---

## 4. View & Manage Uploaded Data  
Once uploaded, the file will appear in **My Data**.  

- Click the **data** to open and preview the content.  
- Use the **Statistic** tab for automatic data insights.  
- Navigate to **Sharing** to share.  

![View Data](/vdata/documentation/mydata/mydata-3.webp)

---

## Next Steps  
Try uploading your first file and explore the available features!  
To start, go here.: [Demo Volantis Data](/vdata/my-data)  
