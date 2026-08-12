# Prompt 4 – Driver Dispatch Brief

## Intended Workflow or Task
Create a clear driver-facing dispatch brief.

## Problem Being Solved
Drivers may receive long or inconsistent dispatch notes with critical instructions buried in text.

## Version 1
**Prompt:** Create a driver brief from these delivery details.

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

## Example Input
Shipment ID: SP421  
Driver ID: D17  
Pickup: Port Melbourne warehouse  
Delivery: Carlton  
Pickup time: 10:30 am  
Delivery deadline: 2:00 pm  
Packages: 4 boxes  
Weight: 32 kg  
Handling: Fragile glass items  
Customer instruction: Call before arrival  
Pickup instruction: Use loading dock B

## ChatGPT Test Evidence
### Version 1 Output
Driver D17 should collect shipment SP421 from Port Melbourne warehouse at 10:30 am and deliver four boxes weighing 32 kg to Carlton before 2:00 pm. The shipment contains fragile glass items. Use loading dock B for pickup and call the customer before arrival.

**Issues & Limitations – Version 1:**
- Important delivery details were combined in a single paragraph.
- Missing information was not clearly identified for the dispatcher or driver.
- The prompt did not stop the AI from adding route, travel or access details.

### Final Version v1.1 Output
**Shipment ID:** SP421  
**Driver ID:** D17  
**Pickup location:** Port Melbourne warehouse  
**Pickup time:** 10:30 am  
**Delivery location:** Carlton  
**Delivery deadline:** 2:00 pm  
**Packages and weight:** 4 boxes, 32 kg  
**Special handling:** Fragile glass items  
**Pickup instructions:** Use loading dock B  
**Customer instructions:** Call before arrival  
**Missing information:** None

**Improvements – Final v1.1:**
- Added fixed driver-facing headings so important details are easier to scan.
- Added a missing-information field and a rule to use confirmed data only.
- Prevented invented routes, travel times and access instructions.

### Comparison
Version 1 was readable but placed most operational details in a paragraph. Version 1.1 used fixed headings, making the brief faster for a driver or dispatcher to scan. It also included a missing-information field and explicitly prevented invented routes, travel times or access instructions.

## Test Result
The improved prompt generated a scannable driver brief with consistent headings and no invented route information.

## Automation Potential
**High.** Can convert approved dispatch records into standard driver instructions.

## Risks and Limitations
Incorrect source data will still produce an incorrect brief.

## Mitigation and Human Oversight
Dispatch staff verify the brief before release to the driver.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Requested a driver brief without defining the layout, missing-data behaviour or boundaries on route and access information. | The output included the correct facts but placed them in a paragraph, making rapid operational scanning harder. | Even accurate content can be less useful when the output format does not match the user's workflow. |
| Final v1.1 | Added fixed driver-facing headings, a “Not provided” rule and constraints against inventing routes, travel times or access details. | The same information became a clear, scannable dispatch brief with all important fields separated and no unsupported additions. | Designing the output around the end user's workflow improves usability, while constraints reduce operational risk. |
