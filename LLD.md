# Low Level Design

LLD will be maintained module-by-module.

## Standard Layers

Controller
    ↓
Application Service
    ↓
Domain
    ↓
Repository Interface
    ↓
Infrastructure

## Rules

- Controllers contain no business logic.
- Constructor injection only.
- Domain logic must not depend on HTTP.
- External services must be accessed through interfaces.
- DTOs must not replace domain models.
- Persistence entities must not automatically become API contracts.
- Avoid static global business state.
- Avoid God classes.
- Prefer composition over inheritance.
- Business rules must be testable independently.

## Example

SaleController
    ↓
CompleteSaleUseCase
    ↓
Sale Domain
    ↓
Inventory Contract
    ↓
SaleRepository

A successful sale may publish:

SaleCompleted

Consumers may respond independently.