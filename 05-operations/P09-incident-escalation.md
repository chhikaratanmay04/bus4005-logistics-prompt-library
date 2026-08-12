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

## Test Result
The final prompt separated confirmed information from missing facts and avoided unsupported conclusions.

## Automation Potential
**Medium.** Useful for structuring incident information for management review.

## Risks and Limitations
This prompt cannot replace emergency procedures, formal investigations or safety expertise.

## Mitigation and Human Oversight
All safety-related incidents require human management review and normal company incident procedures.
