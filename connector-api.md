# 🔌 API Connector — Integrate External APIs into My Data

## Overview  
The **API Connector** allows you to pull data from any external REST API into **My Data**. This lets you enrich your datasets with external services and custom integrations — with full control over parameters, headers, and response structure.

![API Connector](/vdata/documentation/mydata/api-1.webp)

---

## 1. Define Your API Endpoint  

![API Connector](/vdata/documentation/mydata/api-2.webp)

Start by specifying your API endpoint configuration:

| Field         | Description                                                                  |
|---------------|------------------------------------------------------------------------------|
| **Base URL**  | Main domain of your API (e.g. `https://demo.volantis.io`)                   |
| **Path**      | Resource path (e.g. `/vdata/api/v1/metadata/connectors`)                    |
| **Method**    | HTTP method to use: `GET`, `POST`, etc.                                      |
| **Response Type** | Format of the API response: `collection`, `detail`, or `plaintext`         |

The final URL will be composed as:  `https://demo.volantis.io/vdata/api/v1/metadata/connectors`

---

## 2. Add Custom Headers (Optional)  

![API Connector](/vdata/documentation/mydata/api-3.webp)

If your API requires authentication or custom headers (e.g. API keys, organization ID, content type), you can define them using a valid JSON format:

```json
{
  "x-org-id": "1",
  "apikey": "sCS5rrsAfdsaPZDQSxXJVnnoXJQA9Z3N"
}
```

> 🔐 Headers are sent with each request. Make sure to keep API keys secure.

---

## 3. Add Query Parameters (Optional)  

![API Connector](/vdata/documentation/mydata/api-4.webp)


You can include static query parameters to filter or modify the data retrieved:

```json
{
  "filter": "type:eq:xlsx"
}
```

> 🧩 These parameters will be appended to the URL as standard query strings.

---

## 4. Configure Optional Pagination  

![API Connector](/vdata/documentation/mydata/api-5.webp)

If the API supports pagination, configure the appropriate fields to fetch data in batches:

| Field            | Example     | Description                                            |
|------------------|-------------|--------------------------------------------------------|
| **Limit Field**  | `limit`     | Number of items per request                           |
| **Offset Field** | `offset`    | Number of items to skip from the beginning            |
| **Page Field**   | `page`      | Page number, if your API uses page-based navigation   |

Only include what your API supports.

---

## 5. Map the Response Structure  

![API Connector](/vdata/documentation/mydata/api-6.webp)

Specify the fields used to extract metadata and actual data from the response:

| Field             | Example     | Description                                    |
|------------------|-------------|------------------------------------------------|
| **Total Field**   | `total`     | Key containing total record count             |
| **Result Field**  | `data`      | Key containing the array of records           |

### Example API Response:
```json
{
  "total": 28,
  "data": [
    { "id": 1, "name": "file.xlsx", "type": "xlsx" }
  ]
}
```

---

## 6. Finalize & Save  

![API Connector](/vdata/documentation/mydata/api-7.webp)
![API Connector](/vdata/documentation/mydata/api-8.webp)

- After filling in all fields, click Preview to test the API request and validate the response structure.
- If the response is correct, click Save to finalize and activate the connector.

Your API is now integrated with **My Data** and ready for querying or visual output.