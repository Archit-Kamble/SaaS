# Testing Strategy

No feature is complete merely because it works manually once.

## Testing Levels

### Unit Tests

Business rules and domain logic.

### Integration Tests

Database, repositories and module interactions.

### API Tests

Endpoints, validation, authentication and authorization.

### End-to-End Tests

Critical business workflows.

## Critical Flows

Examples:

Login
Create Product
Receive Stock
Sell Product
Return Product
Make Payment
Generate Invoice

## Sector Tests

Garment and Sweet Shop modules require sector-specific test suites.

## AI Tests

AI output must never be trusted as deterministic business truth.

Test:

- Provider unavailable
- Timeout
- Invalid response
- Hallucinated values
- Empty response

Core shop operations must continue during AI failure.