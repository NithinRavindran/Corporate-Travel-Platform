# Workflow: Trip Management

## Purpose

Give travellers and authorised arrangers a single view of a business trip and its related reservations, documents, status updates and service requests.

## Trip workspace

A trip may contain:
- Traveller and trip purpose.
- Origin, destination and travel dates.
- One or more flight reservations.
- Hotel reservation(s).
- Ground transport or other supported services.
- Approval and policy history.
- Booking references and supplier status.
- Change, cancellation and support requests.

## Core user journey

1. Open trip using an authorised account.
2. Review itinerary and component status.
3. View supplier references and relevant booking terms.
4. Access available support and servicing actions.
5. Submit an eligible change or cancellation request.
6. Receive status updates as supplier outcomes are confirmed.
7. Review final trip and servicing history.

## Requirements

- A trip can contain multiple travel components with independent booking states.
- Trip-level status must not hide a failed or pending component.
- Changes to one component must not silently overwrite another component.
- Itinerary updates should follow confirmed supplier changes.
- Access must respect traveller, arranger and administrator permissions.
- Documents and personal travel information must be stored and exposed according to policy.

## Exceptions

- One component is confirmed while another remains pending.
- A traveller changes after booking.
- Supplier schedule changes.
- A reservation is cancelled but refund remains pending.
- A trip is split, combined or re-associated by an authorised operations user.
