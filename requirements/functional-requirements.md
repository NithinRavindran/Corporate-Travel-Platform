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
| FR-09 | Search | Search supported flight and hotel suppliers | Must | Supplier scope defined by market |
| FR-10 | Display | Show price, schedule, terms and policy status | Must | Explain policy labels |
| FR-11 | Revalidation | Recheck price and availability before booking | Must | Supplier dependent |
| FR-12 | Booking | Submit request and capture supplier response | Must | Idempotency / reconciliation |
| FR-13 | Status | Show pending, confirmed, failed and cancelled states accurately | Must | State mapping |
| FR-14 | Itinerary | Present confirmed trip details to authorised users | Must | Access-controlled |
| FR-15 | Servicing | Record supported changes and cancellations | Must | Supplier capabilities vary |
| FR-16 | Reporting | Provide booking and policy reporting | Must | Includes spend insights |
| FR-17 | Notifications | Notify users about approval, booking and itinerary changes | Must | Channel preferences |
| FR-18 | Audit | Record important policy, approval and booking actions | Must | Traceability |
| FR-19 | Multi-city | Create a parent trip containing multiple ordered destinations and travel legs | Must | Preserve leg-level dates and references |
| FR-20 | International | Support destination country, local time zone, local currency and organisation reporting currency | Must | Show conversion source / date |
| FR-21 | International | Capture organisation-required travel document / destination reminders | Must | Use approved content; no legal advice |
| FR-22 | Connections | Represent transit, overnight connections and time-zone date changes | Must | Avoid ambiguous local / base times |
| FR-23 | Segment policy | Evaluate policy at trip and segment level | Must | Explain rule result per affected leg |
| FR-24 | Component booking | Track flight, hotel and other supported components independently within a trip | Must | Support partial outcomes |
| FR-25 | Mobile trip | Provide mobile trip overview, itinerary, booking status and service request access | Must | Responsive or supported mobile app |
| FR-26 | Mobile alerts | Send configurable in-app / push alerts for approval and meaningful trip changes | Must | Secure notification content |
| FR-27 | Mobile access | Apply authentication, role permissions and approved secure offline itinerary behaviour | Must | Privacy and device controls |
| FR-28 | Spend view | Compare actual, booked / committed, forecast and budgeted spend | Must | Define currency and period |
| FR-29 | Forecast | Forecast spend by entity, department, cost centre, destination and category | Must | Show assumptions and confidence |
| FR-30 | Policy insights | Analyse exception patterns, compliance trends and approval bottlenecks | Must | Drill-down by rule / segment |
| FR-31 | Policy recommendations | Surface evidence-based policy review recommendations | Should | Human approval required for changes |
| FR-32 | Forecast monitoring | Track forecast variance and data freshness | Must | Flag low coverage / quality |
