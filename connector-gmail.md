# 📧 Connecting Gmail to My Data  

## Overview  
This tutorial explains how to connect your **Gmail account** to **My Data**. The Gmail connector allows you to import email data directly from your Google account, select specific fields such as sender, subject, and date, apply filters using Gmail labels, and prepare the data for further analysis, tracking, or reporting.

---

## 1. Select a Google Account  
To begin, connect your Google account to authorize Gmail data access.

![Google Account Connection](/vdata/documentation/mydata/connect-gmail.webp)  

1. Click **"Add New Account"** on the Gmail connector page.  
2. Choose your Google account from the list.  
3. Follow the authorization prompts to grant Volantis access.  
4. Once connected, a configuration sidebar will appear.

---

## 2. Configure Gmail Data Import  
After connecting your account, configure how email data should be imported.

![Select Account Gmail](/vdata/documentation/mydata/select-account-gmail.webp)  ![Configure Gmail Data](/vdata/documentation/mydata/configuration-gmail.webp)  

1. Enter a **Dataset Name** (e.g., "Gmail Account example@gmail.com").  
2. Choose the **Download Initial Data** range (e.g., "Last Three Days").  
3. **Select Columns** to include (e.g., Created At, Subject, From, To, etc.).  
4. **Select Labels** (e.g., "All Messages," "INBOX," "SENT," etc.).  
5. Click **"Save Data"** to finalize the connection.

---

**Done!**  
Your Gmail data is now available in **My Data**. You can preview the dataset, apply filters, or use it as input in the **Pipeline** for processing and visualization.