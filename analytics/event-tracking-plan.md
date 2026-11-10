# Event Tracking Plan

## Naming principles
Use consistent past-tense event names, stable identifiers, timestamps and explicit event versioning. Use pseudonymous user identifiers where possible.

| Event | Trigger | Suggested properties |
|---|---|---|
| travel_request_started | User begins a request | request_id, channel, trip_type |
| travel_request_submitted | Valid request submitted | request_id, entity_id, cost_centre_present |
| policy_evaluated | Policy engine completes evaluation | request_id, policy_version, outcome, rule_codes |
| approval_requested | Approval task created | request_id, approver_group |
| approval_decided | Approver records decision | request_id, decision, elapsed_time |
| travel_search_submitted | Search is submitted | search_id, product_type, market |
| travel_option_selected | User selects an option | search_id, supplier_id, product_type |
| booking_submitted | Booking request sent to provider | booking_id, supplier_id, product_type |
| booking_status_changed | Booking state changes | booking_id, old_state, new_state, source |
| service_request_created | Change / cancellation request opened | booking_id, service_type |
| service_request_closed | Service request completed | booking_id, service_type, resolution |

## Privacy controls
Do not include passport numbers, payment card information, sensitive employee details or unnecessary free text in analytics events. Keep operational identifiers in secured systems and use approved pseudonymous keys for analysis.
