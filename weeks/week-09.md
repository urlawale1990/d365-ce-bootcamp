# Week 9 — Customer Service fundamentals

- Saturday: case lifecycle, case form, subjects, parent/child cases, resolving and cancelling. Guided lab: log and resolve 5 cases.
- Sunday: queues, routing rules, entitlements, SLAs and SLA KPIs; test an SLA breach.
- Reading: *Dynamics 365 Customer Service overview*; *Create and manage queues*; *Define SLAs*.
- Homework: Contoso support process map (intake, routing, escalation).

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Functional Requirements Document (FRD)
- **Activity:** Structure of an FRD/FDD: scope, processes, data model, forms, rules, integrations, reports, NFRs
- **Deliverable:** FRD draft for the Sales module

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — Warranty SLA:**

| Setting | Value |
| --- | --- |
| Applies when | Case type = Warranty |
| Calendar | Mon–Fri 08:00–17:30, UK holidays |
| KPI 1: First response | 4 working hours (warning at 3) |
| KPI 2: Resolve by | 2 working days (warning at 1.5) |
| Success action | Email the customer “Your repair is booked” |

**Contoso example — FRD entry:** *FR-23 Warranty routing.* When a case with Case type = Warranty is created, a routing rule assigns it to the Warranty queue. Traces to US-12 and BR-02. Tested by TS-12.

**Why this is good:** SLA times use working hours, and every FRD entry traces back to a requirement and forward to a test.

## Northwind capstone (complete during the week)

- **Task:** Write the FRD for Northwind Sales; set up complaint and billing queues, 2 SLAs and routing rules
- **Deliver:** FRD draft + working service desk
- **Acceptance check:** A complaint case routes to the right queue and shows SLA timers

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
