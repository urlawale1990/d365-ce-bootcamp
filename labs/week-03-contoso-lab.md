# Week 3 lab: users, licences and security roles

Both labs run in the **Contoso** environment. Never post passwords in the class chat.

---

## Saturday 14 November: 4 users with licences (about 35 minutes)

### The users

| Name | Username | Job | Licence |
| --- | --- | --- | --- |
| Alex Morgan | alex.morgan@*yourtenant*.onmicrosoft.com | Sales Manager | Dynamics 365 Sales |
| Sam Patel | sam.patel@*yourtenant*.onmicrosoft.com | Salesperson | Dynamics 365 Sales |
| Priya Nair | priya.nair@*yourtenant*.onmicrosoft.com | Service Agent | Dynamics 365 Customer Service |
| Raj Singh | raj.singh@*yourtenant*.onmicrosoft.com | Service Manager | Dynamics 365 Customer Service |

Licence names in a trial look like *Dynamics 365 Sales Enterprise* or *Dynamics 365 Customer Service Enterprise*. Any trial licence that includes the app is fine.

### Step 1 — Create the users in Microsoft 365

1. [Microsoft 365 admin centre](https://admin.microsoft.com) → **Users → Active users → Add a user**.
2. Enter first name, last name, display name and username.
3. Let it create a password and tick **Require this user to change their password when they first sign in**. Keep the password private.
4. **Assign product licences:** tick the licence from the table above. **Next → Finish adding**.
5. Repeat for all four.

### Step 2 — Add them to the Contoso environment

1. [Power Platform admin centre](https://admin.powerplatform.microsoft.com) → **Environments → Contoso → Settings → Users + permissions → Users**.
2. Select **+ Add user**, search for the user, and add them. This pulls them in straight away instead of waiting for the sync.

### Step 3 — Give each user a standard role

1. Select the user → **Manage security roles**.
2. Tick the role, then **Save**:

| User | Role for now |
| --- | --- |
| Alex Morgan | Sales Manager |
| Raj Singh | Customer Service Manager |
| Sam Patel | Salesperson (changed to a custom role on Sunday) |
| Priya Nair | Customer Service Representative (changed to a custom role on Sunday) |

A licence lets someone in; a security role decides what they can do. In a trial, roles are not given automatically.

### Saturday checks

- [ ] All 4 users exist in Microsoft 365 with the right licence.
- [ ] All 4 appear in Contoso's user list.
- [ ] Each one has a security role.

---

## Sunday 15 November: custom roles and testing access (about 35 minutes)

### Step 1 — Create Contoso Sales Rep

1. Contoso → **Settings → Users + permissions → Security roles**.
2. Select **Salesperson → Copy**. Name it `Contoso Sales Rep`. **Save**.

### Step 2 — Create Contoso Support Agent

1. Select **Customer Service Representative → Copy**. Name it `Contoso Support Agent`.
2. Open the new role, search for the **Opportunity** table, and set **Read** to **None**. **Save**.

Business reason: Contoso doesn't want service agents seeing sales pipeline values.

### Step 3 — Assign the custom roles

| User | Remove | Add |
| --- | --- | --- |
| Sam Patel | Salesperson | Contoso Sales Rep |
| Priya Nair | Customer Service Representative | Contoso Support Agent |

Roles add up: if Priya keeps the old role as well, she can still see opportunities.

### Step 4 — Test as each user

1. Open an **InPrivate** (Edge) or **Incognito** (Chrome) window.
2. Sign in as **Sam Patel** and open Sales Hub. Opportunities should be visible.
3. Sign out, then sign in as **Priya Nair**. Try to open **Opportunities**. Access should be denied or the list empty.

### Step 5 — Teams and sharing (if time allows)

1. **Settings → Users + permissions → Teams → + Create team:** `Contoso Service Team`, type *Owner*, the top business unit. Add Priya and Raj.
2. In Sales Hub, open **Bristol Housing Co-op → Share** and share it with Sam Patel with Read access.

### Sunday checks

- [ ] Contoso Sales Rep and Contoso Support Agent exist.
- [ ] Sam and Priya have only their custom roles.
- [ ] Signed in as Priya, opportunities can't be seen.
- [ ] You can explain: privilege × access level = what a user can do, and to whose records.

---

## Homework

Fill in a **security matrix** for Contoso: one row per role, one column per table (Account, Contact, Opportunity, Case), with the access level for Read, Write and Delete. Use the [security design and role matrix template](../templates/07-security-design-and-role-matrix.md).
