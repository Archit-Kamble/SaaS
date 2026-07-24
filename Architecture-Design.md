# Architecture Design

## Architectural Goal

Build a modular multi-tenant SaaS that supports multiple retail sectors without
duplicating the entire application for each sector.

## Architecture

                    Clients
         ┌────────────┼────────────┐
       Mobile        Web        Future Apps
         └────────────┼────────────┘
                      ↓
                  API Layer
                      ↓
              Application Layer
                      ↓
       ┌──────────────┼───────────────┐
       ↓              ↓               ↓
 Retail Core    Sector Extensions   Intelligence
       ↓              ↓               ↓
       └──────────────┼───────────────┘
                      ↓
                  Data Layer
                      ↓
                 PostgreSQL

## Architectural Principles

- Modular Monolith initially
- Clean boundaries between modules
- SOLID
- Dependency inversion
- Domain events where appropriate
- API contracts
- Multi-tenancy
- Sector extensions
- External integrations behind interfaces

## Important Decision

Do NOT begin with microservices.

The initial system should be a well-structured modular monolith.

Modules should have boundaries strong enough that selected modules can be
extracted into services later if scale requires it.

## Dependency Direction

Sector modules may depend on stable Retail Core contracts.

Retail Core must NOT depend on Garment, Sweet Shop or other sector-specific modules.

Example:

Correct:

Garment → Inventory

Incorrect:

Inventory → Garment