# Week 3 — Administration and security

- Saturday: tenants vs environments, environment types (trial, sandbox, production, developer), Power Platform admin centre, Microsoft 365 admin centre. Guided lab: add 4 users and assign licences.
- Sunday: security model — business units, security roles, teams, field security, record ownership and sharing. Lab: build a Sales Manager and Support Agent role and test access as each user.
- Reading: *Manage environments in Power Platform*; *Security concepts in Dataverse*.
- Homework: a security matrix table for Contoso (role × table × privilege).

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Requirements gathering
- **Activity:** Interview techniques, open vs closed questions; turn notes into requirements; MoSCoW priority
- **Deliverable:** Business Requirements Document (BRD) v1

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — one user, one role, tested:**

| User | Role | Can do | Cannot do | Tested by |
| --- | --- | --- | --- | --- |
| Priya (service agent) | Customer Service Representative (copy) | Create and update cases in her business unit | See opportunities; see the *Contract value* column | Signed in as Priya and tried to open an opportunity — access denied ✔ |

**Contoso BRD extract:**

| ID | Requirement | Priority | Source |
| --- | --- | --- | --- |
| BR-03 | Warranty repairs are booked within 2 working days of the request | Must | Raj Singh, Service Manager |
| BR-09 | Agents cannot see service-plan prices | Must | Finance |

**Why this is good:** security is *tested*, not assumed, and requirements describe business needs (“booked within 2 days”), not solutions (“build an SLA”).

## Northwind capstone (complete during the week)

- **Task:** Create users for a receptionist, clinic manager, sales rep and support lead; run a mock discovery interview with a classmate playing the COO
- **Deliver:** Users with roles + interview notes + BRD v1
- **Acceptance check:** Each user sees only what their role allows; BRD has 15+ requirements with MoSCoW priority

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
