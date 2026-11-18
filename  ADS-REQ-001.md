# ANTENYI DIGITAL SERVICES
## User and Account Management Requirements

**Document ID:** ADS-REQ-001  
**Document Title:** User and Account Management Requirements  
**Version:** 1.0 — Working Draft  
**Status:** PROPOSED — Awaiting Review and Approval  
**Project:** Antenyi Digital Services (ADS)  
**Priority:** Foundational — Required before account-dependent marketplace development.

---

## 1. Purpose

This document defines how users will register, access, manage and use accounts on the Antenyi Digital Services marketplace.

The system must support individual customers, businesses, sellers, buyers, administrators and employees through a secure, consistent and manageable account structure.

The design must prevent unnecessary duplication of accounts, unauthorised access, identity misuse, privilege abuse and improper handling of personal and business information.

## 2. Core Design Principles

The account management system shall follow these principles:

1. One person should ordinarily maintain one primary platform account.
2. An account may have multiple authorised capabilities, such as buying and selling.
3. Individual and business account information must be distinguishable.
4. Registration must not automatically grant seller or administrative privileges.
5. Access must be based on verified account status and assigned permissions.
6. Sensitive information must only be accessible to authorised parties.
7. Account activities must be traceable through appropriate audit records.
8. Users must have reasonable control over their account information.
9. Account recovery must be secure and resistant to impersonation.
10. Account restrictions must be applied fairly and with appropriate review mechanisms.
11. The system must support future growth without requiring a complete redesign of its account architecture.

## 3. Supported User Types

### 3.1 Individual Buyers

Individuals purchasing products or services for personal or household use.

Capabilities may include:
- Browse products and services.
- Maintain a personal profile.
- Save delivery addresses.
- Add products to a shopping cart.
- Place orders.
- Make payments.
- Track orders and deliveries.
- Access purchase history.
- Submit complaints and refund requests.
- Manage communication preferences.

### 3.2 Business Buyers

Businesses, retailers, institutions and other organisations purchasing through ADS.

Capabilities may include:
- Maintain business profile information.
- Identify authorised representatives.
- Manage business delivery addresses.
- Place retail, wholesale or bulk orders.
- Request quotations.
- Access business purchasing history.
- Download relevant transaction documents.
- Manage authorised business users where approved.
- Submit complaints and service requests.

Business accounts must not automatically receive credit facilities or deferred-payment privileges.

### 3.3 Individual Sellers

Individuals approved to offer eligible products or services.

Capabilities may include:
- Apply for seller status.
- Submit required verification information.
- Create and manage an approved seller profile.
- Manage eligible product and service listings.
- Receive and process orders.
- Manage fulfilment information.
- View sales and financial records.
- Submit support requests.
- Respond to buyer complaints within authorised procedures.

Seller capabilities must only become active after the required approval process.

### 3.4 Business Sellers

Registered businesses and other eligible commercial organisations approved to sell through ADS.

Capabilities may include:
- Maintain a business seller profile.
- Submit business verification information.
- Identify authorised representatives.
- Manage approved shops.
- Manage authorised staff accounts where supported.
- Create and manage listings.
- Process orders.
- View financial statements and settlement records.
- Manage customer service responsibilities.

Business registration or verification must not be treated as automatic approval to sell every category of product.

### 3.5 Administrators

Authorised individuals responsible for managing defined areas of the platform.

Administrator access must be assigned according to specific responsibilities and permissions.

Administrative privileges must not be automatically granted to every employee or technical operator.

### 3.6 Employees and Operational Staff

Staff members may be assigned access to specific operational functions, including:
- Customer support.
- Seller verification.
- Listing moderation.
- Order monitoring.
- Dispute investigation.
- Financial review.
- Compliance monitoring.
- Technical operations.

Each employee must have an individual account. Shared employee login accounts must not be permitted.

## 4. Unified Account Structure

**Requirement:** ADS should use a unified account architecture.

A user who wishes to purchase products and also operate an approved seller account should not need to maintain two unrelated personal accounts.

The system should distinguish between:

- The primary user identity.
- Personal profile information.
- Business profiles and affiliations.
- Buyer capabilities.
- Seller capabilities.
- Assigned administrative or employee permissions.

A user may therefore have several authorised relationships or capabilities without duplicating their primary identity.

For example, an individual may:
1. Register an account.
2. Purchase products as an individual buyer.
3. Apply to become a seller.
4. Receive seller approval.
5. Operate an approved seller profile.
6. Continue purchasing through the same account.

The system must keep these activities and their associated permissions appropriately separated.

## 5. Registration Requirements

### 5.1 General Registration

The platform shall provide a clear registration process.

The registration process should collect only information necessary for account creation and the user's intended activities.

Proposed basic registration information:
- Full name.
- Email address.
- Mobile telephone number.
- Password or approved authentication credential.
- Country of residence or operation.
- Acceptance of applicable terms and privacy notices.

Email and telephone verification requirements must be defined in the authentication and account security document.

### 5.2 Individual Registration

Individuals should be able to register without first applying to become sellers.

Browsing must remain available without registration.

Users must sign in before completing checkout, in accordance with the previously approved buyer experience framework.

### 5.3 Business Registration

Business users should be able to create or associate a business profile with their primary account.

Depending on the organisation's legal structure and activities, relevant information may include:
- Business or organisation name.
- Business registration details, where applicable.
- Business address.
- Business contact information.
- Authorised representative information.
- Relevant verification documents.

The platform must distinguish between information required to create a business buyer profile and additional information required to obtain seller approval.

### 5.4 Seller Registration

Seller registration shall be an application process rather than automatic activation.

Applicants may be required to provide:
- Personal or business identity information.
- Contact information.
- Business registration details, where applicable.
- Operating address.
- Proposed seller category.
- Product or service information.
- Relevant licences, permits or certificates where applicable.
- Payout-related information through an approved process.

The required evidence must depend on seller type, category, legal requirements and risk.

## 6. Business Accounts and Authorised Representatives

Business accounts should support organisational access without giving every associated individual unrestricted authority.

The system should eventually support:
- Business owners.
- Directors or authorised representatives.
- Purchasing officers.
- Finance personnel.
- Order managers.
- Customer service personnel.
- Other approved business users.

Each person must use an individual login.

The business owner or authorised administrator should be able to assign and revoke permitted business-level access.

The platform must retain records of who authorised each business user and the permissions assigned.

## 7. Account Profiles

### 7.1 Personal Profile

A personal profile may contain:
- Full name.
- Contact information.
- Profile image, if provided.
- Country and relevant address information.
- Communication preferences.
- Account security settings.

### 7.2 Business Profile

A business profile may contain:
- Organisation name.
- Business type.
- Registration information, where applicable.
- Business contact details.
- Business address.
- Authorised representatives.
- Relevant verification status.

### 7.3 Seller Profile

An approved seller profile may contain:
- Seller or shop name.
- Business description.
- Approved operating categories.
- Shop contact information.
- Delivery and fulfilment coverage.
- Seller verification status.
- Relevant policies and disclosures.
- Seller performance information, where appropriate.

Public seller information must be separated from confidential verification information.

## 8. Multiple Roles and Account Relationships

The system must support multiple authorised roles without allowing users to grant themselves privileges.

Examples:
- An individual buyer who also becomes a seller.
- A business buyer that later applies to become a business seller.
- A business owner who authorises employees to manage orders.
- An employee who receives a specific operational role.

Role assignment must be controlled by an authorised process.

A user's ability to purchase must not automatically grant permission to sell.

Seller approval must not automatically grant administrative privileges.

Business affiliation must not automatically grant access to every business record.

## 9. Account Information and Privacy

ADS must apply data minimisation and purpose limitation.

Requirements:
- Collect only information necessary for defined purposes.
- Explain why sensitive information is requested.
- Restrict access to confidential information.
- Protect identity and business verification documents.
- Avoid exposing private contact details unnecessarily.
- Maintain appropriate retention and deletion procedures.
- Provide appropriate processes for correcting inaccurate information.
- Respect applicable privacy rights and legal obligations.
- Record relevant consent and communication preferences.

Personal data must not be used for unrelated purposes without an appropriate legal basis.

## 10. Account Dashboard Requirements

Each account type should receive an interface appropriate to its authorised capabilities.

### Individual Buyer Dashboard
- Profile management.
- Addresses.
- Orders.
- Payments.
- Delivery tracking.
- Complaints and refunds.
- Saved products.
- Communication preferences.

### Business Buyer Dashboard
- Business profile.
- Authorised users.
- Orders and quotations.
- Transaction records.
- Delivery information.
- Complaints and service requests.
- Relevant purchasing documents.

### Seller Dashboard
- Seller profile.
- Shop management.
- Listings.
- Inventory.
- Orders.
- Fulfilment.
- Customer enquiries.
- Sales records.
- Commissions and settlement information.
- Seller support and compliance notices.

### Staff and Administrator Dashboard
Access must be determined by assigned responsibilities.

Administrative dashboards must not expose information or functions that the logged-in staff member is not authorised to use.

## 11. Account Status Management

The account system should support clearly defined statuses.

Proposed statuses include:

- Pending verification.
- Active.
- Restricted.
- Suspended.
- Under review.
- Deactivated.
- Closed.

Different capabilities may have different statuses.

For example, a user may have an active buyer account while their seller application remains pending.

Suspending seller privileges should not automatically suspend unrelated buyer capabilities unless a justified security, legal or policy reason requires it.

Every significant status change must have:
- A recorded reason.
- An authorised initiating party.
- A timestamp.
- An appropriate audit record.
- A review or appeal route where applicable.

Detailed status-transition rules will be established in the Account Lifecycle Requirements document.

## 12. Account Recovery and User Support

Users must have an appropriate way to recover access to their accounts.

Recovery processes must:
- Verify that the requester is authorised.
- Avoid exposing passwords or authentication secrets.
- Prevent unauthorised changes to account ownership.
- Provide appropriate security notifications.
- Record significant recovery activities.
- Include additional safeguards for privileged accounts.

High-risk account recovery must receive stronger verification than ordinary account recovery.

## 13. Accessibility and Usability

The account system must:
- Work on mobile phones, tablets and desktop devices.
- Provide clear instructions and validation messages.
- Avoid unnecessary registration steps.
- Support accessible forms and navigation.
- Use understandable language.
- Provide appropriate feedback when actions succeed or fail.
- Avoid revealing confidential information through error messages.

WCAG 2.2 AA is adopted as the project's accessibility target.

## 14. Security and Abuse Prevention

The account architecture must be designed to reduce:
- Fake accounts.
- Impersonation.
- Account takeover.
- Unauthorised role assignment.
- Business identity misuse.
- Seller identity fraud.
- Employee privilege abuse.
- Unauthorised access to business information.
- Unauthorised access to financial records.
- Automated registration abuse.

Controls will be specified in the Authentication and Account Security Requirements and Roles and Permissions Matrix.

## 15. Scalability and Future Expansion

The account architecture should accommodate:
- More countries.
- Additional seller categories.
- More business account types.
- Additional staff roles.
- Business team management.
- New verification providers.
- Additional authentication methods.
- Future mobile applications and approved integrations.

These capabilities should be introduced when justified rather than implemented prematurely.

## 16. Initial Acceptance Criteria

The account management foundation will not be considered complete until tests demonstrate that:

1. An individual can register and manage a personal account.
2. A business profile can be associated with an authorised user.
3. One user can hold multiple approved capabilities.
4. A buyer cannot automatically obtain seller privileges.
5. A seller application can be submitted and reviewed.
6. Seller approval is controlled by authorised personnel.
7. Business users cannot access information beyond their permissions.
8. Staff accounts are individually identifiable.
9. Public profiles do not expose confidential verification documents.
10. Account status changes are recorded.
11. Account recovery follows defined security requirements.
12. Users can manage permitted profile information.
13. Unauthorised users cannot access protected account functions.
14. Account functionality works on supported mobile and desktop screen sizes.
15. Automated tests cover normal, invalid, unauthorised and abuse-related scenarios.

## 17. Decisions Register

| ID | Decision | Status |
|---|---|---|
| ADS-ACC-001 | ADS will use a unified primary user account architecture. | PROPOSED |
| ADS-ACC-002 | One account may support multiple authorised capabilities. | PROPOSED |
| ADS-ACC-003 | Individual and business profiles will be supported. | PROPOSED |
| ADS-ACC-004 | Seller registration will require approval before selling. | AGREED |
| ADS-ACC-005 | Administrative and employee accounts will use individual credentials. | AGREED |
| ADS-ACC-006 | Business accounts will support authorised representatives and controlled access. | PROPOSED |
| ADS-ACC-007 | Browsing will be available without registration. | AGREED |
| ADS-ACC-008 | Sign-in will be required before checkout. | AGREED |
| ADS-ACC-009 | Account capabilities and statuses will be managed independently where appropriate. | PROPOSED |
| ADS-ACC-010 | Confidential verification information will be separated from public profiles. | PROPOSED |
| ADS-ACC-011 | Account activities and important status changes will be auditable. | AGREED |
| ADS-ACC-012 | WCAG 2.2 AA will be the accessibility target. | AGREED |

## 18. Outstanding Questions

The following matters require review before final approval:

1. Should an individual account be allowed to operate multiple seller shops?
2. Should a business account support multiple authorised users from the first operational release, or should this capability be introduced later?
3. Should business buyers and business sellers use the same business profile structure, with different permissions and verification requirements?
4. Should users be allowed to register using either email or telephone number, or should both be required?
5. Should a user be able to change their primary email or telephone number without support intervention, subject to additional verification?
6. Which account information should be visible publicly on seller profiles?
7. What should happen when a business owner leaves an organisation or loses authority over its account?

## 19. Approval

This document remains a working draft until reviewed and approved.

Final approval will establish the user and account management requirements baseline for ADS development.

**Guiding principle:** Every account must represent an identifiable user or authorised organisational relationship, and every capability must be granted through a controlled and traceable process.