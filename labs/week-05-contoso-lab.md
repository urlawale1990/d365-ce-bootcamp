# Week 5 lab: forms, views, dashboards and an app

Both labs run in the **Contoso** environment, inside the **Contoso Configuration** solution. You need the Week 4 tables (Appliance, Service Contract) first.

Menu names in Power Apps change from time to time. If one doesn't match exactly, look for the closest match.

---

## Saturday 28 November: forms and views (about 40 minutes)

### Step 1 — Add the columns this week needs

In **Contoso Configuration → Tables**:

| Table | New column | Data type |
| --- | --- | --- |
| Appliance | Appliance status | Choice (local): Ordered, Installed, Decommissioned (default Ordered) |
| Appliance | Decommission reason | Multiple lines of text |
| Case | Appliance | Lookup → Appliance |

To change **Case**, first **Add existing → Table → Case**, without all components.

### Step 2 — Redesign the Appliance main form

1. **Appliance → Forms → Information** (main form) → open in the form designer.
2. Rename the first tab **Summary**. Put these in it: Name, Serial number, Account, Appliance type, Install date, Warranty end, Appliance status, Under warranty.
3. Add a second tab **Service history** with two subgrids: **Cases** (related to this appliance) and **Service Contracts**.
4. **Header:** Warranty end, Owner.
5. Put **Decommission reason** in a section at the bottom of Summary.
6. **Save and publish**.

### Step 3 — Quick create and quick view

1. **Appliance → Forms → + New form → Quick create form:** Name, Serial number, Account, Appliance type, Install date. **Save and publish**.
2. Turn on quick create for the table: **Appliance → Properties → Advanced options → Allow quick create**. **Save**.
3. On the Appliance main form, add a **Quick view** component showing the account's **Account Card** quick view form, under the Account lookup.

### Step 4 — Three views

In **Appliance → Views**, create:

| View | Filter | Columns | Sort |
| --- | --- | --- | --- |
| Active appliances | Appliance status is not Decommissioned | Name, Account, Appliance type, Install date | Name |
| Warranty ending in 30 days | Warranty end is in the next 30 days | Name, Account, Warranty end | Warranty end |
| Appliances by account | Status = Active | Account, Name, Appliance type | Account, then Name |

**Save and publish** each.

### Saturday checks

- [ ] The Appliance form has Summary and Service history tabs and a header.
- [ ] + New from the Appliances subgrid on an account opens the quick create form.
- [ ] The account's details show on the Appliance form via the quick view.
- [ ] Three new system views exist and return sensible records.

---

## Sunday 29 November: charts, dashboard, app, command button, email templates (about 70 minutes)

### Step 1 — Add test data

Create at least 4 more appliances across different accounts and types, and 3 cases linked to appliances (Case → Appliance lookup), so charts have something to show.

### Step 2 — Charts

In **Appliance → Charts**, create **Appliances by type** (column chart, legend Appliance type, count of Name). In **Case → Charts**, create **Open cases by priority**.

### Step 3 — Build the Contoso Service app

1. In the solution: **New → App → Model-driven app**. Name: `Contoso Service`.
2. In the navigation, add a group **Customers** (Accounts, Contacts) and a group **Service** (Appliances, Service Contracts, Cases).
3. **Save**, then **Publish**, then **Play** to test it.

### Step 4 — Service Manager dashboard

1. In the solution: **New → Dashboard → Classic dashboard** (2-column layout). Name: `Service Manager`.
2. Add 4 charts: Open cases by priority, Appliances by type, a **list** of the *Warranty ending in 30 days* view, and one more chart of your choice.
3. **Save**, then add the dashboard to the Contoso Service app navigation. **Publish** the app.

### Step 5 — “Mark as installed” command button

1. Open the **Contoso Service** app in the designer → **Appliances** → **…** → **Edit command bar** → **Main form**.
2. **+ New → Command**. Label: `Mark as installed`. Icon: any.
3. **Action:** Run formula. **OnSelect:**

   ```
   Patch(Appliances, Self.Selected.Item, {'Appliance status': 'Appliance status (Appliances)'.Installed})
   ```

4. **Visibility:** Show on condition from formula:

   ```
   Self.Selected.Item.'Appliance status' <> 'Appliance status (Appliances)'.Installed
   ```

5. **Save and publish**. Open an Ordered appliance in the app and test the button.

If the formula shows an error, check the column and choice names in the formula bar's autocomplete. They must match your display names exactly.

### Step 6 — Email templates

In Sales Hub, open **Settings → Templates → Email templates** (or the **App settings** area) and create two templates:

| Template | Type | Subject | Body (short) |
| --- | --- | --- | --- |
| Quote follow-up | Opportunity | Your Contoso service quote | Thank you for your interest. Your quote is attached… |
| Case received | Case | We’ve received your request | We’ve logged your request and an engineer will contact you within 2 working days… |

Insert the contact's first name with **Insert dynamic text**.

### Sunday checks

- [ ] The Contoso Service app opens with Customers and Service groups.
- [ ] The Service Manager dashboard shows 4 components.
- [ ] Mark as installed changes an Ordered appliance to Installed and then disappears.
- [ ] Two email templates exist.

---

## Homework

Finish the **Service Manager** dashboard with 4 charts, and draw the Contoso **as-is and to-be process maps** using the [process map template](../templates/04-as-is-to-be-process-map.md).
