# Multi-agent customer service for a bank (n8n)

Project from my AI Business Automation Specialist training (Beam Institute of Technology, August 2026). Test data only.

## What it does
- Router agent classifies each inquiry into 5 categories. A code switch checks the result, anything unexpected goes to a human.
- Agent 1 answers product questions (fully autonomous).
- Agent 2 handles account operations and blocks a card on an antifraud hold, then hands the case to Agent 3.
- Agent 3 handles security incidents and acts only after human approval.
- Human-in-the-loop by email: confirm, edit or replace the agent's draft.
- Evaluation agent (Claude as independent judge, agents run on GPT-4o) scores every answer on 7 criteria.

## Results from testing
- 19 test inquiries, average quality score 4.4 of 5
- Same case: agent draft 3.9, after human edit 4.9
- The judge found a real design defect before a human noticed it

## Design principle
The more irreversible and visible an action, the lower the agent's autonomy.

## Files
- `MultiAgent_Bank_Customer_Service_n8n_Alexej_Kotelnikov.json`: n8n workflow, import via n8n > Import from file. Credentials and sheet IDs removed. Agent prompts are in Russian (course language), sticky notes in English.
- `Project_Showcase_MultiAgent_Bank_n8n_Alexej_Kotelnikov.pdf`: 2-page overview with the workflow canvas.
