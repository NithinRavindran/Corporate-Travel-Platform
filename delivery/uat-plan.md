# User Acceptance Testing Plan

## Scope

Corporate travel request, domestic / international and multi-city itinerary, policy evaluation, approval, flight / hotel booking, mobile trip management, post-booking servicing and spend intelligence.

## Participants

Representative travellers, arrangers, approvers, corporate administrators, travel operations, finance users and travel programme managers.

## Entry criteria

- Agreed test scope and scenarios.
- Test environment and synthetic accounts ready.
- Policy rules, approval matrix, budgets and cost-centre data configured.
- Supplier sandbox / mock integration available.
- Mobile test devices / supported browser configurations available.
- Forecast test dataset with known expected outputs prepared.
- Test data is synthetic and contains no real employee travel or payment details.

## Test scenarios

| ID | Scenario | Expected result |
|---|---|---|
| UAT-01 | Submit complete in-policy request | Request recorded and follows configured approval rule |
| UAT-02 | Submit out-of-policy request | Policy reason visible and exception routed |
| UAT-03 | Approver delegates decision | Workflow follows valid delegation and records routing |
| UAT-04 | Reject request | Rejection reason and actor are recorded |
| UAT-05 | Supplier confirms booking | Booking moves to mapped confirmed state |
| UAT-06 | Supplier times out | Booking remains pending / unknown pending reconciliation |
| UAT-07 | Supplier changes price | Revised offer is shown before user accepts |
| UAT-08 | Duplicate callback received | No duplicate booking record is created |
| UAT-09 | User requests cancellation | Eligibility and terms are shown and request is tracked |
| UAT-10 | Finance export runs | Required booking and cost allocation fields are available |
| UAT-11 | Create multi-city trip | Ordered legs, dates, local times and component references are retained |
| UAT-12 | International trip crosses time zones | Local and reporting times are labelled and date boundaries are correct |
| UAT-13 | International trip uses multiple currencies | Conversion context is visible and transaction currency is retained |
| UAT-14 | One multi-city leg fails | Parent trip shows partial state and identifies affected component |
| UAT-15 | Traveller opens trip on mobile | Itinerary, status and permitted service actions are accessible |
| UAT-16 | Material schedule change occurs | Configured mobile notification is delivered without exposing sensitive details |
| UAT-17 | Mobile user views offline itinerary | Approved cached fields are labelled with last-sync time |
| UAT-18 | Finance user views spend forecast | Actual, committed, forecast and budget are distinguished |
| UAT-19 | Forecast data coverage is incomplete | Confidence / limitation is visible |
| UAT-20 | Policy insight identifies exception trend | Supporting breakdown is available; no rule changes automatically |

## Exit criteria

- Critical and high-severity defects resolved or explicitly accepted.
- Core domestic, international and multi-city journeys pass.
- Policy and approval decisions are auditable.
- Booking outcomes reconcile to supplier source.
- Mobile permission, notification and stale-data behaviours pass.
- Forecast definitions, variance and data-quality limitations are accepted by finance.
- Operations and support teams approve the runbook.
- Business owner records sign-off and known limitations.
