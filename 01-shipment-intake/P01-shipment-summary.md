## Current Version v1.1

## Intended Workflow-
Shipment intake and order processing.

## Problem Being Solved-
Shipment information can arrive in inconsistent formats, requiring staff to manually identify important delivery details. 

## Prompt Text
Pickup location: Sunshine warehouse
Delivery location: Richmond
Delivery date: Tomorrow
Delivery deadline: Before 3:00 pm
Number of packages: Two cartons
Weight: 18 kg
Special handling requirements: Fragile items
Customer instructions: Phone call before delivery

## Inputs
Shipment information

## Expected Output
Structured shipment summary.

## Automation Potential
High. The prompt could be integrated with a shipment intake system to convert unstructured shipment information into a consistent format. 

## Human Oversight
Staff should review unusual, incomplete or high-value shipments before dispatch.

## Risks and Limitations 
- Missing source information
- AI incorrectly interpreting instructions
- Privacy risks if personal customer information is unnecessarily processed 
- AI may not understand unusual logistics terminology

## Mitigation 
- Use only supplied information
- Do not infer missing details
- Human review for exceptions
- Minimise unnecessary personal data

## Version History 

### v1.0 Prompt: 
Delivery Summary
Customer: Sarah
Pickup: Two cartons from Sunshine warehouse, tomorrow morning
Delivery: Richmond, before 3:00 pm
Total weight: 18 kg
Handling: Fragile items—handle with care
Instruction: Call the customer before delivery


Test result: 
The prompt successfully identified the main shipment details, including pickup and delivery locations, delivery date and deadline, number of packages, weight, special handling requirements, and customer instructions. The output was clear and easy to understand.

Problem: Output was not consistent and important fields could be missed. 

### v1.1 Changes: Added role, fixed fields, grounding instruction and missing-information rule.

Result: The output became more structured and predictable.
