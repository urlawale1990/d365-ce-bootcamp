# Northwind Week 2 data: accounts, contacts and activities

14 accounts (8 clinics, 6 corporate clients), 20 contacts and 15 activities, built from the [call sheet](week-02-call-sheet.csv). All names, phone numbers, emails and websites are fictional.

## Part A: 14 accounts

### 8 clinics

| Clinic | Address 1: City |
| --- | --- |
| Northwind Manchester Central | Manchester |
| Northwind Manchester Salford | Manchester |
| Northwind London Bridge | London |
| Northwind London Soho | London |
| Northwind Leeds North | Leeds |
| Northwind Leeds Central | Leeds |
| Northwind Birmingham | Birmingham |
| Northwind Bristol | Bristol |

### 6 corporate clients

| Account Name | Main Phone | Address 1: City | Website | Description |
| --- | --- | --- | --- | --- |
| Fabrikam Logistics | 0121 496 0201 | Birmingham | fabrikam.example | 240 staff, interested in Plus package |
| Adventure Works | 020 7946 0202 | London | adventureworks.example | Existing client, 2027 renewal |
| Tailspin Toys | 0161 496 0203 | Manchester | tailspintoys.example | Asked for Executive brochure |
| Wide World Importers | 0113 496 0204 | Leeds | wideworldimporters.example | New LinkedIn lead, wellness days |
| Litware Inc | 0117 496 0205 | Bristol | litware.example | Demo held, proposal due |
| Proseware | 020 7946 0206 | London | proseware.example | Referred by Adventure Works |

Fabrikam Logistics appears twice on the call sheet. Create it once.

## Part B: 20 contacts

Create each one from its account's **Contacts** subgrid, so the company fills in automatically.

| # | First | Last | Job title | Email | Mobile | Account |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Helen | Brooks | Patient | helen.brooks@mail.example | 07700 900301 | Northwind Manchester Central |
| 2 | Joe | Carter | HR Director | joe.carter@fabrikam.example | 07700 900302 | Fabrikam Logistics |
| 3 | Ravi | Mehta | Patient | ravi.mehta@mail.example | 07700 900303 | Northwind London Bridge |
| 4 | Lucy | Grant | Head of People | lucy.grant@adventureworks.example | 07700 900304 | Adventure Works |
| 5 | Oliver | King | Patient | oliver.king@mail.example | 07700 900305 | Northwind Leeds North |
| 6 | Mark | Evans | Benefits Manager | mark.evans@tailspintoys.example | 07700 900306 | Tailspin Toys |
| 7 | Sara | Ahmed | Patient | sara.ahmed@mail.example | 07700 900307 | Northwind Birmingham |
| 8 | Nina | Shaw | Wellbeing Lead | nina.shaw@wideworldimporters.example | 07700 900308 | Wide World Importers |
| 9 | Peter | Lowe | Patient | peter.lowe@mail.example | 07700 900309 | Northwind Bristol |
| 10 | Chris | Bell | Operations Director | chris.bell@litware.example | 07700 900310 | Litware Inc |
| 11 | Emma | Ward | Patient | emma.ward@mail.example | 07700 900311 | Northwind London Soho |
| 12 | Leo | Grant | Patient | leo.grant@mail.example | 07700 900312 | Northwind Manchester Salford |
| 13 | Anita | Rose | HR Manager | anita.rose@proseware.example | 07700 900313 | Proseware |
| 14 | Kate | Moss | Patient | kate.moss@mail.example | 07700 900314 | Northwind Leeds Central |
| 15 | Fiona | Clarke | Practice Manager | fiona.clarke@northwind.example | 07700 900315 | Northwind Manchester Central |
| 16 | James | Ortiz | Practice Manager | james.ortiz@northwind.example | 07700 900316 | Northwind London Bridge |
| 17 | Aisha | Begum | Practice Manager | aisha.begum@northwind.example | 07700 900317 | Northwind Leeds North |
| 18 | Tom | Riley | Practice Manager | tom.riley@northwind.example | 07700 900318 | Northwind Birmingham |
| 19 | Grace | Wu | Practice Manager | grace.wu@northwind.example | 07700 900319 | Northwind Bristol |
| 20 | Daniel | Price | Practice Manager | daniel.price@northwind.example | 07700 900320 | Northwind London Soho |

## Part C: 15 activities

Log each one from its account's timeline so Regarding fills in automatically. Choose the right activity type for each channel, and add the follow-up as a task with a due date.

| # | Account (Regarding) | Channel | With | Date | Subject | Follow-up (due) |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Northwind Manchester Central | Phone | Helen Brooks | Mon 2 Nov | Weekend opening hours for physio | — |
| 2 | Fabrikam Logistics | Email | Joe Carter | Mon 2 Nov | Interested in Plus package for 240 staff | Send Plus package quote (Fri 6 Nov) |
| 3 | Northwind London Bridge | Phone | Ravi Mehta | Tue 3 Nov | Complaint: 40-minute wait | Escalate complaint to Patient Services (Wed 4 Nov, High) |
| 4 | Adventure Works | Meeting | Lucy Grant | Tue 3 Nov, 10:00–11:00 | 2027 contract renewal discussion | Book follow-up renewal meeting (Tue 10 Nov) |
| 5 | Northwind Leeds North | Phone | Oliver King | Wed 4 Nov | Billing query: double charge | Pass double-charge query to Finance (Thu 5 Nov) |
| 6 | Tailspin Toys | Email | Mark Evans | Wed 4 Nov | Requested Executive package brochure | Send Executive package brochure (Fri 6 Nov) |
| 7 | Northwind Birmingham | Phone | Sara Ahmed | Thu 5 Nov | Is fasting needed for a blood test? | — |
| 8 | Wide World Importers | Phone | Nina Shaw | Thu 5 Nov | LinkedIn lead: wellness days | Qualify wellness-days lead (Mon 9 Nov) |
| 9 | Northwind Bristol | Email | Peter Lowe | Fri 6 Nov | Complaint: rude receptionist | Escalate complaint to Patient Services (Mon 9 Nov, High) |
| 10 | Litware Inc | Meeting | Chris Bell | Fri 6 Nov, 14:00–15:00 | Demo of health-check packages | Send health-check proposal (Fri 13 Nov) |
| 11 | Northwind London Soho | Phone | Emma Ward | Mon 9 Nov | Request to move appointment | — |
| 12 | Fabrikam Logistics | Phone | Joe Carter | Mon 9 Nov | Asked about 10% volume discount | Update quote with 10% volume discount (Wed 11 Nov) |
| 13 | Northwind Manchester Salford | Email | Leo Grant | Tue 10 Nov | Lost results letter | Resend results letter (Wed 11 Nov) |
| 14 | Proseware | Email | Anita Rose | Tue 10 Nov | Referral from Adventure Works | Call Anita Rose back (Fri 13 Nov) |
| 15 | Northwind Leeds Central | Phone | Kate Moss | Wed 11 Nov | Billing query: corporate employee charged | Pass billing query to Finance (Thu 12 Nov) |
