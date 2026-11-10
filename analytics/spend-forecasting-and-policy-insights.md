# Advanced Spend Forecasting and Policy Insights

## Purpose

Provide travel managers, finance teams and authorised budget owners with forward-looking visibility into travel spend and explainable insights into policy compliance and operational behaviour.

This capability supports planning and policy review. It does not replace the organisation's finance system of record or automatically alter policy rules.

## Spend categories and views

Present clearly distinguished values:

- **Actual:** posted or reconciled spend from the agreed finance source.
- **Booked / committed:** confirmed supplier reservations and other defined commitments not yet posted as actual.
- **Estimated:** expected amount for a request or trip that is not yet confirmed.
- **Forecast:** modelled future spend for a defined period and scope.
- **Budget:** approved financial allocation from the authoritative budget source.

Avoid adding these values together without agreed rules for overlap and accounting treatment.

## Forecast dimensions

Authorised users should be able to analyse by:
- Organisation entity.
- Department and cost centre.
- Traveller segment or grade where permitted.
- Destination country / region.
- Domestic versus international travel.
- Travel category (air, hotel, ground transport and others).
- Supplier or channel.
- Time period (month, quarter, financial year).
- Project / business purpose where available and authorised.

## Forecast inputs

Potential inputs include:
- Historical actual travel spend.
- Confirmed and committed bookings.
- Submitted / approved requests with estimated value.
- Seasonality and calendar effects.
- Destination and category mix.
- Supplier price trends where licensed and reliable.
- Policy thresholds and known programme changes.
- Budget and cost-centre mapping.

The product should record data source, refresh timestamp, coverage, exclusions, forecast horizon and assumptions.

## Forecast approach

Start with transparent baseline methods before introducing more complex prediction:
1. Establish historical spend baselines by category and segment.
2. Incorporate confirmed and committed booking values.
3. Add approved and open request estimates with clear probability / status treatment.
4. Apply seasonality or trend methods only when historical coverage supports them.
5. Compare forecast against realised actuals at a fixed horizon.
6. Show confidence intervals or data-quality indicators where methodologically appropriate.
7. Record model / methodology version and refresh timestamp.

Do not present a forecast as certain or as a financial commitment.

## Policy insights

Provide explainable views for:
- Policy compliance by rule, category, entity and period.
- Most frequent exception reasons.
- Out-of-policy selection and approval outcomes.
- Advance-purchase behaviour.
- Cabin / hotel category patterns against configured rules.
- Preferred supplier utilisation.
- Approval turnaround and bottleneck stages.
- Booking and cancellation behaviour that may affect spend.
- Repeated supplier or route cost differences where comparisons are valid.

## Insight-to-action workflow

1. User selects reporting scope and period.
2. Platform displays trends and identifies a notable pattern.
3. User opens the insight to see underlying rule, segment, denominator and sample size.
4. Platform distinguishes observed data from suggested interpretation.
5. Travel manager / policy owner reviews the context.
6. Authorised owner records a decision: no action, investigate, pilot policy change or update policy.
7. Policy configuration changes follow the normal approval, testing and versioning process.

## Product requirements

- Actual, committed, estimated, forecast and budget amounts are clearly labelled.
- Currency and exchange-rate basis are visible.
- Users can drill down from summary to the permitted underlying breakdown.
- Forecast shows horizon, refresh time, coverage and assumptions.
- Forecast accuracy is measured against realised actuals at consistent horizons.
- Policy insight shows numerator, denominator, period and applicable rule version.
- Small samples and incomplete data are flagged.
- No policy changes are made automatically based on an insight.

## Metrics

| Metric | Definition concept |
|---|---|
| Forecast variance | Forecast minus actual for the same scope and period |
| Forecast accuracy | Error using an agreed metric and fixed forecast horizon |
| Forecast bias | Systematic tendency to over- or under-forecast |
| Budget variance | Actual plus defined commitments minus approved budget |
| Data coverage | Share of spend / bookings mapped to the required reporting dimensions |
| Policy compliance | Eligible bookings satisfying applicable policy rules / eligible bookings |
| Exception concentration | Share of exceptions attributable to a rule, category or segment |
| Insight action rate | Reviewed insights resulting in a recorded decision / reviewed insights |

## Risks and controls

- Poor or delayed finance data can distort forecasts.
- Double counting actual and committed amounts can materially overstate exposure.
- Unstable exchange rates can make currency comparisons misleading.
- Small segments can create misleading policy conclusions.
- Forecasts can inherit historical bias.
- Policy insight must not become automatic employee surveillance or opaque scoring.
- Access to spend data must follow entity, role and financial confidentiality rules.

## Acceptance criteria

- Finance user can compare actual, committed, forecast and budget for a selected period.
- Forecast filters work across permitted entity, cost centre, destination and category dimensions.
- Forecast displays source freshness, horizon and assumptions.
- Low data coverage is flagged.
- Forecast accuracy can be evaluated against actuals after the period closes.
- Policy insights explain the underlying rule and sample size.
- Users can record a policy review decision, while actual policy changes require the approved policy governance workflow.
