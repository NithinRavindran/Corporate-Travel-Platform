# Acceptance Criteria

## Story: Submit a trip request

**Given** an authenticated employee has permission to request travel  
**When** all configured mandatory trip fields are valid and the request is submitted  
**Then** the platform creates a request reference, records the submitter and timestamp, and evaluates applicable policy rules.

## Story: Display policy result

**Given** a request matches a configured policy rule  
**When** policy evaluation completes  
**Then** the platform displays the policy outcome and the relevant explanation.

**Given** a request violates a policy rule  
**When** the user reviews the result  
**Then** the platform identifies the relevant rule and explains whether an alternative or exception approval is available.

## Story: Route approval

**Given** a request requires approval  
**When** it is submitted  
**Then** it is routed to the configured approver based on the applicable hierarchy and delegation rules.

**Given** an approver rejects a request  
**When** the decision is submitted  
**Then** the platform records the approver, timestamp and reason and notifies authorised request participants.

## Story: Confirm supplier booking

**Given** an approved request has a selected itinerary  
**When** the platform submits a booking request and receives a valid supplier confirmation  
**Then** it records supplier references and updates the booking state according to the agreed confirmation / ticketing rules.

**Given** the supplier response times out  
**When** the booking outcome is unknown  
**Then** the platform displays a pending / unknown state and initiates the defined reconciliation process without blindly creating a duplicate booking.

## Quality checklist

- [ ] Role and permission scenarios
- [ ] Missing and invalid request data
- [ ] Policy boundary and conflicting rule scenarios
- [ ] Delegate and approver absence scenarios
- [ ] Supplier timeout, error and duplicate callback scenarios
- [ ] Price / availability change before booking
- [ ] Partial booking outcome where multiple products are involved
- [ ] Audit history and notification verification
- [ ] Accessibility, privacy and security validation
