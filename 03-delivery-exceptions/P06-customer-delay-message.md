# Prompt 6 – Customer Delay Message

## Intended Workflow or Task
Draft customer communication for confirmed delivery delays.

## Problem Being Solved
Staff repeatedly write similar delay messages and may communicate inconsistently.

## Version 1
**Prompt:** Write a message to a customer whose delivery is late.

**Issue:** The AI could invent reasons, ETAs, promises, refunds or compensation.

## Final Version – v1.1
### Prompt Text
You are a customer communication assistant for a last-mile logistics company.

Draft a short professional delay message using only the approved information provided.

The message must:
1. Address the customer by name if provided
2. Identify the shipment ID if provided
3. Acknowledge the delay
4. State the confirmed updated ETA only if provided
5. State the confirmed reason only if provided
6. Apologise for the inconvenience
7. Say that the customer will be updated if further confirmed information becomes available

Do not promise a refund, discount, compensation or guaranteed delivery time. Do not invent a reason or ETA.

Keep the message under 100 words.

Approved information:
[DELAY INFORMATION]

Add this heading above the message: **Draft – staff review required**

## Test Result
The improved prompt produced a consistent customer message while preventing unsupported promises.

## Automation Potential
**High** for drafting; **human approval required** before sending.

## Risks and Limitations
Incorrect or outdated ETA information could mislead customers.

## Mitigation and Human Oversight
Staff verify the latest operational data and approve every customer-facing message.
