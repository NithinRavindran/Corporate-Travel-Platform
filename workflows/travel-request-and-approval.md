# Workflow: Travel Request and Approval

## Primary flow

1. Employee or authorised arranger selects traveller(s).
2. User chooses single-destination or multi-city trip type.
3. User enters trip purpose, cost allocation and ordered journey legs with origin, destination, dates and relevant local times.
4. Platform validates required details, date sequence and international context.
5. Platform evaluates policy at trip and segment level.
6. Platform determines whether approval is required.
7. In-policy / auto-approval requests follow configured rules; other requests enter approval queue.
8. Approver reviews trip context, leg-level itinerary, policy outcome, estimated cost and relevant budget context.
9. Approver approves, rejects or requests clarification.
10. Platform records decision, comments, actor and timestamp.
11. Approved request becomes eligible for booking.
12. Booking workflow starts separately and tracks supplier confirmation for each component.
13. Traveller and arranger can monitor the trip on web or mobile.

## Key states

Draft → Submitted → Policy Review → Pending Approval → Approved / Rejected / Returned for Clarification → Ready to Book → Booking In Progress.

A request can be withdrawn or expire subject to configured business rules. Each trip leg and booking component also retains its own status.

## Multi-city and international checks

- Ordered legs and destination sequence are valid.
- Local times and time zones are explicit.
- Overnight and date-line cases are represented correctly.
- Currency context is clear when estimates are shown.
- Policy evaluation identifies trip-level and affected segment-level outcomes.

## Edge cases

- Approver is unavailable.
- Delegate is not eligible or has expired delegation.
- Request changes after approval.
- Dates, traveller list or price change after approval.
- Request violates more than one policy rule.
- Cost centre is inactive.
- Traveller profile is incomplete.
- Multi-city leg dates overlap or connections are not feasible.
- Currency conversion metadata is unavailable.

## Product decisions required

Define approval thresholds, hierarchy precedence, delegation, escalation, expiry, reapproval triggers and whether approval applies to the request, selected itinerary or both.
