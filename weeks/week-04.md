# Week 4 — Dataverse data model

- Saturday: tables (standard, custom, activity), column types, choices, calculated, rollup and Power Fx formula columns, alternate keys, 1:N and N:N relationships, relationship behaviours. Guided lab: create a *Contoso Configuration* solution and publisher.
- Sunday: build *Appliance* and *Service Contract* tables with relationships to Account; add choices and a rollup column. Then create a free Azure DevOps project and load the Contoso user stories onto a Boards backlog with priorities and sprints.
- Reading: *Create and manage tables in Dataverse*; *Manage columns and relationships*.
- Homework: draw the Contoso entity relationship diagram.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** User stories and acceptance criteria
- **Activity:** Write “As a… I want… so that…” stories with Given/When/Then criteria and manage them on Azure DevOps Boards
- **Deliverable:** Product backlog of 25 user stories

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — a user story with acceptance criteria:**

> **US-12** As a service agent, I want warranty cases to go straight to the Warranty queue so that I don't sort them by hand.
>
> **Given** a new case with Case type = Warranty, **when** it is saved, **then** it appears in the Warranty queue within 1 minute.
>
> Links to BR-02 · Priority: Must · Azure DevOps work item #34

**Contoso example — a custom table design:**

| Table | Column | Type | Required |
| --- | --- | --- | --- |
| Appliance (cnt_appliance) | Serial number | Text (50) | Yes |
| | Install date | Date only | Yes |
| | Account | Lookup → Account | Yes |
| | Warranty end | Formula column: Install date + 2 years | — |

**Why this is good:** the story is testable, it traces to a requirement, and the table lives in a solution with the `cnt` prefix — nothing in the Default solution.

## Northwind capstone (complete during the week)

- **Task:** Turn the BRD into 20 user stories; design and build Northwind tables (Clinic, Health Package, Booking)
- **Deliver:** Backlog + tables in a Northwind solution with its own publisher
- **Acceptance check:** Stories have acceptance criteria; all components sit in the solution, none in Default

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
