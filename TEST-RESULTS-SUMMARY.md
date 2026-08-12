# BUS4005 Logistics Prompt Library – Test Results Summary

## Testing Method
Each of the 10 prompts was tested in ChatGPT using the same example input for both versions:

1. Run Version 1.
2. Record the output and identify weaknesses.
3. Run the improved Final Version (v1.1) with the same input.
4. Compare structure, consistency, grounding, business usability and remaining limitations.

The full prompts, inputs, outputs and comparisons are stored in the individual P01–P10 files.

## Results

| Prompt | Main Version 1 Issue | Improvement in v1.1 | Result |
|---|---|---|---|
| P01 Shipment Summary | No fixed output format | Exact shipment fields and missing-data rule | More consistent intake summary |
| P02 Shipment Data Check | Required and optional fields unclear | Defined mandatory fields and READY/REVIEW status | More reliable completeness check |
| P03 Delivery Priority | Urgency was subjective | Defined priority rules and auditable reasoning | More consistent dispatch support |
| P04 Driver Dispatch Brief | Critical details buried in prose | Fixed driver-ready headings | Faster and clearer operational reading |
| P05 Delay Classification | Delay severity undefined | Time-based categories and approved action set | More controlled exception handling |
| P06 Customer Delay Message | Could make unsupported promises | Grounding, word limit and staff-review label | Safer customer communication |
| P07 Complaint Triage | No standard categories or urgency | Controlled categories and urgency rules | Better complaint routing |
| P08 Complaint Response | Could promise unapproved actions | Approved-action constraint and tracking-number request | Safer response drafting |
| P09 Incident Escalation | Could make unsupported escalation/safety conclusions | Confirmed-vs-missing structure and no-blame constraints | Better management review support |
| P10 Shift Handover | Open and completed work mixed together | Structured sections for actions, issues and completed work | Clearer shift transfer |

## Overall Evaluation
The testing showed that simple prompts can produce understandable outputs but often rely on the model's judgement for structure, missing information and recommended actions. The v1.1 prompts improved reliability by adding business roles, clear fields, controlled categories, grounding instructions, missing-information rules and human-review requirements.

The prompt library is suitable for supporting repetitive logistics administration, but it is not designed to replace human decisions involving dispatch exceptions, customer commitments, safety incidents or formal investigations.
