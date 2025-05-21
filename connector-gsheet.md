# 📑 Connecting Google Sheets to My Data  

## Overview  
This tutorial explains how to connect Google Sheets to My Data for seamless data integration. By using the Google Sheets connector, you can import spreadsheets directly from Google Drive, automatically detect and map structured tabular data, and leverage your sheet data for processing, analysis, and visualization.

---

## 1. Select a Google Account  
To get started, connect a Google account that has access to the desired Google Sheet.

### Steps:  
1. Click **"Add New Account"** on the **Connect to Google Sheet** page.  
2. A list of available Google accounts will appear.  
3. Select the **Google account** you wish to use.  
4. Follow the authorization prompts to grant Volantis the required permissions.  
5. After a successful connection, the system will display a list of accessible **Google Sheets** from the selected account.
  

![Google Sheet Connection](/vdata/documentation/mydata/add-account-gsheet.webp)  

---

## 2. Select a Google Sheet  
Once the account is connected, choose a Google Sheet to import.

![Select Account](/vdata/documentation/mydata/select-account-gsheet.webp)  ![Select G-Sheet](/vdata/documentation/mydata/select-gsheet.webp)  


### Steps:  
1. Browse the list of available Google Sheets.  
2. Select the sheet you want to use with **My Data**.  

---

## 3. Mapping Data from Tabular Files  
After selecting a sheet, the system will automatically detect the tabular structure.  
Use the **Data Mapping Configuration** to review and adjust the import settings.


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

**Done!**  
Your Google Sheet is now successfully connected to **My Data**, and you can start using it for further analysis.  