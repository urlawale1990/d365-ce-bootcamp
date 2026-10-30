# Week 11 — Customer Insights

- Saturday: Customer Insights – Data (unified customer profile) and – Journeys (real-time marketing). Guided lab: create a segment of Contoso customers.
- Sunday: build a marketing email, a form and a simple trigger-based journey; consent basics and GDPR.
- Reading: *Customer Insights – Journeys overview*; *Create segments*; *Create a journey*.
- Homework: a welcome journey for new service-contract customers.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Solution management
- **Activity:** Publishers and prefixes; managed vs unmanaged; solution layers; patches and upgrades; segmented solutions
- **Deliverable:** Solution strategy document

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — solution strategy (extract):**

| Decision | Contoso choice | Reason |
| --- | --- | --- |
| Publisher / prefix | Contoso Home Services / `cnt` | Every custom component is identifiable |
| Solutions | ContosoCore, ContosoSales, ContosoService | Smaller, independent deployments |
| Test / Prod | Managed only | Clean upgrades and uninstall |

**Contoso example — journey:** segment *Boiler owners, service due in 30 days, consent = Yes* → email “Time for your annual service” → wait 7 days → if not opened, send reminder.

**Why this is good:** the strategy gives a reason for each decision, and the journey respects consent.

## Northwind capstone (complete during the week)

- **Task:** Write Northwind's solution strategy; build a reminder journey for annual health checks in Customer Insights
- **Deliver:** Solution strategy + segment + journey
- **Acceptance check:** Strategy names publisher, prefix, managed/unmanaged policy; journey sends to the segment

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
