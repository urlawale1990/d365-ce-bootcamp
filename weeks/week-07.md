# Week 7 — Sales Hub, lead to cash

- Saturday: sales lifecycle; leads, qualification, opportunities, stakeholders, competitors; the lead-to-opportunity BPF. Guided lab: qualify 3 leads.
- Sunday: products, price lists, discount lists; quotes, orders, invoices; close won/lost.
- Reading: *Dynamics 365 Sales overview*; *Manage leads and opportunities*.
- Homework: take one deal from lead to invoice and record each step with screenshots.


### Microsoft Learn modules (in the bootcamp collection)

- [Explore Dynamics 365 Sales](https://learn.microsoft.com/training/modules/explore-dynamics-365-sales/) — module
- [Manage leads with Dynamics 365 Sales](https://learn.microsoft.com/training/modules/manage-leads-dynamics-365-sales/) — module
- [Manage opportunities with Dynamics 365 Sales](https://learn.microsoft.com/training/modules/manage-opportunities-dynamics-365-sales/) — module
- [Process sales orders with Dynamics 365 Sales](https://learn.microsoft.com/training/modules/process-sales-orders-dynamics-365-sales/) — module

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Data modelling and ERD
- **Activity:** Identify entities, attributes, relationships and cardinality; map to standard tables first
- **Deliverable:** Contoso ERD + data dictionary

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — ERD in words:** Account 1:N Contact · Account 1:N Appliance · Appliance 1:N Case · Appliance 1:N Service Contract · Account 1:N Opportunity → Quote → Order.

**Contoso example — worked quote:** Riverside Builders, 50 boiler service plans × £120 = £6,000, less 5% builder discount (from the *Builder* discount list) = **£5,700**.

**Why this is good:** the ERD matches what is actually built, and the discount comes from a discount list, not a number typed by hand.

## Northwind capstone (complete during the week)

- **Task:** Draw the Northwind ERD; configure the corporate wellness sales cycle lead → opportunity → quote
- **Deliver:** ERD + data dictionary + one closed-won deal
- **Acceptance check:** ERD matches what is built; quote uses a Northwind price list

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
