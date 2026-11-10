# Product Risk Register

| Risk | Potential impact | Mitigation / response | Owner |
|---|---|---|---|
| Incorrect policy configuration | Unauthorised or unnecessarily blocked travel | Versioning, test scenarios, policy owner approval | Corporate admin |
| Incorrect approval routing | Delayed or invalid decisions | Explicit hierarchy, delegation rules and audit trail | Business owner |
| Supplier timeout / unknown outcome | Duplicate booking or uncertainty | Idempotency and reconciliation process | Engineering / operations |
| Price or availability changes | User dissatisfaction and cost variation | Revalidation and renewed user acceptance | Product / supplier ops |
| Traveller data exposure | Privacy and trust impact | Least privilege, minimisation, retention controls | Security / privacy |
| Missing cost allocation | Finance reconciliation gaps | Required-field validation and reference-data sync | Finance |
| Provider API change | Booking disruption | Version monitoring, contract tests and change process | Integration owner |
| Unclear refund status | Customer confusion and support demand | Separate cancellation and refund states | Travel operations |
| Poor metric definitions | Misleading business decisions | Metric owner, denominator and source documentation | Product analytics |

## Review cadence
Review risks during discovery, release planning and operational reviews. Record likelihood, impact, residual risk and evidence for each risk in the active delivery context.
