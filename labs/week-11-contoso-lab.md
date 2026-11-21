# Week 11 lab: Customer Insights – Data and – Journeys

Customer Insights needs its own trial. Its menus change often: if a name doesn't match exactly, look for the closest match.

---

## Step 0 — Start the Customer Insights trial (before class, Saturday 23 January)

1. From the [Customer Insights page](https://dynamics.microsoft.com/ai/customer-insights/) select **Try for free** with your work account.
2. Note which environment it installs into. If it creates a new environment, that's fine: you'll add Contoso test contacts there in Step 1.

---

## Saturday 23 January: unified profiles and a segment (about 45 minutes)

### Step 1 — Contoso contacts with consent

In the Customer Insights environment, open **Customer Insights – Journeys** and check the 10 Contoso contacts from [Week 2](week-02-contoso-lab-data.md) exist. If not, create them (or **Import from Excel**). Then set consent on 6 of them:

| Contact | Email consent (Contact point consent or Allow email) |
| --- | --- |
| Sam Brooks, Priya Shah, Tom Hughes, Grace Okafor, Dan Walsh, Aisha Rahman | Opted in / Allow |
| Oliver Grant, Mei Chen, Chris Evans, Fatima Ali | Not set |

Use email addresses you control (e.g. your own work address with +tags) if you want to see the emails arrive.

### Step 2 — Tour Customer Insights – Data (trainer-led, 15 minutes)

1. Open **Customer Insights – Data** with the sample data the trial provides.
2. Follow one customer through **Data sources → Unify → Customers**: several source records become one **unified customer profile**.
3. Look at a profile's activities, measures (e.g. total spend) and segments.

Discussion: why would Contoso want one profile for a landlord who appears in the service system, the billing system and the newsletter list?

### Step 3 — Build a segment of Contoso customers

1. **Customer Insights – Journeys → Audience → Segments → + New segment**.
2. Name: `Contoso customers with consent`.
3. Rule: Contact → **Account (Company Name) → Relationship Type** equals **Customer**.
4. Add a condition for email consent, as your trial offers it.
5. **Save** and **Mark as ready to use**. Check the member count.

Expected members: contacts at Riverside Builders, Northgate Lettings and Bristol Housing Co-op who have consent. That's Sam, Priya, Tom and Grace, so 4.

### Saturday checks

- [ ] You can explain a unified customer profile in one sentence.
- [ ] Consent is set on 6 contacts.
- [ ] The segment is live and returns 4 members.

---

## Sunday 24 January: email, form and a journey (about 70 minutes)

### Step 1 — Marketing email

1. **Channels → Emails → + New email**. Name: `Time for your annual service`.
2. Subject: `Time for your annual boiler service`. Body: greeting with the contact's **first name** (personalisation), two lines of text, and a button **Book my service** linking to a page of your choice.
3. Check the footer includes an unsubscribe link (or compliance settings). **Ready to send**.

### Step 2 — Marketing form

1. **Channels → Forms → + New form**. Name: `Book a service`.
2. Fields: First name, Last name, Email, Preferred date (date), with a consent tick box.
3. **Publish**, and preview it.

### Step 3 — Trigger-based journey

1. **Engagement → Journeys → + New journey → Trigger-based**.
2. Name: `Annual service reminder`.
3. Start: a trigger or the segment `Contoso customers with consent`, as your trial allows.
4. Steps:
   1. Send email **Time for your annual service**.
   2. Wait **7 days**.
   3. **If/then branch:** email opened? No → send the email again as a reminder.
5. **Publish** (or **Test** with your own contact if publishing is restricted in the trial).

### Step 4 — Consent and GDPR (discussion, 10 minutes)

- Why does the journey only reach contacts with consent?
- What happens when someone selects unsubscribe?
- What must Contoso record to prove consent?

### Sunday checks

- [ ] One email with personalisation and an unsubscribe link.
- [ ] One published form with a consent tick box.
- [ ] One journey with a wait and a branch, using your segment.

---

## Homework

Design a **welcome journey for new service-contract customers**: trigger, emails, waits and branches, on paper or in the trial. Then draft the Contoso **solution strategy** with the [solution strategy template](../templates/09-solution-strategy.md).
