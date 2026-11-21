# Week 9 Northwind task: FRD for Sales, complaint and billing queues, SLAs

**Due:** Sat 16 January (see [due dates](README.md#due-dates)) · **Technique:** [Week 9 Contoso lab](../../labs/week-09-contoso-lab.md)

## The brief

The COO wants “no complaint to sit unanswered for more than 2 days”, and last year 14% of complaints took more than 10 working days. Build a working service desk for complaints and billing queries, and write the functional design for Sales.

## Client material

- [Client brief](../01-client-brief.md) · [Stakeholders](../02-stakeholders.md) (Priya Shah, Tom Walsh)
- [FRD template](../../templates/08-functional-requirements-document-frd.md)

## Deliver

1. **FRD draft for Northwind Sales**: scope, processes, data model, forms, rules, reports, each entry tracing to a requirement.
2. **Queues** for complaints and billing queries.
3. **Routing rules** that send each type of case to the right queue.
4. **Two SLAs** with a working-hours calendar (e.g. complaints and billing), with first-response and resolution KPIs.
5. Test cases showing routing and SLA timers working, with screenshots.

## Pass checks

- [ ] A complaint case routes to the complaints queue and shows SLA timers.
- [ ] A billing query routes to the billing queue.
- [ ] SLA times use working hours, and the complaint SLA meets the COO's 2-day target.
- [ ] Every FRD entry traces back to a requirement.

## Hints

- How will Dynamics 365 know a case is a complaint? Consider Case type or a subject.
- What warning time gives Priya's team a chance to act before a breach?
- Remember the call sheet complaints (London Bridge wait, Bristol receptionist) as test data.
