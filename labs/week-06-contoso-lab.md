# Week 6 lab: business rules, a business process flow, solutions and auditing

Both labs run in the **Contoso** environment, inside the **Contoso Configuration** solution. You need the Week 5 columns (Appliance status, Decommission reason) first.

---

## Saturday 5 December: three business rules on Appliance (about 40 minutes)

Create each rule from **Appliance → Business rules → + New business rule**. Check the **Scope** (top right) before you save, then **Save** and **Activate**.

### Rule 1 — Decommissioning (scope: Appliance main form, or All Forms)

- **Condition:** Appliance status equals Decommissioned.
- **If true:** Set Business Required on **Decommission reason** = Business Required; Lock **Install date**.
- **If false:** Set Business Required on Decommission reason = Not Business Required; Unlock Install date.
- Name: `Decommission rules`.

### Rule 2 — Install date needed once installed (scope: All Forms)

- **Condition:** Appliance status equals Installed.
- **If true:** Set Business Required on **Install date** = Business Required.
- Name: `Installed needs install date`.

### Rule 3 — No warranty when decommissioned (scope: Entity)

- **Condition:** Appliance status equals Decommissioned.
- **If true:** Set Field Value: **Under warranty** = No.
- Name: `Decommissioned clears warranty`.

Scope **Entity** (table) means the rule runs on the server when the record is saved, even from an import or a flow. Form scope only runs while someone has the form open.

### Saturday checks

- [ ] On an appliance, choosing Decommissioned makes Decommission reason required and locks Install date.
- [ ] Choosing Installed makes Install date required.
- [ ] Change an appliance to Decommissioned in the table's data grid (not the form) and save: Under warranty becomes No.
- [ ] All three rules are Activated and sit in Contoso Configuration.

---

## Sunday 6 December: BPF, solution export and import, auditing (about 70 minutes)

### Step 1 — Appliance installation business process flow

1. In the solution: **New → Automation → Process → Business process flow**. Name: `Appliance installation`. Table: **Appliance**.
2. Build three stages:

   | Stage | Data steps |
   | --- | --- |
   | Order | Account (required), Appliance type (required), Serial number |
   | Install | Install date (required), Appliance status |
   | Handover | Under warranty, Owner |

3. **Save**, **Validate**, then **Activate**.
4. Open an Ordered appliance and move it through the three stages.

### Step 2 — Export the solution, managed and unmanaged

1. **Solutions → Contoso Configuration → Publish all customisations**.
2. Select **Export solution → Next**, increase the version to `1.0.0.1`.
3. Export as **Unmanaged** and download the zip. Then export again as **Managed**.

Keep both files. Unmanaged is your editable backup; managed is what you would deploy to Test or Production.

### Step 3 — Import the managed solution into Northwind, then remove it

1. Switch to the **Northwind** environment → **Solutions → Import solution**.
2. Browse to the **managed** zip → **Next → Import**.
3. Check the Appliance table appears in Northwind and can't be edited (it's managed).
4. **Delete** the solution from Northwind. Its tables disappear cleanly. That is the point of managed solutions.

Only do this with the managed file, and remove it afterwards so Northwind stays your own capstone.

### Step 4 — Turn on auditing

1. [Power Platform admin centre](https://admin.powerplatform.microsoft.com) → **Environments → Contoso → Settings → Audit and logs → Audit settings**.
2. Tick **Start auditing** and **Log access**. **Save**.
3. In the solution: **Appliance → Properties → Advanced options** → tick **Audit changes to its data**. **Save**. Do the same for **Account**.
4. Change an appliance's Appliance status, then open the record → **Related → Audit history**.

### Sunday checks

- [ ] The Appliance installation BPF shows on Appliance forms and moves through three stages.
- [ ] You have an unmanaged and a managed zip of Contoso Configuration 1.0.0.1.
- [ ] The managed import into Northwind worked and was removed.
- [ ] Audit history shows your change with old and new values.

---

## Homework

Take the Phase 2 checkpoint quiz and keep your **exported unmanaged solution file** safe. You will need it again in Week 8.
