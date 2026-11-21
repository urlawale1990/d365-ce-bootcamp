# Week 4 lab: Contoso data model

Two guided labs in the **Contoso** environment. Everything you build goes inside the **Contoso Configuration** solution, never the Default solution.

**Before you start:** check the environment name at the top right of [make.powerapps.com](https://make.powerapps.com) says Contoso, not Northwind.

---

## Saturday 21 November: solution and publisher (about 25 minutes)

### Step 1 — Create the solution and publisher

1. Go to [make.powerapps.com](https://make.powerapps.com), select the **Contoso** environment (top right), then **Solutions**.
2. Select **+ New solution**.
3. **Display name:** `Contoso Configuration`. The **Name** fills in as `ContosoConfiguration`.
4. Next to **Publisher**, select **+ New publisher** and enter:

   | Field | Value |
   | --- | --- |
   | Display name | Contoso Home Services |
   | Name | contosohomeservices |
   | Prefix | cnt |
   | Choice value prefix | leave the number that fills in |

5. **Save** the publisher, check it is selected, leave the version as `1.0.0.0`, then **Create**.

### Step 2 — Add the Account table

1. Open **Contoso Configuration**.
2. Select **Add existing → Table → Account → Next**.
3. **Don't** tick *Include all components*. Select **Add**.

Why: we only add what we change. Ticking *Include all components* pulls hundreds of objects into the solution.

### Step 3 — Create a global choice

1. In the solution, select **New → More → Choice**.
2. **Display name:** `Appliance type`.
3. Add four items: `Boiler`, `Oven`, `Fridge`, `Washing machine`.
4. **Save**.

### Step 4 — Make it your preferred solution (optional)

Solutions → select **Contoso Configuration** → **…** → **Set preferred solution**. New components you create elsewhere now land in it by default.

### Saturday checks

- [ ] The **Contoso Configuration** solution exists in Contoso.
- [ ] Its publisher is **Contoso Home Services** with prefix **cnt**.
- [ ] Account is in the solution, without all its components.
- [ ] The Appliance type choice's name starts with `cnt_`.
- [ ] Nothing new appears in the Default solution.

Anything named `new_` or `cr…` was created outside the solution. Delete it and create it again inside Contoso Configuration.

---

## Sunday 22 November: Appliance and Service Contract tables (about 70 minutes)

### Step 1 — Create the Appliance table

1. Open **Contoso Configuration** → **New → Table → Table**.
2. **Display name:** `Appliance` (plural: `Appliances`).
3. Open **Advanced options**: check **Record ownership** is *User or team*, and rename the **Primary column** to `Name`.
4. **Save**. The table's name is `cnt_appliance`.

### Step 2 — Add the Appliance columns

Open **Appliance → Columns → + New column** for each row:

| Display name | Data type | Required | Notes |
| --- | --- | --- | --- |
| Serial number | Single line of text, max 50 | Business required | |
| Appliance type | Choice → *Sync with global choice* → Appliance type | Business required | Use the choice from Saturday |
| Install date | Date only | Business required | |
| Account | Lookup → related table **Account** | Business required | Creates the Account 1:N Appliance relationship |
| Under warranty | Yes/No | Optional | |
| Warranty end | Formula | — | Formula below |

Formula for **Warranty end**:

```
DateAdd('Install date', 2, TimeUnit.Years)
```

### Step 3 — Set the relationship behaviour

1. Open **Appliance → Relationships**, then the many-to-one relationship to **Account**.
2. Set the behaviour so that deleting an account is **restricted** while it still has appliances (*Referential, restrict delete*, or *Custom* with Delete = *Restrict*).
3. **Save**.

Why: nobody should lose an appliance's service history by deleting a customer by mistake.

### Step 4 — Add an alternate key

1. **Appliance → Keys → + New key**.
2. **Display name:** `Serial number key`. Tick **Serial number**. **Save**.

The key stops two appliances having the same serial number, and lets imports update records instead of duplicating them.

### Step 5 — Create the Service Contract table

1. **New → Table → Table**. **Display name:** `Service Contract`; primary column `Contract number`; ownership *User or team*.
2. Add these columns:

| Display name | Data type | Required |
| --- | --- | --- |
| Account | Lookup → Account | Business required |
| Appliance | Lookup → Appliance | Optional |
| Start date | Date only | Business required |
| End date | Date only | Business required |
| Annual fee | Currency | Business required |
| Cover level | Choice (local): Basic, Standard, Premium | Optional |

### Step 6 — Add a rollup column to Account

1. Open **Account** (inside the solution) → **Columns → + New column**.
2. **Display name:** `Number of appliances`. **Data type:** Whole number. **Behaviour:** Rollup. **Save**, then **Edit** the rollup.
3. **Related entity:** Appliances (Account). **Aggregation:** COUNT of Appliance. **Save and close**.

### Step 7 — Test it

1. Open the **Appliances** table in **Edit** (data view) and add two appliances for **Peak Homes Ltd**:

   | Name | Serial number | Appliance type | Install date | Under warranty |
   | --- | --- | --- | --- | --- |
   | Peak Homes boiler 1 | BX-1001 | Boiler | 12 March 2025 | Yes |
   | Peak Homes oven 1 | OV-2001 | Oven | 1 September 2023 | No |

2. Check **Warranty end** shows 12 March 2027 for the boiler.
3. Try to add a third appliance with serial number `BX-1001`. It should be refused.
4. Open **Peak Homes Ltd** in Sales Hub. If **Number of appliances** isn't on the form yet, check it in the Accounts table data view. Recalculate it if it still shows 0 (rollups refresh on a schedule).

### Sunday checks

- [ ] Appliance (`cnt_appliance`) and Service Contract (`cnt_servicecontract`) exist inside Contoso Configuration.
- [ ] Both have a lookup to Account.
- [ ] Deleting Peak Homes Ltd is blocked while it has appliances.
- [ ] Warranty end calculates two years after the install date.
- [ ] Duplicate serial numbers are refused.
- [ ] Number of appliances on Peak Homes Ltd shows 2.
- [ ] Nothing new appears in the Default solution.

Forms, views and adding the new tables to an app come in Week 5.

---

## Sunday workshop: Contoso backlog in Azure DevOps (about 40 minutes)

### Step 1 — Set up Azure DevOps

1. Go to [dev.azure.com](https://dev.azure.com) and sign in. Create a free organization if asked.
2. **+ New project:** name `Contoso CRM`, visibility **Private**.
3. Under **Advanced**, choose the **Agile** work item process (so the item type is *User Story*). **Create**.
4. **Project settings → Boards → Project configuration:** add **Sprint 1** and **Sprint 2**, each two weeks long, starting Monday 23 November.

### Step 2 — Write and load the stories

Write **25 user stories** for Contoso and add each one in **Boards → Backlogs → + New Work Item**:

- **Title:** As a [role] I want [goal] so that [value].
- **Acceptance Criteria:** Given [situation] when [action] then [result you can test].
- **Priority:** 1 = Must, 2 = Should, 3 = Could.
- **Tags:** the requirement it comes from, e.g. `BR-02`.

Example:

> **As a service agent, I want warranty cases to go straight to the Warranty queue so that I don't sort them by hand.**
>
> Given a new case with Case type = Warranty, when it is saved, then it appears in the Warranty queue within 1 minute.
>
> Priority 1 · Tag BR-02

### Step 3 — Plan the sprints

Drag the Priority 1 stories into **Sprint 1** and the Priority 2 stories into **Sprint 2**.

### Workshop checks

- [ ] 25 stories on the backlog, each with a role, a goal and a reason.
- [ ] Every story has testable Given/When/Then acceptance criteria.
- [ ] Every story has a priority and a requirement tag.
- [ ] Sprint 1 holds only Must stories.

Use the [user story backlog template](../templates/03-user-story-backlog.md) to draft before you type them in.

---

## Homework

Draw the **Contoso entity relationship diagram**: Account, Contact, Appliance and Service Contract, with each relationship labelled 1:N or N:N. Paper, PowerPoint or draw.io are all fine. See the [ERD and data dictionary template](../templates/06-erd-and-data-dictionary.md).
