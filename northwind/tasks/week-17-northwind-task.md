# Week 17 Northwind task (optional): a patient-facing agent

**Due:** Sat 13 March (see [due dates](README.md#due-dates)) · **Technique:** [Week 17 Contoso lab](../../labs/week-17-contoso-lab.md)

## The brief

Receptionists answer the same 20 questions every day. Build an agent that answers them from the knowledge base and logs complaints as cases, without ever exposing medical or contract data.

## Client material

- Your Week 10 knowledge base · [Client brief](../01-client-brief.md) (data rules)

## Deliver

1. A **Copilot Studio agent** that answers the 20 common reception questions from your knowledge articles.
2. A **complaint topic** that collects details and creates a case routed to the complaints queue.
3. A **test set** of 10 questions, including ones the agent must refuse or hand over, with results.
4. Screenshots or a recording of the agent working.

## Pass checks

- [ ] The agent answers at least 8 of 10 test questions correctly.
- [ ] It never shows medical or contract data.
- [ ] Every complaint creates a case in the complaints queue.

## Hints

- Write the agent's instructions as rules: what it may answer, what it must refuse, when it hands over to a person.
- What should it say if someone describes a medical emergency?
