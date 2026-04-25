---
applyTo: "**/api/**/*.py, **/routes/**/*.py, **/models/**/*.py"
---

# API Design Conventions

## RESTful Principles

- **Nouns over Verbs**: Use resources in paths (e.g., `/users` instead of `/getUsers`).
- **HTTP Methods**:
  - `GET`: Retrieve data (idempotent, no side effects).
  - `POST`: Create new resources.
  - `PUT`: Replace/Update entire resources.
  - `PATCH`: Partial updates.
  - `DELETE`: Remove resources.
- **Pluralization**: Use plural nouns for collection paths (e.g., `/items` vs `/items/{id}`).

## Data Handling

- **JSON Standard**: All requests and responses must use `CamelCase` or `snake_case` (choose one for the project) consistently.
- **Pydantic Models**: Mandatory use of Pydantic for request validation and response serialization.
- **Pagination**: Any endpoint returning a list must support `limit` and `offset` (or cursor-based) pagination.

## Error Handling

- **Consistent Response**: Always return a structured error body:
  ```json
  { "error": "Error Type", "message": "Human readable description" }
  ```
- **Status Codes**:
  - `200/201`: Success.
  - `400`: Validation/Client error.
  - `401/403`: Auth/Permission issues.
  - `404`: Resource not found.
  - `500`: Server-side failures.

## Documentation & Safety

- **OpenAPI/Swagger**: Ensure all endpoints have clear summaries and descriptions for auto-generation.
- **Idempotency**: Ensure `POST` requests include an `Idempotency-Key` header where critical (e.g., payments).
- **Versioning**: Prefix all routes with a version (e.g., `/v1/resource`).
