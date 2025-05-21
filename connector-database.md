# 🛢️ Connecting a Database to My Data

## Overview  
This tutorial explains how to connect relational database sources such as **MySQL**, **PostgreSQL**, and **SQLite** to **My Data**. Using database connectors, you can integrate structured data from existing databases, securely access both live and static datasets, and utilize that data for transformation, analysis, and real-time visualization within the platform.


---

## 1. Connecting MySQL & PostgreSQL  
To connect a **MySQL** or **PostgreSQL** database, provide the following credentials:

### Required Fields:
- **Database Name**: Name of the target database.
- **Database URL**: Hostname of the database server.
- **Database Port**: Default: `3306` for MySQL, `5432` for PostgreSQL.
- **Database Username**: Authorized user account for access.
- **Database Password**: Corresponding password for the user.

Click **"Connect Database"** to establish the connection.

![PostgreSQL Connection](/vdata/documentation/mydata/connect-db.webp)

---

## 2. Connecting SQLite  
To use a **SQLite** database, upload your `.sqlite` or `.db` file directly.

Click **"Upload File"**, then select the SQLite database file **or** paste the **URL link** of the database file.

![SQLite Connection](/vdata/documentation/mydata/connect-sqlite.webp)

---

## 3. Select Tables  
After a successful connection, you can choose which tables to include in **My Data**.

- A list of available tables will be shown.
- Select the tables you need.
- Click **"Next"** to proceed.

![Table Selection](/vdata/documentation/mydata/select-tabel.webp)

---

## 4. Config Connector  
Before completing the setup, passign a name to your connector configuration.

- Enter a **Data Name** that represents your database connection.
- Click **"Save"** to finish.

![Name Connector](/vdata/documentation/mydata/config-db.webp)

After completing these steps, your database data will be available in **My Data** for further processing.