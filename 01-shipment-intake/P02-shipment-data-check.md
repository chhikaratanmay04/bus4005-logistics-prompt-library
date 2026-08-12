# Prompt 2 – Shipment Data Check

## Version 1

### Prompt
Check this shipment information and tell me what is missing:

[SHIPMENT INFORMATION]

### Example Input
Shipment ID: LG204
Pickup: Laverton warehouse
Delivery: Footscray
Delivery date: 14 August 2026
Packages: 3 cartons
Total weight: 27 kg

### Test Output
The shipment includes an ID, pickup location, delivery location, delivery date, package quantity and weight. A customer contact number and delivery deadline may be missing.

### Issues Identified
- The prompt does not define which fields are mandatory.
- The AI may decide that optional information is required.
- There is no standard PASS/REVIEW result.
- There is no instruction to avoid assumptions.
