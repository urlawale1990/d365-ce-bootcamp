# Week 17 — Copilot and AI agents (optional, if time permits)

A bonus weekend after the capstone. Run it if the cohort finished on schedule, or offer it as a paid add-on or alumni session. It deepens the Copilot content from Weeks 8, 10 and 14 and prepares learners for AI-heavy interviews and the AB-210 and AB-620 exams.

**Saturday (2h): Copilot for the functional consultant**

| Time | Segment | Content |
| --- | --- | --- |
| 0:00–0:25 | The Copilot landscape | Microsoft 365 Copilot vs Copilot in Dynamics 365 vs Copilot Studio vs agents; what each is for and who licenses it |
| 0:25–0:50 | Setting it up | Enabling Copilot features in the Power Platform admin centre and app settings; data movement across regions; who can use what |
| 0:50–1:10 | Responsible AI and data security | How Copilot respects Dataverse security roles; sensitive data (Northwind health data!); human review of AI output |
| 1:10–1:55 | Guided lab | Enable and use Copilot in Sales and Customer Service end to end on Contoso: summarise an account, draft a quote email, summarise a case, draft a resolution reply, ask questions in natural language |
| 1:55–2:00 | Wrap-up | Prep for Sunday's build |

**Sunday (2h): build an agent with Copilot Studio**

- Lab (75 min): build a Contoso support agent in Copilot Studio that answers questions from knowledge articles and Dataverse data, adds a topic for “report a fault”, and calls a Power Automate flow to create a case. Publish it to Microsoft Teams and test it.
- Explore (15 min): the prebuilt agents in Sales and Customer Service available in the trial, and when to use a prebuilt agent vs build your own.
- Consultant workshop (30 min): AI use-case discovery — questions to ask a client, adding AI requirements to the fit-gap, governance and success measures.

**Reading:** *Copilot Studio fundamentals*; *Copilot in Dynamics 365 Sales*; *Copilot in Dynamics 365 Customer Service*; *Responsible AI FAQ for Dynamics 365 and Power Platform*.

**Northwind capstone:** a patient-facing agent that answers the 20 common reception questions from the knowledge base and logs complaints as cases routed to the complaints queue. Acceptance check: the agent answers 8 of 10 test questions correctly, never shows medical or contract data, and every complaint creates a case with the right queue.

**Certification link:** strengthens AB-210 (Sales AI Consultant) and prepares for AB-620 (AI Agent Builder Associate).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — agent design:**

| Part | Contoso choice |
| --- | --- |
| Agent | *Contoso Repair Helper* |
| Knowledge | Published knowledge articles only |
| Instructions | Answer appliance questions from articles; never quote prices; hand over to a person for safety issues (gas smell) |
| Topic | *Book a repair* → collect name, email, appliance serial, fault → flow creates a Warranty case → reply with case number |
| Test set | 10 questions: 8 answerable, 2 that must be refused or handed over |

**Why this is good:** the agent has clear limits, uses trusted knowledge only, and does real work (creates a case) instead of only chatting.
