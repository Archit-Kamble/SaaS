# Database Design

Database: PostgreSQL

## General Rules

Every applicable business table should consider:

- id
- tenant_id
- created_at
- updated_at
- created_by
- updated_by
- version/status where required

Identifiers should not expose assumptions about sequential business ordering.

## Core Entities

Initial candidates:

Tenant
Shop
Branch
Employee
Role
Permission

Product
ProductVariant
Category
Brand

Inventory
StockMovement
Location

Supplier
Purchase
PurchaseItem

Sale
SaleItem
Payment

Customer
CustomerAddress

Expense

## Sector Extension

Garment-specific data must not pollute generic Product with dozens of nullable columns.

Example:

Product
    ↓
Garment-specific representation
    ↓
FabricRoll / garment attributes

Sweet-shop-specific structures should follow the same principle.

## Financial Rule

Financial amounts must use precise decimal numeric types.

Floating-point types must not be used for monetary values.

## History

Important business transactions should generally be preserved rather than overwritten.

Examples:

- Sale
- Payment
- Stock Movement
- Purchase
- Return