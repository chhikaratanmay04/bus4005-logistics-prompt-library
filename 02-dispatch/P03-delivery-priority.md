# Prompt 3 – Delivery Priority

## Intended Workflow or Task
Support dispatch prioritisation.

## Problem Being Solved
Dispatch staff may receive several time-sensitive shipments and need a consistent first-pass classification.

## Version 1
**Prompt:** Decide how urgent this delivery is: [DELIVERY DETAILS]

**Issue:** Priority definitions were subjective and inconsistent.

## Final Version – v1.1
### Prompt Text
You are a dispatch support assistant for a last-mile logistics company.

Classify the delivery into exactly one priority category using only the information provided:

- **High:** delivery is due within 3 hours, explicitly marked urgent/same-day, or has a strict time-critical deadline.
- **Medium:** delivery is due later the same day but is not otherwise marked urgent.
- **Low:** delivery is due after today and no urgent requirement is provided.
- **Review Required:** information is insufficient to apply the rules above.

Return:
1. Priority
2. Facts used
3. Reason for classification
4. Missing information, if any
5. Dispatcher review required: Yes/No

Do not assign a driver, route or new deadline.

Delivery details:
[DELIVERY DETAILS]

## Example Input
Shipment ID: SP310  
Pickup time: 8:00 am today  
Delivery deadline: 11:00 am today  
Service type: Same-day delivery  
Special handling: None provided

## ChatGPT Test Evidence
### Version 1 Output
This delivery should be treated as **high priority** because it is a same-day shipment with a short delivery window between 8:00 am and 11:00 am.

### Final Version v1.1 Output
1. **Priority:** High
2. **Facts used:** Pickup time is 8:00 am today; delivery deadline is 11:00 am today; service type is Same-day delivery.
3. **Reason for classification:** The shipment is explicitly marked same-day and the delivery deadline is within a three-hour window, which meets the High-priority rules.
4. **Missing information:** None required for this classification.
5. **Dispatcher review required:** Yes

### Comparison
Both versions identified the shipment as urgent, but Version 1 relied on general judgement. Version 1.1 applied a defined rule, showed the exact facts used and made the decision auditable. It also prevented the AI from assigning a driver, route or new deadline and clearly signalled that a dispatcher should review a High-priority case.

## Test Result
The final prompt constrained the decision to stated business rules and made the reasoning auditable.

## Automation Potential
**Medium.** Useful as a dispatch decision-support flag, not an autonomous dispatch rule.

## Risks and Limitations
Business priorities may change and unusual deliveries may require exceptions.

## Mitigation and Human Oversight
Dispatcher reviews High and Review Required cases and overrides the AI when operational context requires it.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a broad urgency question without defining priority categories, thresholds or review requirements. | The AI correctly called the example High priority, but the decision depended on general judgement rather than documented business rules. | Classification can appear correct while still being difficult to audit or reproduce if category rules are not explicit. |
| Final v1.1 | Added High/Medium/Low/Review Required rules, required facts and reasoning, and prevented driver, route or deadline decisions. | The output applied a clear High-priority rule, explained the facts used and flagged dispatcher review. | Rule-based prompting makes classifications more transparent and consistent while preserving human control over operational decisions. |
