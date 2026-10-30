# Week 12 — Power Automate

- Saturday: flow types, Dataverse connector, triggers and actions, conditions, expressions basics. Guided lab: email the account owner when a high-priority case is created.
- Sunday: approval flow for quote discounts over 10%; a scheduled flow for overdue tasks; error handling and run history.
- Reading: *Get started with Power Automate*; *Use the Dataverse connector*.
- Homework: one flow that solves a Contoso requirement of the learner's choice.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Environment strategy and ALM
- **Activity:** Dev / Test / UAT / Prod; Power Platform pipelines; deployment checklist; release notes
- **Deliverable:** Environment and deployment plan

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — flow design:**

| Part | Choice |
| --- | --- |
| Name | *Case — notify owner of high priority* |
| Trigger | Dataverse: when a Case row is added, filter `prioritycode eq 1` |
| Steps | Get the account owner → send email with case title and link |
| Settings | Environment variable *Service mailbox*; connection references for Dataverse and Outlook |
| Lives in | *ContosoService* solution |

**Why this is good:** the trigger is filtered so the flow only runs when needed, nothing is hard-coded, and it travels with the solution.

## Northwind capstone (complete during the week)

- **Task:** Build 2 flows (booking confirmation, overdue complaint escalation) using environment variables; write a deployment plan
- **Deliver:** Flows + environment and deployment plan
- **Acceptance check:** Flows deploy to Test as part of the managed solution without editing

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
