# Prompt 2 – Shipment Data Check

## Intended Workflow or Task
Pre-dispatch shipment validation.

## Problem Being Solved
Incomplete records can reach dispatch staff and create avoidable delays or rework.

## Version 1
**Prompt:** Check this shipment information and tell me what is missing.

**Issue:** Mandatory fields were undefined and the AI could treat optional fields as required.

## Final Version – v1.1
### Prompt Text
You are a shipment validation assistant for a last-mile logistics company.

Check the shipment record using only the information provided.

Required fields:
- Shipment ID
- Pickup location
- Delivery location
- Delivery date
- Number of packages
- Weight

Check these additional fields if provided:
- Delivery deadline
- Customer instructions
- Special handling requirements

Return exactly:
1. Validation status: READY or REVIEW REQUIRED
2. Required fields present
3. Required fields missing
4. Additional information provided
5. Staff action required

Mark **READY** only when every required field is provided. Do not guess or create missing information.

## Example Input
Shipment ID: LG204  
Pickup: Laverton warehouse  
Delivery: Footscray  
Delivery date: 14 August 2026  
Packages: 3 cartons  
Total weight: 27 kg

## ChatGPT Test Evidence
### Version 1 Output
The shipment contains the shipment ID, pickup location, delivery location, delivery date, package quantity and total weight. Information that may still be needed includes a delivery deadline, customer instructions and any special handling requirements.

**Issues & Limitations – Version 1:**
- The prompt did not define which shipment fields were mandatory.
- Optional details were presented as if they might be missing requirements.
- There was no standard READY or REVIEW REQUIRED validation result.

### Final Version v1.1 Output
1. **Validation status:** READY
2. **Required fields present:** Shipment ID, Pickup location, Delivery location, Delivery date, Number of packages, Weight
3. **Required fields missing:** None
4. **Additional information provided:** None
5. **Staff action required:** No completeness follow-up required. Staff should verify the accuracy of the supplied shipment information before dispatch.

**Improvements – Final v1.1:**
- Defined required and optional fields clearly for consistent validation.
- Added READY/REVIEW REQUIRED rules and prohibited guessing missing data.
- The output now gives a clear, repeatable pre-dispatch completeness check.

### Comparison
Version 1 treated optional information as though it might be missing requirements because the original prompt did not define mandatory fields. Version 1.1 used explicit validation rules and correctly marked the shipment READY because every required field was present. The improved prompt is more predictable and suitable for pre-dispatch checking.

## Test Result
The final version provided a repeatable READY/REVIEW REQUIRED decision based only on defined fields.

## Automation Potential
**High.** Can flag incomplete records before dispatch processing.

## Risks and Limitations
A field can be present but incorrect; the AI cannot verify addresses, weights or customer data against source systems.

## Mitigation and Human Oversight
Use AI for completeness checking only. Staff or system validation must confirm accuracy.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Asked the AI to identify missing shipment information without defining which fields were mandatory or optional. | The output correctly recognised the supplied fields but suggested optional details might be missing requirements. | Validation prompts need explicit business rules; otherwise the AI may apply its own judgement about what information is required. |
| Final v1.1 | Defined six mandatory fields, separated optional fields, added READY/REVIEW REQUIRED status and prohibited guessing. | The same record was consistently classified as READY and the output clearly separated required, missing and additional information. | Controlled validation criteria improve consistency, but human or system checks are still required to verify whether supplied data is accurate. |
