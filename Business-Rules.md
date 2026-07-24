# Business Rules

Every business rule receives a permanent identifier.

Format:

BR-{DOMAIN}-{NUMBER}

Example:

BR-INV-001

## General

BR-GEN-001
Every business record belongs to a tenant/shop context.

BR-GEN-002
AI must never be the authoritative source for financial or inventory values.

BR-GEN-003
Critical business operations must remain available when AI services are unavailable.

BR-GEN-004
Critical modifications must be auditable.

## Inventory

BR-INV-001
Inventory must not become negative unless explicitly permitted by shop configuration.

BR-INV-002
Every stock-changing operation must create a stock movement record.

BR-INV-003
A completed sale reduces available inventory.

BR-INV-004
An accepted customer return increases inventory when the returned product is resellable.

BR-INV-005
Low-stock thresholds may vary by product or variant.

BR-INV-006
Dead-stock rules must be configurable because different sectors and products have different sales cycles.

## AI

BR-AI-001
AI recommendations are advisory.

BR-AI-002
AI cannot silently modify inventory, financial transactions or customer balances.

BR-AI-003
Deterministic calculations such as revenue, tax, profit and stock quantity must be performed by application logic.

BR-AI-004
AI should operate primarily on validated and aggregated business data.

## Customer

BR-CUS-001
Customer communication preferences must be respected.

BR-CUS-002
Customer relationship recommendations should be suggestions to the shop owner unless automation has been explicitly enabled.

## Sector Rules

Garment-specific rules use:

BR-GAR-XXX

Sweet-shop rules use:

BR-SWT-XXX