# Tables API Endpoints

## Overview

The **Tables API** enables flexible management of table resources within the Volantis platform.

With the Tables API, you can:

*   **Retrieve table metadata** including structure, columns, and display information.  
*   **Access and preview data** from specific tables, complete with pagination, sorting, and filtering.  
*   **Create and update tables** by defining names, connectors, and column properties like primary keys and uniqueness.  
*   **Insert and manage records** within tables through RESTful endpoints.  
*   **Monitor data availability** and trigger refresh operations for up-to-date insights.  

The Tables API streamlines interaction with structured datasets, enabling smooth data management and integration across the Volantis ecosystem.

--- 

## Available Endpoints


### 1. Get All Tables
Retrieve a list of all available tables with pagination options.


**Endpoint:** `GET /tables`


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
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/tables?page=1&per_page=2" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```


**Example Response:**
```json
{
  "results": [
    {
      "id": "tableid_12345",
      "connector_id": "conn_12345",
      "name": "customers",
      "display_name": "Customer Database",
      "size": null,
      "metadata": {
        "columns": [
          {
            "key": "c_0",
            "col_index": 0,
            "data_type": "integer",
            "alias": "id",
            "origin_column": "c_0"
          },
          {
            "key": "c_1",
            "col_index": 1,
            "data_type": "text",
            "alias": "name",
            "origin_column": "c_1"
          }
        ],
        "columns_simple": [
          "c_0",
          "c_1"
        ]
      },
      "data_available": true,
      "created_at": "2025-03-10T14:22:10Z",
      "updated_at": "2025-03-10T14:22:10Z"
    },
    {
      "id": "tableid_67890",
      "connector_id": "conn_67890",
      "name": "products",
      "display_name": "Product Catalog",
      "size": null,
      "metadata": {
        "columns": [
          {
            "key": "c_0",
            "col_index": 0,
            "data_type": "integer",
            "alias": "id",
            "origin_column": "c_0"
          },
          {
            "key": "c_1",
            "col_index": 1,
            "data_type": "text",
            "alias": "product_name",
            "origin_column": "c_1"
          }
        ],
        "columns_simple": [
          "c_0",
          "c_1"
        ]
      },
      "data_available": true,
      "created_at": "2025-03-11T09:15:33Z",
      "updated_at": "2025-03-11T09:15:33Z"
    }
  ],
  "total": 42
}
```


### 2. Get Table Details
Retrieve detailed information about a specific table.


**Endpoint:** `GET /tables/:tableId`


**URL Parameters:**
- `tableId`: The ID of the table to retrieve


**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```


**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/tables/tableid_12345" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```


**Example Response:**
```json
{
  "id": "tableid_12345",
  "connector_id": "conn_12345",
  "name": "customers",
  "display_name": "Customer Database",
  "size": null,
  "metadata": {
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
        "alias": "name",
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
        "alias": "email",
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
  "data_available": true,
  "embedding_available": null,
  "embedding_model": null,
  "token_size": null,
  "created_at": "2025-03-10T14:22:10Z",
  "updated_at": "2025-03-10T14:22:10Z"
}
```


### 3. Get Table Data
Retrieve actual data from a specific table.


**Endpoint:** `GET /tables/:tableId/data`


**URL Parameters:**
- `tableId`: The ID of the table


**Query Parameters:**
- `limit` (optional): Maximum number of rows to return (default: 100)
- `offset` (optional): Number of rows to skip (default: 0)
- `sort` (optional): Field to sort by, format: `field_name:asc` or `field_name:desc`
- `filter` (optional): Filter data, format: `field_name:operator:value` (e.g., `age:gt:30`)


**Headers:**
```
apikey: YOUR_API_KEY
Accept: application/json
```


**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/tables/tableid_12345/data?limit=5&sort=created_at:desc" 
  -H "apikey: YOUR_API_KEY" 
  -H "Accept: application/json"
```


**Example Response:**
```json
{
  "results": {
    "keys": [
      "c_0",
      "c_1",
      "c_2"
    ],
    "display_names": [
      "ID",
      "Name",
      "Email"
    ],
    "data": [
      [
        1,
        "John Doe",
        "john.doe@example.com"
      ],
      [
        2,
        "Jane Smith",
        "jane.smith@example.com"
      ],
      [
        3,
        "Robert Johnson",
        "robert.johnson@example.com"
      ],
      [
        4,
        "Maria Garcia",
        "maria.garcia@example.com"
      ],
      [
        5,
        "Wei Chen",
        "wei.chen@example.com"
      ]
    ]
  },
  "total": 42
}
```


### 4. Insert Table Data
Add new data to a specific table.


**Endpoint:** `POST /tables/:tableId`


**URL Parameters:**
- `tableId`: The ID of the table


**Headers:**
```
apikey: YOUR_API_KEY
Content-Type: application/json
Accept: application/json
```


**Request Body:**
```json
{
  "data": [
    {
      "name": "Alex Thompson",
      "email": "alex.thompson@example.com",
      "age": 28,
      "active": true
    },
    {
      "name": "Sarah Wilson",
      "email": "sarah.wilson@example.com",
      "age": 34,
      "active": true
    }
  ]
}
```


**Example Request:**
```bash
curl -X POST "https://demo.volantis.io/vdata/api/public/v1/tables/tableid_12345" 
  -H "apikey: YOUR_API_KEY" 
  -H "Content-Type: application/json" 
  -H "Accept: application/json" 
  -d '{
    "data": [
      {
        "name": "Alex Thompson",
        "email": "alex.thompson@example.com",
        "age": 28,
        "active": true
      },
      {
        "name": "Sarah Wilson",
        "email": "sarah.wilson@example.com",
        "age": 34,
        "active": true
      }
    ]
  }'
```


**Example Response:**
```json
{
  "success": true,
  "message": "Data inserted successfully",
  "inserted_count": 2,
  "inserted_ids": [43, 44]
}
```
