# BUS4005 Logistics Prompt Library

**Assessment:** BUS4005 – Generative AI for Business, Assessment 1  
**Business field:** Last-mile logistics and delivery operations  
**Model tested on:** ChatGPT  
**Portfolio purpose:** Demonstrate 10 tested and iterated prompts that support workflow automation while retaining human oversight.

## Business Context
A mid-sized logistics company receives shipment details, dispatch instructions, delivery exceptions, customer complaints and operational notes in different formats. Staff spend time manually extracting information, classifying issues, drafting messages and preparing handovers. This prompt library standardises those repetitive tasks.

## Prompt Library
| ID | Prompt | Workflow | Automation Potential | Risk |
|---|---|---|---|---|
| P01 | Shipment Summary | Shipment intake | High | Low |
| P02 | Shipment Data Check | Shipment intake | High | Medium |
| P03 | Delivery Priority | Dispatch | Medium | Medium |
| P04 | Driver Dispatch Brief | Dispatch | High | Medium |
| P05 | Delay Classification | Delivery exceptions | Medium | Medium |
| P06 | Customer Delay Message | Delivery exceptions | High | Medium |
| P07 | Complaint Triage | Customer service | High | Medium |
| P08 | Complaint Response | Customer service | High | Medium |
| P09 | Incident Escalation | Operations | Medium | High |
| P10 | Shift Handover | Operations | High | Medium |

## Prompt Chaining
Shipment intake: **P01 → P02 → P03 → P04**  
Delivery exception: **P05 → P06**  
Customer complaint: **P07 → P08**  
Operational incident: **P09 → P10**

## Prompting Strategies Used
- Role prompting to define the AI as a logistics operations assistant.
- Grounding constraints such as “use only the information provided”.
- Fixed output structures to improve consistency.
- Controlled categories for classification tasks.
- Missing-information rules to reduce hallucination.
- Human-review requirements for customer communication, dispatch decisions and safety incidents.

## ChatGPT Testing Guide
The repository includes **[CHATGPT-TEST-PROMPTS.md](CHATGPT-TEST-PROMPTS.md)** with a realistic test input for every prompt, testing goals, evaluation criteria and a standard comparison prompt for analysing Version 1 against the Final Version.

Use the same input for both versions so the effect of prompt improvement can be compared fairly. Actual ChatGPT outputs should be retained as testing evidence rather than invented.

## Iteration Evidence
Each prompt file contains Version 1, issues identified, an improved Final Version, test results, automation potential, risks, limitations and mitigation. GitHub commit history provides additional evidence of prompt development.

The repository history now separately documents:
1. Initial Version 1 prompt testing.
2. Improved final prompt versions and workflow controls.
3. Addition of the standard ChatGPT testing and comparison guide.

## Responsible Use
The library is designed to support staff rather than make final operational, safety, legal or compensation decisions. Human review is required where information is incomplete, a customer-facing response is produced, safety is involved or a dispatch decision may materially affect service.
