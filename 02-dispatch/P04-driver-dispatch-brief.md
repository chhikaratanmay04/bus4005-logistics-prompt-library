# Prompt 4 – Driver Dispatch Brief

## Intended Workflow or Task
Create a clear driver-facing dispatch brief.

## Problem Being Solved
Drivers may receive long or inconsistent dispatch notes with critical instructions buried in text.

## Version 1
**Prompt:** Create a driver brief from these delivery details: [DELIVERY DETAILS]

**Issue:** Important facts could be buried in prose and missing details were not flagged.

## Final Version – v1.1
### Prompt Text
You are a dispatch assistant for a last-mile logistics company.

Create a concise driver dispatch brief using only the confirmed details provided.

Use these headings:
- Shipment ID
- Driver ID
- Pickup location
- Pickup time
- Delivery location
- Delivery deadline
- Packages and weight
- Special handling
- Pickup instructions
- Customer instructions
- Missing information

If a field is not provided, write **“Not provided”.**

Do not create routes, travel times, access instructions or customer details that are not supplied.

Delivery details:
[DELIVERY DETAILS]

## Test Result
The improved prompt generated a scannable driver brief with consistent headings and no invented route information.

## Automation Potential
**High.** Can convert approved dispatch records into standard driver instructions.

## Risks and Limitations
Incorrect source data will still produce an incorrect brief.

## Mitigation and Human Oversight
Dispatch staff verify the brief before release to the driver.
