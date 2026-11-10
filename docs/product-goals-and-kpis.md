# Product Goals and KPIs

Targets should be set only after baseline measurement, segmentation and agreement on data definitions.

| Goal | Candidate KPI | Definition / notes |
|---|---|---|
| Improve request completion | Request completion rate | Complete valid requests / requests started |
| Improve approval flow | Approval turnaround time | Time from submission to final decision; report median and percentiles |
| Improve policy clarity | Policy exception rate | Requests requiring exception / eligible requests, segmented by rule |
| Improve booking reliability | Booking success rate | Supplier-confirmed bookings / eligible booking attempts |
| Improve traveller experience | Post-trip satisfaction | Survey score with response-rate context |
| Improve servicing | Time to resolve service request | Time from accepted case to resolution |
| Improve finance readiness | Cost allocation completeness | Confirmed bookings with valid required cost allocation / confirmed bookings |
| Improve operational efficiency | Support contacts per trip | Relevant support contacts / completed trips |

## Guardrail metrics

- Duplicate booking and duplicate charge incidents.
- Unconfirmed bookings incorrectly displayed as confirmed.
- Out-of-policy bookings without the required approval.
- Refund and cancellation exceptions.
- Supplier timeout and error rates.
- Privacy, permission and audit incidents.
- Traveller satisfaction and accessibility issues.

## Measurement principles

- Define event names and eligibility before comparing periods.
- Segment by channel, entity, geography, travel category and booking provider where appropriate.
- Separate platform-controlled time from supplier-controlled time.
- Avoid using a single average when distributions are skewed.
- Do not optimise approval speed at the expense of policy quality or booking reliability.
