# Workflow: Trip Management

## Purpose

Give travellers and authorised arrangers a single view of a business trip and its related destinations, travel legs, reservations, documents, status updates and service requests across web and mobile.

## Trip workspace

A trip may contain:
- Traveller and trip purpose.
- One or more ordered destinations and travel legs.
- Local departure / arrival dates, times and time zones.
- One or more flight reservations.
- Hotel reservation(s) for relevant cities.
- Ground transport or other supported services.
- Local currency and organisation reporting currency context.
- Approval and policy history at trip and segment level.
- Booking references and supplier status for each component.
- Change, cancellation and support requests.
- Approved travel reminders and traveller assistance information.

## Core user journey

1. Open trip using an authorised account on web or supported mobile device.
2. Review trip summary and ordered itinerary legs.
3. View local dates, times, time zones, supplier references and relevant booking terms.
4. Review component-level booking, ticketing and service status.
5. Access permitted support and servicing actions.
6. Submit an eligible change or cancellation request.
7. Receive status updates as supplier outcomes are confirmed.
8. Review final trip, service and notification history.

## Multi-city and international requirements

- A parent trip contains multiple ordered legs and destinations.
- Each leg retains its own dates, local times, time zone, supplier and booking references.
- Overnight connections and date-boundary changes are represented clearly.
- Trip-level status must not hide a failed or pending leg.
- Currency conversion is labelled with base currency, rate date and source where available.
- Policy evaluation can produce both trip-level and segment-level outcomes.

## Mobile requirements

- Present an at-a-glance upcoming trip list and trip timeline.
- Show essential itinerary, booking references, confirmation state and relevant contacts.
- Allow supported service requests from the trip view.
- Deliver configurable alerts for approval, confirmation and material itinerary changes.
- Clearly label last-synchronised time for cached information.
- Apply authentication, device/session controls and role-aware visibility.
- Secure offline access is limited to approved essential fields and must not imply live supplier status.

## Exceptions

- One component is confirmed while another remains pending.
- A traveller changes after booking.
- Supplier schedule changes across time zones.
- A reservation is cancelled but refund remains pending.
- A trip is split, combined or re-associated by an authorised operations user.
- Mobile device is offline or notification permission is disabled.
- Cached itinerary is stale and must be refreshed before a live action.
