# Prompt 7 – Complaint Triage

## Intended Workflow or Task
Classify and prioritise customer complaints.

## Problem Being Solved
Complaints arrive in free text and require manual sorting before the correct team can respond.

## Version 1
**Prompt:** Classify this logistics customer complaint: [CUSTOMER COMPLAINT]

**Issue:** No approved categories or urgency rules were defined.

## Final Version – v1.1
### Prompt Text
You are a complaint triage assistant for a logistics company.

Using only the customer complaint, select exactly one primary category:
- Late Delivery
- Damaged Package
- Missing Delivery
- Wrong Delivery
- Driver Conduct
- Billing
- Safety
- Other

Assign one urgency level:
- High: injury, safety concern, threat, discrimination, legal action or missing high-risk goods is explicitly reported
- Medium: damaged/missing delivery, repeated service failure or unresolved billing problem
- Low: routine dissatisfaction without immediate risk

Return:
1. Primary category
2. Secondary issue, if applicable
3. Urgency
4. Factual summary
5. Reason for classification
6. Recommended staff action

Do not assign blame or invent facts.

Customer complaint:
[CUSTOMER COMPLAINT]

## Example Input
My parcel arrived one day late and the outer box was crushed, although the item inside seems okay. I would like someone to call me.

## ChatGPT Test Evidence
### Version 1 Output
This complaint relates to a late delivery and damaged packaging. It should be sent to customer service for follow-up because the customer has asked to be contacted.

### Final Version v1.1 Output
1. **Primary category:** Damaged Package
2. **Secondary issue:** Late Delivery
3. **Urgency:** Medium
4. **Factual summary:** The customer reports that the parcel arrived one day late and the outer box was crushed. The customer states that the item inside appears okay and has requested a phone call.
5. **Reason for classification:** Package damage is the main issue and damaged deliveries are defined as Medium urgency. Late delivery is also reported as a secondary issue.
6. **Recommended staff action:** Route the complaint to customer service for review and contact the customer as requested. Confirm shipment details and the reported package condition before deciding any further action.

### Comparison
Version 1 identified the general issues but did not apply a standard category or urgency level. Version 1.1 selected one primary category, captured the secondary issue, applied a defined Medium urgency rule and provided a factual summary without assigning blame. This makes the result easier to route and manage consistently.

## Test Result
The final prompt produced consistent categories and clearer escalation priority.

## Automation Potential
**High.** Suitable for routing complaints into customer-service queues.

## Risks and Limitations
Ambiguous complaints can be misclassified and the model cannot verify a customer's claim.

## Mitigation and Human Oversight
High-priority and uncertain complaints require staff review before action.
