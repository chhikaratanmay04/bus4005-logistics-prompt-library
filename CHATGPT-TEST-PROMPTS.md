# ChatGPT Testing Prompts – BUS4005 Logistics Prompt Library

This file provides the test inputs and comparison prompt used to evaluate the 10 logistics prompts in this portfolio.

## How to Test Each Prompt

For each prompt:

1. Open the relevant P01–P10 Markdown file in this repository.
2. Copy **Version 1** into ChatGPT and use the matching test input below.
3. Save the output as the Version 1 test result.
4. Copy the **Final Version (v1.1)** and use the exact same test input.
5. Save the final-version output.
6. Compare both outputs using the comparison prompt at the end of this file.
7. Do not invent results. Keep the actual ChatGPT outputs as evidence of testing.

---

## P01 – Shipment Summary

### Test Input
Sarah needs two cartons picked up from Sunshine warehouse tomorrow morning and delivered to Richmond before 3 pm. Total weight is 18 kg. Fragile items. Customer requested a phone call before delivery.

### Testing Goal
Check whether the improved prompt extracts shipment information into a consistent structure without inventing missing details.

---

## P02 – Shipment Data Check

### Test Input
Shipment ID: LG204  
Pickup: Laverton warehouse  
Delivery: Footscray  
Delivery date: 14 August 2026  
Packages: 3 cartons  
Total weight: 27 kg

### Testing Goal
Check whether the improved prompt identifies missing information consistently and avoids treating optional information as confirmed requirements.

---

## P03 – Delivery Priority

### Test Input
Shipment ID: SP310  
Pickup time: 8:00 am today  
Delivery deadline: 11:00 am today  
Service type: Same-day delivery  
Special handling: None provided

### Testing Goal
Check whether the improved prompt applies clearly defined priority rules rather than making an unsupported judgement.

---

## P04 – Driver Dispatch Brief

### Test Input
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

### Testing Goal
Check whether the improved prompt creates a driver-ready briefing with important operational details clearly separated.

---

## P05 – Delay Classification

### Test Input
Shipment ID: SP510  
Original delivery deadline: 3:30 pm  
New estimated arrival: 4:20 pm  
Driver note: Road closure on CityLink caused the delay.  
Customer contacted: No

### Testing Goal
Check whether the improved prompt uses controlled delay categories, factual reasoning and an appropriate next-action recommendation.

---

## P06 – Customer Delay Message

### Test Input
Customer name: Alex  
Shipment ID: SP522  
Original delivery time: 3:30 pm  
New estimated arrival: 4:20 pm  
Reason provided: Road closure

### Testing Goal
Check whether the improved prompt produces a professional message using only approved information without promising refunds, compensation or unsupported actions.

---

## P07 – Complaint Triage

### Test Input
My parcel arrived one day late and the outer box was crushed, although the item inside seems okay. I would like someone to call me.

### Testing Goal
Check whether the improved prompt classifies the complaint consistently, identifies urgency and recommends an appropriate staff action without assigning blame.

---

## P08 – Complaint Response

### Test Input
Customer complaint: My parcel arrived one day late and the outer box was crushed, although the item inside seems okay. I would like someone to call me.

Approved action: Customer service staff will review the delivery record after receiving the shipment or tracking number.

### Testing Goal
Check whether the improved prompt acknowledges the complaint, asks for the required information and avoids unauthorised promises or admissions of liability.

---

## P09 – Incident Escalation

### Test Input
A forklift lightly contacted a pallet and two cartons fell. No injury was reported. One carton has visible damage. The area has been secured. The supervisor has not yet been informed.

### Testing Goal
Check whether the improved prompt separates confirmed facts from missing information, avoids unsupported safety or legal conclusions and clearly identifies the need for supervisor review.

---

## P10 – Shift Handover

### Test Input
SP610 delayed 45 minutes; new ETA 6:00 pm; customer notified.  
SP611 delivery failed because customer was unavailable; redelivery pending.  
WH-14 damaged carton isolated in warehouse; supervisor review pending.  
SP612 delivered successfully.

### Testing Goal
Check whether the improved prompt separates completed work from outstanding actions and produces a consistent handover for the next shift.

---

# Comparison Prompt

After testing Version 1 and Final Version with the same input, paste both outputs into ChatGPT and use this prompt:

> Compare the Version 1 output and the Final Version output for this logistics workflow prompt.
>
> Identify:
> 1. Improvements in structure
> 2. Improvements in accuracy
> 3. Improvements in consistency
> 4. Reduction in unsupported assumptions
> 5. Improvements in business usability
> 6. Remaining limitations
>
> Use simple academic language. Base the comparison only on the two outputs provided. Do not invent test results.

---

## Evaluation Criteria

Use the following criteria when discussing prompt improvement:

| Criterion | What to Check |
|---|---|
| Accuracy | Does the output correctly use the supplied information? |
| Completeness | Are all required fields or issues addressed? |
| Consistency | Does the output follow the required format? |
| Grounding | Does it avoid inventing missing details? |
| Business usability | Can logistics staff quickly understand and use the output? |
| Risk control | Does it respect human-review, privacy and decision boundaries? |

## Human Oversight Reminder

The prompts support logistics staff but do not replace operational judgement. Staff should review incomplete shipments, dispatch priorities, customer-facing messages, complaints, incidents and any output involving safety, legal responsibility or compensation.