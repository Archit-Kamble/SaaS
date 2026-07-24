# Smart Retail OS — Project Milestones

## Purpose

Milestones define measurable checkpoints for Smart Retail OS.

A milestone is complete only when its acceptance criteria are satisfied.

"Code written" does NOT mean "milestone completed."

---

# M0 — Market Discovery

## Goal

Confirm that real retailers experience problems Smart Retail OS intends to solve.

## Activities

- Visit garment shops
- Visit sweet shops
- Study existing software
- Understand manual workflows
- Record objections
- Record requested features
- Understand hardware availability
- Understand willingness to pay

## Initial Findings

Early shop visits have shown:

- Some traditional owners may strongly resist software-based management.
- Existing software users are interested when meaningful differentiation exists.
- Working demonstrations produce significantly better conversations than explaining hypothetical features.
- Real users naturally suggest additional workflow features when they can interact with a working product.
- Service reminders were requested during tyre-shop validation.

## Completion Criteria

Market discovery is never permanently "finished", but initial discovery is sufficient to proceed when recurring problems and useful workflows have been identified.

Status: IN PROGRESS

---

# M1 — Product Definition

## Goal

Clearly define what Smart Retail OS is and what it is not.

## Required Documentation

- Vision
- Requirements
- Modules
- Business Rules
- Roadmap
- Sector Strategy
- Product Principles

## Completion Criteria

Both founders can independently explain:

- Target customer
- Problem
- Solution
- Core value proposition
- Sector strategy
- Basic/Professional/Master positioning

Status: IN PROGRESS

---

# M2 — Architecture Foundation

## Goal

Freeze enough architecture to safely begin implementation.

## Required

- Architecture Design
- HLD
- Initial LLD standards
- Database standards
- API standards
- Testing strategy
- Technology stack
- Multi-tenancy strategy
- Security strategy

## Completion Criteria

No major unresolved architectural question prevents development of the first vertical slice.

Status: PENDING

---

# M3 — Garment Domain Specification

Owner: Archit

## Goal

Document real garment-shop workflows in detail.

## Required Workflows

Examples:

- Product creation
- Purchase from supplier
- Vendor bill entry
- Stock receiving
- Product placement
- Product search
- Billing
- Payment
- Return
- Exchange
- Customer creation
- Fabric roll
- Meter-based selling
- Roll cutting
- Reorder
- Dead stock
- Low stock
- Customer follow-up

## Every Workflow Must Define

- Goal
- Actor
- Preconditions
- UI
- Inputs
- Buttons
- Validation
- Business logic
- Database effects
- Module effects
- Events
- Notifications
- Failure cases
- Edge cases
- Acceptance criteria

## Completion Criteria

A developer/AI should be able to implement the first Garment MVP without inventing missing business behaviour.

Status: PENDING

---

# M4 — Sweet Shop Domain Specification

Owner: OM

## Goal

Understand and document sweet-shop operations from real businesses.

Do not assume garment rules apply to sweets.

Potential areas to investigate:

- Weight-based sales
- Batch inventory
- Manufacturing
- Expiry
- Wastage
- Packaging
- Daily production
- Ingredients
- Orders
- Festival demand

These are discovery topics, not finalized requirements.

## Completion Criteria

Real workflows have been validated and documented sufficiently to implement the Sweet Shop MVP.

Status: PENDING

---

# M5 — Retail Core MVP

## Goal

Build the common platform required by sector modules.

Expected capabilities:

- Authentication
- Shop
- Employee
- Product
- Inventory
- Customer
- Supplier
- Purchase
- Billing
- Payment
- Basic reporting

## Completion Criteria

A shop can perform a complete basic transaction:

Login
    ↓
Product Exists
    ↓
Stock Available
    ↓
Customer Selected
    ↓
Sale
    ↓
Payment
    ↓
Inventory Updated
    ↓
Invoice Generated
    ↓
History Recorded

All critical automated tests pass.

Status: PENDING

---

# M6 — Garment MVP

## Goal

Use Smart Retail OS in Archit's own garment shop.

## Completion Criteria

The shop can perform real daily operations through the software.

Minimum validation:

- Real products
- Real inventory
- Real purchases
- Real customers
- Real bills
- Real payments
- Real returns where applicable

Garment-specific inventory works correctly.

System can be used without depending on developer intervention for normal transactions.

Status: PENDING

---

# M7 — Sweet Shop MVP

Owner: OM

## Goal

Deploy a working Sweet Shop vertical using the same Retail Core.

## Important Validation

This milestone proves that Smart Retail OS is genuinely sector-extensible.

If large parts of Retail Core must be duplicated for Sweet Shop, architecture must be reviewed.

Status: PENDING

---

# M8 — Analytics

## Goal

Convert transactional data into useful business information.

Required capabilities may include:

- Revenue trends
- Profit analysis
- Inventory movement
- Fast-moving products
- Slow-moving products
- Dead stock
- Customer segmentation
- Supplier performance

## Completion Criteria

Analytics produces reliable results from real shop data.

Status: PENDING

---

# M9 — AI Business Intelligence

## Goal

Use validated business data to provide actionable recommendations.

Potential capabilities:

- AI reports
- Business advisor
- Dead-stock suggestions
- Reorder explanations
- Customer recommendations
- Demand insights

## Completion Criteria

AI provides useful recommendations while core operations continue normally when AI is disabled/unavailable.

Status: PENDING

---

# M10 — Relationship Engine

## Goal

Help shop owners strengthen customer relationships.

Capabilities may include:

- Birthday reminders
- VIP customer lists
- Inactive customer detection
- Customer follow-ups
- WhatsApp campaigns
- Festival communication
- Purchase-history context

## Product Principle

Automation should strengthen personal relationships, not replace them.

Status: PENDING

---

# M11 — Smart Shop Automation

## Goal

Reduce repetitive manual work.

Potential capabilities:

- OCR supplier bills
- Barcode generation
- Barcode scanning
- Thermal printing
- Voice announcements
- Automated alerts
- WhatsApp integration

Status: PENDING

---

# M12 — Production Pilot

## Goal

Run Smart Retail OS in multiple real shops.

## Measure

- Daily active usage
- Number of bills
- Inventory accuracy
- Errors
- Support requests
- Time saved
- Dead stock improvements
- Customer engagement
- Owner satisfaction

## Completion Criteria

Multiple shops can operate reliably without developers being physically present.

Status: PENDING

---

# M13 — Paid SaaS Launch

## Goal

Accept external paying customers.

Plans under consideration:

### Basic
Approx. ₹300/month

Focus:
Basic shop operations and billing.

### Professional
Approx. ₹1,500/month

Focus:
Business management, multi-user capabilities, analytics and selected intelligence features.

### Master
Approx. ₹2,000/month

Focus:
Advanced AI, analytics, automation, customer engagement, voice and other premium capabilities.

Pricing remains subject to market validation.

## Completion Criteria

- Subscription management works
- Onboarding works
- Billing works
- Backups work
- Security reviewed
- Monitoring exists
- Support process exists
- Customer can operate without developer involvement

Status: PENDING

---

# M14 — First 10 Paying Shops

Goal:

10 businesses actively paying and using Smart Retail OS.

Success is NOT defined only by registration.

Customers must actually use the product.

Status: PENDING

---

# M15 — First 100 Paying Shops

Validate:

- Product-market fit signals
- Support scalability
- Infrastructure
- Pricing
- Retention
- Onboarding
- Hardware compatibility

Status: PENDING

---

# M16 — 500 Shops

Focus moves toward:

- Operational scalability
- Automation
- Partner ecosystem
- Stronger infrastructure
- Sector expansion

Status: PENDING

---

# M17 — 2,000 Paying Shops

Long-term commercial milestone.

At approximately ₹2,000 average revenue per customer this could represent a significant SaaS business, but customer count, retention and actual ARPU must be measured rather than assumed.

Status: FUTURE