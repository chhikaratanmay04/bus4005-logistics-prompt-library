# Prompt 2 – Shipment Data Check

## Intended Workflow or Task
Pre-dispatch shipment validation.

## Problem Being Solved
Incomplete records can reach dispatch staff and create avoidable delays or rework.

## Version 1
**Prompt:** Check this shipment information and tell me what is missing: [SHIPMENT INFORMATION]

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

Shipment record:
[SHIPMENT INFORMATION]

## Test Result
The final version provided a repeatable READY/REVIEW REQUIRED decision based only on defined fields.

## Automation Potential
**High.** Can flag incomplete records before dispatch processing.

## Risks and Limitations
A field can be present but incorrect; the AI cannot verify addresses, weights or customer data against source systems.

## Mitigation and Human Oversight
Use AI for completeness checking only. Staff or system validation must confirm accuracy.
