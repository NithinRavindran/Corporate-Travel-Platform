# Workflow: Post-booking Servicing

## Scope

Support authorised users managing an existing confirmed trip, including amendments, cancellations, schedule changes and refund tracking where supported by supplier capability.

## Service request lifecycle

Submitted → Eligibility Check → Supplier Action Pending → Supplier Confirmed / Rejected → Financial Reconciliation Pending → Completed.

## Amendment flow

1. User selects booking and requested change.
2. Platform retrieves applicable supplier terms and eligibility.
3. User reviews price difference, penalties and conditions.
4. Required internal approval is obtained if configured.
5. Request is submitted to supplier.
6. Supplier response and new references are recorded.
7. Itinerary is updated only when change confirmation is received.

## Cancellation / refund flow

1. Retrieve cancellation terms and calculate estimated charges where available.
2. Display the distinction between estimated and final refund.
3. Obtain confirmation from authorised user.
4. Submit cancellation request.
5. Track supplier cancellation confirmation.
6. Track refund status separately from cancellation status.
7. Preserve original and updated booking history.

## Requirements

- Never imply a refund is complete merely because a cancellation request was submitted.
- Preserve the original booking and change timeline.
- Show ownership and next action for unresolved service requests.
- Respect role permissions and supplier-specific restrictions.
