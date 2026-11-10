# Corporate Travel Product Metrics Catalogue

Metrics below are candidate definitions. Agree final denominator, eligibility, business calendar, channel, currency basis and ownership before reporting.

| Metric | Candidate definition | Segmentation |
|---|---|---|
| Request completion rate | Valid submitted requests / requests started | Entity, department, user role |
| Approval turnaround | Time from submission to final decision | Approver group, request type |
| Policy exception rate | Requests requiring exception / policy-evaluated requests | Rule, category, entity |
| Search-to-book conversion | Confirmed bookings / eligible searches | Channel, category, market |
| Booking success rate | Supplier-confirmed bookings / valid booking submissions | Supplier, product, channel |
| Unknown booking outcome rate | Requests requiring reconciliation / booking submissions | Provider, product |
| Multi-city trip completion | Trips with all required components confirmed / eligible multi-city trips submitted | Number of legs, market |
| International trip request completion | Valid international requests submitted / international requests started | Destination region, entity |
| Cost allocation completeness | Confirmed bookings with valid required allocation / confirmed bookings | Entity, department |
| Servicing resolution time | Time from accepted service request to closure | Request type, supplier |
| Support contacts per trip | Relevant support contacts / completed trips | Channel, travel category |
| Mobile trip engagement | Eligible trips with a meaningful mobile trip action / eligible trips | Device, traveller segment |
| Mobile notification delivery | Delivered notifications / eligible notification attempts | Notification type, platform |
| Traveller satisfaction | Post-trip survey result with response-rate context | Trip type, entity |
| Forecast variance | Forecast amount versus actual spend for a defined period and scope | Entity, cost centre, category |
| Forecast accuracy | Error between forecast and actual using an agreed method and horizon | Forecast horizon, segment |
| Budget variance | Actual + committed spend minus budget | Entity, department, period |
| Policy compliance rate | Bookings meeting applicable policy / eligible bookings | Rule, category, entity |
| Approval bottleneck time | Time spent in each approval stage | Approver group, request type |

## Guardrails

- Duplicate booking / charge incidents.
- Supplier-confirmation mismatch.
- Unapproved out-of-policy booking rate.
- Cancellation and refund exception rate.
- Privacy / access incidents.
- Traveller satisfaction and accessibility.
- Forecast bias, data coverage and outlier sensitivity.
- Mobile notification failure and stale offline itinerary exposure.

## Measurement notes

- Distinguish actual, booked / committed, forecast and budget amounts.
- Specify the currency conversion basis and rate date.
- Forecast accuracy is meaningful only with a fixed forecast horizon and sufficient actuals.
- Segment mobile activity by eligible trips and supported devices.
- Do not compare policy compliance across organisations without accounting for policy differences.
