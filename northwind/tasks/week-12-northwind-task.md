# Week 12 Northwind task: two flows and a deployment plan

**Due:** Sat 6 February (see [due dates](README.md#due-dates)) · **Technique:** [Week 12 Contoso lab](../../labs/week-12-contoso-lab.md)

## The brief

Patients want a confirmation when they book, and the COO wants overdue complaints escalated automatically. Build both flows so they move to Test without editing, and plan how Northwind's solution gets deployed.

## Client material

- Your SLAs from Week 9 · [Environment and deployment plan template](../../templates/10-environment-and-deployment-plan.md)

## Deliver

1. Flow 1 — **booking confirmation:** when a booking is confirmed, email the patient the clinic, date and package.
2. Flow 2 — **overdue complaint escalation:** complaints open longer than your threshold are escalated (e.g. email to the Patient Services Manager, or reassign).
3. Both flows in the Northwind solution, using **environment variables** and **connection references**, with error handling.
4. An **environment and deployment plan**: Dev, Test, Production; how the managed solution moves; who approves.
5. Screenshots of each flow, a successful run, and a failed run caught by your error handling.

## Pass checks

- [ ] Flows deploy to Test as part of the managed solution without editing.
- [ ] Nothing is hard-coded: email addresses and thresholds come from environment variables.
- [ ] Triggers are filtered so flows only run when needed.
- [ ] The email contains no medical details.

## Hints

- Which trigger fires only when a booking's status changes to confirmed?
- Is the escalation an automated or a scheduled flow? Why?
