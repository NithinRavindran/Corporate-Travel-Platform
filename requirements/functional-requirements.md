# Functional Requirements

| ID | Area | Requirement | Priority | Notes |
|---|---|---|---|---|
| FR-01 | Identity | Authenticate users through approved identity mechanism | Must | Enterprise configuration dependent |
| FR-02 | Access | Enforce traveller, arranger, approver, admin and operations permissions | Must | Least privilege |
| FR-03 | Profile | Associate traveller with organisation entity and required attributes | Must | Minimise personal data |
| FR-04 | Request | Capture origin, destination, dates, purpose, travellers and cost allocation | Must | Configurable fields |
| FR-05 | Validation | Validate required fields and date / traveller constraints | Must | Explain errors |
| FR-06 | Policy | Evaluate applicable policy rules for selected trip and product | Must | Versioned rules |
| FR-07 | Exception | Capture out-of-policy reason and route for approval | Must | Audit decision |
| FR-08 | Approval | Route to configured approver or delegate | Must | Escalation rules |
| FR-09 | Search | Search supported flight and hotel suppliers | Must | Supplier scope defined for MVP |
| FR-10 | Display | Show price, schedule, terms and policy status | Must | Explain policy labels |
| FR-11 | Revalidation | Recheck price and availability before booking | Must | Supplier dependent |
| FR-12 | Booking | Submit request and capture supplier response | Must | Idempotency / reconciliation |
| FR-13 | Status | Show pending, confirmed, failed and cancelled states accurately | Must | State mapping |
| FR-14 | Itinerary | Present confirmed trip details to authorised users | Must | Access-controlled |
| FR-15 | Servicing | Record supported changes and cancellations | Should | Supplier capabilities vary |
| FR-16 | Reporting | Provide booking and policy reporting | Should | Data definitions required |
| FR-17 | Notifications | Notify users about approval and booking status changes | Should | Preference and channel rules |
| FR-18 | Audit | Record important policy, approval and booking actions | Must | Traceability |
