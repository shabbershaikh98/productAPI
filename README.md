# Product API

## Overview
The Product API is a simple Express-based API designed to calculate the total value of a list of products based on their price and quantity. This API is ideal for applications that need to manage product data efficiently.

## Base URL
http://localhost:3000/api/products


## Endpoints

### 1. Calculate Total Value of Products
- **Endpoint**: `/total-value`
- **Method**: `POST`
- **Description**: Accepts a list of product objects and returns the total value of all products.

#### Request

- **Headers**:
  - `Content-Type: application/json`
  
- **Body**:
  The request body should be a JSON array of product objects. Each product object should contain:
  - `name`: Name of the product (string)
  - `price`: Price of the product (number)
  - `quantity`: Quantity of the product (number)

**Example Request Body**:
```json
[
  { "name": "Product 1", "price": 10, "quantity": 3 },
  { "name": "Product 2", "price": 20, "quantity": 2 }
]

uccess (HTTP 200): On a successful request, the API will return:

json
{
  "totalValue": 70
}