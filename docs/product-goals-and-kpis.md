# Product Goals and KPIs

Targets should be set only after baseline measurement, segmentation and agreement on data definitions.

| Goal | Candidate KPI | Definition / notes |
|---|---|---|
| Improve request completion | Request completion rate | Complete valid requests / requests started |
| Support complex travel | Multi-city trip completion | Multi-city trips with all required components confirmed / eligible multi-city trips |
| Improve international readiness | International request completion | Valid international requests submitted / international requests started |
| Improve approval flow | Approval turnaround time | Time from submission to final decision; report median and percentiles |
| Improve policy clarity | Policy exception rate | Requests requiring exception / eligible requests, segmented by rule |
| Improve booking reliability | Booking success rate | Supplier-confirmed bookings / eligible booking attempts |
| Improve mobile experience | Mobile trip engagement | Eligible trips with meaningful mobile trip actions / eligible trips |
| Improve mobile communication | Notification delivery rate | Delivered notifications / eligible notification attempts |
| Improve traveller experience | Post-trip satisfaction | Survey score with response-rate context |
| Improve servicing | Time to resolve service request | Time from accepted case to resolution |
| Improve finance readiness | Cost allocation completeness | Confirmed bookings with valid required allocation / confirmed bookings |
| Improve spend visibility | Forecast variance | Forecast versus actual spend for fixed scope and horizon |
| Improve forecast quality | Forecast accuracy | Error versus actual using an agreed method and horizon |
| Improve policy governance | Policy compliance rate | Eligible bookings meeting applicable policy / eligible bookings |
| Improve operational efficiency | Support contacts per trip | Relevant support contacts / completed trips |

## Guardrail metrics

- Duplicate booking and duplicate charge incidents.
- Unconfirmed bookings incorrectly displayed as confirmed.
- Out-of-policy bookings without the required approval.
- Refund and cancellation exceptions.
- Supplier timeout and error rates.
- Privacy, permission and audit incidents.
- Forecast bias, missing data and confidence coverage.
- Mobile notification failures and stale itinerary exposure.
- Traveller satisfaction and accessibility issues.

## Measurement principles

- Define events and eligibility before comparing periods.
- Segment by channel, entity, geography, travel category and booking provider.
- Separate platform-controlled time from supplier-controlled time.
- Distinguish actual, committed, forecast and budgeted amounts.
- Specify base currency and conversion rate date.
- Fix forecast horizon and measure accuracy against realised actuals.
- Avoid using a single average when distributions are skewed.
- Do not optimise approval speed at the expense of policy quality or booking reliability.
