# Workflow: Corporate Travel Policy Engine

## Purpose

Evaluate trip and travel-product attributes against organisation rules and explain the resulting policy status to users and approvers. Policy evaluation supports single-city, multi-city, domestic and international itineraries.

## Example rule dimensions

- Organisation entity and department.
- Traveller role, grade or employee category.
- Origin, destination, country and domestic / international classification.
- Trip dates, duration, advance-purchase window and time-zone context.
- Trip-level destination count, duration and budget.
- Leg-level route, cabin, connection and overnight conditions.
- Travel category and cabin / room type.
- Fare / rate flexibility and cancellation terms.
- Price threshold, budget availability or preferred supplier.
- Required approval authority.
- International destination reminders or additional review steps configured by the organisation.

Actual rules must be supplied and approved by each organisation. Destination reminders must use approved information and must not be presented as legal or immigration advice.

## Evaluation flow

1. Resolve traveller and organisation context.
2. Resolve policy version effective for the trip.
3. Validate parent-trip attributes and ordered itinerary legs.
4. Resolve country, local date / time and relevant travel category for each leg.
5. Evaluate trip-level and segment-level rules using documented precedence.
6. Produce outcome: In Policy, Out of Policy, Approval Required or Unable to Evaluate.
7. Return explanation codes, affected rule(s) and leg(s).
8. Record policy version and evaluation timestamp.
9. Route for approval or allow the next permitted action.
10. Re-evaluate when material trip details change, following configured reapproval rules.

## Rule governance

- Version every policy.
- Define effective date and expiry.
- Identify rule owner and approver.
- Test changes against representative domestic, international and multi-city scenarios.
- Log publication and rollback.
- Prevent ambiguous conflicting rules or provide deterministic precedence.
- Use insight reports to inform review, but never silently modify active policy rules.

## Acceptance expectations

- Same input and policy version produce consistent result.
- Missing data returns an explicit unable-to-evaluate state, not a false compliant result.
- User-facing explanations do not expose restricted internal policy configuration.
- A leg-level exception identifies the affected leg and rule.
- Policy updates do not silently change the historic evaluation record of an existing request.
- Insight-driven policy changes follow the same approval and versioning governance as manual changes.
