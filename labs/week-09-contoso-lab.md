# Week 9 lab: Customer Service fundamentals

The first weekend back after the break. Do **Step 0** before anything else, then both labs run in the **Customer Service Hub** (or Customer Service workspace) in your new **Contoso** environment.

Admin centre menus change often. If a name doesn't match exactly, look for the closest match.

---

## Step 0 — Rebuild Contoso on your new trial (Saturday 9 January, start of class)

1. Start new **Sales** and **Customer Service** trials with your Microsoft 365 work account, as in [Week 1](week-01-contoso-lab.md). Extend the Microsoft 365 trial, or start a new one if it has expired.
2. Name the environments **Contoso** and **Northwind** again, and check both have Sales and Customer Service installed.
3. In Contoso: **make.powerapps.com → Solutions → Import solution** → your **unmanaged** Contoso Configuration 1.0.0.2 zip → **Import**. Then **Publish all customisations**.
4. Re-create the 5 accounts and 10 contacts from [Week 2 lab data](week-02-contoso-lab-data.md), or import your Week 8 Excel exports with **Import from Excel**.
5. Add at least 4 appliances again (Week 4 Step 7 and Week 5 Step 1).
6. Do the same for Northwind with your Northwind solution, on your own during the week.

Check: the Contoso Service app opens and shows Appliances.

---

## Saturday 9 January: cases from start to finish (about 35 minutes, after Step 0)

### Step 1 — Subjects

**Customer Service admin centre → Case settings → Subjects** (or Service Management → Subjects). Create:

- Boilers
- Ovens
- Fridges
- Washing machines
- Gas safety

### Step 2 — Add Warranty to Case type

1. In Contoso Configuration: **Add existing → Table → Case** if it isn't there.
2. **Case → Columns → Case type** → edit its choice → add **Warranty**. **Save** and **Publish**.

### Step 3 — Log and resolve 5 cases

**Cases → + New** for each. Link Appliance where you have one.

| # | Case title | Customer | Contact | Subject | Case type | Priority | Origin |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | Boiler showing error E119 | Riverside Builders | Sam Brooks | Boilers | Warranty | High | Phone |
| 2 | Oven door hinge broken | Peak Homes Ltd | Aisha Rahman | Ovens | Problem | Normal | Email |
| 3 | Gas safety certificate request, 12 flats | Northgate Lettings | Grace Okafor | Gas safety | Request | Normal | Web |
| 4 | Fridge not cooling | Bristol Housing Co-op | Fatima Ali | Fridges | Warranty | High | Phone |
| 5 | How do I bleed a radiator? | Thames Property Group | Oliver Grant | Boilers | Question | Low | Email |

Then:

1. **Resolve** case 5 with resolution `Sent radiator bleeding guide`.
2. **Resolve** case 1 with resolution `Engineer re-pressurised boiler`, after logging a phone call on it.
3. **Cancel** case 3 with a note: `Customer booked with another provider`.

### Step 4 — Parent and child cases

1. Create case `Boilers failing across Riverside site` for Riverside Builders.
2. Open case 1 (or a new Riverside case) → **Parent case** = the site-wide case.
3. Try to resolve the parent. Check the setting under **Case settings → Parent and child case settings** to see what happens to child cases.

### Saturday checks

- [ ] Five subjects exist; Case type includes Warranty.
- [ ] Five cases logged; two resolved, one cancelled, two still open.
- [ ] A parent case has at least one child.

---

## Sunday 10 January: queues, routing, entitlements and SLAs (about 70 minutes)

### Step 1 — Warranty queue

**Customer Service admin centre → Queues → + New:** name `Warranty`, type *Private*, members Priya Nair and Raj Singh.

### Step 2 — Basic routing rule

1. **Customer Service admin centre → Routing → Basic routing rule sets → + New:** `Contoso case routing`.
2. Rule item: **If** Case type equals Warranty, **then** route to queue **Warranty**.
3. **Save** and **Activate**.
4. Create a new Warranty case and select **Save & Route**. Check it lands in the Warranty queue.

### Step 3 — Entitlement

**Customer Service admin centre → Entitlements → + New** (or Service terms → Entitlements):

- Name: `Riverside Gold support 2027`
- Customer: Riverside Builders
- Start and end: 1 January – 31 December 2027
- Allocation type: Number of cases; Total terms: 10
- **Activate**

Open a new Riverside case and pick the entitlement. Remaining terms should drop to 9 when the case is resolved.

### Step 4 — Calendar and Warranty SLA

1. **Customer service schedule → + New:** `UK working hours`, Monday–Friday 08:00–17:30, time zone London.
2. **Service terms → SLA KPIs:** create `First response` (applicable on Case, KPI field *First Response By*) and `Resolve by` (*Resolve By*).
3. **Service terms → SLAs → + New:** `Warranty SLA`, table Case, calendar UK working hours.
4. Add two SLA items, each applicable when **Case type equals Warranty**:

   | SLA item | KPI | Warn after | Fail after | Success action |
   | --- | --- | --- | --- | --- |
   | Warranty first response | First response | 3 hours | 4 hours | — |
   | Warranty resolution | Resolve by | 1.5 days | 2 days | Email the customer “Your repair is booked” |

5. **Activate** the SLA and set it as the default, or set it on the Riverside entitlement.

### Step 5 — Test an SLA breach

Working-hour SLAs take hours to breach, so build a quick test copy:

1. Create a second SLA `Test SLA` with a 24×7 calendar and one item: First response, warn after **2 minutes**, fail after **5 minutes**.
2. Make it the default for a moment, create a Warranty case, and watch the timer on the form go from green to amber to red.
3. Switch the default back to Warranty SLA.

### Sunday checks

- [ ] A Warranty case goes to the Warranty queue with Save & Route.
- [ ] Riverside has an active entitlement with 10 cases.
- [ ] The Warranty SLA uses UK working hours and has two KPIs.
- [ ] You saw an SLA timer breach on the test case.

---

## Homework

Draft the **FRD for the Sales module** using the [FRD template](../templates/08-functional-requirements-document-frd.md). Every entry traces back to a requirement and forward to a test.
