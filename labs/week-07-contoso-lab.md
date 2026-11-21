# Week 7 lab: Sales Hub, lead to cash

Both labs run in **Sales Hub** in the **Contoso** environment. Saturday works with leads and opportunities; Sunday sets up a small product catalogue and takes one deal from quote to invoice.

---

## Saturday 12 December: qualify 3 leads (about 40 minutes)

### Step 1 — Create 3 leads

**Leads → + New** for each:

| Topic | First / last name | Company | City | Business phone | Lead source | Description |
| --- | --- | --- | --- | --- | --- | --- |
| Boiler servicing for 60 flats | Lucy Price | Harbour View Homes | Liverpool | 0151 496 0301 | Web | Landlord with 60 flats, wants annual boiler servicing |
| Gas safety checks, new portfolio | James Cole | Greenleaf Estates | Nottingham | 0115 496 0302 | Trade show | Bought 30 houses, needs gas safety certificates |
| Appliance cover for student lets | Ella Turner | Campus Lets Leeds | Leeds | 0113 496 0303 | Partner referral | 25 student houses, interested in appliance cover |

### Step 2 — Work the lead-to-opportunity process

On each lead, use the **Lead to Opportunity Sales Process** bar at the top:

1. **Qualify stage:** fill in Existing contact? (No), Purchase timeframe, Estimated budget, Purchase process, Identify decision maker.
2. Select **Qualify** on the command bar. Dynamics 365 creates an **account**, a **contact** and an **opportunity**.
3. Open the new opportunity and check the account and contact are linked.

Expected budgets: Harbour View £7,000; Greenleaf £3,500; Campus Lets £3,000.

### Step 3 — Develop the Harbour View opportunity

1. Open **Boiler servicing for 60 flats** (the opportunity).
2. **Stakeholders:** add Lucy Price as *Decision maker*.
3. **Competitors:** create and add `BoilerCare UK`.
4. Move the process bar to **Develop** and fill in Customer need: `Annual servicing for 60 flats, one visit a year each`.
5. Log a **phone call** on the timeline: `Discovery call: confirmed 60 flats, wants a quote by Friday`.

### Saturday checks

- [ ] Three leads qualified into accounts, contacts and opportunities.
- [ ] Harbour View has a stakeholder, a competitor and a logged call.
- [ ] You can explain why Qualify creates three records, not one.

---

## Sunday 13 December: catalogue, quote, order, invoice, close (about 70 minutes)

Week 8 builds the full catalogue. Today you set up just enough to quote.

### Step 1 — Unit group

**App settings** (bottom-left area switcher in Sales Hub) → **Product catalog → Unit groups → + New**: name `Plan`, primary unit `Plan`. **Save**.

### Step 2 — Products

**Product catalog → Families & products → Add product** for each, using unit group **Plan** and default unit **Plan**:

| Name | Product ID | Decimals supported |
| --- | --- | --- |
| Bronze plan | PLAN-B | 0 |
| Silver plan | PLAN-S | 0 |
| Gold plan | PLAN-G | 0 |

Each product starts as **Draft**. Leave them for now; publish after Step 4.

### Step 3 — Discount list

**Product catalog → Discount lists → + New:** name `Builder`, type *Percentage*. Add ranges:

| Begin quantity | End quantity | Percentage |
| --- | --- | --- |
| 20 | 49 | 5 |
| 50 | 9999 | 8 |

### Step 4 — Price list

1. **Product catalog → Price lists → + New:** name `Builders 2027`, currency GBP, start 1 January 2027. **Save**.
2. Add **Price list items** for all three products, unit Plan, pricing method *Currency amount*: Bronze £90, Silver £120, Gold £180. Set **Discount list** = Builder on each.
3. Go back to each product, set **Default price list** = Builders 2027, then **Publish**.

### Step 5 — Quote

1. Open the **Harbour View** opportunity. Set **Price list** = Builders 2027.
2. **Product line items → + Add product:** Silver plan, quantity **40**.
3. Check the line: 40 × £120 = £4,800, less 5% Builder discount = **£4,560**.
4. Move the process to **Propose**, then **+ New Quote** from the Quotes subgrid. The products copy across.
5. On the quote: **Activate Quote**.

### Step 6 — Order and invoice

1. On the active quote: **Create Order**. Open the order and check the total is £4,560.
2. On the order: **Create Invoice**.

### Step 7 — Close the opportunities

1. **Harbour View** opportunity → **Close as Won**, actual revenue £4,560.
2. **Greenleaf Estates** opportunity → **Close as Lost**, status reason *Out-Sold*, competitor **BoilerCare UK**.

### Sunday checks

- [ ] Three products published, each with a Builders 2027 price.
- [ ] The Harbour View quote, order and invoice all show £4,560.
- [ ] Harbour View is Won; Greenleaf is Lost to BoilerCare UK.
- [ ] Campus Lets Leeds is still open (you'll use it in Week 8).

---

## Homework

Take one more deal from lead to invoice on your own and screenshot each step: lead, qualify, opportunity, quote, order, invoice, close.
