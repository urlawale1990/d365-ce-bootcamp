# Week 2 lab: using D365 like a user

Both labs run in **Sales Hub** in the **Contoso** environment. Type everything in by hand: the point is to learn the forms, required fields and lookups.

---

## Saturday 7 November: accounts, contacts, search and views (about 40 minutes)

### Step 1 — Create 5 accounts and 10 contacts

Use the records in [Week 2 lab data](week-02-contoso-lab-data.md):

1. **Accounts → + New** for each of the 5 accounts → **Save & Close**.
2. For each account, open it and add its 2 contacts from the **Contacts** subgrid (**+ New Contact**), so the company fills in automatically.
3. Set each account's **Primary Contact** to the first contact listed for it.

### Step 2 — Find things

1. **Global search:** type `Brooks` in the search bar at the top. Sam Brooks should appear.
2. **Grid search:** in **Accounts**, use *Filter by keyword* to find `Peak`.
3. Switch the Accounts view from **My Active Accounts** to **All Accounts** and back.

### Step 3 — Views vs forms

1. Open **Riverside Builders**. This is the **form**: one record.
2. Go back. The list is a **view**: many records with columns and a filter.
3. Open the **Timeline** on Riverside Builders and post a note: `Interested in annual boiler servicing for 40 properties`.

### Step 4 — Personal settings

Select the **gear icon → Personalization settings** and change one setting, e.g. **Records per page** to 100 or **Time zone** to London.

### Saturday checks

- [ ] 5 accounts and 10 contacts exist, each contact linked to its account.
- [ ] Every account has a Primary Contact.
- [ ] Global search for "Brooks" finds Sam Brooks.
- [ ] You can explain view vs form in one sentence.
- [ ] One personal setting changed.

---

## Sunday 8 November: activities, views and Excel (about 45 minutes)

### Step 1 — Log 8 activities

Open each account and add the activity from its **Timeline (+)**, so **Regarding** is set automatically.

| # | Account | Type | Subject | Details |
| --- | --- | --- | --- | --- |
| 1 | Riverside Builders | Phone Call | Boiler not heating, asked for engineer visit | Call to Sam Brooks, direction Incoming |
| 2 | Riverside Builders | Task | Book engineer visit | Due tomorrow, priority High |
| 3 | Northgate Lettings | Email | Quote for 25 gas safety checks | To Tom Hughes |
| 4 | Northgate Lettings | Appointment | Site survey, Leeds portfolio | Next Tuesday 10:00–11:00, required: Grace Okafor |
| 5 | Peak Homes Ltd | Phone Call | Interested in annual servicing plan | Call with Dan Walsh, Outgoing |
| 6 | Thames Property Group | Task | Send service plan brochure | Due Friday, to Oliver Grant |
| 7 | Bristol Housing Co-op | Phone Call | Complaint: engineer missed appointment | Call from Fatima Ali, Incoming |
| 8 | Bristol Housing Co-op | Task | Call back with new appointment | Due today, priority High |

Leave the email as a draft if your trial can't send mail. Mark activity 1 as complete.

### Step 2 — Notes and attachments

On **Peak Homes Ltd**, add a timeline **Note** titled `Site list` and attach any small file (a text file or PDF).

### Step 3 — Build a personal view

1. **Accounts → Create view** (or **Edit columns** and **Edit filters**, then **Save as new view**).
2. **Filter:** Relationship Type equals **Customer** AND Address 1: City equals Manchester, Leeds or Sheffield.
3. **Columns:** Account Name, Address 1: City, Primary Contact, Main Phone.
4. **Sort:** Account Name A–Z.
5. **Save as:** `Customers in the North`.

Expected result: Riverside Builders and Northgate Lettings.

### Step 4 — Export to Excel

1. Open your **Customers in the North** view.
2. **Export to Excel → Export to Excel** (static worksheet).
3. Open the file and check it has the same rows and columns as the view.

### Sunday checks

- [ ] 8 activities, each showing on the right account's timeline.
- [ ] Every activity has Regarding set.
- [ ] Activity 1 is completed; the follow-up tasks are open with due dates.
- [ ] The personal view shows exactly 2 accounts.
- [ ] The Excel file matches the view.

---

## Homework

Write a 1-page user guide for a new Contoso salesperson: how to find an account, log a call properly and use the Customers in the North view. Screenshots welcome.
