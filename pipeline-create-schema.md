# 🏗️ Create Schema – Volantis Pipeline

## Overview  
The **Create Schema** feature allows users to define a new table (schema) structure to store and manage data across pipelines or API interactions. It also provides granular control over who can access, modify, or delete the data through **API Rules**.

This feature is useful for:

- Structuring custom datasets.  
- Defining primary keys for unique identification.  
- Controlling user permissions with API access rules.  
- Setting up authentication-ready tables.

---

## Configuration

![Create Schema Config](/vdata/documentation/pipeline/create-schema/create-schema-col.webp)

| Section                 | Property                  | Description                                                                 | Example                |
|-------------------------|---------------------------|-----------------------------------------------------------------------------|------------------------|
| **User Auth Table**     | Toggle                    | Enable this if the table should be used as an authentication user table.   | OFF (default)          |
| **Table Name**          | Input Field               | The name of the new table/schema.                                           | `schema_fc854f`        |
| **Columns**             | Column List               | Add one or more columns with optional primary key designation.              | `id`, `name`, `email`  |
| **Primary Key**         | Checkbox                  | Mark one or more columns as the primary identifier.                         | `id`                   |
| **+ New Column**        | Action Button             | Add a new column definition to the schema.                                  | –                      |

---

## API Rules

![API Rules Config](/vdata/documentation/pipeline/create-schema/create-schema-api.webp)

This section allows fine-grained access control to the schema via API endpoints.

| Rule Type       | Description                                                   | Default Behavior                     | Example Expression                 |
|------------------|---------------------------------------------------------------|--------------------------------------|------------------------------------|
| **List Rule**     | Defines who can list all records in the table.               | Open to everyone if left empty       | `user.role == "admin"`             |
| **View Rule**     | Controls access to individual record details.                | Open to everyone if left empty       | `user.email == record.email`       |
| **Create Rule**   | Determines who is allowed to create new records.             | Open to everyone if left empty       | `user.authenticated == true`       |
| **Update Rule**   | Restricts record editing to specific users or roles.         | Open to everyone if left empty       | `user.id == record.owner_id`       |
| **Delete Rule**   | Specifies who can delete records.                            | Open to everyone if left empty       | `user.role == "admin"`             |

---

## Table Operations

### Get Table Data
- **Endpoint**: `GET /public/v1/collections/:connectorId/tables/:tableId/data`
- **Query Parameters**:
  - `filter`: Filter the data
  - `sort`: Sort the results
  - `limit`: Limit number of records
  - `offset`: Offset for pagination

**Response Example**:
```json
{
    "results": {
        "keys": [
            "c_0",
            "c_1",
            "c_2",
            "c_3",
            "c_4",
            "c_5",
            "c_6",
            "c_7"
        ],
        "display_names": [
            "id",
            "title",
            "description",
            "approval",
            "file",
            "id_user",
            "id_ip",
            "id_subsektor"
        ],
        "data": [
            [
                "405d6b7d-b860-47e4-a52c-ec38b6c8e3e7",
                "HALOO",
                "qwertyuiopsdfghjkl",
                "Pending",
                "{\"collectionId\":\"1zgvndcbgqg2sri\",\"collectionName\":\"assets\",\"created\":\"2025-04-17 13:03:15.190Z\",\"file\":\"218185530_963332904522359_4929439101503047646_n_TbMjK3AyIP.jpg\",\"id\":\"1a2yng16f3tcukw\",\"mime\":\"image/jpeg\",\"size\":29172,\"updated\":\"2025-04-17 13:03:15.190Z\"}",
                "990570db-e0e8-4a80-ab3f-e8bdfb039d3d",
                null,
                null
            ]
        ]
    },
    "total": 1
}
```

### Insert Table Data
- **Endpoint**: `POST /public/v1/collections/:connectorId/tables/:tableId/data`
- **Body**:
```json
{
    "table_id": "561583266793010121",
    "keys": [
        "c_1",
        "c_2",
        "c_3",
        "c_4"
    ],
    "data": [
        [
            "Motor",
            "10000",
            "217f2bad-55b7-4166-8281-f77f6c98a11e",
            "active"
        ]
    ]
}
```

**Response Example**:
```json
{
    "data": [
        [
            "aasasas",
            "asasas",
            "Pending",
            "441890d0-b150-4bb4-85e8-1cf09ba79e50",
            "0"
        ]
    ],
    "inserted_ids": [
        "2a3e8f98-10c4-4d17-8dd8-90a9c53ec3cf"
    ],
    "keys": [
        "c_1",
        "c_2",
        "c_3",
        "c_5",
        "c_6"
    ]
}
```

### Update Table Data
- **Endpoint**: `PUT /public/v1/collections/:connectorId/tables/:tableId/data/:dataId`
- **Body**:
```json
{
    "table_id": "562563790814655433",
    "_id": "cf26eb2c-693a-49cc-8436-1299f78ae868",
    "keys": [
        "c_1",
        "c_2"
    ],
    "row_data": [
        "qwertyuio",
        "qwertyu"
    ]
}
```

**Response Example**:
```json
{
    "_id": "cf26eb2c-693a-49cc-8436-1299f78ae868",
    "keys": [
        "c_1",
        "c_2"
    ],
    "row_data": [
        "qwertyuio",
        "qwertyu"
    ],
    "table_id": "562563790814655433"
}
```

### Delete Table Data
- **Endpoint**: `DELETE /public/v1/collections/:connectorId/tables/:tableId/data/:dataId`

**Response Example**:
```json
{
    "status": "ok"
}
```

## Saving the Schema

Once your schema is ready:
- Make sure the table name is unique and meaningful.
- Add all necessary columns and set the primary key(s).
- Configure access rules if needed.
- Click **Save** to finalize schema creation.

### Data Types

| Type | Description | Example Value |
|------|-------------|---------------|
| String | Text data | `"John Doe"` |
| Integer | Whole numbers | `42` |
| Float | Decimal numbers | `3.14` |
| Boolean | True/false values | `true` |
| Timestamp | Date and time | `"2024-03-20T15:30:00Z"` |
| JSON | JSON objects | `{"key": "value"}` |
| Attachment | File attachments | `file.pdf` |

### Column Properties

| Property | Description | Required |
|----------|-------------|----------|
| Name | Column identifier | Yes |
| Data Type | Type of data stored | Yes |
| Primary Key | Unique identifier | No |
| Format | Data format specification | No |

## Endpoints

```
BASE_URL : https://demo.volantis.io/vdata/api
```

### Auth

Used to register new users, authenticate existing ones, and retrieve authenticated user information.

| Endpoint | Method | URL | Description |
|----------|--------|-----|-------------|
| Register | POST | `/public/v1/collections/:connectorId/user/register` | Registers a new user |
| Login | POST | `/public/v1/collections/:connectorId/user/login` | Authenticates the user and returns an authentication token |
| Get Current User | GET | `/public/v1/collections/:connectorId/user/me` | Retrieves details of the currently authenticated user |

#### Register Details

**Body (JSON)**:
```json
{
  "keys": ["c_1", "c_2", "c_3", "c_4", "c_5"],
  "data": [
    [
      "admin",
      "admin",
      "admin@mail.com",
      "admin123",
      {
        "roles": ["admin"]
      }
    ]
  ]
}
```

**Response Example**:
```json
{
  "table_id": "562563790495888329",
  "keys": ["c_1", "c_2", "c_3", "c_4", "c_5"],
  "data": [
    [
      "admin",
      "admin",
      "admin@mail.com",
      "$2a$10$sU1cWmQgKlL4cC.Qy0Oj8uElvK4WcR51B9wc2rHk4qhPRutLV3YFi",
      {
        "roles": ["admin"]
      }
    ]
  ],
  "inserted_ids": null
}
```

#### Login Details

**Body (JSON)**:
```json
{
  "email": "abcdefg@mail.com",
  "password": "123456"
}
```

**Response Example**:
```json
{
  "status_code": 200,
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImtyZWF0b3JAbWFpbC5jb20iLCJleHAiOjE3NDUxNjE1ODgsIm5hbWUiOiJrcmVhdG9yIiwicm9sZSI6WyJjcmVhdG9yIl0sInVzZXJfaWQiOiI5OTA1NzBkYi1lMGU4LTRhODAtYWIzZi1lOGJkZmIwMzlkM2QiLCJ1c2VybmFtZSI6ImtyZWF0b3IifQ.bYh-pwcxILxj-gr4I23VJwkEDAxkICUsE0ttOhL6uMU"
}
```

#### Get Current User Details

**Headers**:
- `Authorization: Bearer <your_token_here>`

**Response Example**:
```json
{
  "email": "kreator@mail.com",
  "name": "kreator",
  "role": [
    "creator"
  ],
  "user_id": "990570db-e0e8-4a80-ab3f-e8bdfb039d3d",
  "username": "kreator"
}
```

