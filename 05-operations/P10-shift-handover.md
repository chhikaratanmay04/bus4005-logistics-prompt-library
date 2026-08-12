# Prompt 10 – Shift Handover

## Intended Workflow or Task
Create a structured logistics shift handover.

## Problem Being Solved
Unstructured handover notes can hide urgent unfinished work and increase the risk of tasks being missed.

## Version 1
**Prompt:** Summarise these logistics notes for the next shift.

**Issue:** Completed and outstanding work were mixed together and priority actions were not obvious.

## Final Version – v1.1
### Prompt Text
You are an operations assistant for a last-mile logistics company.

Create a concise shift handover using only the notes provided.

Organise the information under these headings:
1. High-priority outstanding actions
2. Delayed shipments
3. Failed deliveries and redeliveries
4. Damaged goods or warehouse issues
5. Customer follow-ups
6. Completed items
7. Missing information requiring confirmation

For each active item, include the shipment or incident ID if provided, current status, action already taken and next required action.

Do not create deadlines, causes, responsibilities or customer commitments that are not provided.

## Example Input
SP610 delayed 45 minutes; new ETA 6:00 pm; customer notified.  
SP611 delivery failed because customer was unavailable; redelivery pending.  
WH-14 damaged carton isolated in warehouse; supervisor review pending.  
SP612 delivered successfully.

## ChatGPT Test Evidence
### Version 1 Output
Shift handover: SP610 is delayed by 45 minutes with a new ETA of 6:00 pm and the customer has been notified. SP611 was not delivered because the customer was unavailable and redelivery is pending. WH-14 is a damaged carton that has been isolated in the warehouse and is waiting for supervisor review. SP612 was delivered successfully.

**Issues & Limitations – Version 1:** Open actions, completed work and follow-ups were mixed in one paragraph, making priorities harder to scan.

### Final Version v1.1 Output
1. **High-priority outstanding actions**
   - No item is explicitly marked as high priority in the notes.

2. **Delayed shipments**
   - **SP610** – Current status: delayed by 45 minutes; new ETA 6:00 pm. Action already taken: customer notified. Next required action: Not provided.

3. **Failed deliveries and redeliveries**
   - **SP611** – Current status: delivery failed because customer was unavailable. Action already taken: Not provided. Next required action: Redelivery pending.

4. **Damaged goods or warehouse issues**
   - **WH-14** – Current status: damaged carton isolated in warehouse. Action already taken: carton isolated. Next required action: Supervisor review pending.

5. **Customer follow-ups**
   - **SP610** – Customer has already been notified.
   - **SP611** – Customer follow-up information not provided.

6. **Completed items**
   - **SP612** – Delivered successfully.

7. **Missing information requiring confirmation**
   - SP610: next required action not provided.
   - SP611: redelivery timing and action already taken are not provided.
   - WH-14: supervisor review timing/person is not provided.

**Improvements – Final v1.1:** Separated open, completed and missing-information sections, making the handover clearer and more actionable.

### Comparison
Version 1 accurately summarised the notes but mixed completed work, open issues and follow-up requirements in one paragraph. Version 1.1 separated delayed shipments, failed deliveries, warehouse damage, completed work and missing information. It also avoided inventing a priority, deadline or responsible person. The improved output is easier for the incoming shift to scan and action.

## Test Result
The final prompt separated open actions from completed work and made the handover easier for the next shift to act on.

## Automation Potential
**High.** Can standardise handovers from operational notes.

## Risks and Limitations
Missing source notes or incorrect statuses can carry errors into the next shift.

## Mitigation and Human Oversight
Outgoing staff verify the handover before transferring responsibility to the next shift.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general summarisation prompt without separating open actions, completed items or missing information. | The output accurately described the notes but combined delays, failed delivery, warehouse damage and completed work in one paragraph. | Summarisation alone does not guarantee an operationally useful handover because important unfinished work can remain difficult to scan. |
| Final v1.1 | Added seven workflow headings, required status/action/next-action fields and prohibited invented deadlines, responsibilities or commitments. | Open issues, completed work and missing information were clearly separated, and the model avoided creating unsupported priorities or owners. | Workflow-specific structure turns unstructured notes into a more actionable handover while human verification remains necessary before responsibility is transferred. |
