# Week 10 lab: knowledge, the agent workspace and Copilot in Customer Service

Both labs run in the **Contoso** environment, mainly in the **Customer Service workspace**. You need the Week 9 cases and subjects first.

Copilot and survey features in trials change often. If a setting isn't where these steps say, look for the closest match in the **Customer Service admin centre**, and skip anything your trial doesn't offer.

---

## Saturday 16 January: knowledge articles, workspace and Copilot (about 45 minutes)

### Step 1 — Write and publish 5 knowledge articles

**Customer Service workspace → Knowledge articles → + New** for each. Fill in Title, Keywords and Content, set the Subject, then move the article through **Approve** and **Publish**.

| Title | Keywords | Subject | Answer in brief |
| --- | --- | --- | --- |
| My boiler shows error E119 | boiler, E119, pressure | Boilers | Low water pressure. Check the gauge; top up to 1–1.5 bar; if it stays below 1 bar, book an engineer. |
| How to bleed a radiator | radiator, bleed, cold spots | Boilers | Turn heating off, use a radiator key, close when water appears, check boiler pressure after. |
| Oven not heating | oven, element, not heating | Ovens | Check the clock is set and the fuse; if the fan runs but no heat, the element needs replacing. |
| Fridge not cooling | fridge, warm, not cooling | Fridges | Check the thermostat setting, clear vents, defrost if iced; book an engineer if still warm after 24 hours. |
| What a gas safety certificate covers | gas safety, CP12, landlord | Gas safety | Annual check of every gas appliance, flue and pipework; landlords must give tenants a copy. |

### Step 2 — Link articles to cases

1. Open the open **Fridge not cooling** case in the Customer Service workspace.
2. In the **productivity pane** (right side), open **Knowledge search**. It suggests articles based on the case title.
3. **Link** *Fridge not cooling* to the case. Use **Email the content** or copy the link into an email draft.
4. Link the right article to two more cases.

### Step 3 — Explore the workspace

1. Open three cases at once and switch between their **session tabs**.
2. Use the productivity pane's **Smart assist** or **Agent scripts** if your trial shows them.
3. Open the **Customer summary** for a case.

### Step 4 — Copilot in Customer Service (30 minutes)

1. **Customer Service admin centre → Productivity → Copilot** (or **Copilot help pane**) → turn on: case summary, ask a question, write an email.
2. Open the **Boiler showing error E119** case → **Copilot → Summarise**.
3. In the Copilot pane, **Ask a question:** *What does error E119 mean?* Check Copilot answers from your knowledge article.
4. **Draft an email** to the customer explaining the next step. Edit it before you'd send it.

Discuss: what must an agent check before sending a Copilot-drafted reply?

### Saturday checks

- [ ] Five published knowledge articles with keywords and subjects.
- [ ] Three cases have a linked article.
- [ ] Copilot summarised a case and answered from your knowledge base.

---

## Sunday 17 January: omnichannel tour, surveys and analytics (about 60 minutes)

### Step 1 — Omnichannel and Contact Center (trainer demo, 20 minutes)

Watch the trainer show unified routing, chat and voice channels in the admin centre. No lab: these need extra licences and setup. Note for your FRD: which Contoso requests would suit chat?

### Step 2 — A case resolution survey (20 minutes)

Use whichever survey tool your trial offers (Customer Insights – Journeys forms and surveys, or Customer Voice):

1. Create a survey `How did we do?` with 3 questions: overall rating (1–5), was the problem fixed (Yes/No), comments (text).
2. Note how it would be sent when a case is resolved (an automated email or a Power Automate flow on case resolution).

### Step 3 — Customer Service analytics (20 minutes)

1. **Customer Service admin centre → Insights** (or Analytics) → turn on **Customer Service historical analytics**.
2. Open the analytics dashboard in the workspace. With few cases it will be thin; look at what it measures: incoming cases, resolution time, SLA compliance.
3. Create a personal view **Cases resolved this month** (status Resolved, modified this month).

### Sunday checks

- [ ] You can explain unified routing in one sentence.
- [ ] A 3-question resolution survey exists (or is designed on paper if your trial has no survey tool).
- [ ] Historical analytics is on, and you have a Cases resolved this month view.

---

## Homework

Configure a case-resolution survey and a service analytics view, and finish **FRD v1.0 with the RTM** using the [FRD template](../templates/08-functional-requirements-document-frd.md).
