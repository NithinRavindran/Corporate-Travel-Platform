# Approval Rules — Example Scenarios

These examples illustrate rule design only. Actual approval thresholds and authority must be configured and approved by each corporate customer.

| Scenario | Illustrative rule outcome | Workflow expectation |
|---|---|---|
| Request meets standard policy and configured threshold | May be auto-approved if permitted | Record policy version and auto-decision |
| Request exceeds configured cabin / hotel cap | Exception approval required | Show rule reason and route to authorised approver |
| International trip requires additional review | Additional approval may apply | Route through configured hierarchy |
| Request includes multiple travellers | Apply rules per traveller and request aggregation rule | Avoid inconsistent partial decisions |
| Request changes after approval | Re-evaluate affected rules | Reapproval where configured |
| Approver unavailable | Valid delegate / escalation rule | Preserve delegation history |
| Cost centre inactive | Block submission or route to correction | Do not silently allocate to a default |

## Design questions
- Are approvals sequential or parallel?
- Which rules take precedence when more than one applies?
- Does a price change require reapproval?
- Does a traveller change invalidate approval?
- How are expired approvals handled?
- What is the audit requirement for automated decisions?
