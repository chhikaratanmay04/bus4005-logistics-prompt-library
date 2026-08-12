# Prompt 10 – Shift Handover

## Version 1

### Prompt
Summarise these logistics notes for the next shift:

[SHIFT NOTES]

### Example Input
SP610 delayed 45 minutes; new ETA 6:00 pm; customer notified.
SP611 delivery failed because customer was unavailable; redelivery pending.
WH-14 damaged carton isolated in warehouse; supervisor review pending.
SP612 delivered successfully.

### Test Output
Shift handover: SP610 is delayed until 6:00 pm and the customer has been notified. SP611 requires redelivery after an unsuccessful delivery because the customer was unavailable. WH-14 is a damaged carton that has been isolated and needs supervisor review. SP612 was delivered successfully.

### Issues Identified
- Outstanding work and completed work are mixed together.
- Priority actions are not clearly identified.
- Missing information is not flagged.
- Different staff may receive differently formatted handovers.
