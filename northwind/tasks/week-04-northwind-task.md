# Week 4 Northwind task: user stories and the Northwind data model

**Due:** Sat 5 December (see [due dates](README.md#due-dates)) · **Technique:** [Week 4 Contoso lab](../../labs/week-04-contoso-lab.md)

## The brief

Your BRD says what Northwind needs. Now turn it into user stories, and design and build the core tables: clinics, the health packages Northwind sells, and the bookings patients make.

## Client material

- Your BRD v1 from Week 3
- [User story backlog template](../../templates/03-user-story-backlog.md) · [ERD and data dictionary template](../../templates/06-erd-and-data-dictionary.md)

## Deliver

1. A **Northwind solution** with its own **publisher** and prefix.
2. **20 user stories** from your BRD in Azure DevOps (or the template), each with Given/When/Then acceptance criteria, a priority and a link to its requirement.
3. Three custom tables in the solution: **Clinic**, **Health Package** and **Booking**, with sensible columns, choices and relationships.
4. A short table design note: each table's columns, data types and relationships, and why.
5. Screenshots: the solution's objects, each table's columns, and the backlog.

## Pass checks

- [ ] Every story has a role, a goal, a reason and testable acceptance criteria.
- [ ] All three tables sit in the Northwind solution with your prefix; nothing in Default.
- [ ] Every Booking links to a clinic and a patient.
- [ ] Relationship behaviours are chosen deliberately (e.g. what happens to bookings if a clinic closes?).

## Hints

- Is a patient a new table, or does Dataverse already have one that fits?
- Can one health package be offered at many clinics, and one clinic offer many packages? What relationship is that?
- Which Booking columns need a choice (e.g. status), and which need a lookup?
- Should Clinic replace the “account names starting with Northwind” workaround from Week 2?
