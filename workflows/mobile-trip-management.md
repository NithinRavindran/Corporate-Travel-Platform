# Workflow: Mobile Trip Management

## Purpose

Give travellers and authorised arrangers secure access to upcoming trips, itineraries, booking status and supported servicing actions while away from a desktop.

## Primary mobile experience

### Trip overview
- Upcoming and in-progress trips.
- Trip summary with destination, dates and traveller context.
- Overall and component-level booking states.
- Next itinerary event and relevant reminders.

### Itinerary
- Ordered multi-city itinerary.
- Local departure and arrival times with time-zone labels.
- Flight / hotel / transfer references and essential details.
- Supplier confirmation state and last-updated time.
- Relevant support contacts and organisation travel assistance details.

### Actions
- View approval and booking status.
- Open supported change / cancellation request.
- Contact travel operations through approved support channel.
- Access permitted trip documents.
- Review notification and privacy preferences.

## Notification events

Notifications may be generated for:
- Request submitted or returned for clarification.
- Approval decision.
- Booking confirmed, failed or requiring reconciliation.
- Material flight schedule / itinerary change received from an approved source.
- Hotel or transfer status update, where supported.
- Upcoming trip reminder based on organisation configuration.
- Service request status update.

Each notification should deep-link to the relevant trip when the user is authenticated and authorised. Lock-screen content should avoid exposing sensitive personal or itinerary information.

## Low-connectivity behaviour

- Cache only approved essential itinerary fields.
- Encrypt protected local data and apply device/session controls.
- Clearly display last-synchronised timestamp.
- Mark cached supplier status as potentially stale.
- Do not allow an offline action to appear completed before server confirmation.
- Provide explicit refresh / retry behaviour when connectivity returns.
- Define remote logout, cache expiry and data removal behaviour.

## Accessibility and usability

- Support responsive layouts and accessible labels.
- Provide readable time-zone and date information.
- Make status distinguishable without relying on colour alone.
- Support screen readers and adequate touch targets.
- Minimise typing during travel with secure, permission-aware access to known trip details.

## Acceptance criteria

- Authenticated traveller can locate an upcoming trip and view its itinerary.
- Local times and time zones are visible for international legs.
- Traveller can see last-updated time for booking status.
- Permitted service actions are available based on role and supplier capability.
- Notification preferences are respected.
- Sensitive details are not exposed in notification previews by default.
- Offline itinerary clearly indicates cached status and last sync time.
- An offline request is queued or rejected transparently and is not represented as completed until acknowledged by the platform.

## Mobile product metrics

- Eligible trips with mobile trip views.
- Mobile task completion rate for key trip actions.
- Notification delivery and open rate by notification type.
- Failed / delayed notification rate.
- Stale itinerary access rate.
- Mobile support contacts per trip.
- App / page performance and crash rate, where applicable.

## Security and privacy questions

- What information can be cached and for how long?
- Which device security controls are required?
- How are lost devices and revoked sessions handled?
- Can arranger access be granted and revoked independently?
- What data may appear in push notification payloads?
