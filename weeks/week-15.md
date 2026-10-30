# Week 15 — Data and integration

- Saturday: data import wizard, import templates, data maps, duplicate detection rules, bulk delete, auditing. Guided lab: import 200 messy Contoso records and clean them.
- Sunday: Outlook app, Teams integration, Excel Online, SharePoint document management, server-side sync overview.
- Reading: *Import data*; *Duplicate detection*; *Integrate with Microsoft 365*.
- Homework: a data migration plan for Contoso (source, mapping, cleansing, validation).


### Microsoft Learn modules (in the bootcamp collection)

- [Load/export data and create data views in Dataverse](https://learn.microsoft.com/training/modules/load-export-data-create-data-views/) — module
- [Detect duplicate records and merge](https://learn.microsoft.com/power-platform/admin/detect-duplicate-records) — doc
- [Use Microsoft 365 services with model-driven apps and Dataverse](https://learn.microsoft.com/training/modules/use-services-model-driven-apps/) — module

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Data migration and training
- **Activity:** Migration plan and mapping; training needs analysis; user guides
- **Deliverable:** Migration mapping sheet + user guide

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — migration mapping:**

| Source column | Target | Transformation |
| --- | --- | --- |
| Cust_Name | Account.name | Trim spaces, title case |
| Email | Contact.emailaddress1 | Lowercase; duplicate check on email |
| Install_Dt | cnt_appliance.cnt_installdate | Convert all formats to DD/MM/YYYY; reject blanks |
| Region | Account.address1_city | Map “Mcr” → Manchester, “Ldn” → London |

**Contoso example — user guide page:** *Log a warranty repair.* Who: service agents · Steps 1–6 with screenshots · “If the appliance isn't listed…” troubleshooting box.

**Why this is good:** every column has a rule, decisions about bad data are written down, and the guide is one task per page.

## Northwind capstone (complete during the week)

- **Task:** Import 300 legacy Excel records with a mapping sheet and duplicate rules; write a receptionist user guide
- **Deliver:** Migration mapping + clean data + user guide
- **Acceptance check:** No duplicates; guide lets a classmate complete a booking unaided

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
