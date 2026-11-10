# Workflow: Booking and Approval Exception Handling

| Exception | Expected product response | Operational control |
|---|---|---|
| Missing trip details | Highlight required fields and block invalid submission | Record validation reason |
| Policy cannot be evaluated | Explain missing / invalid policy inputs | Route to authorised admin if unresolved |
| Approver unavailable | Apply configured delegate / escalation rule | Preserve routing history |
| Supplier timeout | Display pending / unknown outcome | Reconcile before retry |
| Price changed | Show revised total and conditions | Obtain user acceptance where required |
| Inventory unavailable | Offer refreshed options | Do not create false confirmation |
| Duplicate supplier callback | Avoid duplicate booking update | Retain event and processing audit |
| Partial service booking | Show component-level states | Apply defined recovery / operations process |
| Cancellation rejected | Explain supplier response and available next step | Assign service case owner |
| Refund delayed | Show refund pending separately | Track provider / finance follow-up |

## Exception record

Each exception should capture:
- Unique reference.
- Related request / trip / booking.
- Category and severity.
- Source system and correlation ID.
- Current owner and next action.
- Created / updated timestamps.
- Resolution and audit history.
