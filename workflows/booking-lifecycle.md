# Workflow: Booking Lifecycle

## Important distinction

A corporate travel request may be approved before any supplier reservation exists. **Approval is not booking confirmation.** The product must represent request workflow and supplier booking workflow separately.

## Representative booking states

| State | Meaning |
|---|---|
| Ready to Book | Required internal approval is complete |
| Price / Availability Check | Supplier data is being revalidated |
| Booking Submitted | Request has been sent to supplier |
| Pending Supplier Response | Outcome is not yet confirmed |
| Confirmed | Required supplier confirmation condition is met |
| Ticketing Pending | Flight reservation exists but ticket issuance is incomplete, where applicable |
| Ticketed | Ticket issuance is confirmed, where applicable |
| Failed | Supplier rejected or booking failed with known outcome |
| Unknown / Reconciliation Required | Request outcome cannot yet be determined |
| Cancelled | Cancellation is confirmed according to supplier rules |

## Booking flow

1. Retrieve selected offer and its validity conditions.
2. Revalidate price, inventory and rules.
3. Present any material price or condition change for user acceptance.
4. Submit booking with an idempotency strategy where supported.
5. Persist request and supplier correlation references.
6. Process synchronous response or asynchronous callback.
7. Map supplier state to platform state without losing original details.
8. Reconcile unknown outcomes before any retry that could create a duplicate.
9. Notify authorised users of meaningful state changes.

## Product requirements

- Maintain booking timeline and source references.
- Record timestamps and status-change actors.
- Handle duplicate callbacks idempotently.
- Make supplier-specific ticketing requirements clear.
- Do not show unconfirmed requests as confirmed.
- Support manual operations review for unresolved states.
