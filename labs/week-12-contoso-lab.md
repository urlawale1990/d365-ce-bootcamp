# Week 12 lab: Power Automate

Three cloud flows for Contoso, all created **inside the Contoso Configuration solution** so they travel with it. Use the Contoso users from Week 3 as owners and approvers.

Always create flows from **Solutions → Contoso Configuration → New → Automation → Cloud flow**, not from the Power Automate home page, so they get connection references.

---

## Saturday 30 January: email the account owner about high-priority cases (about 45 minutes)

### Step 1 — Environment variable

1. In the solution: **New → More → Environment variable**.
2. Display name: `Service mailbox`. Data type: Text. Default value: your own work email address. **Save**.

### Step 2 — Create the flow

1. **New → Automation → Cloud flow → Automated**. Name: `Case — notify owner of high priority`.
2. Trigger: **Dataverse → When a row is added, modified or deleted**.

   | Setting | Value |
   | --- | --- |
   | Change type | Added |
   | Table name | Cases |
   | Scope | Organization |
   | Filter rows | `prioritycode eq 1` |

3. **+ New step → Dataverse → Get a row by ID:** table **Accounts**, Row ID = **Customer (Value)** from the trigger. Rename it `Get account`.
4. **+ New step → Dataverse → Get a row by ID:** table **Users**, Row ID = **Owner (Value)** from *Get account*. Rename it `Get owner`.
5. **+ New step → Office 365 Outlook → Send an email (V2):**

   | Field | Value |
   | --- | --- |
   | To | **Primary Email** from *Get owner* |
   | CC | the **Service mailbox** environment variable |
   | Subject | `High-priority case: ` + **Case Title** |
   | Body | Account name, case title, description, and a link to the case |

6. **Save**.

### Step 3 — Test

1. Create a case with **Priority = High** for Riverside Builders.
2. Open the flow → **Run history**. Check it succeeded and the email arrived.
3. Create a **Normal** priority case. The flow should **not** run: that's the filter working.

### Saturday checks

- [ ] The flow and its environment variable are in Contoso Configuration.
- [ ] A High case sends the email; a Normal case doesn't trigger the flow.
- [ ] You can read the run history and open each step's inputs and outputs.

---

## Sunday 31 January: an approval flow and a scheduled flow (about 70 minutes)

### Flow 2 — Approve quote discounts over 10%

1. **New → Automation → Cloud flow → Automated**. Name: `Quote — approve discount over 10%`.
2. Trigger: Dataverse **When a row is added, modified or deleted**. Change type *Added or Modified*, table **Quotes**, scope Organization, **Select columns** `discountpercentage`, filter rows `discountpercentage gt 10`.
3. **Approvals → Start and wait for an approval:** type *Approve/Reject – First to respond*. Title: `Discount approval: ` + quote **Name**. Assigned to: Alex Morgan's email. Details: quote name, customer, discount %, total amount.
4. **Condition:** *Outcome* is equal to `Approve`.
   - **If yes:** Dataverse **Update a row** on the quote: Description = `Discount approved by Alex Morgan`.
   - **If no:** **Send an email (V2)** to the quote owner: `Discount on ` + quote name + ` was rejected. Comments: ` + *Responses Comments*.
5. **Save** and test: open a draft quote, set **Quote Discount (%)** to 12, and save. Approve it from the **Approvals** centre in Power Automate (or the email), and check the quote's description.

### Flow 3 — Daily summary of overdue tasks

1. **New → Automation → Cloud flow → Scheduled**. Name: `Tasks — daily overdue summary`. Repeat every 1 day at 07:00, time zone London.
2. **Dataverse → List rows:** table **Tasks**, filter rows:

   ```
   statecode eq 0 and scheduledend lt @{utcNow()}
   ```

3. **Data operation → Create HTML table** from the *value* of List rows, with columns Subject and Due date (scheduledend).
4. **Condition:** `length(outputs('List_rows')?['body/value'])` is greater than 0.
   - **If yes:** **Send an email (V2)** to the **Service mailbox** variable, subject `Overdue tasks today`, body = the HTML table.
5. **Save**, then **Run** it manually to test.

### Error handling

1. In Flow 1, add a **Scope** called `Try` around the steps after the trigger, and a second scope `Catch` after it.
2. On `Catch`, select **… → Configure run after** → tick only **has failed** and **has timed out**.
3. Inside `Catch`, send an email to the Service mailbox: `Flow failed: ` + `workflow()?['run']?['name']`.
4. Test by temporarily breaking a step (e.g. a wrong table), run it, check the Catch email, then fix it.

### Sunday checks

- [ ] A 12% discount triggers an approval; approving it updates the quote.
- [ ] The scheduled flow emails a table of overdue tasks, and sends nothing when there are none.
- [ ] Flow 1 has Try/Catch scopes and you've seen the Catch run.
- [ ] All three flows sit in Contoso Configuration with connection references.

---

## Homework

Build **one flow that solves a Contoso requirement of your choice** from your BRD. Write down its trigger, filter, steps and what happens if it fails.
