# Prompt 5 – Delay Classification

## Intended Workflow or Task
Classify active delivery delays for operations staff.

## Problem Being Solved
Delay reports can be inconsistent, making it harder to decide which cases need immediate attention.

## Version 1
**Prompt:** Classify this delivery delay and explain the problem: [DELAY DETAILS]

**Issue:** Severity terms were undefined and the AI could recommend unapproved actions.

## Final Version – v1.1
### Prompt Text
You are an operations assistant for a last-mile logistics company.

Classify the delay using only the confirmed information provided:

- Low: estimated delay is 30 minutes or less
- Medium: estimated delay is 31–60 minutes
- High: estimated delay is more than 60 minutes, the delivery deadline will be missed by more than 60 minutes, or a safety/security issue is explicitly reported
- Review Required: the delay length cannot be determined

Return:
1. Shipment ID
2. Delay category
3. Original deadline
4. Current ETA
5. Reported reason
6. Customer contacted: Yes/No/Not provided
7. Recommended administrative action

Recommended actions must be limited to: monitor, contact customer, or escalate to operations manager. Do not create a new ETA or decide compensation.

Delay details:
[DELAY DETAILS]

## Test Result
The final version gave a repeatable classification and kept recommendations inside an approved action set.

## Automation Potential
**Medium.** Suitable for exception queues and alerts.

## Risks and Limitations
ETA data may change rapidly and safety issues can require context beyond the prompt.

## Mitigation and Human Oversight
Operations staff confirm live ETA information and immediately review any safety-related case.
