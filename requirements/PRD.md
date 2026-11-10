# Product Requirements Document: Corporate Travel Request-to-Booking

**Status:** Portfolio sample — draft  
**Product area:** Corporate travel platform  
**Primary journey:** Trip request, policy validation, approval and booking

## 1. Summary

Provide an integrated corporate travel journey in which an employee or authorised arranger can create a trip request, understand policy outcomes, obtain required approval, search supported travel inventory and track supplier booking status.

## 2. Problem

Travel requests, policy checks, approvals and supplier booking confirmation may be spread across separate tools and manual hand-offs. The product should improve clarity, traceability and operational visibility.

## 3. Goals

- Make trip requests complete and understandable.
- Apply configured policy rules consistently.
- Route approval requests to the correct decision-maker.
- Distinguish approved travel requests from supplier-confirmed bookings.
- Provide traceable booking and post-booking status.

## 4. Non-goals

- Replacing an enterprise expense or ERP platform.
- Guaranteeing supplier availability or price.
- Supporting every supplier or country in the first release.
- Automatically approving exceptions without configured authority.

## 5. Users

Employee / traveller, travel arranger, approver, corporate administrator, travel operations agent and finance analyst.

## 6. MVP scope

1. User identity, roles and traveller profile.
2. Trip request creation and validation.
3. Configurable policy evaluation.
4. Approval workflow and decision history.
5. Flight and hotel search through selected suppliers.
6. Price / availability revalidation.
7. Booking submission and supplier status.
8. Itinerary view and operational exception visibility.

## 7. Functional requirements

See [functional requirements](functional-requirements.md), [user stories](user-stories.md) and [acceptance criteria](acceptance-criteria.md).

## 8. Key business rules

- Policy must be evaluated using the correct organisation, entity, traveller role, destination, trip dates and travel category.
- Approval of a trip request does not equal supplier booking confirmation.
- A booking must not be displayed as confirmed until the required supplier confirmation / ticketing condition is met.
- Out-of-policy requests must capture a reason and follow configured approval authority.
- Changes and cancellations must respect supplier fare / rate terms and retain an audit history.

## 9. Integrations

Identity / HR, flight content and booking providers, hotel suppliers, payment or central billing where applicable, expense / ERP and notification services.

## 10. Non-functional requirements

Security, privacy, availability, performance, accessibility, auditability, observability, data retention and recoverability must be defined with engineering and enterprise stakeholders.

## 11. Analytics

Track request completion, policy exceptions, approval turnaround, search-to-book conversion, booking success, supplier errors, servicing resolution time and cost allocation completeness.

## 12. Risks and dependencies

See [risk register](../governance/risk-register.md). Key dependencies include policy ownership, identity data quality, supplier contracts, provider API capabilities and finance data definitions.

## 13. Release approach

Pilot with a limited business unit, defined travel categories and selected suppliers. Validate policy outcomes, booking reconciliation and support readiness before expanding.
