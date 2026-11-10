# Event Tracking Plan

## Naming principles

Use consistent past-tense event names, stable identifiers, timestamps and explicit event versioning. Use pseudonymous user identifiers where possible.

| Event | Trigger | Suggested properties |
|---|---|---|
| travel_request_started | User begins a request | request_id, channel, trip_type |
| trip_leg_added | User adds a destination / leg | trip_id, leg_id, leg_sequence, domestic_international |
| travel_request_submitted | Valid request submitted | request_id, entity_id, cost_centre_present, leg_count |
| policy_evaluated | Policy engine completes evaluation | request_id, policy_version, outcome, rule_codes, affected_leg_ids |
| approval_requested | Approval task created | request_id, approver_group |
| approval_decided | Approver records decision | request_id, decision, elapsed_time |
| travel_search_submitted | Search is submitted | search_id, product_type, market, leg_id |
| travel_option_selected | User selects an option | search_id, supplier_id, product_type, leg_id |
| booking_submitted | Booking request sent to provider | booking_id, supplier_id, product_type |
| booking_status_changed | Booking state changes | booking_id, old_state, new_state, source |
| mobile_trip_viewed | Traveller opens trip on mobile | trip_id, app_version, cached_or_live |
| mobile_service_action_started | Traveller starts supported service action | trip_id, service_type, channel |
| mobile_notification_sent | Push / in-app notification submitted | notification_type, platform, trip_id |
| mobile_notification_delivered | Delivery receipt received where supported | notification_type, platform |
| itinerary_cache_viewed | User opens cached itinerary | trip_id, cache_age_bucket, last_sync_bucket |
| service_request_created | Change / cancellation request opened | booking_id, service_type |
| service_request_closed | Service request completed | booking_id, service_type, resolution |
| spend_forecast_generated | Forecast is refreshed | forecast_id, scope_type, horizon, currency, method_version |
| spend_forecast_viewed | User views forecast | forecast_id, scope_type, period, role |
| policy_insight_viewed | User opens a policy insight | insight_type, rule_code, period, segment_type |
| policy_review_decision_recorded | Owner records an insight decision | insight_type, decision_type, policy_version |

## Event governance

- Define event owner, schema version and data-quality checks.
- Use stable internal identifiers and avoid raw personal identifiers in analytics.
- Record currency, period and forecast horizon as explicit dimensions.
- Ensure mobile events distinguish cached information from live server responses.
- Use consistent leg and parent-trip references for multi-city analysis.

## Privacy controls

Do not include passport numbers, payment card information, sensitive employee details, device identifiers beyond approved pseudonymous use, precise personal location or unnecessary free text in analytics events. Keep operational identifiers in secured systems and use approved pseudonymous keys for analysis.
