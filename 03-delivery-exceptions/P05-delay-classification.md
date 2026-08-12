# Prompt 5 – Delay Classification

## Version 1

### Prompt
Classify this delivery delay and explain the problem:

[DELAY DETAILS]

### Example Input
Shipment ID: SP510
Original delivery deadline: 3:30 pm
New estimated arrival: 4:20 pm
Driver note: Road closure on CityLink caused the delay.
Customer contacted: No

### Test Output
The shipment is delayed by about 50 minutes because of a road closure. This is a significant delay and the customer should be informed.

### Issues Identified
- No official delay categories are defined.
- The term “significant” is subjective.
- The output does not have a consistent operational structure.
- The AI could recommend actions that are not approved by the business.
