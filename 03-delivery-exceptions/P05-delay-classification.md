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

## Example Input
Shipment ID: SP510  
Original delivery deadline: 3:30 pm  
New estimated arrival: 4:20 pm  
Driver note: Road closure on CityLink caused the delay.  
Customer contacted: No

## ChatGPT Test Evidence
### Version 1 Output
Shipment SP510 is experiencing a significant delay of about 50 minutes because of a road closure on CityLink. The customer has not yet been contacted, so the customer should be informed about the delay and updated arrival time.

### Final Version v1.1 Output
1. **Shipment ID:** SP510
2. **Delay category:** Medium
3. **Original deadline:** 3:30 pm
4. **Current ETA:** 4:20 pm
5. **Reported reason:** Road closure on CityLink
6. **Customer contacted:** No
7. **Recommended administrative action:** Contact customer

### Comparison
Version 1 used the subjective term “significant” because the original prompt did not define severity levels. Version 1.1 calculated the 50-minute delay against a clear rule and classified it as Medium. The final version also restricted the recommended action to an approved list, improving consistency and reducing the chance of unapproved operational or compensation decisions.

## Test Result
The final version gave a repeatable classification and kept recommendations inside an approved action set.

## Automation Potential
**Medium.** Suitable for exception queues and alerts.

## Risks and Limitations
ETA data may change rapidly and safety issues can require context beyond the prompt.

## Mitigation and Human Oversight
Operations staff confirm live ETA information and immediately review any safety-related case.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Asked the AI to classify a delay without defining severity thresholds or limiting the actions it could recommend. | The output correctly described the 50-minute delay but called it “significant,” a subjective label that could vary between runs. | Operational classifications need measurable thresholds rather than vague language. |
| Final v1.1 | Added time-based Low/Medium/High rules, a Review Required category and a restricted set of administrative actions. | The 50-minute delay was consistently classified as Medium and the recommended action was limited to “Contact customer.” | Numeric rules and controlled action choices make exception handling more consistent and reduce the risk of unsupported decisions. |
