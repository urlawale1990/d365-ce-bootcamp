# Week 14 lab: Power BI and Copilot Studio

Saturday builds a Contoso service report in Power BI; Sunday builds a simple agent in Copilot Studio. Both use the **Contoso** environment.

**Power BI Desktop runs on Windows only.** On a Mac, build the report in the Power BI service in your browser instead (**Create → Pick a published semantic model**, or ask the trainer for a shared model). You may need to start a free Power BI Pro trial with your work account to publish and share.

---

## Saturday 13 February: Contoso service performance report (about 50 minutes)

### Step 1 — Make sure there's data

You need at least 10 cases across different months, priorities and appliance types, with some resolved. Add more if needed.

### Step 2 — Connect to Dataverse

1. Open **Power BI Desktop** → sign in with your work account.
2. **Get data → Dataverse** → pick the **Contoso** environment.
3. Select the tables **Case** (incident), **Account** and **Appliance** (cnt_appliance) → **Transform data**.
4. Remove columns you don't need, keeping case title, created on, modified on, priority, status, case type, customer and appliance. **Close & Apply**.
5. In **Model view**, check Case → Appliance and Case → Account relationships exist (create them if not).

### Step 3 — Measures

Create these in the **Case** table (**New measure**):

```
Cases = COUNTROWS(incident)

Resolved cases = CALCULATE([Cases], incident[statecode] = 1)

Avg resolution days =
AVERAGEX(
    FILTER(incident, incident[statecode] = 1),
    DATEDIFF(incident[createdon], incident[modifiedon], DAY)
)
```

Modified On is a stand-in for the resolution date in this lab. In a real report you'd use the case resolution record or a resolved-on column.

### Step 4 — Build the “Service performance” page

| Visual | Fields |
| --- | --- |
| Line chart | Cases by month of Created On |
| Card | Resolved cases |
| Bar chart | Avg resolution days by Appliance type |
| Table | Open cases by Priority |
| Slicers | Appliance type; Account city (region) |

Give the page the title **Service performance** and check every visual responds to the slicers.

### Step 5 — Publish and embed

1. **Publish** to **My workspace** (or a shared workspace).
2. In the Power Platform admin centre or Contoso's advanced settings, turn on **Allow Power BI visualization embedding** (System settings → Reporting).
3. In the Contoso Service app, create a dashboard and add a **Power BI tile** or **Power BI dashboard** showing the report.

### Saturday checks

- [ ] The report connects to Contoso Dataverse.
- [ ] Five visuals and two slicers on one page.
- [ ] The report is published, and visible inside the Contoso Service app (if embedding is available in your trial).

---

## Sunday 14 February: an agent in Copilot Studio (about 60 minutes)

### Step 1 — Create the agent

1. Go to [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com), sign in with your work account, and select the **Contoso** environment (top right). Start a Copilot Studio trial if asked.
2. **Create → New agent**. Name: `Contoso Repair Helper`.
3. **Instructions:**

   > You help Contoso Home Services customers with appliance questions. Answer only from the knowledge provided. Never quote prices. If someone mentions a gas smell or a safety risk, tell them to call the gas emergency line and offer to connect them to a person.

### Step 2 — Add knowledge

Add your Week 10 knowledge articles as a knowledge source: **Knowledge → + Add knowledge → Dataverse** and pick the **Knowledge Article** table, or upload the five articles as documents if that option isn't available.

### Step 3 — Test with 10 questions

Use the **Test** pane:

| # | Question | Expected |
| --- | --- | --- |
| 1 | My boiler says E119, what does that mean? | Low pressure, top up to 1–1.5 bar |
| 2 | How do I bleed a radiator? | The steps from the article |
| 3 | My oven isn't getting hot | Check clock and fuse; element may need replacing |
| 4 | Fridge is warm | Thermostat, vents, defrost, then engineer |
| 5 | What does a gas safety certificate cover? | Annual check of appliances, flues, pipework |
| 6 | Do landlords have to give tenants the certificate? | Yes, a copy |
| 7 | What pressure should my boiler be? | 1–1.5 bar |
| 8 | My radiators have cold spots at the top | Bleed the radiator |
| 9 | How much is the Gold plan? | Refuses to quote prices |
| 10 | I can smell gas | Safety message and hand over to a person |

Pass mark: 8 of 10 answered as expected.

### Step 4 — Publish (optional)

**Publish**, then **Channels → Demo website** or **Microsoft Teams** to try it outside the test pane.

### Sunday checks

- [ ] Contoso Repair Helper answers from your knowledge articles.
- [ ] It refuses to quote prices and handles the gas safety question safely.
- [ ] At least 8 of 10 test questions pass.

---

## Homework

Publish the Power BI report and embed it in a dashboard. Then write test scripts for your capstone with the [test plan template](../templates/12-test-plan-and-test-scripts.md) and log results and defects in Azure DevOps.
