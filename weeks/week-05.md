# Week 5 — The user interface

- Saturday: main, quick create and quick view forms; form sections, tabs, subgrids; system vs personal views. Guided lab: redesign the Appliance form.
- Sunday: charts, dashboards, interactive dashboards; build a model-driven app and sitemap that exposes the new tables; add a command bar button with Power Fx (e.g. “Mark as installed”); create email templates for quotes and case responses.
- Reading: *Design model-driven app forms*; *Create views, charts and dashboards*.
- Homework: a Contoso Service Manager dashboard with 4 charts.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Process mapping
- **Activity:** As-is and to-be maps for Contoso sales and service (swimlanes, BPMN basics)
- **Deliverable:** As-is and to-be process maps

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — Appliance main form layout:**

- **Tab 1 “Summary”:** Serial number, Account, Install date, Warranty end, Status
- **Tab 2 “Service history”:** subgrid of Cases for this appliance; subgrid of Service Contracts
- **Header:** Warranty end, Owner

**Views:** *Active appliances*, *Warranty ending in 30 days*, *Appliances by account*.

**Dashboard “Service manager”:** open cases by priority · cases by appliance type · warranties ending this month · average resolution days.

**Why this is good:** the most-used fields are on the first tab, related records appear as subgrids instead of extra fields, and every view answers a real question someone asks.

## Northwind capstone (complete during the week)

- **Task:** Map as-is and to-be booking process; build Booking forms, views and a clinic manager dashboard
- **Deliver:** Process maps + UI
- **Acceptance check:** Form follows the to-be process; dashboard shows bookings by clinic and status

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
