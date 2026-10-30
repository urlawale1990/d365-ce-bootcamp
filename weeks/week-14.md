# Week 14 — Reporting and AI

- Saturday: reporting options (views, charts, dashboards, Excel templates, Power BI); Power BI Desktop with the Dataverse connector. Guided lab: a Contoso service performance report.
- Sunday: Copilot Studio basics — build an agent that answers questions from knowledge articles; Copilot features in Sales and Customer Service.
- Reading: *Power BI with Dataverse*; *Copilot Studio fundamentals*.
- Homework: publish the Power BI report and embed it in a dashboard; log capstone test results and defects in Azure DevOps.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Testing
- **Activity:** Test plan, test scripts from acceptance criteria, UAT planning; test cases and defects tracked in Azure DevOps linked back to user stories
- **Deliverable:** Test scripts for 10 stories

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — report page “Service performance”:** cases by month (line) · % cases meeting SLA (card) · average resolution days by appliance type (bar) · open cases by priority (table) · slicers for region and appliance type. Data source: Dataverse connector.

**Contoso example — test script:**

| Script | Step | Expected | Actual | Result |
| --- | --- | --- | --- | --- |
| TS-12 | Create case, type Warranty | Appears in Warranty queue | As expected | Pass |
| TS-12 | Change type to Repair | Moves to Repair queue | Stayed in Warranty | Fail → BUG-31 in Azure DevOps |

**Why this is good:** the report answers a manager's questions at a glance, and the test log is honest — a real test run finds defects.

## Northwind capstone (complete during the week)

- **Task:** Build a Power BI report on bookings and complaints; write test scripts for 10 stories and run them
- **Deliver:** Report + executed test scripts with defects logged
- **Acceptance check:** Report filters by clinic; scripts trace to acceptance criteria

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
