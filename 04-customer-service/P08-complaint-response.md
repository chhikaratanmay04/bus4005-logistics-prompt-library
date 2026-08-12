# Prompt 8 – Complaint Response

## Intended Workflow or Task
Draft a professional response to a logistics complaint.

## Problem Being Solved
Customer-service teams spend time writing repetitive acknowledgements and may accidentally make unapproved promises.

## Version 1
**Prompt:** Reply to this logistics customer complaint.

**Issue:** The response could promise compensation or actions that were not approved.

## Final Version – v1.1
### Prompt Text
You are a customer care assistant for a logistics company.

Draft a professional response using only the complaint and approved action provided.

The response must:
1. Acknowledge the customer's experience
2. Apologise for the inconvenience
3. Summarise the issue without assigning blame
4. Explain the approved next step
5. Ask for the shipment or tracking number if it is not provided
6. End with a respectful closing

Do not promise a refund, discount, replacement, compensation or specific investigation outcome unless explicitly included in the approved action. Do not admit legal responsibility.

Keep the response under 150 words.

Add this heading: **Draft – staff review required**

## Example Input
Customer complaint: My parcel arrived one day late and the outer box was crushed, although the item inside seems okay. I would like someone to call me.

Approved action: Customer service staff will review the delivery record after receiving the shipment or tracking number.

## ChatGPT Test Evidence
### Version 1 Output
We’re sorry to hear that your parcel arrived late and that the outer box was crushed. We understand your concern and apologise for the inconvenience. We will look into the delivery and arrange for someone to contact you about the issue.

**Issues & Limitations – Version 1:** The response could imply unapproved investigation, contact or compensation commitments.

### Final Version v1.1 Output
**Draft – staff review required**

Dear Customer,

We’re sorry that your parcel arrived one day late and that the outer box was crushed. We apologise for the inconvenience this has caused.

Our customer service team can review the delivery record once we receive your shipment or tracking number. Please provide that number so the matter can be reviewed. We have also noted your request to be contacted.

Kind regards,  
Customer Service Team

**Improvements – Final v1.1:** Limited the reply to approved actions, requested missing tracking details and added staff review controls.

### Comparison
Version 1 was polite but stated that the business would “look into” the delivery and arrange contact without a clearly supplied approval rule. Version 1.1 limited the response to the approved next step, requested the missing tracking information, avoided blame and did not promise compensation or a particular investigation outcome. The final version is therefore safer and more operationally controlled.

## Test Result
The final prompt retained a professional tone while keeping commitments inside approved business actions.

## Automation Potential
**High** for drafting, with staff approval before sending.

## Risks and Limitations
Poor or incomplete approved information can produce an unhelpful response.

## Mitigation and Human Oversight
Staff investigate the complaint, approve commitments and check the final response.

## Audit Log
| Version | Change Made | Observed Effect | Lesson Learned |
|---|---|---|---|
| Version 1 | Used a general reply instruction with no approved-action boundary, tracking-information rule or restrictions on commitments. | The response was polite but implied that the business would investigate and arrange contact without a clearly defined approval constraint. | A professional tone alone is not enough; customer-service prompts also need limits on what the AI is authorised to promise. |
| Final v1.1 | Added an approved-action input, required missing tracking information to be requested, prohibited refunds/compensation/legal admissions and added staff review. | The output followed the supplied next step, requested the tracking number and avoided unsupported promises or blame. | Separating drafting from business decision authority makes AI useful for customer service while keeping commitments under human control. |
