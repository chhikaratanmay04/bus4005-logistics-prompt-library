# Prompt 9 – Incident Escalation

## Intended Workflow or Task
Prepare a management escalation summary for operational incidents.

## Problem Being Solved
Important incident facts may be scattered through shift notes and can be mixed with assumptions.

## Version 1
**Prompt:** Summarise this warehouse incident and say if it should be escalated: [INCIDENT DETAILS]

**Issue:** The AI was asked to make an escalation decision without defined controls and could make safety or liability conclusions.

## Final Version – v1.1
### Prompt Text
You are an operations assistant for a logistics company.

Prepare a confidential incident escalation summary using only the information provided.

Use these headings:
1. Incident summary
2. Date/time
3. Location
4. People involved
5. Confirmed damage or disruption
6. Reported injury or safety concern
7. Actions already taken
8. Missing information
9. Recommended next administrative step
10. Person responsible for review

If information is missing, write **“Not provided – follow-up required”.**

Do not determine the cause, assign blame, make medical conclusions or decide legal responsibility. If an injury, safety concern or serious operational disruption is explicitly reported, state **“Immediate management review required.”**

Incident details:
[INCIDENT DETAILS]

## Example Input
A forklift lightly contacted a pallet and two cartons fell. No injury was reported. One carton has visible damage. The area has been secured. The supervisor has not yet been informed.

## ChatGPT Test Evidence
### Version 1 Output
A forklift contacted a pallet, causing two cartons to fall. No injuries were reported, but one carton was visibly damaged. The area has been secured. The incident should be escalated to the supervisor for review because equipment contact and product damage occurred.

### Final Version v1.1 Output
1. **Incident summary:** A forklift contacted a pallet and two cartons fell.
2. **Date/time:** Not provided – follow-up required
3. **Location:** Not provided – follow-up required
4. **People involved:** Not provided – follow-up required
5. **Confirmed damage or disruption:** One carton has visible damage.
6. **Reported injury or safety concern:** No injury was reported. No separate safety concern was explicitly provided.
7. **Actions already taken:** The area has been secured.
8. **Missing information:** Date/time, exact location, people involved and any further incident details are not provided and require follow-up.
9. **Recommended next administrative step:** Inform the supervisor and arrange management review under normal incident procedures.
10. **Person responsible for review:** Not provided – follow-up required

### Comparison
Version 1 made a direct escalation judgement without defined controls. Version 1.1 separated confirmed facts from missing information, avoided assigning cause or blame and clearly identified what still needed follow-up. The final prompt is more suitable for sensitive operational incidents because it supports management review without replacing formal safety or investigation procedures.

## Test Result
The final prompt separated confirmed information from missing facts and avoided unsupported conclusions.

## Automation Potential
**Medium.** Useful for structuring incident information for management review.

## Risks and Limitations
This prompt cannot replace emergency procedures, formal investigations or safety expertise.

## Mitigation and Human Oversight
All safety-related incidents require human management review and normal company incident procedures.
