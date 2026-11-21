# Week 8 lab: configuring Sales, Copilot, and saving your work before the break

Both labs run in **Sales Hub** in the **Contoso** environment. This is the **last session before the trials end** (31 December). The export at the end of Sunday is not optional.

Copilot and sales accelerator features in trials change often. If a setting isn't where these steps say, look for the closest match in **App settings**, and skip anything your trial doesn't offer.

---

## Saturday 19 December: the Contoso catalogue, territories and goals (about 40 minutes)

You created a unit group, three products, a price list and a discount list in Week 7. Today you organise them properly.

### Step 1 — Product family with a property

1. **App settings → Product catalog → Families & products → Add family:** `Service plans`.
2. On the family, **Product properties → + New:** `Visits per year`, data type *Whole number*, default 1.
3. Move Bronze, Silver and Gold plan into the **Service plans** family (open each draft or revise each published product → set **Parent** = Service plans). Set Visits per year: Bronze 1, Silver 2, Gold 4.
4. **Publish** the family and its products.

### Step 2 — A new product and a bundle

1. **Add product:** `Gas safety certificate`, ID `GSC`, unit group Plan. Add it to **Builders 2027** at £65. Publish.
2. **Add bundle:** `Landlord bundle`, ID `BUN-L`, unit group Plan. Bundle products: Silver plan (1) and Gas safety certificate (1). Add it to Builders 2027 at £170. Publish.

### Step 3 — Sales territories

**App settings → Territories** (or Settings → Business management → Sales territories) → create:

| Territory | Manager | Members |
| --- | --- | --- |
| North | Alex Morgan | Sam Patel |
| South | Alex Morgan | — |

### Step 4 — A goal

1. **App settings → Goal metrics:** check **Revenue** exists (it's built in).
2. **Goals → + New:** `Sam Q1 2027 revenue`, metric Revenue, owner/manager Alex Morgan, goal owner Sam Patel, from 1 January to 31 March 2027, target £20,000. **Save** → **Recalculate**.

### Saturday checks

- [ ] Service plans family with a Visits per year property on each plan.
- [ ] Landlord bundle published and priced at £170.
- [ ] North and South territories exist.
- [ ] Sam has a Q1 2027 revenue goal.

---

## Sunday 20 December: forecasting, sales accelerator, Copilot and the export (about 70 minutes)

### Step 1 — Forecast (15 minutes)

1. **App settings → Forecast configuration → + New** → template **Org chart forecast**.
2. Name: `Contoso Q1 2027`. Hierarchy top user: Alex Morgan. Period: Quarterly, starting Q1 2027.
3. Activate it, then open **Forecasts** and view it. Edit Sam's Campus Lets Leeds opportunity to close in February 2027 with £3,000 and check it rolls up.

### Step 2 — Sales accelerator (15 minutes)

1. **App settings → Sales accelerator** (or **Get started with sales accelerator**) → turn it on for your security roles.
2. Create a **sequence**: `New lead follow-up` with 3 steps: Email (day 0), Phone call (day 2), Task “Send brochure” (day 5).
3. Connect it to a lead and open the **Work list** to see the next step.
4. If **Assignment rules** are available: create one that assigns leads from Liverpool to Sam Patel.

### Step 3 — Copilot in Sales (30 minutes)

1. **App settings → Copilot** (or **Copilot in Sales** settings) → turn Copilot on for Sales Hub.
2. Open the **Harbour View Homes** account → Copilot pane → **Summarise this account**.
3. Open the Campus Lets Leeds opportunity → ask Copilot **What’s new with this opportunity?**
4. Draft an email with Copilot: *Follow up on the appliance cover proposal and suggest a call next week.* Review and edit it before you would send it.
5. Ask Copilot to **prepare me for my meeting** with Campus Lets Leeds.

Discuss: what should a human always check in Copilot's output before it goes to a customer?

### Step 4 — Save your work before the trials end (15 minutes, everyone)

1. **Solutions → Contoso Configuration → Publish all customisations → Export solution**. Version `1.0.0.2`, **Unmanaged**. Download it. Export again as **Managed** and keep both. You'll import the unmanaged one in January so you can keep building.
2. Export the data you'll need again. For each, open the view, **Export to Excel**, and save the file:

   | Table | View |
   | --- | --- |
   | Accounts | All Accounts |
   | Contacts | All Contacts |
   | Appliances | Active appliances |
   | Service Contracts | Active Service Contracts |
   | Products | All Products (or screenshot the catalogue) |

3. Do the same for **Northwind**: export your Northwind solution (unmanaged) and its accounts, contacts and custom tables.
4. Save everything in one folder named `D365 bootcamp backup` on your own computer or OneDrive.

### Sunday checks

- [ ] A forecast shows Q1 2027.
- [ ] A 3-step sequence exists and appears on a lead's work list.
- [ ] Copilot summarised an account and drafted an email.
- [ ] **You have Contoso Configuration 1.0.0.2 (unmanaged and managed), your Northwind solution, and Excel exports saved outside the trial.**

---

## Over the break

On **9 January** you start new trials and import these files (Week 9 lab, Step 0). Without the export, you'd rebuild Weeks 4–8 by hand.
