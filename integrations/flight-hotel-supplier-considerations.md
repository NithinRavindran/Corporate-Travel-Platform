# Flight and Hotel Supplier Considerations

## Flights

Product requirements should clarify:
- Search input and passenger / traveller constraints.
- Fare families, cabin, baggage and ancillary content.
- Fare rules and change / cancellation terms.
- Price and availability revalidation.
- Reservation, PNR and ticketing states.
- Schedule changes, voids, exchanges and refunds.
- GDS, NDC or direct-connect source attribution where relevant.

## Hotels

Product requirements should clarify:
- Property, room, occupancy and guest details.
- Rate plan, meal plan, taxes and inclusions.
- Cancellation deadline and penalty.
- Guarantee / payment conditions.
- Availability and rate revalidation.
- Reservation confirmation and supplier reference.
- Modification, cancellation and refund status.

## Shared integration requirements

- Supplier-specific error and status mapping.
- Request correlation and audit references.
- Timeout and retry behaviour.
- Idempotency and duplicate callback protection.
- Rate limits and availability freshness.
- Reconciliation for unknown booking outcomes.
- Operational ownership and supplier escalation.

## Product design principle

Normalise the comparison experience where it helps users, but do not hide supplier-specific rules or commercial conditions that materially affect the traveller or organisation.
