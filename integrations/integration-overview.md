# Integration Overview

## Product integration landscape

| System / provider | Purpose | Key product data | Product considerations |
|---|---|---|---|
| HRIS / employee directory | Employee identity and organisation structure | Employee ID, status, manager, entity, department, cost centre | Source of truth, sync cadence, leaver handling |
| Identity provider | Authentication and role assignment | User identity, groups, claims | SSO, MFA, least privilege, mobile session controls |
| Flight distribution provider | Flight search and booking | Schedules, fares, availability, booking refs, ticket status | Fare revalidation, provider-specific states, ticketing |
| Hotel supplier | Hotel inventory and reservation | Property, room, rate, terms, confirmation | Rate validity, cancellation policy, occupancy |
| Expense / ERP / finance | Spend allocation, budget and reconciliation | Actuals, commitments, budget, cost centre, invoice refs | Source-of-truth hierarchy, currency and duplicate prevention |
| Exchange-rate source | Currency display and conversion | Currency pair, rate, effective date, source | Separate estimates from accounting rates |
| Mobile notification service | Push / in-app communications | Recipient token, event, template, delivery status | Consent, preference, secure payload, retry |
| Device / mobile platform services | Secure mobile access | Device / session state, app version, cache metadata | Approved device controls, cache expiry, remote logout |
| Destination information source | Approved destination reminders | Destination metadata, update timestamp, source | Licensed / approved content, accuracy and disclaimer |
| Data / reporting platform | Analytics, forecast and finance reporting | Booking, request, policy, spend and event data | Lineage, quality, access and retention |

## Integration design questions

- Which system owns each data element?
- Is communication synchronous, asynchronous or batch?
- How are identity and organisation changes handled?
- How are rate limits, pagination and provider outages handled?
- What does success mean for each provider transaction?
- How are retries made safe?
- How are duplicate events detected?
- How are unknown outcomes reconciled?
- Which source is authoritative for actuals, commitments, budgets and currency rates?
- How are forecast inputs refreshed and quality-checked?
- What information may be exposed to each user role and mobile notification channel?
- What data can be cached securely for offline mobile use, and for how long?

## Product acceptance expectations

- Provider errors are mapped to actionable platform outcomes.
- Original provider references and timestamps remain traceable.
- Sensitive credentials are stored outside source control.
- Integration health, notification delivery and data freshness are observable.
- Finance data, exchange-rate source and forecast input lineage are documented.
- Mobile cached data has expiry, access controls and last-sync metadata.
- Data ownership and reconciliation responsibility are documented.
