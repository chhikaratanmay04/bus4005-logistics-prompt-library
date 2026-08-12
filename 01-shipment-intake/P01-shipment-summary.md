# Prompt 1 – Shipment Summary

## Intended Workflow or Task
Shipment intake and order processing.

## Problem Being Solved
Shipment information may arrive as unstructured text, forcing staff to manually identify delivery details.

## Version 1
**Prompt:** Summarise the following delivery information.

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

## Example Input
Sarah needs two cartons picked up from Sunshine warehouse tomorrow morning and delivered to Richmond before 3 pm. Total weight is 18 kg. Fragile items. Customer requested a phone call before delivery.

## ChatGPT Test Evidence
### Version 1 Output
**Delivery Summary**
- Pickup: Sunshine warehouse, tomorrow morning
- Delivery: Richmond, before 3 pm
- Packages: Two cartons
- Total weight: 18 kg
- Handling: Fragile items
- Customer request: Call before delivery

**Issues & Limitations – Version 1:**
- The output used AI-chosen headings instead of a fixed business format.
- Pickup and delivery timing were mixed with location details.
- There was no clear rule for missing information or unsupported assumptions.

### Final Version v1.1 Output
**Pickup location:** Sunshine warehouse  
**Delivery location:** Richmond  
**Delivery date:** Tomorrow  
**Delivery deadline:** Before 3 pm  
**Number of packages:** Two cartons  
**Weight:** 18 kg  
**Special handling requirements:** Fragile items  
**Customer instructions:** Phone call before delivery

**Improvements – Final v1.1:**
- Added exact shipment fields so every output follows the same structure.
- Added grounding and a “Not provided” rule to reduce invented information.
- The result is clearer, more consistent and easier to use in logistics systems.

### Comparison
Version 1 captured the main facts but combined timing information with locations and used its own headings. Version 1.1 produced the exact eight-field structure requested, separated each operational field and added a clear rule for handling missing information. The improved version is more consistent and easier to transfer into a logistics system.

## Test Result
The improved prompt produced a consistent eight-field shipment summary and clearly separated supplied facts from missing information.

## Automation Potential
**High.** Suitable for standardising shipment intake before data entry into a transport management system.

## Risks and Limitations
Incomplete source information, ambiguous wording, unusual logistics terminology and privacy risks.

## Mitigation and Human Oversight
Use only supplied information, show missing fields explicitly and require staff review for incomplete, unusual or high-value shipments.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a basic summarisation instruction without fixed fields, grounding rules or missing-information handling. | The main shipment facts were captured, but pickup/delivery timing was combined with locations and the output headings were chosen by the AI. | A general prompt can produce understandable output, but it is not reliable enough for consistent operational data entry. |
| Final v1.1 | Added a logistics operations role, eight required output fields, a use-only-provided-information rule and a “Not provided” instruction for missing data. | The output became structured, predictable and easier to transfer into a logistics system while reducing the risk of invented details. | Role, fixed structure and explicit missing-data controls improve prompt reliability and automation readiness. |
