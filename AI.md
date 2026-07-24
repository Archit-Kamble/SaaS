# AI Project Context

Project: Smart Retail OS

Stage: Initial Architecture / MVP

## Mission

Build an intelligent Retail Operating System for small and medium retailers.

Primary goals:

- Reduce dead stock
- Increase profit
- Improve sales
- Reduce manual work
- Improve customer relationships
- Preserve business knowledge
- Provide actionable intelligence

## Current Strategy

Develop sector-by-sector on top of a shared Retail Core.

Current ownership:

Archit -> Garment
OM -> Sweet Shop

## Architecture

Modular Monolith
Multi-Tenant SaaS
SOLID
Clean module boundaries
Event-driven interactions where appropriate
Sector extensions
PostgreSQL

## Important Product Principles

AI assists; it does not own business truth.

Core operations must work without AI.

Common functionality belongs in Retail Core.

Sector-specific functionality belongs in sector extensions.

Do not duplicate the platform for each sector.

Documentation is the source of truth.

## Current Phase

Requirements + Architecture + UI Specification

## Before Coding

Read:

Vision.md
Requirements.md
Business-Rules.md
Architecture-Design.md
Modules.md
Database.md
HLD.md
LLD.md
APIs.md
UI.md
Testing.md

Do not invent missing business rules.

## Current Priority

1. Finalize shared Retail Core.
2. Document Garment workflows.
3. Document Sweet Shop workflows.
4. Define first vertical slices.
5. Implement only after acceptance criteria are clear.