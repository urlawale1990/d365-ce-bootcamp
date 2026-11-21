# Week 2 Northwind task: accounts, contacts, activities and a region view

**Due:** Sat 28 November (see [due dates](README.md#due-dates)) · **Technique:** [Week 2 Contoso lab](../../labs/week-02-contoso-lab.md)

## The brief

Northwind's interactions live in a shared inbox and 12 phone lines. Load the first two weeks of contact history so every clinic and client has a proper timeline.

## Client material

- [Week 2 call sheet](../week-02-call-sheet.csv): 15 interactions
- [Week 2 accounts, contacts and activities](../week-02-accounts-contacts-activities.md): the records to create
- [Stakeholders](../02-stakeholders.md)

## Deliver

1. **14 accounts:** 8 clinics and 6 corporate clients.
2. **20 contacts**, each linked to the right account.
3. **15 activities**, each with the right activity type and Regarding set, and follow-ups as tasks with due dates.
4. A personal view **Clinics by region** that shows only the clinics, with their city.
5. Screenshots: the accounts list, one clinic's timeline, and the view.

## Pass checks

- [ ] One Fabrikam Logistics account, not two.
- [ ] Every activity appears on the correct account's timeline.
- [ ] Phone calls, emails and meetings use the matching activity type; nothing is logged as a plain note.
- [ ] Follow-ups are tasks with due dates; the two complaints are marked High.
- [ ] The view shows the 8 clinics and no corporate clients.

## Hints

- Which activity type does a “Meeting” become in Dynamics 365?
- How can a view tell clinics from corporate clients when both are accounts? Look at what the clinic names have in common.
- What would a good receptionist do with the London Bridge complaint, beyond logging it?
