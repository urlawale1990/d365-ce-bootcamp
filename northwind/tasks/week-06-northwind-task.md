# Week 6 Northwind task: fit-gap, business rules, booking BPF and solution export

**Due:** Sat 19 December (see [due dates](README.md#due-dates)) · **Technique:** [Week 6 Contoso lab](../../labs/week-06-contoso-lab.md)

## The brief

Before building more, Northwind needs to know what fits out of the box and what doesn't. Then enforce the booking rules in the system and package your work so it can move between environments.

## Client material

- Your 20 user stories from Week 4
- [Fit-gap matrix template](../../templates/05-fit-gap-matrix.md)

## Deliver

1. A **fit-gap matrix** for all 20 stories: fit, configure, customise, third-party or gap, with how it's met and effort in days.
2. **Three business rules** on Booking (or another Northwind table) that enforce real rules from your BRD. At least one with table (entity) scope.
3. A **booking business process flow** with stages that match your to-be process.
4. Your Northwind solution exported as **managed** and **unmanaged** zips.
5. Proof the managed solution imports cleanly into a second environment (e.g. Contoso, then removed).

## Pass checks

- [ ] Every story is classified, with how it's met and an effort estimate.
- [ ] Each business rule traces to a requirement.
- [ ] The BPF guides a booking from first contact to completed.
- [ ] Both zips exist and the managed import works without errors.

## Hints

- Try standard features first; “customise” should be the exception, with a reason.
- Business rule ideas: what must be filled in before a booking is confirmed? What can't change after it's completed?
- **Before the break:** also export your data to Excel. Your trial ends by 31 December.
