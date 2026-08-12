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

Add this heading above the message: **Draft – staff review required**

## Example Input
Customer name: Alex  
Shipment ID: SP522  
Original delivery time: 3:30 pm  
New estimated arrival: 4:20 pm  
Reason provided: Road closure

## ChatGPT Test Evidence
### Version 1 Output
Hi Alex, we’re sorry that shipment SP522 is running late due to a road closure. Your updated estimated arrival time is 4:20 pm. We apologise for the inconvenience and appreciate your patience.

**Issues & Limitations – Version 1:**
- The message was usable but had no rules limiting unsupported details or promises.
- The AI could potentially invent a reason, ETA, refund or compensation in other cases.
- There was no clear indication that staff should review the message before sending.

### Final Version v1.1 Output
**Draft – staff review required**

Hi Alex,

We apologise for the delay to shipment SP522. The confirmed reason provided is a road closure, and the current estimated arrival time is 4:20 pm. We’re sorry for the inconvenience. We will update you if further confirmed information becomes available.

Kind regards,  
Customer Service Team

**Improvements – Final v1.1:**
- Limited the response to approved and confirmed information only.
- Prohibited refunds, compensation, guarantees and invented ETAs or reasons.
- Added a staff-review label and kept the message concise and professional.

### Comparison
Version 1 produced a usable message but had no built-in controls over promises or unsupported details. Version 1.1 clearly labelled the message as a draft, used only approved information, retained the confirmed ETA and reason, and added a rule against refunds, compensation and guaranteed delivery times. This makes the final version safer for customer-facing use.

## Test Result
The improved prompt produced a consistent customer message while preventing unsupported promises.

## Automation Potential
**High** for drafting; **human approval required** before sending.

## Risks and Limitations
Incorrect or outdated ETA information could mislead customers.

## Mitigation and Human Oversight
Staff verify the latest operational data and approve every customer-facing message.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a simple request to write a delay message without limiting the information, promises or actions the AI could include. | The message was polite and useful, but there were no safeguards against invented ETAs, reasons, refunds or guarantees in other cases. | Customer-facing prompts require stronger controls because unsupported statements can create service and reputational risk. |
| Final v1.1 | Added a customer-communication role, grounding to approved information, a 100-word limit, prohibited compensation/guarantees and added a staff-review label. | The output remained concise and professional while clearly using only the confirmed reason and ETA and signalling human approval before sending. | Grounding, explicit prohibitions and human-review instructions make AI-generated customer communication safer for operational use. |
