# Prompt 3 – Delivery Priority

## Version 1

### Prompt
Decide how urgent this delivery is:

[DELIVERY DETAILS]

### Example Input
Shipment ID: SP310
Pickup time: 8:00 am today
Delivery deadline: 11:00 am today
Service type: Same-day delivery
Special handling: None provided

### Test Output
This delivery appears to be high priority because it has a short same-day delivery window.

### Issues Identified
- No priority categories are defined.
- The reasoning can vary between runs.
- The AI may use assumptions that are not part of company policy.
- Staff cannot easily use the result in an automated dispatch workflow.
