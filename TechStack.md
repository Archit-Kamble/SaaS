# Smart Retail OS — Technology Stack

## Status

Version: 0.1
Status: Initial Architecture
Last Updated: 2026

---

# 1. Technology Philosophy

Smart Retail OS must be:

- Production ready
- Secure
- Multi-tenant
- Modular
- Extensible
- Cost efficient
- Easy to maintain
- Suitable for mobile, tablet and desktop
- Capable of supporting multiple retail sectors
- Independent of individual AI/payment/communication providers where practical

Technology should be selected based on business requirements, not trends.

---

# 2. Architecture Style

Initial Architecture:

**Modular Monolith**

We will NOT start with microservices.

Reasons:

- Two-person development team
- Easier deployment
- Easier debugging
- Lower infrastructure cost
- Simpler transactions
- Faster development

However, module boundaries must remain strong enough to allow future extraction into services if required.

---

# 3. Backend

## Primary Language

Java 21

## Framework

Spring Boot

## Major Components

- Spring Web
- Spring Security
- Spring Data JPA
- Bean Validation
- Spring Actuator

Additional dependencies must be introduced only when justified.

---

# 4. Database

Primary Database:

PostgreSQL

Used for:

- Shops
- Users
- Products
- Inventory
- Sales
- Purchases
- Suppliers
- Customers
- Payments
- Expenses
- Business configuration
- Audit information

## Database Rules

- Monetary values use DECIMAL/NUMERIC.
- Important transactions are preserved.
- Tenant isolation is mandatory.
- Database migrations must be version controlled.
- Schema changes must not be performed manually in production.

Database migration technology:

To be finalized before implementation.

---

# 5. Web Frontend

Framework:

React

Language:

TypeScript

The application must support:

- Desktop
- Tablet
- Mobile browser

The UI should be responsive and touch friendly.

---

# 6. Mobile Strategy

Initial priority:

Responsive Web Application / PWA where practical.

A dedicated mobile application should be introduced only when native functionality or business requirements justify it.

Possible future technology:

Flutter

Decision must be documented before implementation.

---

# 7. Authentication & Authorization

Backend:

Spring Security

Authentication mechanism:

To be finalized during Authentication module design.

Requirements:

- Secure authentication
- Role-based authorization
- Employee permissions
- Shop/tenant isolation
- Session/token revocation strategy
- Auditability

Roles may include:

- Owner
- Manager
- Cashier
- Employee
- Accountant

Final permissions must be configurable according to business requirements.

---

# 8. AI Layer

AI must be provider-independent where practical.

Architecture:

Application
    ↓
AI Service Interface
    ↓
AI Provider Adapter
    ↓
External AI Provider

This prevents business logic from directly depending on one AI company.

Possible capabilities:

- Business Advisor
- AI Reports
- Customer Recommendations
- Dead Stock Suggestions
- Reorder Explanation
- OCR assistance
- Natural language interaction
- Image understanding/search

## AI Rule

AI must not be the authoritative calculator for:

- Revenue
- Profit
- Tax
- Inventory
- Customer balances
- Supplier balances

These are calculated by deterministic application logic.

AI receives validated/aggregated information and generates explanations or recommendations.

---

# 9. Analytics / Data Science

Initial analytics should use application/database calculations.

Examples:

- Sales trends
- Inventory turnover
- Dead stock
- Fast-moving stock
- Slow-moving stock
- ABC analysis
- Customer segmentation
- Profitability
- Seasonal patterns

Advanced forecasting/data science technologies will be selected only after sufficient real business data exists.

Do not introduce ML merely because the product contains AI.

---

# 10. OCR

Purpose:

Convert vendor bill photographs into structured purchase information.

Architecture:

Image
    ↓
OCR
    ↓
Structured Draft
    ↓
Validation
    ↓
Owner Verification
    ↓
Purchase Creation

OCR output must not directly modify inventory without validation/verification.

Provider:

To be decided.

---

# 11. File / Image Storage

Required for:

- Product images
- Saree images
- Vendor bills
- Generated documents
- Other media

Storage must be abstracted behind a storage service.

Possible production implementation:

Object storage.

Exact provider will be selected during deployment design.

---

# 12. Notifications

Supported channels may include:

- WhatsApp
- SMS
- Email
- Push Notification
- In-app Notification

Architecture:

Notification Service
        ↓
Channel Interface
        ↓
WhatsApp / SMS / Email / Push Adapter

Business modules should not directly depend on individual communication providers.

---

# 13. Voice

Requirements:

- Marathi
- Hindi
- English
- Configurable shop language

Example:

"Archit Kamble yanchya kadun ₹2,350 rupaye prapt jhale. Dhanyavaad."

Potential capabilities:

- Payment announcement
- Sales announcement
- Reminder announcement
- AI suggestions
- Multilingual TTS

TTS provider:

To be finalized.

Voice failure must never block payment or billing.

---

# 14. Hardware Integration

System should eventually support:

- Thermal Printer
- Barcode Scanner
- Barcode Label Printer
- QR Scanner
- Tablet
- Desktop
- Mobile
- Speaker/Soundbox

Hardware should be optional wherever possible.

A shop should be able to start with minimal hardware.

---

# 15. Payments

Potential payment modes:

- Cash
- UPI
- Card
- Credit
- Split payment

Payment-provider integration must remain separate from core billing logic.

Specific providers/integrations will be selected after technical and commercial evaluation.

---

# 16. Reporting

Reports may include:

- Daily
- Weekly
- Monthly
- Quarterly
- Yearly
- Profit
- Sales
- Inventory
- Customer
- Supplier
- Tax

Reports should be generated from deterministic business data.

AI may explain reports but should not replace report calculations.

---

# 17. Testing

Backend:

JUnit 5

Mocking/integration tooling will be selected according to module requirements.

Testing layers:

- Unit
- Integration
- API
- End-to-End
- Security
- Performance where required

Critical financial and inventory flows require automated tests.

---

# 18. API

Style:

REST initially

Base:

/api/v1/

API documentation:

OpenAPI / Swagger

---

# 19. Version Control

Platform:

GitHub

Branch strategy:

main
feature/*
fix/*

Every production change should be traceable.

---

# 20. CI/CD

Initial requirements:

- Build automatically
- Run automated tests
- Reject failing builds
- Package application
- Deploy safely

Exact CI/CD implementation will be selected during deployment setup.

---

# 21. Deployment

Cloud provider:

Not permanently locked yet.

AWS is a candidate.

Architecture must avoid unnecessary infrastructure during the MVP stage.

Primary goal:

Reliable deployment at reasonable cost.

---

# 22. Observability

Production system should eventually support:

- Application logs
- Error tracking
- Health checks
- Performance metrics
- Audit logs
- Alerts

Spring Boot Actuator may provide application health information.

---

# 23. Caching

Do not introduce caching prematurely.

Caching should be added only when measurements show a need.

Potential future technology:

Redis

---

# 24. Search

Initial:

PostgreSQL-based search.

Future:

Dedicated search technology may be introduced if product/image/catalogue search requirements justify it.

---

# 25. Technology Decision Rule

Before adding a major technology ask:

1. What problem does it solve?
2. Can the existing stack solve the problem?
3. What complexity does it introduce?
4. What does it cost?
5. Can two developers maintain it?
6. Does it improve the customer experience?

If these questions do not justify it, do not introduce the technology.


## Recommended stack

Layer	Smart Retail OS choice
IDE	Android Studio
Client	Flutter
Client language	Dart
State management	Riverpod
Backend	Java 21 + Spring Boot
Main database	PostgreSQL
Authentication	Spring Security
API	REST /api/v1
API docs	OpenAPI/Swagger
ORM	Spring Data JPA / Hibernate
DB migrations	Flyway
File/image storage	Object storage later
Local Flutter storage	SharedPreferences only for simple preferences; secure storage for secrets/tokens
PDF/printing	Flutter PDF + Printing initially
Testing	JUnit + Spring Boot tests + Flutter tests
Version control	Git + GitHub
Architecture	Modular Monolith + sector extensions
AI	Provider abstraction; provider chosen later
Deployment	Decide later after MVP requirements