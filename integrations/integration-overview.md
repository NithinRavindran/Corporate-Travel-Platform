# Integration Overview

## Product integration landscape

| System / provider | Purpose | Key product data | Product considerations |
|---|---|---|---|
| HRIS / employee directory | Employee identity and organisation structure | Employee ID, status, manager, entity, department | Source of truth, sync cadence, leaver handling |
| Identity provider | Authentication and role assignment | User identity, groups, claims | SSO, MFA, least privilege |
| Flight distribution provider | Flight search and booking | Schedules, fares, availability, booking refs, ticket status | Fare revalidation, provider-specific states, ticketing |
| Hotel supplier | Hotel inventory and reservation | Property, room, rate, terms, confirmation | Rate validity, cancellation policy, occupancy |
| Expense / ERP | Spend allocation and reconciliation | Cost centre, entity, booking cost, invoice refs | Mapping, duplicate prevention, financial controls |
| Notification service | User and approver communications | Recipient, template, event, delivery status | Consent, channel preference, retry |
| Data / reporting platform | Analytics and finance reporting | Booking, request, policy and event data | Data lineage, access, retention |

## Integration design questions

- Which system owns each data element?
- Is communication synchronous, asynchronous or batch?
- How are identity and organisation changes handled?
- How are rate limits, pagination and provider outages handled?
- What does success mean for each provider transaction?
- How are retries made safe?
- How are duplicate events detected?
- How are unknown outcomes reconciled?
- What information may be exposed to each user role?

## Product acceptance expectations

- Provider errors are mapped to actionable platform outcomes.
- Original provider references and timestamps remain traceable.
- Sensitive credentials are stored outside source control.
- Integration health and backlog are observable.
- Data ownership and reconciliation responsibility are documented.
