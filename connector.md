# Data Connector Endpoints

## Overview  

The **Volantis Connector** enables seamless integration between Volantis and various external data sources.

With the Connector, you can:

*   **Define connections** using templates tailored for databases, APIs, file systems, and more.  
*   **Configure parameters** such as host, port, credentials, and authentication methods.  
*   **Establish validated connections** that serve as data pipelines' entry points.  
*   **Reuse connector instances** across multiple pipelines and jobs to streamline your workflow.  

The Connector simplifies the process of extracting data from multiple systems, making it ready for further transformation and analysis within the Volantis platform.

---

## Available Endpoints

### 1. Get All Connectors
Retrieve a list of all available connectors with pagination and filtering options.

**Endpoint:** `GET /data`

**Query Parameters:**
- `page` (optional): Page number for pagination (default: 1)
- `per_page` (optional): Number of results per page (default: 20)

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/data?page=1&per_page=2" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```

**Example Response:**
```json
{
  "results": [
      {
        "id": "conn_12345",
        "name": "MySQL Production",
        "type": "mysql",
        "created_at": "2025-02-15T14:32:10Z",
        "last_sync": "2025-03-10T08:15:22Z"
      },
      {
        "id": "conn_67890",
        "name": "PostgreSQL Analytics",
        "type": "postgresql",
        "created_at": "2025-01-20T09:45:33Z",
        "last_sync": "2025-03-11T12:40:15Z"
      }
    ],
    total: 123
  }
}
```

___

### 2. Get Connector Details
Retrieve detailed information about a specific connector.

**Endpoint:** `GET /data/:connectorId`

**URL Parameters:**
- `connectorId`: The ID of the connector to retrieve

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/data/conn_12345" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```

___

### 3. Add Custom Connector
Create a new custom connector to connect to your data source.

**Endpoint:** `POST /data`

**Headers:**
```
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```

**Request Body:**
```json
{
  "name": "Example Push Connector",
  "tables": [
    {
      "name": "book",
      "display_name": "Book Database",
      "metadata": {
        "columns": [
          {
            "key": "id",
            "data_type": "integer"
          },
          {
            "key": "title",
            "data_type": "text"
          },
          {
            "key": "author",
            "data_type": "text"
          }
        ]
      }
    }
  ]
}
```

**Example Request:**
```bash
curl -X POST "https://demo.volantis.io/vdata/api/public/v1/data" 
  -H "apikey:  YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "name": "New Data Warehouse",
    "display_name": "Book Database",
    "metadata": {
        "columns": [
          {
            "key": "id",
            "data_type": "integer"
          },
          {
            "key": "title",
            "data_type": "text"
          },
          {
            "key": "author",
            "data_type": "text"
          }
        ]
      }
  }'
```

**Example Response:**
```json
{
  "id": "conid_123",
  "name": "Example Push Connector",
  "size": null,
  "type": "custom",
  "mime": null,
  "metadata": {},
  "ai_summary": null,
  "total_table": 1,
  "total_device": 0,
  "data_available": false,
  "embedding_available": null,
  "embedding_model": null,
  "token_size": null,
  "owner": {
    "id": "userid_123",
    "name": "",
    "username": "user",
    "email": "user@volantis.io"
  },
  "created_at": "2025-03-12T11:36:19.109029+07:00",
  "updated_at": "2025-03-12T11:36:19.109029+07:00",
  "job_id": null,
  "last_runner_id": null,
  "user_id": "userid_123",
  "org_id": "1",
  "tables": [
    {
      "id": "tableid_123",
      "name": "book",
      "display_name": "Book Database",
      "size": null,
      "metadata": {
        "view": null,
        "columns": [
          {
            "key": "c_0",
            "col_index": 0,
            "data_type": "integer",
            "alias": "id",
            "generated": false,
            "format_column": null,
            "origin_column": "c_0",
            "origin_table": null,
            "origin_key": null,
            "field_id": null,
            "format_timezone": null
          },
          {
            "key": "c_1",
            "col_index": 1,
            "data_type": "text",
            "alias": "title",
            "generated": false,
            "format_column": null,
            "origin_column": "c_1",
            "origin_table": null,
            "origin_key": null,
            "field_id": null,
            "format_timezone": null
          },
          {
            "key": "c_2",
            "col_index": 2,
            "data_type": "text",
            "alias": "author",
            "generated": false,
            "format_column": null,
            "origin_column": "c_2",
            "origin_table": null,
            "origin_key": null,
            "field_id": null,
            "format_timezone": null
          }
        ],
        "columns_simple": [
          "c_0",
          "c_1",
          "c_2"
        ],
        "columns_display": null,
        "rows": null,
        "config": null,
        "large_index": "0",
        "relations": null
      },
      "statistics": null,
      "ai_summary": null,
      "data_available": false,
      "embedding_available": null,
      "embedding_model": null,
      "token_size": null,
      "created_at": "2025-03-12T11:36:19.112171798+07:00",
      "updated_at": "2025-03-12T11:36:19.112171798+07:00"
    }
  ]
}
```

___

### 4. Edit Connector
Edit your connector name

**Endpoint** `PUT /data/:connectorId`

**URL Parameters:**
- `connectorId`: The ID of the connector to retrieve

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Request Body:**
```json
{
    "name": "New name"
}
```

**Example Request:**
```bash
curl -X PUT "https://demo.volantis.io/vdata/api/public/v1//data/:connectorId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "name": "New name"
  }'
```

**Example Response:**
```json
{
  "id": "connector_id",
  "name": "New name",
  "size": 14130,
  "type": "csv",
  "mime": null,
  "total_table": 1,
  "data_available": true,
  "created_at": "2025-03-12T17:13:49.082793+07:00",
  "updated_at": "2025-03-13T10:40:06.085419+07:00"
}
```

___

### 5. Delete Connector  

Delete a connector.  

**Endpoint:** `DELETE /data/:connectorId`  

**URL Parameters:**  
- `connectorId`: The ID of the connector to delete.  

**Headers:**  
```  
apikey: YOUR_API_KEY  
Accept: application/json  
```  

**Example Request:**  
```bash
curl -X DELETE "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```  

**Example Response:**  
```json
{
  no content
}
```  

___

### 6. Get Tables for a Connector
Retrieve all tables available for a specific connector.

**Endpoint:** `GET /data/:connectorId/tables`

**URL Parameters:**
- `connectorId`: The ID of the connector

**Headers:**
```
apikey:  YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/data/conn_12345/tables" 
  -H "apikey:  YOUR_API_KEY" 
  -H "Accept: application/json"
```

**Example Response:**
```json
{
  "results": [
    {
      "id": "tableid_12345",
      "connector_id": "conn_12345",
      "name": "tabel-test add connectors",
      "display_name": "tabel_test",
      "size": null,
      "metadata": {
        "columns": [
          {
            "key": "c_0",
            "col_index": 0,
            "data_type": "text",
            "alias": "name",
            "origin_column": "c_0"
          },
          {
            "key": "c_1",
            "col_index": 1,
            "data_type": "text",
            "alias": "kelas",
            "origin_column": "c_1"
          }
        ],
        "columns_simple": [
          "c_0",
          "c_1"
        ],
        "rows": null
      },
      "data_available": false,
      "created_at": "2025-03-11T15:41:12.424629+07:00",
      "updated_at": "2025-03-11T15:41:12.424629+07:00"
    }
  ],
  "total": 1
}
```

____

### 7. Get Table Details
Retrieve detailed information about a specific table.

**Endpoint:** `GET /data/:connectorId/tables/:tableId`

**URL Parameters:**
- `connectorId`: The ID of the connector
- `tableId`: The ID of the table

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/data/conn_12345/tables/tbl_001" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```

**Example Response:**
```json
{
  "id": "tbl_1",
  "connector_id": "con_123",
  "name": "tabel",
  "display_name": "Tabel",
  "size": null,
  "metadata": {
    "columns": [
      {
        "key": "c_0",
        "col_index": 0,
        "data_type": "text",
        "alias": "name",
        "origin_column": "c_0"
      },
      {
        "key": "c_1",
        "col_index": 1,
        "data_type": "text",
        "alias": "kelas",
        "origin_column": "c_1"
      }
    ],
    "columns_simple": [
      "c_0",
      "c_1"
    ],
    "rows": null
  },
  "data_available": false,
  "created_at": "2025-03-11T15:41:12.424629+07:00",
  "updated_at": "2025-03-11T15:41:12.424629+07:00"
}
```

___

Berikut adalah versi yang diperbarui dengan informasi tambahan bahwa tabel hanya dapat ditambahkan jika `type` dari `connector` adalah `custom`.  

---

### 8. Add Table in Connector  
Create a new table in a connector. **Tables can only be added if the connector's type is `custom`**.

**Endpoint:**  
`POST /data/:connectorId/tables`

**Headers:**
```
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```

**Request Body:**
```json
{
    "name": "example",
    "display_name": "Example",
    "metadata": {
        "columns": [
            {
                "alias": "Timestamp",
                "data_type": "timestamp",
                "key": "timestamp"
            },
            {
                "type": "short-answer",
                "question": "Example question?",
                "required": false,
                "responseType": "text",
                "options": [],
                "id": "abcdef",
                "alias": "example_question_1",
                "data_type": "text",
                "field_id": "abcdef",
                "key": "example-question-1"
            }
        ],
        "columns_display": [
            [
                "Timestamp",
                "example_question_1"
            ]
        ]
    }
}
```

**Conditions**
- **Only connectors with `type: "custom"` support adding tables.**
- The `connectorId` must be valid and belong to a `custom` connector.
- The `name` of the table must be unique within the connector.

**Example Request**
```bash
curl -X POST "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "name": "example",
    "display_name": "Example",
    "metadata": {
        "columns": [
            {
                "alias": "Timestamp",
                "data_type": "timestamp",
                "key": "timestamp"
            },
            {
                "type": "short-answer",
                "question": "Example question?",
                "required": false,
                "responseType": "text",
                "options": [],
                "id": "abcdef",
                "alias": "example_question_1",
                "data_type": "text",
                "field_id": "abcdef",
                "key": "example-question-1"
            }
        ],
        "columns_display": [
            [
                "Timestamp",
                "example_question_1"
            ]
        ]
    }
}'
```

**Example Response**
```json
{
    "id": "example_id",
    "name": "example",
    "display_name": "Example",
    "size": null,
    "metadata": {
        "view": null,
        "columns": [
            {
                "key": "c_0",
                "col_index": 0,
                "data_type": "timestamp",
                "alias": "Timestamp",
                "generated": false,
                "format_column": null,
                "origin_column": "c_0",
                "origin_table": null,
                "origin_key": null,
                "field_id": null,
                "format_timezone": null
            },
            {
                "key": "c_1",
                "col_index": 1,
                "data_type": "text",
                "alias": "example_question_1",
                "generated": false,
                "format_column": null,
                "origin_column": "c_1",
                "origin_table": null,
                "origin_key": null,
                "field_id": "abcdef",
                "format_timezone": null
            }
        ],
        "columns_simple": [
            "c_0",
            "c_1"
        ],
        "columns_display": [
            [
                "Timestamp",
                "example_question_1"
            ]
        ],
        "rows": null,
        "config": null,
        "large_index": "0",
        "relations": null
    },
    "statistics": null,
    "ai_summary": null,
    "data_available": false,
    "embedding_available": null,
    "embedding_model": null,
    "token_size": null,
    "created_at": "2025-03-13T11:36:09.497470215+07:00",
    "updated_at": "2025-03-13T11:36:09.497470215+07:00"
}
```

___

### 9. Edit table
Edit your table name

**Endpoint** `PUT /data/:connectorId/tables/:tableId`

**URL Parameters:**
- `connectorId`: The ID of the connector to retrieve
- `tableId`: The ID of the table to retrieve

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Request Body:**
```json
{
    "display_name": "Example"
}
```

**Example Request:**
```bash
curl -X PUT "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables/:tableId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "display_name": "Example"
}'
```

**Example Response:**
```json
{
    "tableId": "example-table-id",
    "connectorId": "example-connector-id",
    "name": "example_file.csv",
    "display_name": "example-data",
    "size": 14130,
    "metadata": {
        "columns": [
            {
                "key": "timestamp",
                "col_index": 0,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "name",
                "col_index": 1,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "email_address",
                "col_index": 2,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "transaction_category",
                "col_index": 3,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "usage_description",
                "col_index": 4,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "project",
                "col_index": 5,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "date",
                "col_index": 6,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "amount",
                "col_index": 7,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "funding_source",
                "col_index": 8,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "Project",
                "col_index": 9,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "reimbursement",
                "col_index": 10,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "_empty_column",
                "col_index": 11,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "_duplicated_0",
                "col_index": 12,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "_duplicated_1",
                "col_index": 13,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "_duplicated_2",
                "col_index": 14,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            },
            {
                "key": "_duplicated_3",
                "col_index": 15,
                "data_type": "String",
                "alias": "",
                "origin_column": ""
            }
        ],
        "columns_simple": [
            "timestamp",
            "name",
            "email_address",
            "transaction_category",
            "usage_description",
            "project",
            "date",
            "amount",
            "funding_source",
            "Project",
            "reimbursement",
            "_empty_column",
            "_duplicated_0",
            "_duplicated_1",
            "_duplicated_2",
            "_duplicated_3"
        ],
        "rows": [
            [
                null,
                "Example Name",
                null,
                "Transport",
                "Example Transaction 1",
                "Example Company",
                "Wednesday, January 1, 2025",
                "Rp275,000",
                "Reimbursement",
                null,
                "Done",
                null,
                null,
                null,
                null,
                null
            ],
            [
                "1/8/2025 16:28:25",
                "Example Name 2",
                null,
                "Marketing",
                "Example Subscription",
                "Marketing",
                "Tuesday, January 7, 2025",
                "Rp333,000",
                "Reimbursement",
                null,
                "Done",
                null,
                null,
                null,
                null,
                null
            ]
        ]
    },
    "data_available": false,
    "created_at": "2025-03-11T10:18:52.119941+07:00",
    "updated_at": "2025-03-13T11:09:32.078434+07:00"
}
```

___

### 10. Delete table
Delete your table name

**Endpoint** `DELETE /data/:connectorId/tables/:tableId`

**URL Parameters:**
- `connectorId`: The ID of the connector to retrieve
- `tableId`: The ID of the table to retrieve

**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X DELETE "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables/tableId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
```

**Example Response:**
```json
{
  no content
}
```

___

### 11. Get Table Data
Retrieve actual data from a specific table.

**Endpoint:** `GET /data/:connectorId/tables/:tableId/data`

**URL Parameters:**
- `connectorId`: The ID of the connector
- `tableId`: The ID of the table

**Query Parameters:**
- `limit` (optional): Maximum number of rows to return (default: 100)
- `offset` (optional): Number of rows to skip (default: 0)
- `sort` (optional): Field to sort by, format: `field_name:asc` or `field_name:desc`
- `filter` (optional): Filter data, format: `field_name:operator:value` (e.g., `age:gt:30`)

**Headers:**
```
apikey:  YOUR_API_KEY
Accept: application/json
```

**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/data/conn_12345/tables/tbl_001/data?limit=5&sort=created_at:desc" 
  -H "apikey:  YOUR_API_KEY" 
  -H "Accept: application/json"
```

**Example Response:**
```json
{
  "results": {
    "keys": [
      "c_0",
      "c_1",
      "c_2",
      "c_3",
      "c_4"
    ],
    "display_names": [
      "Timestamp",
      "1",
      "3",
      "2",
      "Testing "
    ],
    "data": [
      [
        "2025-03-11T11:35:20",
        null, "1zgvndcbgqg2sri-awdjam99d8ffn6d-unsplash_f6_da4r2x5to_AdqFQlXT6f.png",
        "qwertyuiop",
        null]
    ]
  },
  "total": 1
}
```

___

Here’s the API documentation for inserting data into a table with the specified endpoint and request body format:

---

### 12. Insert Data Table  
Insert a new row of data into a table within a connector. This ensures structured data is stored while adhering to the table's predefined schema.

**Endpoint:**  
`POST /data/:connectorId/tables/:tableId/data`  

**Headers:**  
```plaintext
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```  

**Request Body:**  
```json
{
    "table_id": "tableid",
    "keys": [
        "c_0",
        "c_1"
    ],
    "data": [
        [
            "2025-03-12 14:00:00",
            "example"
        ]
    ]
}
```  

**Example Request:**  
```bash
curl -X POST "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables/:tableId/data" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "table_id": "tableid",
    "keys": [
        "c_0",
        "c_1"
    ],
    "data": [
        [
            "2025-03-12 14:00:00",
            "example"
        ]
    ]
}'
```  

**Example Response:**  
```json
{
    "table_id": "tableid",
    "keys": [
        "c_0",
        "c_1",
        "c_2"
    ],
    "data": [
        [
            "2025-03-12 14:00:00",
            "example",
            "example"
        ]
    ]
}
```  

**Notes:** 
- The **connectorId** must be from a connector.  
- `table_id` refers to the target table where data will be inserted.  
- `keys` defines the columns where the corresponding values will be inserted.  
- The data format should follow the schema of the specified table.  
___

### 13. Update Data Table  
Update an existing row in a table within a connector. This modifies specific values while maintaining the original structure.

**Endpoint:**  
`PUT /data/:connectorId/tables/:tableId/data/:dataId`  

**Headers:**  
```plaintext
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```  

**Request Body:**  
```json
{
    "keys": [
        "c_0",
        "c_1",
        "c_2"
    ],
    "row_data": [
        "2025-03-12 14:00:00",
        "example",
        "example"
    ]
}
```  

**Example Request:**  
```bash
curl -X PUT "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables/:tableId/data/:dataId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "keys": [
        "c_0",
        "c_1",
        "c_2"
    ],
    "row_data": [
        "2025-03-12 14:00:00",
        "example",
        "example"
    ]
}'
```  

**Example Response:**  
```json
{
    "table_id": "557397798295843785",
    "_id": "bda86c7a-808a-4bba-8d49-d228129499f7",
    "keys": [
        "c_0",
        "c_1",
        "c_2"
    ],
    "row_data": [
        "2025-03-12 14:00:00",
        "example",
        "example"
    ]
}
```  

**Notes:**  
- The **connectorId** must belong to a connector.  
- `dataId` is the unique identifier of the row to be updated.  
- `keys` defines which columns are being updated.  
- `row_data` contains the updated values corresponding to the defined `keys`.  

___

Here’s the API documentation for deleting data from a table:

---

### 14. Delete Data Table  
Delete a specific row from a table within a connector.

**Endpoint:**  
`DELETE /data/:connectorId/tables/:tableId/data/:dataId`  

**Headers:**  
```plaintext
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```  

**Example Request:**  
```bash
curl -X DELETE "https://demo.volantis.io/vdata/api/public/v1/data/:connectorId/tables/:tableId/data/:dataId" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json"
```  

**Example Response:**  
```json
{
    "status": "ok"
}
```  

**Notes:**  
- The **connectorId** must belong to a **custom** connector.  
- `dataId` is the unique identifier of the row to be deleted.  
- A successful deletion will return a status of `"ok"`.  
