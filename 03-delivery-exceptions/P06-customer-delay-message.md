# Prompt 6 – Customer Delay Message

## Version 1

### Prompt
Write a message to a customer whose delivery is late.

### Example Input
Customer name: Alex
Shipment ID: SP522
Original delivery time: 3:30 pm
New estimated arrival: 4:20 pm
Reason provided: Road closure

### Test Output
Hi Alex, we are sorry that shipment SP522 is running late because of a road closure. Your new estimated arrival time is 4:20 pm. We apologise for the inconvenience and appreciate your patience.

### Issues Identified
- The prompt does not say which facts can be used.
- It could invent a reason, ETA, refund or compensation.
- Tone and length are not controlled.
- There is no human-review instruction before sending.
