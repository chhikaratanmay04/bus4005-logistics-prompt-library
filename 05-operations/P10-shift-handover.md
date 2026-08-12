# Prompt 10 – Shift Handover

## Intended Workflow or Task
Create a structured logistics shift handover.

## Problem Being Solved
Unstructured handover notes can hide urgent unfinished work and increase the risk of tasks being missed.

## Version 1
**Prompt:** Summarise these logistics notes for the next shift: [SHIFT NOTES]

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

Shift notes:
[SHIFT NOTES]

## Test Result
The final prompt separated open actions from completed work and made the handover easier for the next shift to act on.

## Automation Potential
**High.** Can standardise handovers from operational notes.

## Risks and Limitations
Missing source notes or incorrect statuses can carry errors into the next shift.

## Mitigation and Human Oversight
Outgoing staff verify the handover before transferring responsibility to the next shift.
