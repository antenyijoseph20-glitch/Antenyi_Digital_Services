# Antenyi Digital Services
## Multi-Vendor Commerce and Services Marketplace

**Project status:** Product definition and planning  
**Initial launch market:** Nigeria  
**Long-term direction:** International-ready, subject to country-by-country operational and legal readiness  
**Primary repository:** `Antenyi_Digital_Services`

---

## 1. Project Overview

Antenyi Digital Services is a planned multi-vendor digital marketplace that will enable individuals and businesses to discover, promote, sell, purchase, and fulfil products and services through one trusted platform.

The platform is intended to serve three main groups:

1. **Buyers** — people and organisations looking for products or services.
2. **Sellers** — individuals, small businesses, established businesses, and service providers who want to reach customers.
3. **Platform administrators** — authorised operators responsible for marketplace governance, seller approval, safety, transactions, support, and platform operations.

The marketplace will initially focus on Nigeria. Its design should avoid unnecessary country-specific assumptions so that additional markets can be supported later. International availability will only be enabled where the platform has confirmed suitable payment, delivery, customer support, tax, legal, and operational arrangements.

Antenyi Digital Services is not intended to be merely a catalogue website. Its long-term purpose is to provide the core processes required to operate a responsible marketplace: seller onboarding, listing management, discovery, checkout, payment verification, order management, fulfilment, digital delivery, service quotations, refunds, disputes, reviews, seller settlements, and administration.

## 2. Product Vision

Build a dependable, accessible, secure, and commercially sustainable marketplace where:

- Buyers can discover and compare offerings from different sellers.
- Individuals and businesses can apply to sell without an unnecessarily complicated entry process.
- Sellers can manage their shops, listings, orders, and customer interactions.
- Buyers can purchase from more than one seller in a single checkout.
- Each seller can fulfil their part of a multi-seller order independently.
- Physical products, digital products, and services can be offered using workflows appropriate to each type.
- Payments, refunds, seller allocations, and payouts are traceable and auditable.
- Marketplace rules are applied consistently and fairly.
- The platform can expand into additional countries without pretending that every payment, delivery, tax, or legal requirement is identical everywhere.

### Product principles

1. **Trust before growth:** marketplace growth must not come at the expense of buyer and seller safety.
2. **Security by design:** access control, privacy, secure transactions, and abuse prevention must be considered from the beginning.
3. **Clear financial records:** every charge, allocation, refund, adjustment, and payout must be explainable.
4. **Transparent pricing:** buyers and sellers must be able to understand the prices and charges that affect them.
5. **Independent seller fulfilment:** one seller's order problem should not silently corrupt another seller's order.
6. **Accessible experience:** the platform should be usable by people with different abilities, devices, and levels of digital experience.
7. **Evidence-based status:** payment, dispatch, delivery, refunds, and payouts must only show statuses supported by verified events.
8. **Practical simplicity:** build what is needed, keep components understandable, and avoid premature complexity.
9. **Incremental delivery:** implement, test, review, and document the platform in small verified stages.
10. **International readiness without false claims:** prepare for expansion, but enable a country only after its requirements are assessed.

## 3. Scope and Marketplace Offering Types

The intended marketplace will support three broad offering types. All three are part of the intended Release 1 product scope, although implementation may be delivered in phases after detailed requirements and feasibility reviews.

### 3.1 Physical products

Examples include clothing, electronics, household items, accessories, handmade goods, and other tangible products.

Expected capabilities include:

- Product name, description, category, images, price, and seller information.
- Product variations such as size, colour, or model where relevant.
- Stock or availability information.
- Made-to-order products where the seller supports them.
- Delivery or buyer-collection arrangements.
- Order fulfilment and delivery tracking appropriate to the selected method.
- Cancellation, return, refund, and dispute workflows governed by published policies.

### 3.2 Digital products

Examples include downloadable documents, templates, graphics, learning materials, software assets, and other digital content that the platform is authorised to distribute.

Expected capabilities include:

- Product information, price, previews, and licence or usage terms.
- Secure storage and controlled access to purchased files or content.
- Access only after payment has been verified.
- Download or access records where appropriate.
- Protection against unauthorised public access to paid files.
- Clear digital-product refund, replacement, and licence policies.

The platform must not assume that every digital product is freely redistributable. Sellers must confirm that they have the rights to offer their content.

### 3.3 Services

Examples include design, repairs, consulting, lessons, professional services, creative work, and other services that can be purchased or commissioned.

Two service purchase models are intended:

- **Fixed-price services:** the buyer purchases a clearly described service at a published price.
- **Quotation-based services:** the buyer submits a request and the seller responds with a proposal or quotation.

An accepted quotation should record the agreed scope, price, deliverables, deadline or schedule, revision terms, and payment arrangement. A seller must not unilaterally change an accepted quotation. Changes should be agreed and recorded by the relevant parties.

Service workflows may require milestones, completion evidence, revision requests, cancellation rules, and dispute handling. The exact rules must be documented before implementation.

## 4. Users, Roles, and Permissions

The platform will use role-based access control. A user must only be able to view or change information that their role and relationship to the relevant record authorise.

### 4.1 Public visitors

Visitors who are not signed in should be able to:

- Browse public shops and approved listings.
- Search and filter public offerings.
- View public seller and product information.
- Read public reviews where permitted.
- View marketplace policies and help information.
- Begin the registration or seller-application process.

Visitors must not be able to access private account information, order records, protected digital files, seller dashboards, or administrative functions.

### 4.2 Buyers

Registered buyers should be able to:

- Manage their profile and contact information.
- Maintain appropriate delivery addresses.
- Add eligible offerings to a cart.
- Purchase from multiple sellers in one checkout.
- View the parent order and each seller-specific order.
- Track fulfilment independently for each seller.
- Access purchased digital products when payment is verified.
- Submit service requests and review quotations.
- Communicate with sellers about relevant orders or enquiries.
- Request eligible cancellations, returns, refunds, or dispute reviews.
- Leave reviews for verified purchases, subject to moderation rules.
- Manage notification preferences and account settings.

### 4.3 Sellers

Sellers may be individuals or registered businesses. A seller account must be reviewed and approved before the seller can operate publicly.

Approved sellers should be able to:

- Manage their shop profile and public business information.
- Create and manage eligible listings.
- Manage product variations and stock where applicable.
- Set service availability and respond to quotation requests.
- View and process their own seller orders.
- Arrange fulfilment using supported methods.
- Communicate with buyers about relevant enquiries and orders.
- View their own transaction and payout records.
- Respond to eligible reviews.
- Respond to disputes and provide supporting evidence.
- Review pricing calculations before publishing listings.

A seller must not access another seller's private orders, financial records, customer information, or management functions unless a specifically authorised platform workflow permits it.

### 4.4 Platform administrators and support staff

Administrative permissions should be divided by responsibility rather than giving every staff member unrestricted access.

Depending on assigned permissions, authorised staff may:

- Review seller applications and verification information.
- Approve, reject, restrict, or suspend seller accounts.
- Review and moderate listings.
- Manage categories and marketplace settings.
- Investigate reports, suspicious activity, and disputes.
- Review payment, refund, ledger, and payout records.
- Manage platform policies and configurable fees.
- Handle support requests.
- Review audit events and operational health.

Sensitive actions should require appropriate permissions and be recorded in an audit trail. Access to private messages or sensitive identity information should be restricted, justified, and logged.

## 5. Seller Onboarding and Marketplace Approval

The intended onboarding model is open application with controlled approval.

1. An individual or business submits a seller application.
2. The platform collects only the information necessary for the stated verification and operational purposes.
3. The application enters a review state.
4. An authorised administrator reviews the application and may approve, reject, or request further information.
5. An approved seller can complete the required shop setup.
6. The seller's first listings require administrator approval before becoming publicly visible.
7. Trusted-seller privileges may later allow eligible sellers to publish subsequent listings without individual manual review.

Trusted status must be configurable and revocable. It must not be granted automatically merely because a seller reaches an arbitrary sales count. The platform should consider account history, complaints, fulfilment performance, policy compliance, and other documented risk indicators.

The platform should support individual sellers without requiring every seller to have company registration. Verification requirements must be appropriate to seller type, risk, payment-provider requirements, and applicable law.

Identity and payout information are sensitive. They must be protected, access-controlled, retained only as justified, and never exposed on public shop pages.

## 6. Listings, Moderation, and Marketplace Safety

Listings must meet marketplace rules before publication.

The platform should support:

- Listing drafts, submitted, approved, rejected, suspended, and archived states.
- Administrator review of new sellers' first listings.
- Automated checks where useful and reliable.
- Buyer reporting of suspicious, misleading, prohibited, or infringing listings.
- Seller appeals or correction requests where appropriate.
- Moderation records and reasons for significant decisions.
- Restrictions for prohibited, unsafe, illegal, counterfeit, infringing, or deceptive offerings.

The platform must define a prohibited-listing policy before launch. It should also define intellectual-property complaint handling, seller responsibility for listing accuracy, and procedures for urgent safety concerns.

## 7. Shops, Catalogue, Search, and Discovery

Each approved seller should have a public shop page containing permitted business information and active approved listings.

The catalogue should support a structured category system that can grow without requiring code changes for every new category.

Planned discovery capabilities include:

- Search by product, service, shop, and relevant keywords.
- Category and subcategory browsing.
- Filters appropriate to offering type.
- Sorting by relevant attributes.
- Clear seller identity and listing information.
- Sponsored or featured placements as a future revenue feature.

Search ranking and paid placement must not mislead buyers. Sponsored content should be clearly identified. Search must not expose private or unapproved listings.

## 8. Cart, Checkout, and Multi-Seller Orders

The intended buyer experience supports a cart containing eligible items from multiple sellers.

A multi-seller checkout should create:

- **One parent customer order** representing the buyer's overall checkout.
- **A separate seller order for each seller** included in that checkout.

Each seller order must be independently manageable for:

- Order acceptance or processing.
- Stock allocation where applicable.
- Dispatch and delivery.
- Buyer collection.
- Digital fulfilment.
- Service milestones or completion.
- Cancellation.
- Refunds and disputes.
- Seller financial allocation and payout eligibility.

The buyer should have a unified view of the parent order while being able to inspect and track each seller order separately.

A failure involving one seller must not silently change the fulfilment state or financial records of another seller. The system must define how partial payment failures, partial cancellations, partial refunds, and partial fulfilment are handled.

The exact checkout rules for mixed physical, digital, and service carts must be specified and tested. If some combinations cannot safely be supported in the first release, checkout should explain the restriction rather than create an inconsistent order.

## 9. Pricing and Marketplace Revenue

### 9.1 Initial commercial direction

The current intended starting position is:

- Buyer registration: free.
- Seller registration: free.
- Standard listings: free initially.
- No separately displayed buyer marketplace service fee at checkout initially.
- Future revenue may include sponsored or featured placements and premium seller services.
- A configurable marketplace contribution is being considered as part of the listing-price calculation.

### 9.2 Seller desired amount and advertised price

The working pricing proposal is that a seller enters the amount they want to receive for the item or service, and the platform calculates an additional marketplace contribution to produce the advertised price.

Illustrative example only:

| Component | Illustrative amount |
|---|---:|
| Seller's desired amount | ₦20,000 |
| Marketplace contribution | ₦400 |
| Advertised price before other charges | ₦20,400 |

**Important commercial clarification:** under this formula, the buyer pays the full advertised price and the seller's desired amount is preserved before any separately applicable deductions or adjustments. The buyer is therefore funding the added contribution through the higher advertised price. This is not a shared-cost arrangement in which the seller and buyer each pay part of the contribution.

The business owner must decide whether this is the intended commercial model or whether the platform should use a genuinely shared contribution. The exact rate, calculation method, rounding rules, category differences, tax treatment, and presentation must be approved before implementation.

### 9.3 Pricing integrity

The eventual pricing system should:

- Keep rates and rules configurable by authorised administrators.
- Show sellers the calculation before publication.
- Clearly disclose the advertised price to buyers.
- Record the seller's desired amount, contribution, rate, advertised price, and pricing-rule version.
- Preserve a price snapshot on completed orders.
- Keep delivery charges and payment-provider charges distinct.
- Define how discounts, promotions, refunds, partial refunds, and price changes affect each component.
- Avoid silently changing the financial terms of an existing order.

No percentage or fixed contribution rate is confirmed by this README.

## 10. Payments and Payment Verification

The intended first-release payment methods are:

- Bank card.
- Bank transfer.

A recognised payment provider should be selected after a documented evaluation of its suitability for the marketplace.

Payment requirements include:

- Use provider-hosted or appropriately tokenised payment flows where possible.
- Do not store full card numbers or card security codes.
- Verify payment using authenticated provider responses, webhooks, and reconciliation processes.
- Do not treat a buyer-uploaded screenshot or receipt as proof of payment.
- Protect webhook endpoints against forgery, replay, and duplicate processing.
- Make payment processing idempotent so repeated events do not create duplicate charges or allocations.
- Record provider references and payment events for reconciliation.
- Support pending, successful, failed, reversed, refunded, and other necessary states.
- Keep payment state separate from order, fulfilment, delivery, and service-completion state.

Payment-provider capabilities must be confirmed rather than assumed. In particular, the project must investigate whether a provider supports the required marketplace or sub-merchant model, seller verification, split settlements, delayed settlements, refunds, transfer reconciliation, fees, settlement timing, and relevant Nigerian regulatory requirements.

The platform must not advertise or implement a fund-holding or escrow arrangement unless the provider and applicable legal framework explicitly support the proposed model.

## 11. Seller Allocations, Payouts, and Financial Records

The preferred business direction is for seller payouts to become eligible after successful delivery confirmation or service completion, subject to unresolved disputes and the actual capabilities and legal terms of the selected payment provider.

No payout should be released for an affected seller order while an applicable unresolved dispute blocks it.

The platform should maintain an auditable financial ledger. It should be possible to explain, for each relevant order:

- The amount paid by the buyer.
- The seller's allocated amount.
- The marketplace contribution.
- Delivery charges.
- Payment-provider charges.
- Discounts or adjustments.
- Refunds and reversals.
- Seller payable balance.
- Payout initiation, result, and reconciliation.

Financial history must not depend only on a mutable balance field. The design should preserve transaction events and use controlled, traceable reversal or adjustment entries rather than deleting or overwriting completed financial records.

The project must confirm the provider's settlement model and applicable law before implementing live seller payouts. A technical ability to calculate a balance does not, by itself, establish that the platform is legally or operationally permitted to hold or release funds.

## 12. Orders, Fulfilment, and Delivery

The platform intends to support three fulfilment arrangements:

1. **Seller-managed delivery:** the seller arranges delivery using their own or independently selected logistics arrangements.
2. **Platform-supported delivery:** the platform connects to a logistics provider or a verified operational delivery process.
3. **Buyer collection:** the buyer collects the order using agreed collection instructions.

The architecture should allow these methods, but a method must not be presented as integrated or operational until its real process has been implemented and tested.

Each seller order should have its own fulfilment record, as appropriate, including:

- Fulfilment method.
- Delivery or collection fee.
- Recipient and destination details.
- Seller dispatch information.
- Logistics provider, if used.
- Tracking reference, if genuinely available.
- Status and status timestamps.
- Delivery or collection confirmation.
- Failure, return, or exception information.

Delivery charges must be clearly distinguished from product prices and marketplace revenue. Tracking and delivery statuses must be based on real events or documented seller/buyer confirmations, not fabricated updates.

## 13. Digital Fulfilment

Digital fulfilment must be distinct from physical delivery.

The platform should:

- Grant access only after verified payment and any required order checks.
- Store protected files outside publicly accessible paths or use an equivalent secure storage design.
- Use authorised, time-limited access mechanisms where appropriate.
- Record relevant access or download events.
- Apply file-type, file-size, malware-scanning, and storage controls appropriate to the implementation.
- Prevent one buyer from accessing another buyer's purchased files.
- Provide clear support and refund processes for failed or incorrect digital delivery.

The precise download limits, licence rules, file-retention periods, and post-refund access rules remain to be defined.

## 14. Service Requests and Quotations

For quotation-based services, the intended workflow is:

1. Buyer submits a service enquiry with the information required by the seller.
2. Seller reviews the request.
3. Seller sends a quotation with scope, price, deliverables, timeline, revisions, and payment terms.
4. Buyer accepts or declines the quotation.
5. An accepted quotation becomes a recorded agreement for the service order.
6. Work proceeds under the agreed terms.
7. Completion, revision, cancellation, and dispute events are recorded.

The platform should preserve quotation versions and acceptance evidence. Changes after acceptance should require documented agreement by the relevant parties.

The project must define whether deposits, milestone payments, full upfront payments, or other arrangements are supported for each service type. These must be implemented only where the payment provider and legal arrangements support them.

## 15. Cancellations, Returns, Refunds, and Disputes

The platform should provide a fair, documented process for buyer and seller issues.

Expected capabilities include:

- Buyer cancellation requests before dispatch, subject to the applicable policy and order state.
- Seller cancellation with a recorded reason.
- Buyer reports for missing, damaged, incorrect, or undelivered products.
- Digital-product access or content complaints.
- Service-quality, scope, deadline, and completion complaints.
- Seller responses and supporting evidence.
- Administrator review and a recorded decision.
- Refund and payout restrictions while relevant disputes remain unresolved.

### Refund accounting

- A full refund should reverse the marketplace contribution associated with the affected transaction, according to the approved pricing policy.
- A partial refund should reverse the corresponding contribution for the affected item or portion, according to a documented calculation rule.
- The original transaction must remain preserved.
- Refunds should be recorded as separate, traceable financial events.
- Provider refund status and actual refund completion must be reconciled.

Before launch, the project must define return windows, evidence requirements, response deadlines, dispute escalation, appeals, digital-product exceptions, service-specific remedies, refund timing, and the treatment of provider fees.

## 16. Reviews and Seller Responses

The intended review model is based on verified purchases.

Expected rules:

- Only eligible verified purchasers may review the relevant offering or seller.
- Reviews may include a rating from 1 to 5 and written comments.
- Product photos may be supported where appropriate.
- Sellers may respond to eligible reviews.
- Sellers must not secretly alter or remove buyer reviews.
- Administrators may moderate content under a published policy.
- Review eligibility and moderation decisions should be traceable.

The platform must define how reviews work for multi-item orders, partial refunds, service milestones, cancelled orders, and disputed transactions.

## 17. Buyer-Seller Communication and Notifications

### 17.1 Communication

The intended initial communication features are:

- Website enquiry forms.
- Order-related buyer-seller messaging.
- Email notification of relevant new messages.
- Reporting of abusive or suspicious messages.
- Support escalation to authorised platform staff.

Real-time chat and WhatsApp integration are future possibilities, not confirmed first-release features.

Private communication must only be accessible to authorised participants and appropriately authorised support staff. Administrative access must be permission-controlled and auditable.

### 17.2 Notifications

The first release is intended to support in-app or website notifications and email notifications.

Potential events include:

- Account and seller-application updates.
- Order placement and processing.
- Payment confirmation or failure.
- Dispatch and delivery updates.
- Digital access availability.
- Service quotation and acceptance.
- Refund and dispute updates.
- Seller payout events.
- New messages and support responses.
- Important security notices.

A notification must only report an event that has actually occurred and been verified. SMS and WhatsApp notifications may be considered later.

## 18. Security, Privacy, and Trust

Security and privacy are core product requirements, not optional enhancements to be added after launch.

The implementation should address, at minimum:

- Secure authentication and account recovery.
- Role-based permissions and seller/customer data isolation.
- Strong protection for administrator accounts.
- Secure session and cookie settings.
- Input validation and output encoding.
- CSRF protection where applicable.
- Protection against SQL injection, cross-site scripting, broken access control, and common web vulnerabilities.
- Rate limiting and abuse prevention.
- Secure file upload and download handling.
- Secret management through environment or secret-management facilities.
- Encryption in transit and appropriate protection at rest.
- Secure payment-provider integration and webhook validation.
- Audit logs for sensitive actions.
- Dependency and vulnerability management.
- Backups and recovery testing.
- Data minimisation, retention, deletion, and access procedures.
- Incident response and security monitoring.

### 18.1 Security reference points

The project intends to use recognised standards and guidance as engineering references, including:

- **OWASP Application Security Verification Standard (ASVS):** use a risk-appropriate verification baseline, with Level 2 as a proposed target for the general application and additional controls for sensitive administrative and financial functions.
- **OWASP API Security Top 10:** use it when designing APIs and integrations, especially for object-level and function-level authorisation.
- **PCI DSS:** confirm the applicable responsibilities with the selected payment provider, acquiring institution, and qualified advisers. Using a third-party processor can reduce card-data exposure but does not automatically remove all obligations.
- **WCAG 2.2 AA:** use as the proposed accessibility target.
- **Nigeria Data Protection Act 2023 and applicable NDPC guidance:** assess obligations for personal-data processing in Nigeria.
- **GDPR and other local privacy laws:** assess applicability based on the people, organisation, and processing activities involved in each market.

These references are engineering and compliance planning inputs. Mentioning a standard does not mean the platform is certified or compliant. Compliance claims must only be made after a suitable assessment.

### 18.2 Privacy principles

The platform should collect only information needed for clear purposes, explain how it is used, restrict access, protect it, and define retention and deletion rules.

Before launch, the project should prepare and review appropriate privacy notices, consent or other lawful-basis processes where applicable, seller and buyer terms, data-subject request procedures, retention schedules, and cross-border data-transfer arrangements.

## 19. Accessibility, Usability, and International Readiness

The platform should be usable on modern desktop and mobile browsers and should be designed for responsive layouts.

Accessibility should be considered from the beginning, including:

- Keyboard navigation.
- Visible focus indicators.
- Meaningful labels and instructions.
- Appropriate colour contrast.
- Text alternatives for meaningful images.
- Clear form errors and status messages.
- Semantic page structure.
- Accessible authentication and checkout.
- Screen-reader-compatible controls.

The proposed target is WCAG 2.2 AA, subject to testing.

### International-readiness considerations

The architecture and product requirements should allow for future support of:

- Multiple currencies and currency-specific formatting.
- Country-specific addresses and phone formats.
- Time zones and date/time display.
- Language and localisation.
- Country-specific payment methods.
- Delivery coverage and logistics providers.
- Tax rules and invoicing requirements.
- Consumer protection and return rules.
- Privacy and data-transfer requirements.
- Local seller verification and payout arrangements.

International readiness does not mean that every country is automatically supported. Each country must pass a documented readiness assessment before buyers or sellers in that market are enabled.

## 20. Proposed Technical Direction

The following is the current technical recommendation for evaluation. It is **proposed**, not a final implementation decision.

| Area | Proposed direction | Reason |
|---|---|---|
| Programming language | Python 3.12 or a supported newer version after compatibility review | Maintainable ecosystem and user's learning path |
| Web framework | Django | Built-in authentication, permissions, ORM, admin foundation, and security features |
| Front end | Django templates, HTML, CSS, JavaScript, and Bootstrap where useful | Practical responsive interface without requiring a separate front-end application initially |
| Local database | SQLite for early local development if suitable | Simple local setup |
| Production database | PostgreSQL | Strong relational database capabilities and production suitability |
| Data access | Django ORM with reviewed database constraints and migrations | Maintainable data modelling |
| Testing | Django test framework and/or pytest | Automated verification |
| Version control | Git and GitHub | Traceable development and collaboration |
| File storage | Local development storage; production object storage or equivalent secure service | Controlled and scalable file handling |
| Payments | A vetted payment provider selected after capability and compliance review | Avoid building card processing ourselves |
| Deployment | A reputable production hosting environment selected after operational review | Secure, monitored deployment |

### Why Django is currently preferred

A marketplace has complex users, permissions, records, workflows, and administrative needs. Django provides a mature foundation for many of these concerns. It does not automatically make the application secure or correct; the project must still design permissions, workflows, data constraints, tests, and operational controls carefully.

The final architecture should be based on documented requirements and trade-offs, not framework popularity alone.

## 21. Proposed Application Boundaries

The application should be modular, but modules should be introduced only when they represent a meaningful responsibility.

Potential domains include:

- Accounts and identity.
- Seller shops and onboarding.
- Catalogue and listings.
- Inventory and availability.
- Cart and checkout.
- Orders and seller orders.
- Payments and provider integrations.
- Financial ledger and payouts.
- Physical fulfilment and delivery.
- Digital delivery.
- Services and quotations.
- Reviews and moderation.
- Messaging and notifications.
- Disputes and customer support.
- Administration, audit, and reporting.

These are conceptual boundaries, not an instruction to create a separate Django app for every item immediately. Related responsibilities may be grouped where that produces a simpler and safer design.

## 22. Data Integrity and Core Engineering Rules

The system must preserve consistency across orders, payments, fulfilment, and financial records.

Key rules include:

- Use database constraints and transactions for critical operations.
- Use stable identifiers for important records.
- Prevent duplicate processing of payment events and other retryable operations.
- Keep parent orders and seller orders related but independently manageable.
- Preserve order-price and policy snapshots where later changes must not alter historical transactions.
- Record important state transitions and who or what initiated them.
- Do not trust values submitted by a browser without server-side validation and authorisation.
- Do not allow a seller to change another seller's records by manipulating identifiers.
- Do not delete completed financial events to correct mistakes; use auditable reversal or adjustment records.
- Define explicit state transitions rather than allowing arbitrary status changes.
- Use background jobs and retry policies only where justified, with monitoring and failure handling.

## 23. Reliability, Performance, and Operations

A production marketplace needs more than working application code.

The project should plan for:

- Environment separation for local development, testing, staging, and production.
- Secure configuration and secret management.
- Automated database and file backups.
- Periodic restore tests.
- Error logging and operational monitoring.
- Alerts for important failures.
- Database migration procedures.
- Payment and payout reconciliation.
- Safe retries for external provider failures.
- Protection against traffic spikes and abusive requests.
- File storage capacity and cleanup policies.
- Dependency updates and security patching.
- Incident response and recovery procedures.
- Documented deployment and rollback processes.

Recovery objectives, service availability targets, performance thresholds, retention periods, and monitoring responsibilities must be set before production launch. They should reflect the actual business risk and available operational resources.

## 24. Testing and Quality Assurance

Testing must cover both individual features and complete business workflows.

Expected test categories include:

1. **Unit tests:** calculations, validation, permissions, and individual business rules.
2. **Integration tests:** database operations, payment-provider interfaces, email, file storage, and other integrations.
3. **Workflow tests:** seller application, listing approval, multi-seller checkout, payment, fulfilment, refund, dispute, and payout processes.
4. **Security tests:** access control, seller isolation, authentication, file handling, rate limits, and common vulnerabilities.
5. **Accessibility tests:** automated checks plus manual keyboard and assistive-technology review.
6. **Performance tests:** important pages and transaction workflows under expected load.
7. **Recovery tests:** backup restoration and recovery procedures.
8. **Regression tests:** previously fixed issues must remain fixed.

Testing should include failure and abuse scenarios, not only successful user journeys. Examples include duplicate payment webhooks, payment delays, partial payment failures, one seller cancelling while another fulfils, expired digital links, unauthorised seller access, invalid uploads, provider outages, and interrupted payout processing.

A feature is not complete merely because its page loads. It must meet its acceptance criteria, handle relevant failure cases, and have appropriate tests and documentation.

## 25. Development Roadmap

The roadmap is provisional and should be refined after the requirements and architecture documents are approved.

### Phase 0 — Product definition and project foundation

- Finalise the product vision and business requirements.
- Create functional requirements and acceptance criteria.
- Resolve essential pricing and payment-policy decisions.
- Define user roles and permission boundaries.
- Document key workflows and state transitions.
- Review architecture options.
- Establish coding, testing, documentation, and Git practices.

### Phase 1 — Secure application foundation

- Create the selected framework project.
- Configure environments and secrets.
- Establish database configuration and migrations.
- Implement authentication and role foundations.
- Implement audit and error-handling foundations.
- Add baseline automated tests.

### Phase 2 — Shops and catalogue

- Seller application and approval.
- Shop profiles.
- Categories and listings.
- Listing review and moderation.
- Product and service discovery.

### Phase 3 — Buyer experience and orders

- Buyer accounts and addresses.
- Cart and checkout rules.
- Parent order and seller-order creation.
- Order history and seller order management.
- Defined handling for partial and mixed orders.

### Phase 4 — Payments and financial controls

- Integrate the selected payment provider in a test environment.
- Verify payment events and reconciliation.
- Implement financial ledger records.
- Implement refund workflows.
- Implement seller payout eligibility and provider-supported payout flows only after capability and legal review.

### Phase 5 — Fulfilment and offering-specific workflows

- Physical delivery and collection.
- Digital product access and protection.
- Fixed-price services.
- Service quotations and acceptance.
- Completion and dispute workflows.

### Phase 6 — Trust, support, and marketplace operations

- Reviews and moderation.
- Buyer-seller messaging.
- Notifications.
- Dispute and support dashboards.
- Reporting and administrative controls.

### Phase 7 — Production readiness

- Security review and remediation.
- Accessibility review.
- Performance and reliability testing.
- Privacy and legal review.
- Backup and restore testing.
- Operational monitoring and incident procedures.
- User acceptance testing.
- Controlled launch and post-launch monitoring.

### Phase 8 — Measured expansion

- Evaluate additional payment and logistics providers.
- Complete country-specific readiness assessments.
- Introduce localisation and additional currencies as approved.
- Expand seller and buyer coverage gradually.
- Review operational capacity before each expansion.

## 26. Release 1 Boundaries

The intended Release 1 product includes the foundations for:

- Public browsing and discovery.
- Buyer registration and sign-in before checkout.
- Seller applications and administrator approval.
- Individual and business seller profiles.
- First-listing administrator approval.
- Physical, digital, and service listings.
- Multi-seller cart and parent/seller order structure.
- Card and bank-transfer payment integration, subject to provider selection.
- Payment verification.
- Order management.
- Supported physical fulfilment methods.
- Secure digital fulfilment.
- Fixed-price and quotation-based services.
- Refund and dispute foundations.
- Verified-purchase reviews.
- Website and email notifications.
- Basic enquiry and order-related messaging.
- Administrative oversight and audit records.

This is the intended product scope, not a promise that every feature will be launched simultaneously. Detailed prioritisation, feasibility, acceptance criteria, and release gates will determine the implementation sequence.

Potential future features include real-time chat, WhatsApp integration, SMS notifications, advanced advertising, premium seller subscriptions, advanced analytics, mobile applications, and additional international markets.

## 27. Decisions Register

This register prevents proposals and unresolved questions from being mistaken for approved requirements.

### Agreed business direction

- Multi-vendor marketplace.
- Nigeria-first launch direction, with international expansion only after readiness checks.
- Individual and registered-business sellers.
- Public browsing without registration; buyer registration/sign-in required before checkout.
- Seller applications require administrator approval.
- New sellers' first listings require administrator approval.
- Multi-seller checkout uses one parent order and separate seller orders.
- Physical products, digital products, and services are intended offering types.
- Services include fixed-price and quotation-based models.
- Bank card and bank transfer are intended initial payment methods.
- Buyer and seller registration are free initially.
- Standard listings are free initially.
- Website and email notifications are intended for the first release.
- Verified-purchase reviews are intended.
- Basic website enquiries and order-related messaging are intended.
- Physical fulfilment should accommodate seller-managed delivery, platform-supported delivery, and buyer collection, subject to actual implementation.
- Financial records should be auditable.
- Seller payout eligibility should depend on fulfilment/completion and dispute status, subject to provider capability and applicable law.

### Proposed technical and quality direction

- Django as the preferred framework.
- PostgreSQL for production.
- SQLite may be used for early local development if appropriate.
- WCAG 2.2 AA as the accessibility target.
- OWASP ASVS Level 2 as a proposed general application verification baseline, with additional risk-based controls.
- Modular application boundaries based on domain responsibilities.
- Append-only or otherwise auditable financial event records.
- Separate development, testing, staging, and production environments.

### Decisions still required

- Whether the marketplace contribution is funded entirely through the advertised price or genuinely shared between buyer and seller.
- Exact contribution formula, rate, rounding, tax handling, and category-specific rules.
- Payment provider and confirmed marketplace settlement capabilities.
- Legal and operational model for seller payouts and any delayed settlement.
- Seller verification requirements by seller type and risk.
- Exact stock and availability rules for physical products, digital products, and services.
- Mixed-cart rules for physical, digital, and service offerings.
- Return windows and refund rules.
- Digital-product refund and licence rules.
- Service deposits, milestones, revisions, and completion rules.
- Dispute deadlines, evidence, escalation, and appeal processes.
- Logistics providers and actual platform-supported delivery coverage.
- Supported currencies, countries, languages, and international launch criteria.
- Tax, invoicing, privacy, consumer-protection, and other country-specific obligations.
- Hosting, storage, monitoring, recovery objectives, and production service targets.
- Detailed release priorities and acceptance criteria.

## 28. Documentation Structure

The README is the project overview. Detailed requirements and technical decisions should live in focused documents rather than making this file an unmanageable specification.

The intended documentation structure is:

```text
Antenyi_Digital_Services/
├── README.md
├── docs/
│   ├── product/
│   │   ├── PRODUCT_VISION.md
│   │   ├── BUSINESS_REQUIREMENTS.md
│   │   ├── FUNCTIONAL_REQUIREMENTS.md
│   │   └── USER_STORIES_AND_ACCEPTANCE_CRITERIA.md
│   ├── architecture/
│   │   ├── SYSTEM_ARCHITECTURE.md
│   │   ├── DATABASE_DESIGN.md
│   │   ├── ORDER_PAYMENT_AND_PAYOUT_FLOWS.md
│   │   └── ARCHITECTURE_DECISIONS.md
│   ├── security/
│   │   ├── SECURITY_REQUIREMENTS.md
│   │   ├── THREAT_MODEL.md
│   │   └── PRIVACY_AND_DATA_PROTECTION.md
│   ├── business/
│   │   ├── SELLER_POLICY.md
│   │   ├── BUYER_POLICY.md
│   │   ├── PRICING_AND_FEES.md
│   │   ├── REFUND_AND_DISPUTE_POLICY.md
│   │   └── DELIVERY_AND_FULFILMENT_POLICY.md
│   ├── quality/
│   │   ├── TESTING_STRATEGY.md
│   │   ├── ACCESSIBILITY.md
│   │   └── RELEASE_CHECKLIST.md
│   └── operations/
│       ├── DEPLOYMENT.md
│       ├── BACKUP_AND_RECOVERY.md
│       └── MONITORING_AND_INCIDENT_RESPONSE.md
├── src/                    # Application source, after architecture approval
├── tests/                  # Automated tests, if this layout is adopted
├── .env.example            # Example configuration only; never real secrets
├── .gitignore
└── requirements.txt        # Or the dependency-management format selected
```

This is a target documentation and repository layout, not a claim that these files or directories already exist. The final code layout should follow the approved architecture.

## 29. Project Working Agreement

Development should follow a controlled, reviewable process:

1. Understand the requirement before writing code.
2. Discuss important design choices and their trade-offs.
3. Mark decisions as agreed, proposed, or unresolved.
4. Inspect existing files before changing them.
5. Make small, focused changes.
6. Explain terminal commands before asking the developer to run them.
7. Verify each stage with observable outputs and tests.
8. Do not claim a feature works without testing it.
9. Do not introduce paid services or external integrations without reviewing cost, suitability, and alternatives.
10. Never commit secrets, passwords, API keys, private identity data, or production credentials.
11. Do not push to GitHub, deploy, or make externally visible changes without the project owner's approval.
12. Keep documentation aligned with the implemented behaviour.
13. Record significant architecture and business decisions.
14. Prefer maintainable, understandable solutions over unnecessary complexity.

## 30. Definition of Done

A feature or milestone should not be considered complete until:

- Its requirement and intended behaviour are clear.
- Relevant user roles and permissions are defined.
- Normal and failure scenarios are considered.
- Validation and data-integrity rules are implemented.
- Security and privacy implications are reviewed.
- Appropriate automated tests pass.
- Relevant manual checks are completed.
- User-facing messages and statuses are accurate.
- Documentation is updated.
- Known limitations are recorded.
- The change has been reviewed before any approved commit, push, or deployment.

A production release requires a separate release-readiness review covering security, privacy, accessibility, payments, legal policies, backups, monitoring, support, and operational ownership.

## 31. Important Disclaimer

This document describes the product direction and planned requirements. It is not legal advice, a security certification, a PCI assessment, a guarantee of payment-provider capabilities, or proof of compliance with any country's laws.

Before the platform handles real payments or launches in a new market, the project must obtain appropriate provider, legal, privacy, tax, security, and operational reviews. Compliance and marketplace readiness must be assessed against the actual implementation and business operations.

## 32. Current Project Status

At the time this README is prepared:

- The project is in product-definition and planning.
- The README is a planning document, not evidence of a completed application.
- The detailed requirements, architecture, database design, security plan, and operational procedures still need to be developed and reviewed.
- The payment provider, final pricing formula, and several marketplace policies remain undecided.
- No production payment, logistics, or payout integration should be assumed to exist.

**The next recommended milestone is to review and approve the Business Requirements Specification, then convert the agreed business rules into functional requirements and acceptance criteria before creating the application scaffold.**