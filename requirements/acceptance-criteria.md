# Acceptance Criteria

## Story: Submit a trip request

**Given** an authenticated employee has permission to request travel  
**When** all configured mandatory trip fields are valid and the request is submitted  
**Then** the platform creates a request reference, records the submitter and timestamp, and evaluates applicable policy rules.

## Story: Create a multi-city international trip

**Given** a traveller is creating a trip with more than one destination  
**When** the traveller adds ordered travel legs with dates, local times and destination details  
**Then** the platform maintains one parent trip with independently identifiable segments and validates date / time sequence, required details and applicable policy at trip and leg level.

**Given** a trip crosses time zones or the International Date Line  
**When** itinerary times are displayed  
**Then** each time is labelled with its relevant local time zone and the platform preserves the correct underlying timestamp and travel date.

**Given** trip costs are displayed in a local currency and organisation base currency  
**When** currency conversion is shown  
**Then** the platform identifies the rate date and source where available and retains supplier / transaction currency for reconciliation.

## Story: Display policy result

**Given** a request matches a configured policy rule  
**When** policy evaluation completes  
**Then** the platform displays the policy outcome and relevant explanation.

**Given** a multi-leg itinerary has one out-of-policy segment  
**When** policy evaluation completes  
**Then** the affected segment, rule and available exception path are identified without obscuring compliant segments.

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
**Then** the platform displays a pending / unknown state and initiates reconciliation without blindly creating a duplicate booking.

## Story: Manage a trip on mobile

**Given** an authenticated traveller opens an upcoming trip on a supported mobile device  
**When** the trip workspace loads  
**Then** the traveller can review itinerary segments, booking references, status and available service actions permitted by their role.

**Given** a material booking or schedule update is received  
**When** notifications are enabled for the traveller  
**Then** the platform sends an appropriately protected alert and opens the relevant trip detail when selected.

**Given** the device has limited connectivity  
**When** the traveller accesses an itinerary that is eligible for secure offline access  
**Then** only approved essential information is shown from protected local storage, with its last-synchronised time and no claim that live status is current.

## Story: Review spend forecasts and policy insights

**Given** authorised finance or travel management users open spend analytics  
**When** they select an entity, cost centre, period or travel category  
**Then** the platform presents actual, booked / committed, forecast and budget values with clear definitions and currency context.

**Given** forecast data has limited history or incomplete source coverage  
**When** a forecast is displayed  
**Then** the platform shows the data limitation and confidence indicator rather than presenting the estimate as certain.

**Given** policy insights identify recurring exceptions  
**When** an authorised administrator reviews the insight  
**Then** the platform shows the underlying rule, period, segment and supporting data; no policy configuration is changed automatically.

## Quality checklist

- [ ] Role and permission scenarios
- [ ] Missing and invalid request data
- [ ] Policy boundary and conflicting rule scenarios
- [ ] Delegate and approver absence scenarios
- [ ] Multi-city sequencing and leg-level policy scenarios
- [ ] Time-zone, overnight and date-boundary scenarios
- [ ] Currency conversion and reconciliation scenarios
- [ ] Supplier timeout, error and duplicate callback scenarios
- [ ] Price / availability change before booking
- [ ] Partial booking outcome where multiple components are involved
- [ ] Mobile notification permissions and secure offline behaviour
- [ ] Spend forecast data coverage, variance and confidence scenarios
- [ ] Audit history, accessibility, privacy and security validation
