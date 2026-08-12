# Prompt 1 – Shipment Summary

## Intended Workflow or Task
Shipment intake and order processing.

## Problem Being Solved
Shipment information may arrive as unstructured text, forcing staff to manually identify delivery details.

## Version 1
**Prompt:** Summarise the following delivery information: [SHIPMENT INFORMATION]

**Issue:** The output format was not fixed, missing information was not clearly handled and the AI was not prevented from guessing.

## Final Version – v1.1
### Prompt Text
You are an operations assistant for a last-mile logistics company.

Using only the shipment information provided, extract and organise the following:

- Pickup location
- Delivery location
- Delivery date
- Delivery deadline
- Number of packages
- Weight
- Special handling requirements
- Customer instructions

Do not invent missing information. If information is unavailable, write **“Not provided”.**

Return the answer using the exact headings listed above.

Shipment information:
[SHIPMENT INFORMATION]

## Example Input
Sarah needs two cartons picked up from Sunshine warehouse tomorrow morning and delivered to Richmond before 3 pm. Total weight is 18 kg. Fragile items. Customer requested a phone call before delivery.

## Test Result
The improved prompt produced a consistent eight-field shipment summary and clearly separated supplied facts from missing information.

## Automation Potential
**High.** Suitable for standardising shipment intake before data entry into a transport management system.

## Risks and Limitations
Incomplete source information, ambiguous wording, unusual logistics terminology and privacy risks.

## Mitigation and Human Oversight
Use only supplied information, show missing fields explicitly and require staff review for incomplete, unusual or high-value shipments.
