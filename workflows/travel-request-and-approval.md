# Workflow: Travel Request and Approval

## Primary flow

1. Employee or authorised arranger selects traveller(s).
2. User enters trip purpose, origin, destination, dates, travel category and cost allocation.
3. Platform validates data and evaluates policy.
4. Platform determines whether approval is required.
5. In-policy / auto-approval requests follow configured rules; other requests enter approval queue.
6. Approver reviews trip context, selected options if available, policy outcome and estimated cost.
7. Approver approves, rejects or requests clarification.
8. Platform records decision, comments, actor and timestamp.
9. Approved request becomes eligible for booking.
10. Booking workflow starts separately and tracks supplier confirmation.

## Key states

Draft → Submitted → Policy Review → Pending Approval → Approved / Rejected / Returned for Clarification → Ready to Book → Booking In Progress.

A request can be withdrawn or expire subject to configured business rules.

## Edge cases

- Approver is unavailable.
- Delegate is not eligible or has expired delegation.
- Request changes after approval.
- Dates or price change after approval.
- Request violates more than one policy rule.
- Cost centre is inactive.
- Traveller profile is incomplete.

## Product decisions required

Define approval thresholds, hierarchy precedence, delegation, escalation, expiry, reapproval triggers and whether approval applies to the request, selected itinerary or both.
