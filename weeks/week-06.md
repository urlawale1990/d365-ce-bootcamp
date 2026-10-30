# Week 6 — Logic without code and solutions

- Saturday: business rules (form vs table scope), business process flows, classic workflows vs Power Automate (when to use which). Guided lab: 3 business rules on Appliance.
- Sunday: build a BPF for appliance installation; managed vs unmanaged solutions; export from one environment and import to another; turn on auditing for key tables and review audit history.
- Reading: *Create business rules*; *Business process flows overview*; *Solution concepts (ALM)*.
- Homework: Phase 2 checkpoint quiz (25 questions) + exported solution file.

**Week 6 special session: configuration vs customisation vs extension (45 minutes, replaces the usual 40-minute consultant workshop and feeds straight into the fit-gap)**

| Level | What it means | Who does it | Examples |
| --- | --- | --- | --- |
| Configuration | Using settings the app already provides | Functional consultant | SLAs, queues, product catalogue, forecasts, security roles |
| Customisation (low-code) | Changing the data model, UI and logic without code | Functional consultant | Tables, forms, views, business rules, BPFs, Power Fx, Power Automate, canvas apps |
| Extension (pro-code) | Writing code when low-code can't meet the need | Developer, briefed by the consultant | JavaScript on forms, C# plug-ins, PCF controls, Web API integrations, custom APIs |

- Trainer demo, no coding by learners: show a short form JavaScript, a plug-in registration in the Plug-in Registration Tool, and a PCF control on a form, so learners recognise each one.
- When to recommend each: always try configuration first, then low-code; recommend code only for complex validation across tables, heavy integrations, high-volume server-side logic or custom UI controls.
- Writing a gap specification for a developer: the requirement, why low-code can't meet it, expected behaviour, data involved, test cases, and the acceptance criteria.
- Exercise: classify 10 Contoso requirements into the three levels, then write one developer gap specification. These classifications become the Fit type column of the Week 6 fit-gap matrix.

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Fit-gap analysis
- **Activity:** Classify each story: out-of-box / configure / customise / third-party / gap; estimate effort
- **Deliverable:** Fit-gap matrix

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — fit-gap rows:**

| Story | Fit type | How it is met | Effort |
| --- | --- | --- | --- |
| US-07 Pipeline dashboard | Fit | Standard opportunity pipeline and dashboard | 0.5 day |
| US-12 Warranty routing | Configure | Routing rule on Case type | 1 day |
| US-18 Check warranty in ERP | Extend | Developer: API call from a flow or plug-in | 5 days |

**Contoso example — business rule:** *If Status = Decommissioned, then make “Decommission reason” required and lock “Install date”.*

**Why this is good:** standard features are tried first, every row says *how*, and the business rule enforces a real process rule.

## Northwind capstone (complete during the week)

- **Task:** Complete a fit-gap on all 20 stories; build 3 business rules and a booking BPF; export the solution
- **Deliver:** Fit-gap matrix + exported managed and unmanaged solution
- **Acceptance check:** Every story classified with effort; solution imports cleanly into a second environment

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
