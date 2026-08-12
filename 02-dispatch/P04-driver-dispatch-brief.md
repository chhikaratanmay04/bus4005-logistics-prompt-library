# Prompt 4 – Driver Dispatch Brief

## Version 1

### Prompt
Create a driver brief from these delivery details:

[DELIVERY DETAILS]

### Example Input
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

### Test Output
Driver D17 should collect shipment SP421 from Port Melbourne at 10:30 am and deliver four boxes weighing 32 kg to Carlton before 2:00 pm. The shipment contains fragile glass items. Use loading dock B and call the customer before arrival.

### Issues Identified
- Important details are buried in a paragraph.
- The prompt does not specify a standard driver-ready format.
- It does not prevent route or timing assumptions.
- Missing information is not clearly flagged.
