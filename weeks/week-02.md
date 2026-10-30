# Week 2 — Using D365 like a user

- Saturday: app navigation, sitemap, global and relevance search, views vs forms, the timeline, personal settings. Guided lab: create 5 accounts and 10 contacts for Contoso.
- Sunday: log calls, emails, tasks and appointments; notes and attachments; advanced find and the modern view editor; export to Excel.
- Reading: *Get started with model-driven apps*; *Work with records in Dynamics 365*.
- Homework: a 1-page “user guide” for a Contoso salesperson.


### Microsoft Learn modules (in the bootcamp collection)

- [Describe shared activities and integration options in Dynamics 365 customer engagement apps](https://learn.microsoft.com/training/modules/examine-common-activities-integration-options/) — module
- [Get started with model-driven apps in Power Apps](https://learn.microsoft.com/training/modules/get-started-with-model-driven-apps-in-powerapps/) — module

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Stakeholders and discovery
- **Activity:** Stakeholder map; plan a discovery workshop; trainer plays the Contoso sales director
- **Deliverable:** Stakeholder register + workshop agenda

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — logging a call properly:**

| Field | Value |
| --- | --- |
| Activity type | Phone Call (not a Note) |
| Subject | Boiler not heating — asked for engineer visit |
| Regarding | Account: *Riverside Builders* |
| Call to | Contact: *Sam Brooks* |
| Follow-up | Task “Book engineer visit”, due tomorrow, owner: Service desk |

**Saved view “Builders in the North”:** Account · Relationship Type = Builder · Address 1: City is Manchester, Leeds or Sheffield · sorted by Account Name.

**Why this is good:** the right activity type, a clear subject, *Regarding* set so it shows on the account timeline, and a follow-up task so nothing is forgotten.

## Northwind capstone (complete during the week)

- **Task:** Load 10 clinics as accounts, 20 contacts, and log 15 activities from a supplied call sheet
- **Deliver:** Populated environment + saved view
- **Acceptance check:** Activities appear on the correct timelines; a personal view filters by clinic region

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
