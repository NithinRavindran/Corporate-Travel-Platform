# User Acceptance Testing Plan

## Scope
Corporate travel request, policy evaluation, approval, flight / hotel booking status and post-booking servicing.

## Participants
Representative travellers, arrangers, approvers, corporate administrators, travel operations and finance users.

## Entry criteria
- Agreed test scope and scenarios.
- Test environment and synthetic accounts ready.
- Policy rules and approval matrix configured.
- Supplier sandbox / mock integration available.
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

## Exit criteria
- Critical and high-severity defects resolved or explicitly accepted.
- Core business journeys pass.
- Policy and approval decisions are auditable.
- Booking outcomes reconcile to supplier source.
- Operations and support teams approve the runbook.
- Business owner records sign-off and known limitations.
