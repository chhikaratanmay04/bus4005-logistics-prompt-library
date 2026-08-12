# Prompt 1 – Shipment Summary

## Version 1

### Prompt
Summarise the following delivery information:

[SHIPMENT INFORMATION]

### Example Input
Sarah needs two cartons picked up from Sunshine warehouse tomorrow morning and delivered to Richmond before 3 pm. Total weight is 18 kg. Fragile items. Customer requested a phone call before delivery.

### Test Output
Delivery Summary
- Pickup: Sunshine warehouse
- Delivery: Richmond
- Pickup time: Tomorrow morning
- Delivery deadline: Before 3 pm
- Packages: Two cartons
- Weight: 18 kg
- Handling: Fragile
- Customer instruction: Call before delivery

### Issues Identified
- The prompt does not define a fixed output structure.
- It does not say what to do when information is missing.
- It does not prevent the AI from guessing details.
- Different runs may format the same shipment differently.
