# Week 15 lab: data import, duplicates and Microsoft 365 integration

Saturday imports 200 messy records into Contoso and cleans them. Sunday connects Contoso to Outlook, Teams, Excel and SharePoint.

**Lab file:** [week-15-contoso-messy-import.csv](week-15-contoso-messy-import.csv), 200 rows from Contoso's “old system”. All names and contacts are fictional.

What's wrong with it (on purpose):

| Problem | Examples |
| --- | --- |
| Extra spaces and wrong case in company names | `  Ashford Lettings `, `DOCKSIDE APARTMENTS`, `jubilee homes` |
| City abbreviations and capitals | `Mcr`, `Ldn`, `Brum`, `B'ham`, `Sheff`, `LEEDS` |
| Phone numbers in four formats | `0113 189 110`, `+44113550513`, `(0161) 825686`, `0161825686` |
| Dates in three formats | `08/05/2022`, `2021-04-25`, `16 May 2021` |
| Blank values | 8 rows with no email, 11 with no install date |
| Duplicates | 12 people appear twice, with the email in a different case |
| Appliance types that don't match the choice | `boiler`, `Washer`, `fridge freezer`, `Cooker` |

---

## Saturday 20 February: import and clean 200 records (about 55 minutes)

### Step 1 — Duplicate detection rule (before importing)

1. Contoso **Advanced settings → Settings → Data management → Duplicate detection rules → New**.
2. Name: `Contacts with same email`. Base and matching record type: **Contact**. Criteria: **Email**, *Exact match*, tick **Ignore blank values** and leave case-insensitive matching on.
3. **Save and close → Publish**.
4. In **Duplicate detection settings**, check *During data import* is ticked.

### Step 2 — Clean the file in Excel

Save a copy as `contoso-import-clean.xlsx` and fix:

1. **Company names:** a helper column with `=PROPER(TRIM(A2))`, then paste as values over Cust_Name. Check names like *Co-op* and *O'Brien* afterwards.
2. **Cities:** Find and replace `Mcr` → Manchester, `Ldn` → London, `Brum` and `B'ham` → Birmingham, `Sheff` → Sheffield, then PROPER the column.
3. **Emails:** `=LOWER(D2)`.
4. **Appliance type:** map `boiler` → Boiler, `Washer` → Washing machine, `fridge freezer` → Fridge, `Cooker` → Oven.
5. **Dates:** convert all to one format (DD/MM/YYYY). Leave blanks blank for now.
6. Write down every decision in a short **cleansing log** (what you changed and why).

### Step 3 — Import the accounts

1. Make a sheet with the **unique** company names and their city (Data → Remove duplicates), about 40 rows. Columns: `Account Name`, `Address 1: City`.
2. Save it as CSV. In Sales Hub: **Accounts → Import from CSV** (or Advanced settings → Data management → Imports).
3. Map `Account Name` and `Address 1: City`. Name the data map `Contoso legacy accounts` so you can reuse it. **Finish import**.

### Step 4 — Import the contacts

1. A sheet with: `First Name`, `Last Name`, `Email`, `Business Phone`, `Company Name` (the cleaned Cust_Name). Keep the duplicates in: the rule should catch them.
2. **Contacts → Import from CSV**. Map **Company Name** to the **Account** lookup (matched on Account Name).
3. After it finishes, open **Advanced settings → Data management → Imports** → your import → check **Failures** and **Duplicates**.

### Step 5 — Bulk delete a bad batch

1. **Advanced settings → Data management → Bulk record deletion → New**.
2. Find contacts created today with **Email** = blank. Name the job `Delete imported contacts with no email`, run it now.
3. Check the job's status and how many records it deleted.

### Saturday checks

- [ ] About 40 accounts imported with clean names and cities.
- [ ] Contacts imported and linked to their accounts.
- [ ] The duplicate rule caught the repeated people.
- [ ] A bulk delete job removed the contacts with no email.
- [ ] You have a cleansing log you could hand to a client.

Optional: import the appliances too (Serial, Appliance type, Install date, Account) and see the Serial number alternate key from Week 4 reject duplicates.

---

## Sunday 21 February: Outlook, Teams, Excel and SharePoint (about 60 minutes)

### Step 1 — Dynamics 365 App for Outlook

1. **Power Platform admin centre → Contoso → Settings → Email → Mailboxes** (or Advanced settings → Email configuration): check your own mailbox is **approved** and **tested**.
2. Enable the **Dynamics 365 App for Outlook** for your user (Advanced settings → Dynamics 365 App for Outlook → Add app for all eligible users, or just yourself).
3. Open Outlook on the web, open an email, open the Dynamics 365 add-in, and **Track** the email against Riverside Builders.

If mailbox approval isn't possible in your trial, the trainer demos this step.

### Step 2 — Microsoft Teams integration

1. In Sales Hub: **App settings → Chat and collaborate** (or Microsoft Teams collaboration) → turn on the basic Teams integration.
2. On an opportunity, use **Collaborate** to connect it to a Teams channel, and check the record appears as a tab in Teams.

### Step 3 — Excel Online

Open the **Active appliances** view → **Export to Excel → Open in Excel Online**. Change one appliance's install date, **Save**, and check the change lands in Dynamics 365.

### Step 4 — SharePoint document management

1. **Advanced settings → Settings → Document management → Document management settings**: tick **Appliance** and **Account**, enter a SharePoint site URL from your tenant (e.g. `https://yourtenant.sharepoint.com/sites/Contoso`; create the site first in SharePoint if needed).
2. Choose folder structure **Based on entity → Account**.
3. Open an appliance → **Related → Documents** → upload a PDF (e.g. a warranty card). Find it in SharePoint.

### Step 5 — Server-side sync overview (trainer, 5 minutes)

How server-side sync moves email, appointments and tasks between Exchange and Dynamics 365, and why it replaced the old email router.

### Sunday checks

- [ ] An email tracked from Outlook appears on Riverside's timeline (or you saw the demo).
- [ ] An opportunity is connected to Teams.
- [ ] A change made in Excel Online saved back to Dynamics 365.
- [ ] A document uploaded to an appliance is stored in SharePoint.

---

## Homework

Write a **data migration plan** for Contoso (source, mapping, cleansing rules, validation and counts) with the [data migration template](../templates/13-data-migration-mapping-user-guide-and-cutover-plan.md). Your cleansing log from Saturday is a good start.
