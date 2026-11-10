# Workflow: Multi-city and International Travel

## Purpose

Enable an employee or authorised arranger to plan one business trip that contains multiple destinations, travel legs and related services, including cross-border journeys.

## Trip and leg model

A multi-city trip is represented as one parent trip with ordered legs. Each leg has its own origin, destination, local departure / arrival date and time, time zone, travel mode, supplier reference, booking state and related service requests.

Example structure (illustrative only):

- Trip: Bengaluru → Singapore → London → Bengaluru
- Leg 1: Bengaluru to Singapore
- Stay: Singapore
- Leg 2: Singapore to London
- Stay: London
- Leg 3: London to Bengaluru

The itinerary should not assume that every leg is booked by the same supplier or in one transaction.

## Request creation flow

1. Traveller chooses a single-destination or multi-city trip type.
2. Traveller adds, removes and reorders destinations / travel legs.
3. For each leg, traveller enters origin, destination, date and relevant travel preferences.
4. Platform validates date sequence, impossible overlaps and required segment details.
5. Platform identifies domestic / international legs and applicable destination context.
6. Policy engine evaluates trip-level rules and leg-specific rules.
7. User reviews local times, organisation reporting times, currency context and applicable reminders.
8. Request is submitted to configured approval workflow.

## International travel considerations

- Display departure and arrival times in their respective local time zones.
- Preserve canonical timestamps and the local date / time entered for each leg.
- Handle overnight journeys, daylight-saving transitions and date-line crossings.
- Display supplier currency and organisation reporting currency as separate values.
- Show exchange-rate source and effective date when a conversion is displayed.
- Provide organisation-approved travel document, visa-process and destination reminders; do not present the product as a source of legal or immigration advice.
- Allow country-specific policy and approval rules where configured.
- Provide a way to record required traveller assistance or risk-review steps without exposing sensitive details broadly.

## Policy evaluation

Policy should be evaluated:
- At parent-trip level (e.g. trip budget, duration, international approval).
- At leg level (e.g. cabin, route, advance purchase, destination rules).
- At product level (e.g. hotel rate flexibility, flight fare conditions).

The response should identify which rule applies to which leg and preserve policy version and evaluation timestamp.

## Booking orchestration

- Each component is booked and confirmed according to its supplier workflow.
- Parent-trip status is derived from component states but must not hide a pending or failed component.
- Partial success must be visible; do not show the whole trip as confirmed when a required component is not confirmed.
- Changes to one leg must trigger the required impact review for dependent legs, hotel dates and transfers.
- Revalidate schedules, prices and availability before committing changes.

## Acceptance criteria

- User can add at least two destinations and multiple ordered travel legs to one parent trip.
- Each segment stores local time and time-zone metadata.
- The user can inspect trip-level and segment-level policy outcomes.
- A multi-currency itinerary shows original currency and conversion context.
- Partial booking success is visible at both component and trip level.
- Reordering or changing a leg triggers validation of dependent dates and services.

## Edge cases

- Overnight flight arrives on the next local calendar day.
- Arrival and departure locations use different time zones.
- Daylight-saving transition changes local offset.
- Route crosses the International Date Line.
- A leg is cancelled after a later hotel or transfer is confirmed.
- Supplier returns an unknown outcome for one segment.
- Currency rate is unavailable or stale.
- One segment violates policy while the rest are compliant.

## Product decisions to validate

- Maximum supported number of destinations / legs for the initial release.
- Whether open-jaw and surface segments are supported.
- How travel time and layover duration are calculated and displayed.
- Which exchange-rate source is authoritative for estimates versus accounting.
- Which destination information can be displayed under approved data licensing and governance.
