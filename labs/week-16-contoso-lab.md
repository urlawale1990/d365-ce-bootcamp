# Week 16 lab: UAT, go-live readiness and the capstone

Week 16 is about thinking like a consultant. Saturday's exercise uses Contoso to practise UAT and a go/no-go decision; Sunday is your Northwind capstone presentation.

---

## Saturday 27 February: run UAT on Contoso and decide go or no-go (about 50 minutes)

### Step 1 — Run 5 test scripts

Work in pairs: one person is the **tester**, the other the **business user** who signs off. Run each script in the Contoso environment and record the actual result.

| Script | Steps | Expected result |
| --- | --- | --- |
| TS-01 Log a call | Open Riverside Builders → log a phone call with Regarding set | Call shows on the account timeline |
| TS-05 Qualify a lead | Create a lead → Qualify | Account, contact and opportunity created and linked |
| TS-09 Discount quote | Quote 40 Silver plans on Builders 2027 | Total £4,560 with the Builder discount |
| TS-12 Warranty routing | Create a case with Case type = Warranty → Save & Route | Case lands in the Warranty queue |
| TS-15 Security | Sign in as Priya Nair → open Opportunities | Access denied |

### Step 2 — Log results and defects in Azure DevOps

1. Open your **Contoso CRM** project from Week 4.
2. For each script, record **Pass** or **Fail**.
3. For any failure, create a **Bug** work item: title, steps to reproduce, expected vs actual, severity (1–4), linked to the user story.

### Step 3 — Go/no-go checklist

Complete this honestly for Contoso:

- [ ] All Must stories passed UAT and are signed off
- [ ] No open Severity 1 or 2 defects
- [ ] Data migrated and record counts reconciled
- [ ] Users trained, licences and security roles assigned
- [ ] Hypercare rota for 2 weeks agreed
- [ ] Rollback plan written

Decide **Go** or **No-go**, and write two sentences explaining why. A no-go with a clear reason is a good answer.

### Saturday checks

- [ ] Five scripts run, each with an actual result.
- [ ] At least one bug logged properly (there's usually one to find).
- [ ] A go/no-go decision with a reason.

---

## Sunday 28 February: capstone presentations

Present your **Northwind** solution in 15 minutes. Suggested storyline:

1. **The problem in numbers** (2 minutes): what Northwind struggled with, from your BRD.
2. **One story end to end** (7 minutes): follow one patient enquiry or complaint from first contact to resolution.
3. **The manager's view** (2 minutes): dashboard or report.
4. **Results and go-live plan** (4 minutes): what you delivered against the BRD, what's left, and your go/no-go.

Checks before you present:

- [ ] Your demo data is ready and you've rehearsed the clicks once.
- [ ] You can show the solution, its publisher prefix, and that nothing is in Default.
- [ ] Your portfolio documents are in one folder, ready to submit.

## Homework

Submit your final portfolio.
