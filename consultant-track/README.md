# The consultant track

The last 40 minutes of every Sunday are a consultant workshop. Learners act as consultants for Contoso and build one real project deliverable each week. By Week 16 they hold a complete implementation pack, not just configuration skills.

**Implementation lifecycle taught across the course** (Microsoft Success by Design phases):

1. **Initiate** — discovery, stakeholders, scope, requirements (Weeks 2–4)
2. **Analyse and design** — process maps, fit-gap, ERD, security design, FRD (Weeks 4–9)
3. **Implement** — build in solutions, configuration log, solution management and ALM (Weeks 6–14)
4. **Prepare** — data migration, test scripts, UAT, training material, cutover (Weeks 15–16)
5. **Operate** — go-live, hypercare, change requests, release waves (Week 16)

| Week | Consultant skill | Workshop activity | Deliverable |
| --- | --- | --- | --- |
| 1 | The consultant role | Functional vs technical vs solution architect; who does what on a project; RACI | Personal role map |
| 2 | Stakeholders and discovery | Stakeholder map; plan a discovery workshop; trainer plays the Contoso sales director | Stakeholder register + workshop agenda |
| 3 | Requirements gathering | Interview techniques, open vs closed questions; turn notes into requirements; MoSCoW priority | Business Requirements Document (BRD) v1 |
| 4 | User stories and acceptance criteria | Write “As a… I want… so that…” stories with Given/When/Then criteria and manage them on Azure DevOps Boards | Product backlog of 25 user stories |
| 5 | Process mapping | As-is and to-be maps for Contoso sales and service (swimlanes, BPMN basics) | As-is and to-be process maps |
| 6 | Fit-gap analysis | Classify each story: out-of-box / configure / customise / third-party / gap; estimate effort | Fit-gap matrix |
| 7 | Data modelling and ERD | Identify entities, attributes, relationships and cardinality; map to standard tables first | Contoso ERD + data dictionary |
| 8 | Security design | Translate org chart into business units, roles, teams; least privilege | Security design and role matrix |
| 9 | Functional Requirements Document (FRD) | Structure of an FRD/FDD: scope, processes, data model, forms, rules, integrations, reports, NFRs | FRD draft for the Sales module |
| 10 | FRD completion and sign-off | Peer review of FRDs; requirements traceability matrix (RTM) linking story → design → test | FRD v1.0 + RTM |
| 11 | Solution management | Publishers and prefixes; managed vs unmanaged; solution layers; patches and upgrades; segmented solutions | Solution strategy document |
| 12 | Environment strategy and ALM | Dev / Test / UAT / Prod; Power Platform pipelines; deployment checklist; release notes | Environment and deployment plan |
| 13 | Configuration management | Configuration log; change requests and impact analysis; working with developers on gaps | Configuration log + 1 change request |
| 14 | Testing | Test plan, test scripts from acceptance criteria, UAT planning; test cases and defects tracked in Azure DevOps linked back to user stories | Test scripts for 10 stories |
| 15 | Data migration and training | Migration plan and mapping; training needs analysis; user guides | Migration mapping sheet + user guide |
| 16 | Go-live and beyond | Cutover plan, go/no-go checklist, hypercare, release waves, presenting to stakeholders | Cutover plan + capstone presentation |

### Solution management in depth (Weeks 6, 11 and 12)

Solution management gets three touches because it is where most junior consultants struggle on real projects.

- **Week 6 (hands-on basics):** create a publisher with a Contoso prefix, build only inside a solution, export unmanaged and managed, import into a second environment.
- **Week 11 (strategy):** why nothing is built in the Default solution; managed vs unmanaged and when each is used; solution layering and the active layer; removing an unmanaged layer; patches vs upgrades; adding existing components without bloat; dependencies and missing-component errors.
- **Week 12 (ALM):** Dev → Test → Prod flow; environment variables and connection references for flows; Power Platform pipelines; versioning (1.0.0.0); a deployment checklist and rollback plan.
- **Lab:** each learner deploys their Contoso solution from a “Dev” trial to a second “Test” environment as a managed solution, breaks a dependency on purpose, then fixes it.

### The consultant pack learners graduate with

| Document | Built in week | Template provided |
| --- | --- | --- |
| Stakeholder register and discovery agenda | 2 | Yes |
| Business Requirements Document (BRD) | 3 | Yes |
| User story backlog with acceptance criteria | 4 | Yes |
| As-is / to-be process maps | 5 | Yes |
| Fit-gap matrix | 6 | Yes |
| ERD and data dictionary | 7 | Yes |
| Security design and role matrix | 8 | Yes |
| Functional Requirements Document (FRD) + RTM | 9–10 | Yes |
| Solution strategy and environment/deployment plan | 11–12 | Yes |
| Configuration log and change request | 13 | Yes |
| Test plan and test scripts | 14 | Yes |
| Data migration mapping and user guide | 15 | Yes |
| Cutover plan and go/no-go checklist | 16 | Yes |

All templates, each with a filled-in Contoso example, are in [templates](../templates/README.md).
