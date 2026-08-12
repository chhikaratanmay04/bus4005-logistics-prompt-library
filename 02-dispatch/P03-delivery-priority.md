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

## Test Result
The final prompt constrained the decision to stated business rules and made the reasoning auditable.

## Automation Potential
**Medium.** Useful as a dispatch decision-support flag, not an autonomous dispatch rule.

## Risks and Limitations
Business priorities may change and unusual deliveries may require exceptions.

## Mitigation and Human Oversight
Dispatcher reviews High and Review Required cases and overrides the AI when operational context requires it.
