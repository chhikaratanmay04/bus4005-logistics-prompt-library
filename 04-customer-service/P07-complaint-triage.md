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

## Test Result
The final prompt produced consistent categories and clearer escalation priority.

## Automation Potential
**High.** Suitable for routing complaints into customer-service queues.

## Risks and Limitations
Ambiguous complaints can be misclassified and the model cannot verify a customer's claim.

## Mitigation and Human Oversight
High-priority and uncertain complaints require staff review before action.
