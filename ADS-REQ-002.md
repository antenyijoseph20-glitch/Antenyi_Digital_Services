# ANTENYI DIGITAL SERVICES
## ROLES AND PERMISSIONS MATRIX

**Document ID:** ADS-REQ-002  
**Version:** 1.0 — Working Draft  
**Status:** PROPOSED — Awaiting Review and Approval  
**Project:** Antenyi Digital Services (ADS)  
**Priority:** Foundational — Mandatory  
**Related Document:** ADS-REQ-001 — User and Account Management Requirements

---

## 1. Purpose

This document establishes the roles, responsibilities, permissions and access restrictions for everyone interacting with the Antenyi Digital Services platform.

It defines:

- Who may access particular platform functions.
- What each role is permitted to do.
- Which operations require additional approval.
- Which records users may access or modify.
- How conflicting responsibilities must be separated.
- How administrative privileges are controlled.
- How unauthorised actions are prevented and investigated.

The objective is to ensure that every user receives only the access necessary to perform their authorised responsibilities.

## 2. Governing Principles

The permissions system shall follow these principles.

### 2.1 Least Privilege

Every user receives only the permissions required for their assigned responsibilities.

No user should receive broad administrative access merely for convenience.

### 2.2 Deny by Default

Access must be denied unless an authorised permission explicitly allows the requested action.

A missing permission must never be interpreted as permission granted.

### 2.3 Separation of Duties

Sensitive operations must be divided between different authorised individuals.

For example, the person preparing a seller payout must not independently approve that same payout.

### 2.4 Individual Accountability

Every employee and administrator must operate through an individually identifiable account.

Shared staff accounts are prohibited.

### 2.5 Resource-Level Restrictions

Having a role does not automatically grant access to every record.

For example:
- A seller can manage their own approved shop.
- A seller cannot manage another seller's shop.
- A business employee can access only the business records assigned to them.
- A support employee cannot access unrestricted financial records.

### 2.6 Controlled Privilege Assignment

Users cannot grant themselves additional permissions.

Role assignment and privilege changes must follow authorised procedures.

### 2.7 Auditability

Sensitive access, permission changes, approvals and administrative actions must be recorded.

### 2.8 Independent Oversight

Critical operations must be subject to appropriate independent review.

No individual should have unchecked control over sensitive platform activities.

---

## 3. Permission Architecture

ADS shall use a combination of:

1. Role-Based Access Control (RBAC).
2. Resource-level access restrictions.
3. Business and seller relationship checks.
4. Contextual restrictions for sensitive operations.

RBAC determines the general functions available to a user.

Resource-level checks determine whether the user may perform that function on a particular record.

Contextual restrictions may consider:
- Account status.
- Verification status.
- Business affiliation.
- Shop ownership.
- Transaction ownership.
- Assigned responsibilities.
- Approval status.
- Risk or security restrictions.

### Example

A seller may have permission to update product listings.

However, the system must additionally verify that:
- The seller is approved.
- The seller's account is active.
- The product belongs to a shop they are authorised to manage.
- The product category is approved.
- The requested change is permitted.

Permission to perform an action does not override these restrictions.

---

## 4. External User Roles

### 4.1 Anonymous Visitor

An anonymous visitor is a person browsing ADS without registering or signing in.

Permitted activities:
- Browse public products and services.
- View approved seller profiles.
- Search the catalogue.
- View public product information.
- Read public platform policies.
- Access public help information.
- Register an account.
- Submit permitted public enquiries.

Restricted activities:
- Access private account information.
- Place an order.
- View private order records.
- Access seller dashboards.
- Access administrative functions.
- View confidential seller or buyer information.

### 4.2 Individual Buyer

An individual buyer may:

- Manage their personal profile.
- Manage permitted delivery addresses.
- Browse and save products.
- Maintain a shopping cart.
- Place orders.
- Make payments through approved payment methods.
- View their own transactions.
- Track their orders.
- Submit complaints and refund requests.
- Communicate through approved platform channels.
- Manage promotional communication preferences.

An individual buyer may not:

- Access another buyer's account.
- Modify seller listings.
- Change platform commission rates.
- Approve refunds outside authorised processes.
- Access confidential administrative records.
- Manipulate payment or settlement records.

### 4.3 Business Buyer Owner or Authorised Administrator

This role manages an organisation's buyer account.

Permitted activities:
- Manage authorised business information.
- Manage approved business users.
- Assign permitted business purchasing responsibilities.
- Manage business delivery addresses.
- Access authorised purchasing records.
- Place business orders.
- Request quotations.
- Review relevant business transaction documents.
- Remove or change business users within authorised procedures.

Restrictions:
- Cannot access another organisation's records.
- Cannot obtain automatic credit privileges.
- Cannot modify ADS financial records.
- Cannot access seller information beyond legitimate business needs.
- Cannot bypass legal, payment or platform restrictions.

### 4.4 Business Buyer Member

This role is assigned to an employee or representative of a business buyer.

Permissions may include:
- Browse and select products.
- Prepare shopping carts.
- Place orders if authorised.
- View assigned business orders.
- Manage permitted purchasing tasks.
- Submit authorised enquiries.

Restrictions depend on the permissions assigned by the business administrator.

For example, a purchasing employee should not automatically have authority to change business ownership or manage all financial settings.

### 4.5 Individual Seller Owner

An approved individual seller may:

- Manage their authorised shop.
- Create and update permitted listings.
- Manage inventory and pricing.
- View their own orders.
- Process authorised order activities.
- Manage fulfilment information.
- Respond to buyer enquiries.
- View their own sales records.
- View commission and payout statements.
- Respond to complaints.
- Submit support requests.

Restrictions:
- Cannot approve their own seller application.
- Cannot approve their own disputed refund decisions.
- Cannot alter platform commission rules.
- Cannot change financial ledger entries.
- Cannot access another seller's records.
- Cannot bypass listing moderation.
- Cannot sell prohibited or unapproved products.

### 4.6 Business Seller Owner

The authorised owner or representative of a business seller account may:

- Manage the approved business seller profile.
- Manage authorised shops.
- Appoint permitted business users.
- Assign shop-level responsibilities.
- Manage approved listings.
- Monitor orders and fulfilment.
- Review business seller financial statements.
- Manage permitted business contact information.
- Submit compliance documents.
- Manage seller support and complaints.

Business ownership and authority changes must follow a controlled verification process.

### 4.7 Business Seller Staff

Business sellers may assign different responsibilities to individual employees.

Proposed business-level roles:

**Shop Manager**
- Manage authorised shop settings.
- Manage permitted listings.
- Monitor shop operations.

**Catalogue Manager**
- Create and update product listings.
- Manage product descriptions and images.
- Update inventory and pricing within authorised limits.

**Order Manager**
- View assigned orders.
- Update permitted order statuses.
- Coordinate fulfilment.

**Finance Viewer**
- View authorised sales statements.
- View commissions and settlement information.
- Download permitted financial reports.

**Customer Service Representative**
- Respond to buyer enquiries.
- Handle assigned customer-service matters.
- Escalate complaints.

These roles must be restricted to the relevant business and assigned shops.

Business employees must not automatically receive access to all seller financial or ownership information.

---

## 5. Internal Platform Roles

Internal roles must be individually assigned and controlled.

### 5.1 Platform Governance Owner

Responsible for overall organisational oversight.

Permitted responsibilities may include:
- Approving governance policies.
- Reviewing platform performance.
- Approving organisational role structures.
- Authorising designated senior appointments.
- Reviewing significant risk reports.
- Reviewing major incidents.
- Approving strategic platform changes.

This role must not provide unrestricted direct access to all operational and financial functions.

Sensitive actions remain subject to their separate approval procedures.

### 5.2 User Account Administrator

Responsibilities:
- Review account-related support requests.
- Manage authorised account status changes.
- Assist with account recovery through approved procedures.
- Investigate account access issues.
- Maintain permitted account records.

Restrictions:
- Cannot access user passwords.
- Cannot bypass authentication safeguards.
- Cannot grant themselves additional privileges.
- Cannot independently approve sensitive financial actions.
- Cannot access confidential account information without an authorised purpose.

### 5.3 Seller Verification Officer

Responsibilities:
- Review seller applications.
- Examine submitted verification documents.
- Request additional information.
- Record verification findings.
- Recommend approval, rejection or further investigation.

A verification officer must not approve an application they submitted or improperly influence their own review.

Higher-risk seller categories may require additional independent approval.

### 5.4 Catalogue Moderator

Responsibilities:
- Review submitted listings.
- Approve or reject listings within assigned authority.
- Identify prohibited or misleading content.
- Request corrections.
- Suspend or escalate suspicious listings.
- Record moderation decisions.

Restrictions:
- Cannot alter platform financial settings.
- Cannot approve their own seller application.
- Cannot bypass category-specific requirements.
- Cannot permanently delete relevant evidence of moderation activity.

### 5.5 Order Operations Officer

Responsibilities:
- Monitor order processing.
- Investigate fulfilment problems.
- Assist with delivery-related issues.
- Review permitted order information.
- Coordinate operational escalations.

Restrictions:
- Cannot alter payment ledger entries.
- Cannot independently approve sensitive refunds.
- Cannot access unrelated seller financial records.

### 5.6 Customer Support Officer

Responsibilities:
- Respond to buyer and seller enquiries.
- View authorised support-related records.
- Assist with order enquiries.
- Create complaint records.
- Escalate unresolved issues.
- Communicate authorised decisions.

Restrictions:
- Cannot independently make sensitive financial adjustments.
- Cannot alter evidence.
- Cannot access unrelated private records.
- Cannot close serious complaints without required review.

### 5.7 Dispute Investigator

Responsibilities:
- Investigate assigned disputes.
- Examine permitted transaction information.
- Review relevant evidence.
- Obtain responses from involved parties.
- Document findings.
- Recommend appropriate outcomes.

Restrictions:
- Must not be a party to the dispute.
- Must not improperly favour a buyer or seller.
- Must not alter financial records.
- Must not independently approve a decision where independent approval is required.

### 5.8 Dispute Decision Officer

Responsibilities:
- Review investigation findings.
- Evaluate available evidence.
- Make authorised dispute decisions.
- Approve permitted remedies.
- Record reasons for decisions.

The decision officer should be independent of the parties involved and, where practicable, independent of the investigator.

Appeal arrangements must allow eligible decisions to receive further review.

### 5.9 Finance Operations Officer

Responsibilities:
- Review transaction records.
- Monitor reconciliation.
- Prepare authorised financial reports.
- Calculate commissions through approved system rules.
- Prepare payout instructions.
- Investigate payment discrepancies.
- Prepare permitted financial adjustments for approval.

Restrictions:
- Cannot independently approve their own sensitive financial adjustments.
- Cannot change approved commission rules without authorisation.
- Cannot erase ledger records.
- Cannot approve their own payout preparation.

### 5.10 Finance Approver

Responsibilities:
- Independently review authorised financial operations.
- Approve or reject qualifying payout batches.
- Approve permitted financial adjustments.
- Review supporting evidence.
- Confirm required reconciliation and controls.

Restrictions:
- Must not approve their own prepared transaction.
- Must not bypass approval thresholds.
- Must not alter underlying financial evidence.
- Must not approve transactions outside their authority.

### 5.11 Compliance Officer

Responsibilities:
- Monitor compliance requirements.
- Review seller category restrictions.
- Examine compliance documentation.
- Maintain compliance records.
- Escalate suspected violations.
- Coordinate regulatory reporting where authorised.
- Monitor policy changes.

Restrictions:
- Cannot independently grant legal permissions or certifications.
- Cannot override applicable law.
- Cannot modify financial records without separate authorisation.

### 5.12 Security Administrator

Responsibilities:
- Manage authorised security configurations.
- Review security alerts.
- Coordinate security investigations.
- Manage permitted security controls.
- Coordinate incident containment.
- Review access-control risks.

Restrictions:
- Cannot use security privileges to access unrelated business records.
- Cannot disable audit logging without an authorised emergency procedure.
- Cannot approve their own exceptional privilege escalation.

### 5.13 Technical Operations Officer

Responsibilities:
- Maintain approved application infrastructure.
- Monitor system health.
- Investigate technical errors.
- Perform authorised deployment and maintenance activities.
- Manage approved backups and restoration procedures.

Restrictions:
- Must not have routine access to unnecessary production personal or financial data.
- Must not independently change business records.
- Must not bypass application permissions through unauthorised database access.
- Must not use production data for unauthorised testing.

### 5.14 Internal Auditor

Responsibilities:
- Review authorised audit records.
- Examine control effectiveness.
- Review sensitive operational activities.
- Investigate control weaknesses.
- Prepare independent audit reports.
- Recommend corrective action.

Restrictions:
- Audit access must not automatically grant authority to change the records being audited.
- Auditors must not approve their own operational activities.
- Audit findings must be protected from unauthorised alteration.

---

## 6. Core Permissions Matrix

Legend:

- **A** — Allowed within assigned scope.
- **R** — Review or recommend.
- **P** — Requires additional approval.
- **D** — Denied.
- **C** — Conditional on specific assignment or relationship.

| Function | Buyer | Seller | Support | Verification | Finance | Compliance | Security | Auditor |
|---|---|---|---|---|---|---|---|---|
| Manage own profile | A | A | C | D | D | D | D | D |
| View own orders | A | A | C | D | C | C | D | C |
| Manage own listings | D | A | D | D | D | C | D | C |
| Review seller applications | D | D | D | A | D | C | D | C |
| Approve seller applications | D | D | D | P | D | P | D | C |
| Investigate support cases | C | C | A | C | C | C | C | C |
| Investigate disputes | C | C | R | C | C | C | D | C |
| Decide disputes | D | D | D | D | D | C | D | C |
| View financial statements | C | C | C | D | A | C | D | C |
| Prepare payout batches | D | D | D | D | A | D | D | C |
| Approve payouts | D | D | D | D | P | D | D | C |
| Modify commission rules | D | D | D | D | R | C | D | C |
| Review compliance records | D | C | C | C | C | A | C | C |
| Manage security settings | D | D | D | D | D | D | A | C |
| Review audit records | D | D | C | C | C | C | C | A |

This is a high-level matrix. The final implementation must define more granular permissions for each action and record type.

---

## 7. Sensitive Operations and Approval Controls

The following operations require additional controls.

### 7.1 Seller Approval

- An authorised verification officer reviews the application.
- The officer records findings.
- Higher-risk applications receive additional review.
- The final decision is recorded.
- The applicant receives an appropriate notification.

### 7.2 Financial Adjustments

- One authorised person prepares the adjustment.
- Another authorised person reviews and approves it.
- The system validates the supporting transaction.
- The adjustment is recorded in the financial ledger.
- The original record remains traceable.

### 7.3 Seller Payouts

- Payouts are prepared by authorised finance personnel.
- Approval is performed by a separate authorised individual.
- Approval limits are enforced.
- Duplicate payout attempts are prevented.
- Failed payouts are recorded and investigated.

### 7.4 Commission Changes

- Changes require authorised business approval.
- Changes must be documented.
- Effective dates must be recorded.
- Previous rates must remain traceable.
- Existing transactions must retain their applicable pricing and commission snapshots.

### 7.5 Administrative Privilege Changes

- Role assignments require authorised approval.
- Privilege escalation must have a documented reason.
- Sensitive permission changes must be independently reviewed.
- The affected user must not approve their own privilege escalation.

### 7.6 Refunds and Reversals

- Refund authority must be based on defined limits and responsibilities.
- High-value or exceptional refunds require additional approval.
- Refunds must reference the original transaction.
- Duplicate refund attempts must be prevented.
- All financial consequences must be recorded.

---

## 8. Business and Shop-Level Permissions

The platform must distinguish:

1. User-level permissions.
2. Business-level permissions.
3. Shop-level permissions.
4. Transaction-level permissions.

For example, a business employee may be authorised to manage Shop A but not Shop B.

A finance employee may view authorised financial statements without receiving permission to modify listings.

A customer service employee may access assigned customer enquiries without receiving unrestricted access to the business's financial information.

Business owners must not be able to grant permissions beyond the authority the platform permits them to delegate.

---

## 9. Administrative Privilege Protection

Administrative access must be controlled through:

- Individual administrator accounts.
- Explicit role assignments.
- Least-privilege permissions.
- Additional authentication safeguards.
- Controlled privilege escalation.
- Separation of duties.
- Access reviews.
- Audit logging.
- Immediate restriction of compromised accounts.
- Appropriate review of exceptional access.

No ordinary administrator should be able to:
- Erase audit evidence.
- Modify financial history without traceability.
- Approve their own sensitive financial operations.
- Access every user's confidential information without an authorised purpose.
- Grant themselves unrestricted privileges.
- Disable essential security controls without an approved procedure.

---

## 10. Emergency and Exceptional Access

ADS may require exceptional access during:
- Critical security incidents.
- Serious service outages.
- Emergency financial investigations.
- Business continuity events.

Such access must be governed by a documented emergency-access procedure.

Requirements:
- A legitimate emergency reason.
- Restricted scope.
- Time-limited access.
- Appropriate authorisation.
- Complete activity logging.
- Prompt post-incident review.
- Removal of temporary privileges when no longer required.

Emergency access must not become a routine method of avoiding approval procedures.

---

## 11. Service Accounts and Automated Processes

Not all system activities will be performed by human users.

ADS may require dedicated service identities for:
- Payment notifications.
- Automated order processing.
- Email delivery.
- Scheduled reports.
- Background tasks.
- Approved integrations.
- Backup and monitoring services.

Requirements:
- Each service must have its own identity.
- Permissions must be limited to the required functions.
- Credentials must be protected.
- Service identities must not be used for interactive human login.
- Activities must be traceable.
- Unused service identities must be disabled or removed.
- Production and development service identities must be separated.

Automated processes must not receive unrestricted administrator access.

---

## 12. Permission Assignment and Review

Permission assignment must follow a controlled process.

### Initial Assignment
- Identify the user's responsibilities.
- Select the appropriate role.
- Assign only necessary permissions.
- Obtain required approval.
- Record the assignment.

### Permission Changes
- Record the reason.
- Obtain approval where required.
- Apply the revised permissions.
- Record the change.
- Notify relevant authorised parties where appropriate.

### Periodic Review
Access should be reviewed periodically and whenever:
- An employee changes roles.
- An employee leaves ADS.
- A seller changes ownership.
- A business relationship ends.
- A security incident occurs.
- A role is no longer required.

Privileged and financial permissions should receive more frequent scrutiny than ordinary low-risk permissions.

---

## 13. Conflict-of-Interest Management

Users must not participate in decisions where their personal or financial interests create an unmanaged conflict.

Examples:
- An employee investigating their own seller account.
- A finance officer approving their own payout.
- A dispute officer deciding a complaint involving their own business.
- A verification officer approving their own application.
- An administrator changing their own privileges.

Conflicts must be declared, recorded and managed through reassignment or independent review.

---

## 14. Technical Enforcement Requirements

The permission system must enforce controls at the application and data-access layers.

Requirements include:

1. Deny-by-default permission checks.
2. Server-side authorisation for protected operations.
3. Resource ownership and relationship validation.
4. Protection against insecure direct object references.
5. Consistent permission enforcement across web interfaces and APIs.
6. Protection against privilege escalation.
7. Database-level constraints where appropriate.
8. Secure handling of background tasks and service accounts.
9. Audit records for sensitive permission decisions.
10. Automated tests for authorised and unauthorised access.

Hiding a button or menu item in the interface is not sufficient security.

The server must independently verify every protected operation.

---

## 15. Initial Acceptance Criteria

The roles and permissions system will not be accepted until testing demonstrates that:

1. Users cannot access functions outside their assigned permissions.
2. Sellers cannot access another seller's private records.
3. Business employees cannot access unauthorised business records.
4. Shop-level permissions are enforced.
5. Buyers cannot perform seller or administrative functions.
6. Seller approval follows authorised procedures.
7. Financial preparation and approval are separated.
8. Users cannot approve their own sensitive transactions.
9. Privilege changes are controlled and recorded.
10. Administrators cannot silently erase audit evidence.
11. Service accounts have restricted permissions.
12. Emergency access is time-limited and reviewable.
13. Conflicts of interest can be identified and managed.
14. Access restrictions apply consistently to web pages, APIs and background operations.
15. Unauthorised access attempts are recorded appropriately.
16. Permission changes take effect without relying on outdated sessions or cached privileges.

---

## 16. Decision Register

| ID | Decision | Status |
|---|---|---|
| ADS-RBAC-001 | RBAC will form the foundation of access control. | PROPOSED |
| ADS-RBAC-002 | Resource-level and relationship-based checks will supplement RBAC. | PROPOSED |
| ADS-RBAC-003 | Access will be denied by default. | PROPOSED |
| ADS-RBAC-004 | Users will receive only the permissions necessary for their responsibilities. | AGREED |
| ADS-RBAC-005 | Staff and administrators will use individual accounts. | AGREED |
| ADS-RBAC-006 | Sensitive financial operations will require separation of duties. | AGREED |
| ADS-RBAC-007 | Sensitive financial actions will use two-person approval where required. | AGREED |
| ADS-RBAC-008 | Administrators will not have unchecked authority over all platform operations. | AGREED |
| ADS-RBAC-009 | Business permissions will support individual users and authorised organisational relationships. | PROPOSED |
| ADS-RBAC-010 | Shop-level permissions will be supported. | PROPOSED |
| ADS-RBAC-011 | Service accounts will have restricted, identifiable permissions. | PROPOSED |
| ADS-RBAC-012 | Temporary emergency access will be controlled and audited. | PROPOSED |
| ADS-RBAC-013 | Conflicts of interest will be declared and managed. | AGREED |
| ADS-RBAC-014 | Permission enforcement will apply server-side across all interfaces. | PROPOSED |
| ADS-RBAC-015 | Privileged access will undergo periodic review. | PROPOSED |

---

## 17. Outstanding Decisions

The following matters require review:

1. Should the platform have a single highest-level governance role, or should the highest authority be divided between separate governance and technical/security responsibilities?
2. Should seller verification always require two-person approval, or only for higher-risk categories and applications?
3. What financial approval thresholds should apply to refunds, adjustments and seller payouts?
4. Should business owners be allowed to create custom employee permission combinations, or only assign predefined roles?
5. Should a staff member be allowed to hold multiple internal roles, subject to conflict-of-interest and separation-of-duties restrictions?
6. How frequently should privileged access and financial permissions be reviewed?
7. Which administrative activities should require independent approval regardless of the amount involved?

---

## 18. Approval

This document remains a working draft until reviewed and approved.

Approval will establish the initial roles and permissions baseline for ADS.

**Guiding principle:**

No user should possess more authority than their responsibilities require, and no individual should have unchecked control over sensitive platform operations.