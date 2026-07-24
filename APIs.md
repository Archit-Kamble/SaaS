# API Standards

Base:

/api/v1/

Examples:

POST /api/v1/auth/login
GET  /api/v1/products
POST /api/v1/products
GET  /api/v1/inventory
POST /api/v1/sales

## Standards

Use HTTP methods according to semantics.

GET    -> Read
POST   -> Create / Commands
PUT    -> Full replacement where appropriate
PATCH  -> Partial update
DELETE -> Delete where business rules permit

## Standard Response

{
  "success": true,
  "data": {},
  "error": null,
  "timestamp": ""
}

## Error Response

{
  "success": false,
  "data": null,
  "error": {
    "code": "INSUFFICIENT_STOCK",
    "message": "Requested quantity is unavailable"
  },
  "timestamp": ""
}

## Versioning

All public APIs must be versioned.

Initial version:

/api/v1