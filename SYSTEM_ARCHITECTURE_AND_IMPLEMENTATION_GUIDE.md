# System Architecture and Step-by-Step Implementation Guide

## Antenyi Digital Services

**Version:** 1.0\
**Date:** 18 November 2026\
**Architecture status:** Approved direction; detailed design decisions
and provider choices remain subject to validation.

------------------------------------------------------------------------

## 1. Purpose

This guide translates the approved business direction into a practical
technical plan. It is intended to be followed in sequence, with each
stage inspected, implemented, tested and reviewed before moving forward.

The goal is a secure, maintainable marketplace that can realistically be
built by a small team without introducing unnecessary infrastructure or
premature complexity.

## 2. Approved architecture decisions

  ---------------------------------------------------------------------
  Area                               Decision
  ---------------------------------- ----------------------------------
  Backend language                   Python

  Backend framework                  Django

  Overall architecture               Modular monolith

  Production database                PostgreSQL

  Local database                     SQLite only for suitable early
                                     experiments; use PostgreSQL
                                     locally before database-sensitive
                                     integration testing

  Frontend                           Django templates, HTML, CSS,
                                     JavaScript and Bootstrap

  ORM                                Django ORM

  Authentication                     Django authentication with
                                     marketplace-specific controls

  Authorisation                      Role-based and object-level
                                     permissions

  Integrations                       Provider-independent interfaces

  Testing                            Django tests and pytest-based
                                     tests

  File storage                       Local development storage;
                                     suitable object storage in
                                     production

  Deployment                         Separate development,
                                     testing/staging and production
                                     environments
  ---------------------------------------------------------------------

## 3. Architecture principles

1.  Build one Django application with clear domain boundaries.
2.  Do not create microservices at the beginning.
3.  Do not create one Django app for every database table or minor
    feature.
4.  Keep business rules out of templates and views.
5.  Use service-layer functions for important workflows.
6.  Use database constraints and transactions for critical state
    changes.
7.  Use explicit state transitions.
8.  Make payment and retryable operations idempotent.
9.  Enforce object-level ownership on the server.
10. Preserve financial history; correct mistakes with
    adjustment/reversal entries.
11. Keep provider-specific code behind adapters.
12. Add background processing only when there is a demonstrated need.
13. Treat security, privacy, accessibility and tests as part of each
    feature.
14. Keep architecture documentation current.

## 4. High-level system view

``` text
Browser (visitor / buyer / seller / staff)
                 |
              HTTPS
                 |
        Django web application
                 |
   -----------------------------------
   | Public marketplace and accounts |
   | Seller and catalogue management |
   | Cart, checkout and order domain  |
   | Payment and financial domain    |
   | Fulfilment and digital delivery |
   | Services and quotations         |
   | Support, disputes and reviews   |
   | Administration, audit, reports  |
   -----------------------------------
          |                 |
       PostgreSQL      Integration adapters
                           |
             -------------------------------
             | Payment provider            |
             | Email provider              |
             | Object storage              |
             | Logistics provider          |
             | Optional verification tools|
             -------------------------------
```

The diagram is conceptual. Actual provider selection and integration
must be completed later.

## 5. Suggested Django project structure

Start with a maintainable structure such as:

``` text
Antenyi_Digital_Services/
├── manage.py
├── config/
│   ├── __init__.py
│   ├── settings/
│   │   ├── __init__.py
│   │   ├── base.py
│   │   ├── development.py
│   │   ├── test.py
│   │   └── production.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── apps/
│   ├── accounts/
│   ├── buyers/
│   ├── sellers/
│   ├── catalogue/
│   ├── inventory/
│   ├── cart/
│   ├── orders/
│   ├── payments/
│   ├── finance/
│   ├── fulfilment/
│   ├── digital_goods/
│   ├── services_marketplace/
│   ├── reviews/
│   ├── support/
│   ├── disputes/
│   ├── notifications/
│   ├── governance/
│   └── reporting/
├── templates/
│   ├── base.html
│   ├── public/
│   ├── accounts/
│   ├── buyers/
│   ├── sellers/
│   └── staff/
├── static/
│   ├── css/
│   ├── js/
│   └── images/
├── media/                 # Development only; do not assume public access
├── tests/
│   ├── unit/
│   ├── integration/
│   ├── workflows/
│   └── security/
├── docs/
│   ├── architecture/
│   └── stages/
├── .env.example
├── .gitignore
└── dependency files
```

This is a proposed initial layout, not a requirement to create every app
immediately. Create a Django app when its domain boundary is needed and
understood. Some domains may initially be grouped. Avoid circular
imports and cross-app direct database manipulation.

### 5.1 Domain responsibilities

-   `accounts`: identity, authentication, roles and account security.
-   `buyers`: buyer profiles, business buyer details and addresses.
-   `sellers`: seller applications, shops, verification and seller
    status.
-   `catalogue`: categories, listings, variants, attributes and
    moderation.
-   `inventory`: stock, availability and reservations when rules are
    defined.
-   `cart`: cart and cart-item behaviour.
-   `orders`: parent orders, seller orders, order items and state
    transitions.
-   `payments`: provider adapter, payment attempts, webhook events and
    verification.
-   `finance`: commission records, ledger, refunds, seller earnings and
    payouts.
-   `fulfilment`: delivery, collection, tracking and proof.
-   `digital_goods`: private files, licence terms and purchase access.
-   `services_marketplace`: service listings, quotations, scope changes
    and milestones.
-   `reviews`: verified-purchase reviews and moderation.
-   `support`: enquiries and support cases.
-   `disputes`: complaint evidence, investigation, decisions and
    escalation.
-   `notifications`: email and in-platform notifications.
-   `governance`: staff roles, approval records, audit events and policy
    versions.
-   `reporting`: role-authorised management reports.

## 6. Data modelling rules

### 6.1 General rules

-   Use a custom user model from the beginning, before the first
    migration, if the project requires custom identity fields or account
    behaviour. Decide this before running initial migrations.
-   Use UUIDs or another deliberate stable identifier strategy for
    externally referenced records.
-   Use foreign keys and database constraints.
-   Store money using `DecimalField`, never binary floating-point.
-   Store currency explicitly with monetary values.
-   Define quantity units explicitly.
-   Use timezone-aware timestamps.
-   Use explicit status choices and validated transitions.
-   Add indexes based on actual query patterns.
-   Avoid storing redundant values unless they are deliberate historical
    snapshots.
-   Use migrations; do not manually alter production tables.
-   Do not delete financial history to correct errors.

### 6.2 Core conceptual entities

``` text
User
 ├── BuyerProfile
 ├── SellerProfile
 └── StaffProfile / role assignments

Seller
 ├── Shop
 ├── VerificationCase
 ├── Listing
 │    ├── ProductVariant
 │    ├── ListingAttribute
 │    └── ListingMedia
 └── SellerOrder

Buyer
 ├── Address
 ├── Cart
 └── ParentOrder
      └── SellerOrder
           ├── OrderItem
           ├── PaymentAllocation
           ├── Fulfilment
           ├── Complaint / Dispute
           └── Refund records

Payment
 ├── PaymentAttempt
 ├── ProviderEvent
 └── ReconciliationRecord

Finance
 ├── LedgerEntry
 ├── CommissionRecord
 ├── SellerEarning
 └── Payout

Governance
 ├── StaffRole
 ├── Permission
 ├── Approval
 ├── AuditEvent
 └── PolicyVersion
```

This is a conceptual map, not a final schema. Detailed ERD and
constraints must be completed before implementing complex transaction
workflows.

### 6.3 Parent order and seller order

One buyer checkout may contain items from several sellers. The parent
order represents the checkout, while each seller order is independently
fulfilled and financially tracked.

A seller must only access their own seller orders and related permitted
records. The buyer can view the parent order and all its child seller
orders. One seller's cancellation or delivery must not silently change
another seller's order state.

### 6.4 Financial ledger

Treat the ledger as an auditable record of financial events. Never make
a seller's displayed balance the only source of truth.

For every ledger event, record at minimum: - Unique event/reference
ID. - Related order/payment/refund/payout. - Account or seller
allocation. - Currency and exact decimal amount. - Event type. -
Effective/created timestamp. - Source/provider reference where
relevant. - Actor or system process. - Reversal/adjustment relationship
where applicable.

The exact accounting model and any double-entry design must be reviewed
before live money is handled.

## 7. Business workflow boundaries

### 7.1 Seller onboarding

Application → verification review → decision → shop setup → first
listing review → seller activation.

No seller can publish or transact before the relevant approval
requirements are met.

### 7.2 Listing moderation

Draft → submitted → review → approved/rejected/needs changes → published
or restricted.

Trusted-seller privileges are configurable, earned, monitored,
category-limited and revocable.

### 7.3 Checkout and order creation

Cart validation → price/stock revalidation → fulfilment eligibility →
complete total calculation → buyer confirmation → payment attempt →
verified payment event → parent/seller order state update.

Do not create paid/confirmed order states solely from a browser
redirect. Define carefully how pending payment, bank transfer delays,
expired attempts and partial failures behave before implementation.

### 7.4 Payment event processing

Receive provider event → authenticate signature/source → validate
reference/amount/currency → check idempotency → match expected
transaction → record event → update payment state in a database
transaction → trigger eligible downstream workflow → reconcile.

Never trust the webhook payload without verifying its authenticity and
matching it to the expected transaction.

### 7.5 Refunds and payouts

Refund request → evidence/review → authorised decision → provider refund
request → provider confirmation/reconciliation → ledger entries and
customer notification.

Payout eligibility → risk/dispute checks → authorised approval where
required → provider-supported payout instruction → provider result →
ledger update and reconciliation.

Do not implement escrow or fund holding without legal and provider
confirmation.

## 8. Security architecture

### 8.1 Authentication and authorisation

-   Use Django authentication as the foundation.
-   Use individual accounts; no shared staff logins.
-   Use role-based permissions and object-level checks.
-   Check ownership on every private object request.
-   Apply stronger authentication to privileged accounts.
-   Rate-limit login, password reset, verification and sensitive
    operations.
-   Revoke sessions/tokens after relevant security events.
-   Restrict access to identity documents and private evidence.

### 8.2 Web application controls

-   CSRF protection.
-   Contextual output escaping and XSS prevention.
-   ORM/parameterised database access.
-   Secure cookie and session settings.
-   HTTPS in production.
-   Clickjacking protection.
-   Content Security Policy where feasible.
-   Secure upload validation and private storage.
-   Rate limits and abuse controls.
-   Safe error messages that do not disclose internals.

### 8.3 Financial and integration controls

-   Signed/authenticated webhooks.
-   Idempotency keys and unique event constraints.
-   Amount, currency and reference verification.
-   Replay protection.
-   Provider reconciliation.
-   No card data storage unless a formally assessed compliant design
    requires it; prefer provider-hosted/tokenised handling.
-   Separate preparation, approval and execution for sensitive financial
    actions.
-   Two-person approval for defined sensitive operations.

### 8.4 Secrets

-   Never commit `.env`, API keys, passwords, private keys or production
    credentials.
-   Commit only `.env.example` with placeholders.
-   Use environment-specific secret storage in production.
-   Rotate compromised secrets.
-   Restrict who can read production secrets.

### 8.5 Security baseline

OWASP ASVS Level 2 is a proposed verification target. It is not a
certification. Perform threat modelling and security testing throughout
development.

## 9. Provider-independent integration design

Create an internal interface for each external dependency. The domain
layer should call the internal interface, not provider-specific SDK code
directly.

Examples: - `PaymentGateway` interface: create payment, verify
transaction, refund, retrieve status. - `EmailSender` interface: send
transactional message. - `ObjectStorage` interface: store, retrieve,
delete under controlled policy. - `LogisticsProvider` interface: quote,
create shipment, track, cancel where supported.

Provider adapters translate between the marketplace's internal model and
the external provider.

Do not claim a provider feature until it has been tested in sandbox and
confirmed contractually.

## 10. Environments and configuration

Use separate environments:

1.  Local development.
2.  Automated test.
3.  Staging/pre-production.
4.  Production.

Keep settings separate. Production must use secure secret management,
HTTPS, restricted debug settings, appropriate allowed hosts, secure
cookies, database credentials and logging.

Do not copy live customer or payment data into development. Use
synthetic or properly anonymised test data.

## 11. Testing strategy

Every module should include appropriate tests.

-   Unit: business rules, calculations, validators and permissions.
-   Integration: database, storage and provider adapters.
-   Workflow: end-to-end business journeys.
-   Security: access isolation, IDOR, authentication, uploads and
    payment manipulation.
-   Accessibility: automated and manual checks.
-   Performance: important pages, search and transaction workflows.
-   Recovery: backup restoration and data integrity.
-   Regression: fixed defects remain fixed.

Failure cases are mandatory: duplicate webhook, delayed transfer,
mismatched amount, failed refund, payout failure, seller cancellation,
partial fulfilment, provider outage, expired digital access, invalid
file upload and unauthorised record access.

## 12. Step-by-step build sequence

Do not begin by coding the entire marketplace. Complete the following
steps in order.

### Step 0 --- Confirm the project workspace

1.  Open the existing project repository.
2.  Inspect its files, Git status, branches and README.
3.  Confirm whether any code or migrations already exist.
4.  Back up or commit existing work only with the owner's approval.
5.  Reconcile this guide with the actual repository; do not overwrite
    existing files blindly.

**Verification:** You can explain the current repository state and
identify which documentation is authoritative.

### Step 1 --- Finish requirements and legal readiness

1.  Review the consolidated BRS.
2.  Complete the outstanding legal/regulatory evaluation.
3.  Resolve decisions that block implementation: pricing formula,
    payment model, seller verification, stock rules, mixed cart, return
    deadlines and service terms.
4.  Create user stories and acceptance criteria for the first release.
5.  Define a limited pilot scope.

**Verification:** Every Release 1 feature has an owner, requirement,
acceptance criteria, dependencies and unresolved-risk note.

### Step 2 --- Create a Python environment

After confirming the project's Python version and dependency strategy, a
typical Ubuntu setup is:

``` bash
cd /path/to/Antenyi_Digital_Services
python3 --version
git status --short --branch
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
```

Verify:

``` bash
which python
python --version
python -m pip --version
```

Do not install every possible package at once. Add only dependencies
needed for the approved first step.

### Step 3 --- Create the Django project

After the dependency and supported Django version are selected:

``` bash
python -m pip install "Django<next-major-after-validated-version"
django-admin startproject config .
python manage.py check
```

The version constraint above is illustrative, not a version pin. Select
and lock an actual supported release after checking compatibility. Do
not copy the placeholder constraint literally.

**Verification:** `manage.py check` reports no unresolved configuration
errors, and the development server can start locally.

### Step 4 --- Decide the custom user model before first migrations

1.  Confirm the identity fields and account model.
2.  Create the custom user model if required.
3.  Configure `AUTH_USER_MODEL` before initial migrations.
4.  Add account tests.
5.  Run initial migrations only after the user model decision is
    settled.

**Critical:** Changing the user model after other apps have migrated can
be disruptive. Do not postpone this decision.

### Step 5 --- Configure PostgreSQL early enough

1.  Install/use PostgreSQL locally or use a controlled development
    database.
2.  Configure separate database settings.
3.  Run migrations against PostgreSQL.
4.  Test constraints and transactions against PostgreSQL.
5.  Keep secrets outside source control.

SQLite can be used for simple experiments, but do not rely on
SQLite-only behaviour for production-sensitive workflows.

### Step 6 --- Build the secure foundation

Implement and test: - Authentication. - Buyer/seller/staff identity
foundations. - Role and permission model. - Object-level access
checks. - Session and password controls. - Audit-event foundation. -
Error handling. - Environment settings. - Basic test setup.

Do not add all business features before access-control foundations are
tested.

### Step 7 --- Build seller and catalogue workflows

Implement: - Seller application. - Verification case and decision
history. - Shop profile. - Category model. - Listing model and
category-specific attributes. - Listing moderation. - First-listing
approval. - Trusted-seller privileges only after their rules are
defined.

Test that sellers cannot view or change another seller's data.

### Step 8 --- Build buyer discovery and order structure

Implement: - Public category/search pages. - Buyer account and
addresses. - Product/service detail pages. - Cart. - Checkout
validation. - Parent order and seller orders. - Order state
transitions. - Buyer/seller order dashboards.

Do not connect live payments until order totals, price snapshots and
order relationships are tested.

### Step 9 --- Implement financial domain before live provider integration

Design and test: - Money and currency representation. - Commission
calculation. - Ledger entries. - Payment attempts. - Idempotency. -
Refund records. - Seller earning allocation. - Payout eligibility. -
Reconciliation records.

Exact commission and settlement rules must be approved first.

### Step 10 --- Integrate payment provider in sandbox

1.  Complete provider due diligence.
2.  Confirm marketplace/submerchant and settlement capabilities.
3.  Implement provider adapter.
4.  Verify signatures and references.
5.  Test duplicate, delayed, failed and mismatched events.
6.  Test refunds and reconciliation.
7.  Obtain approval before production credentials or live transactions.

### Step 11 --- Build fulfilment and offering-specific workflows

Implement and test separately: - Seller-managed delivery. - Buyer
collection. - Platform-supported delivery only where a real
provider/process exists. - Secure digital access. - Fixed-price
services. - Quotations and accepted scope. - Milestones and completion
where approved.

### Step 12 --- Build customer protection and operations

Implement: - Cancellation. - Returns/refunds. - Complaints and
disputes. - Evidence handling. - Seller responses. - Reviews. -
Notifications. - Support cases. - Administrative approval matrix. -
Staff permissions and audit reporting.

### Step 13 --- Production readiness

Complete: - Legal/regulatory review. - Privacy review. - Security
assessment. - Accessibility review. - Performance and reliability
tests. - Backup and restoration tests. - Monitoring and alerting. -
Incident response. - Support procedures. - User acceptance tests. -
Pilot plan and rollback plan.

### Step 14 --- Controlled pilot

Start with a limited, approved seller group and category set. Monitor
payment reconciliation, order fulfilment, complaints, refunds, support
workload and security. Expand only after evidence shows the operation is
stable.

## 13. Git and change discipline

-   Use feature branches for meaningful work.
-   Make small, understandable commits.
-   Run tests before commits.
-   Do not commit secrets or personal data.
-   Review diffs before committing.
-   Do not push or deploy without explicit project-owner approval.
-   Keep database migrations in version control.
-   Do not rewrite shared history or delete data casually.

## 14. Definition of done for a development task

A task is complete only when: 1. The requirement and acceptance criteria
are clear. 2. Relevant permission boundaries are implemented. 3.
Validation and data-integrity rules exist. 4. Normal and failure paths
are handled. 5. Security/privacy implications are reviewed. 6. Tests
pass. 7. Manual verification is recorded where appropriate. 8.
Documentation is updated. 9. Known limitations are recorded. 10. No
unapproved external action has occurred.

## 15. Decisions intentionally deferred

Do not select these without assessment: - Hosting provider. - Payment
provider. - Email/SMS provider. - Logistics providers. - Object-storage
provider. - Production service levels and infrastructure sizing. - Exact
Django/Python dependency lock. - Background-job system. - Cache
service. - Search engine beyond the initial database-backed search. -
Mobile app framework.

## 16. Final implementation advice

Build the smallest complete, safe vertical slice first: a visitor can
browse an approved listing; an approved seller owns and manages that
listing; a buyer can register and create an order; the system records
the order accurately; staff can inspect the workflow with proper
permissions and audit records.

Then add payment, fulfilment, refunds and payouts in controlled steps.
Do not launch real payments until legal, provider, pricing, financial
and operational controls are confirmed.
