# Week 1 — Onboarding, D365 CE, Power Platform and your trial environment

**One 2-hour session: Sunday 1 November.** Week 0 onboarding and Week 1 trial setup are merged into a single session. By the end of it, every learner has a Microsoft 365 work account and live Sales and Customer Service trials. Customer Insights follows if there's time, otherwise it's homework before Week 2. No later lab works without these, so this session is protected time for setup.

**Bring to the session:** a mobile phone for sign-in codes (MFA), a payment card for the Microsoft 365 sign-up (verification only), a laptop with an up-to-date Edge or Chrome, and a company name for your tenant, e.g. *ContosoJane*.

### Session plan (2 hours)

| Time | Block | Content |
| --- | --- | --- |
| 0:00–0:20 | Onboarding | Welcome, the course map, how weekends and the weekly Northwind capstone work, expectations (4 live hours + 3–4 hours self-study a week), key dates, class channel |
| 0:20–0:35 | The big picture | D365 CE apps (Sales, Customer Service, Customer Insights); Power Platform (Dataverse, Power Apps, Power Automate, Power BI, Copilot Studio); tenant → environments → apps |
| 0:35–1:05 | Lab Step 1 | Microsoft 365 Business Standard trial and work account |
| 1:05–1:40 | Lab Steps 2–3 | Sales and Customer Service trials; confirm both environments in the Power Platform admin centre |
| 1:40–1:50 | Lab Step 4 | Customer Insights trial (if time allows, otherwise homework) |
| 1:50–2:00 | Wrap-up | Trial rules, homework, GitHub usernames, see you Saturday 7 November |

Post "✅ M365 done" and "✅ D365 done" in the class channel as you finish each step so the trainer can see who needs help.

### Homework before Saturday 7 November

1. Finish any lab step you didn't complete, including Customer Insights (Step 4) and the admin tour (Step 5).
2. Create a Microsoft Learn profile with a **personal** Microsoft account (not the trial work account) and link it to a certification profile, so your badges and exams stay with you for life.
3. Send your GitHub username to the trainer for access to the course materials.
4. Complete the consultant workshop task (personal role map) and the Northwind capstone below.
5. Read the Week 1 Learn modules.

### Trial setup lab

**Step 1 — Create a Microsoft 365 work account (0:35–1:05)**

1. Go to the [Microsoft 365 Business Standard one-month trial](https://www.microsoft.com/en-gb/microsoft-365/business/microsoft-365-business-standard-one-month-trial) and start the free trial.
2. Enter a personal email to begin, then create the new organisation: company name, country (cannot be changed later), and a domain such as *contosojane.onmicrosoft.com*.
3. Create the admin user, e.g. *admin@contosojane.onmicrosoft.com*, set a strong password, and verify by phone.
4. Enter card details to verify. Then in the [Microsoft 365 admin centre](https://admin.microsoft.com) go to **Billing > Your products** and turn off recurring billing so it never charges.
5. Write down: tenant domain, admin username, password. This work account is the key to every trial that follows.

**Step 2 — Dynamics 365 Sales trial (1:05–1:25)**

1. Sign out of everything, open a new private window, go to the [Sales overview page](https://www.microsoft.com/dynamics-365/products/sales) and select **Try for free**.
2. Sign in with the new *onmicrosoft.com* admin account, complete the details, and select **Launch trial** when ready.
3. Confirm the Sales Trial app opens with sample data on the Dashboards page.

**Step 3 — Dynamics 365 Customer Service trial (1:25–1:40)**

1. From the [Customer Service product page](https://www.microsoft.com/dynamics-365/products/customer-service) select **Try for free** and use the same work account.
2. Wait for provisioning, then open the Customer Service workspace and view a sample case.

**Step 4 — Customer Insights trial (1:40–1:50)**

1. From the [Customer Insights page](https://dynamics.microsoft.com/ai/customer-insights/) select **Try for free** with the same work account. A work or school address is required; personal email is not accepted.
2. Start in Customer Insights – Journeys; Customer Insights – Data installs into the same environment.

**Step 5 — Tour the admin side (homework)**

1. Open the [Power Platform admin centre](https://admin.powerplatform.microsoft.com) and find the trial environments, their URLs and expiry dates.
2. Open [make.powerapps.com](https://make.powerapps.com) and switch between environments.
3. Bookmark: Microsoft 365 admin centre, Power Platform admin centre, Power Apps maker portal, each trial app URL.
4. Homework: log in to each trial at least once a week (see trial rules below).

### Trial rules learners must know

- Each D365 trial lasts 30 days and can be [extended once](https://learn.microsoft.com/en-us/power-platform/admin/trial-environments#extend-a-trial-standard-environment) for another 30 days in the Power Platform admin centre.
- A Customer Service trial expires if unused for 14 consecutive days, and an expired trial cannot be reactivated.
- Only one active trial per app at a time; a new trial is possible after the current one ends.
- Trials started on 1 November end on 1 December, or 31 December with the extension, which is before the course resumes after Christmas. **Export your solution in Week 8 (19–20 December)** and start fresh trials on 9 January (Week 9).
- Signing up with a personal email works, but blocks access to the Power Platform admin centre (no adding users, changing security roles or extending). That is why the Microsoft 365 work account comes first.

### Week 1 reading

- [Sign up for a Dynamics 365 Sales trial](https://learn.microsoft.com/dynamics365/sales/sign-up-for-sales-trial) and the [Sales trial FAQs](https://learn.microsoft.com/dynamics365/sales/sales-trial-faq)
- [Sign up for a Customer Service trial](https://learn.microsoft.com/dynamics365/customer-service/implement/try-customer-service) and the [Customer Service trial FAQ](https://learn.microsoft.com/dynamics365/customer-service/implement/trial-faq)
- [Customer Insights – Journeys trial sign-up](https://learn.microsoft.com/dynamics365/customer-insights/journeys/trial-signup)
- [Welcome to Dynamics 365 Sales](https://learn.microsoft.com/dynamics365/sales/overview)
- Microsoft Learn path: *Microsoft Power Platform Fundamentals* (PL-900 content) as background


### Microsoft Learn modules (in the bootcamp collection)

- [Microsoft Power Platform Fundamentals (PL-900)](https://learn.microsoft.com/training/paths/power-plat-fundamentals/) — learning path
- [Describe the foundations of Dynamics 365 customer engagement apps](https://learn.microsoft.com/training/modules/navigate-dynamics-customer-engagement-apps/) — module

## Consultant workshop (homework this week)

- **Skill:** The consultant role
- **Activity:** Functional vs technical vs solution architect; who does what on a project; RACI
- **Deliverable:** Personal role map

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — app recommendation note (extract):**

> *Contoso Home Services sells appliance service plans to homeowners and builders, and repairs appliances under warranty.*
>
> | Need | Recommended app | Why |
> | --- | --- | --- |
> | Track builder deals and service-plan quotes | Dynamics 365 Sales | Pipeline, quotes and forecasts for B2B selling |
> | Log and route repair requests, warranty SLAs | Dynamics 365 Customer Service | Cases, queues, SLAs, knowledge base |
> | Technician visits on site | Dynamics 365 Field Service *(phase 2)* | Scheduling and mobile work orders — not needed for go-live |
> | Reports and small automations | Power Platform | Power BI, Power Automate |

**Why this is good:** each app is tied to a business need, it says what is *not* needed yet, and it fits on one page. Now write the same for Northwind — don't copy the apps, work them out from the brief.

## Northwind capstone (complete during the week)

- **Task:** Set up a separate Northwind environment and admin account; write a 1-page note on which D365 apps Northwind needs and why
- **Deliver:** Working trial + app recommendation
- **Acceptance check:** Environment live; recommendation names Sales and Customer Service with reasons

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday 7 November: 2–3 learners present each week.
