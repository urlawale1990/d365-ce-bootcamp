# Week 3 Northwind task: users, roles, discovery interview and BRD v1

**Due:** Sat 28 November (see [due dates](README.md#due-dates)) · **Technique:** [Week 3 Contoso lab](../../labs/week-03-contoso-lab.md)

## The brief

Northwind has clinics in three regions and people who must see very different things. Set up who can do what, then run your first discovery interview and write the first version of the requirements.

## Client material

- [Client brief](../01-client-brief.md) · [Stakeholders](../02-stakeholders.md)
- Interview notes: released by your trainer **after** you have done your own mock interview
- [BRD template](../../templates/02-business-requirements-document-brd.md)

## Deliver

1. **Business units** for Northwind's regions.
2. **Four users** with licences: a receptionist, a clinic manager, a sales rep and a support lead.
3. A **security role** for each, copied from a standard role where one fits, and tested by signing in as each user.
4. **Interview notes** from a 20–30 minute mock interview with a classmate playing Amara Okafor, the COO.
5. **BRD v1** with at least 15 requirements, each with an ID, MoSCoW priority and source.
6. Screenshots: the users list with roles, and one test showing access denied.

## Pass checks

- [ ] Each user sees only what their role allows, proven by signing in as them.
- [ ] A receptionist can't see the sales pipeline.
- [ ] A clinic manager can't see cases from another region's clinics.
- [ ] The BRD has 15+ requirements, written as business needs (not solutions), with priority and source.
- [ ] Not everything is a Must.

## Hints

- Ask yourself for each role: what must they **read**, what must they **change**, and **whose** records?
- Which access level stops a Leeds manager seeing London's cases?
- Interview with open questions first (“Walk me through…”), then ask “why?” until you reach the business need.
