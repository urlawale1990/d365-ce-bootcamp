# Week 8 — Configuring Sales

- Saturday: Sales Hub app settings, product catalogue design, product families and bundles, sales territories, goals and goal metrics. Guided lab: build the Contoso catalogue.
- Sunday: forecasting, sales accelerator (work list, sequences, assignment rules), Copilot in Sales (30-minute hands-on slot: turn on Copilot features in app settings, record summaries, email drafting, opportunity insights and meeting prep — key AB-210 content).
- Reading: *Configure the product catalogue*; *Configure forecasts*; *Sales accelerator*.
- Homework: configure a quarterly forecast and one sequence.


### Microsoft Learn modules (in the bootcamp collection)

- [Manage and organize your product catalog with Dynamics 365 Sales](https://learn.microsoft.com/training/modules/manage-organize-product-catalog-dynamics-365-sales/) — module
- [Configure forecasts in Dynamics 365 Sales](https://learn.microsoft.com/training/modules/sales-forecasts/) — module
- [Set up Sales accelerator in Dynamics 365 Sales](https://learn.microsoft.com/training/modules/set-up-sales-accelerator/) — module
- [Create sales sequences with Sales Insights](https://learn.microsoft.com/training/modules/sales-sequence/) — module

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Security design
- **Activity:** Translate org chart into business units, roles, teams; least privilege
- **Deliverable:** Security design and role matrix

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — product catalogue:**

| Item | Value |
| --- | --- |
| Unit group | *Plan* (unit: 1 plan) |
| Products | Bronze plan £90 · Silver plan £120 · Gold plan £180 (family: *Service plans*) |
| Price list | *Builders 2027*, all three products priced |
| Discount list | *Builder*: 20–49 plans 5%, 50+ plans 8% |

**Contoso example — security matrix row:** Service Agent · Account: Read (organisation) · Opportunity: none · Case: Create/Write (business unit) · Contract value: hidden (field security).

**Why this is good:** products are published and every product has a price-list item, so quotes don't fail.

## Northwind capstone (complete during the week)

- **Task:** Design the security model; set up product catalogue for health packages, a sales goal and forecast
- **Deliver:** Security matrix + catalogue + forecast
- **Acceptance check:** Matrix matches configured roles; forecast shows Q-pipeline by rep

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
