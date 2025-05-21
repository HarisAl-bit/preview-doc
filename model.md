# Models Endpoints

## Overview

The **Models API** provides a powerful interface for managing machine learning models and running predictions within the Volantis platform.

With the Models API, you can:

*   **List available models** with support for pagination and metadata inspection.  
*   **Access detailed model configurations**, including algorithms, hyperparameters, features, and target columns.  
*   **Generate predictions** by submitting input data to trained models through a dedicated prediction endpoint.  
*   **Track model performance** using metrics such as MAE, MSE, and R², helping ensure model reliability.  
*   **Manage model lifecycle** with support for versioning, ownership tracking, and integration with tables, dashboards, and jobs.  

This API enables seamless integration of machine learning into your data workflows, making it easier to operationalize models and deliver insights in real-time.

---

## Available Endpoints


### 1. Get All Models
Retrieve a list of all available models with pagination options.


**Endpoint:** `GET /models`


**Query Parameters:**
- `page` (optional): Page number for pagination (default: 1)
- `per_page` (optional): Number of results per page (default: 20)


**Headers:**


```
apikey: YOUR_API_KEY
Accept: application / json
```


**Example Request:**


```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/models?page=1&per_page=10"
-H "apikey: YOUR_API_KEY"
-H "Accept: application/json"
```


**Example Response:**
```json
{
  "results": [
    {
      "id": "modelid_12345",
      "name": "Model",
      "table_id": "tableid_123456",
      "user_id": "userid_123456",
      "config": {
        "function_name": "sklearn.ensemble.Model",
        "parameters": {
          "max_depth": {
            "type": "NoneType",
            "value": null
          },
          "n_estimators": {
            "type": "int",
            "value": 100
          },
          "random_state": {
            "type": "int",
            "value": 42
          }
        },
        "features": [
          {
            "key": "c_7",
            "data_type": "float",
            "alias": "2024",
            "encode": "",
            "options": "",
            "origin_table": null,
            "origin_key": null
          }
        ],
        "target": [
          "c_3"
        ],
        "target_details": [
          {
            "key": "c_3",
            "data_type": "float",
            "alias": "2020",
            "encode": "",
            "options": "",
            "origin_table": "537679919488971721",
            "origin_key": "c_3"
          }
        ],
        "accuracy": null,
        "type": ""
      },
      "pocketbase_id": "pocketbaseid",
      "model_available": true,
      "need_training": false,
      "metadata": {
        "accuracy": {
          "mae": 945507.231099999,
          "mse": 3394950083260.61,
          "r2": 0.275267276093314
        },
        "pipeline": null
      },
      "created_at": "2025-03-11T17:31:36.617666+07:00",
      "updated_at": "2025-03-11T17:31:52.49226+07:00",
      "library_id": "libraryid_123",
      "job_id": "jobid_123456",
      "last_runner_id": "lastrunnerid_123456",
      "dashboard_id": "dashboardid_123456",
      "owner": {
        "id": "ownerid_0123",
        "name": "user",
        "username": "user",
        "email": "user@volantis.io"
      }
    },
    {
      "id": "modelid_123456",
      "name": "Model",
      "table_id": "tableid_0123",
      "user_id": "userid_1234",
      "config": {
        "function_name": "sklearn.ensemble.Model",
        "parameters": {
          "max_depth": {
            "type": "int",
            "value": 6
          },
          "n_estimators": {
            "type": "int",
            "value": 100
          }
        },
        "features": [
          {
            "key": "c_1",
            "data_type": "float",
            "alias": "room_count",
            "encode": "",
            "options": "",
            "origin_table": null,
            "origin_key": null
          },
          {
            "key": "c_3",
            "data_type": "float",
            "alias": "size",
            "encode": "",
            "options": "",
            "origin_table": null,
            "origin_key": null
          }
        ],
        "target": [
          "c_5"
        ],
        "target_details": [
          {
            "key": "c_5",
            "data_type": "float",
            "alias": "price",
            "encode": "",
            "options": "",
            "origin_table": null,
            "origin_key": null
          }
        ],
        "accuracy": null,
        "type": ""
      },
      "pocketbase_id": "pocketbaseid_98765",
      "model_available": true,
      "need_training": false,
      "metadata": {
        "accuracy": {
          "mae": 37706014.2374152,
          "mse": 455232418088072900,
          "r2": -8.1119378570965
        },
        "pipeline": null
      },
      "created_at": "2025-03-11T14:52:54.949111+07:00",
      "updated_at": "2025-03-11T14:52:54.953117+07:00",
      "library_id": "libraryid_0123",
      "job_id": "",jobid_0123
      "last_runner_id": "557255185701811145",
      "dashboard_id": "dashboardid_0123",
      "owner": {
        "id": "userid_0123",
        "name": "user",
        "username": "user",
        "email": "user@volantis.io"
      }
    }
  ],
  "total": 536
}
```


### 2. Get Model Details
Retrieve detailed information about a specific model.


**Endpoint:** `GET /models/:modelId`


**URL Parameters:**
- `modelId`: The ID of the model to retrieve


**Headers:**
```
apikey: YOUR_API_KEY
Accept: application / json
  ```


**Example Request:**
```bash
curl -X GET "https://demo.volantis.io/vdata/api/public/v1/models/model_12345"
-H "apikey: YOUR_API_KEY"
-H "Accept: application/json"
  ```


**Example Response:**
```json
{
  "id": "modelid_0123",
  "name": "Random Forest Regressor",
  "table_id": "tableid_123",
  "user_id": "userid_123",
  "config": {
    "function_name": "sklearn.ensemble.Model",
    "parameters": {
      "max_depth": {
        "type": "NoneType",
        "value": null
      },
      "n_estimators": {
        "type": "int",
        "value": 100
      },
      "random_state": {
        "type": "int",
        "value": 42
      }
    },
    "features": [
      {
        "key": "c_7",
        "data_type": "float",
        "alias": "2024",
        "encode": "",
        "options": "",
        "origin_table": null,
        "origin_key": null
      }
    ],
    "target": [
      "c_3"
    ],
    "target_details": [
      {
        "key": "c_3",
        "data_type": "float",
        "alias": "2020",
        "encode": "",
        "options": "",
        "origin_table": "537679919488971721",
        "origin_key": "c_3"
      }
    ],
    "accuracy": null,
    "type": ""
  },
  "pocketbase_id": "pockatebaseid_09876",
  "model_available": true,
  "need_training": false,
  "metadata": {
    "accuracy": {
      "mae": 945507.231099999,
      "mse": 3394950083260.61,
      "r2": 0.275267276093314
    },
    "pipeline": null
  },
  "created_at": "2025-03-11T17:31:36.617666+07:00",
  "updated_at": "2025-03-11T17:31:52.49226+07:00",
  "library_id": "libraryid_098765",
  "job_id": "jobid_123",
  "last_runner_id": "lastrunnerid_12345",
  "dashboard_id": "dashboardid_012345",
  "owner": {
    "id": "ownerid_123",
    "name": "user",
    "username": "user",
    "email": "user@volantis.io"
  }
}
```


### 3. Model Prediction
Use a model to make predictions based on input data.


**Endpoint:** `POST /models/:modelId/predict`


**URL Parameters:**
- `modelId`: The ID of the model to use for prediction


**Headers:**
```
apikey: YOUR_API_KEY
Content - Type: application / json
Accept: application / json
  ```


**Request Body:**
```json
{
  "prediction":[
    { features_alias1: value},
    { features_alias2: value}
  ]
}
```


**Example Request:**
```bash
curl - X POST "https://demo.volantis.io/vdata/api/public/v1/models/model_12345/predict" 
-H "apikey: YOUR_API_KEY"
-H "Content-Type: application/json"
-H "Accept: application/json"
-d '{
  "prediction":[
    { features_alias1: value},
    { features_alias2: value}
  ]
}'
```


**Example Response:**
```json
{
  "prediction": [
    50741.32169999974
  ]
}
````