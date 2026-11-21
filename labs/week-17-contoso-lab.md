# Week 17 lab (optional): Copilot and AI agents

A bonus weekend. Saturday uses Copilot across Sales and Customer Service on Contoso; Sunday builds a fuller Contoso agent that creates cases.

Copilot features and menus change often. If a setting isn't where these steps say, look for the closest match, and skip anything your trial doesn't offer.

---

## Saturday 6 March: Copilot in Sales and Customer Service, end to end (about 45 minutes)

### Step 1 — Check Copilot is on

1. **Power Platform admin centre → Contoso → Settings → Features** (or **Copilot** settings): check Copilot features are allowed.
2. **Sales Hub → App settings → Copilot**: turned on (Week 8).
3. **Customer Service admin centre → Copilot**: turned on (Week 10).

### Step 2 — A sales scenario

1. Open **Harbour View Homes** → Copilot: **Summarise this account**.
2. Open an open opportunity → ask: **What are the next steps on this deal?**
3. Draft a quote follow-up email with Copilot. Change at least one sentence before you'd send it.
4. Ask a natural-language question: **Show me my opportunities closing this quarter.**

### Step 3 — A service scenario

1. Open the **Boiler showing error E119** case → Copilot: **Summarise**.
2. Ask: **What should I tell the customer?** Check it uses your knowledge article.
3. Draft a resolution email; edit it; resolve the case.

### Step 4 — Responsible AI check (15 minutes)

1. Sign in as **Priya Nair** (InPrivate) and ask Copilot about an opportunity. What happens? Copilot respects her security role.
2. Discuss: Northwind holds health information. What should never go into a Copilot prompt or answer? Who reviews AI output before it reaches a patient?

### Saturday checks

- [ ] You used Copilot for an account summary, an email draft and a case summary.
- [ ] You saw Copilot respect Priya's security role.
- [ ] You can name two things a human must always check in Copilot output.

---

## Sunday 7 March: build a Contoso agent that creates cases (about 75 minutes)

Build on **Contoso Repair Helper** from Week 14, or create it again.

### Step 1 — Agent setup

| Part | Value |
| --- | --- |
| Name | Contoso Repair Helper |
| Knowledge | Published Contoso knowledge articles only |
| Instructions | Answer appliance questions from articles; never quote prices; hand over to a person for safety issues (gas smell) |

### Step 2 — “Book a repair” topic

1. **Topics → + Add a topic → From blank**. Name: `Book a repair`. Trigger phrases: *book a repair*, *my appliance is broken*, *I need an engineer*.
2. Add **Question** nodes and save each answer in a variable:

   | Question | Variable | Entity |
   | --- | --- | --- |
   | What's your name? | varName | User's entire response |
   | What's your email address? | varEmail | Email |
   | What's the appliance serial number? | varSerial | User's entire response |
   | What's the fault? | varFault | User's entire response |

3. Add **Call an action → Create a flow**. In the flow (Power Automate opens):
   - Inputs: Name, Email, Serial, Fault.
   - **Dataverse → List rows** on **Appliances**, filter `cnt_serialnumber eq '<Serial>'`, row count 1.
   - **Dataverse → Add a new row** on **Cases**: Case Title = `Repair: ` + Fault, Customer = the appliance's account, Appliance = the found appliance, Case type = Warranty.
   - **Respond to the agent** with the case number (Case Number / ticketnumber).
4. Back in the topic, send a message: `Thanks {varName}, your repair is logged as case {case number}. We'll be in touch within 2 working days.`
5. **Save**.

### Step 3 — Test and publish

1. Test with serial **BX-1001** (Peak Homes boiler from Week 4). Check a Warranty case appears in Contoso and lands in the Warranty queue.
2. Run your 10 test questions from Week 14 again.
3. **Publish → Channels → Microsoft Teams** and try the agent in Teams.

### Step 4 — Explore prebuilt agents (15 minutes)

Look at the prebuilt agents available in Sales and Customer Service in your trial. Discuss when a prebuilt agent is enough and when you'd build your own.

### Sunday checks

- [ ] “Book a repair” collects four answers and creates a case linked to the right appliance.
- [ ] The case lands in the Warranty queue.
- [ ] The agent still passes 8 of 10 knowledge questions.
- [ ] The agent works in Microsoft Teams.

---

## Consultant workshop

AI use-case discovery: list three Contoso processes where AI would help, what data each needs, the risk, and how success is measured.
