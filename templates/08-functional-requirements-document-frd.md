# Functional Requirements Document — FRD (Weeks 9–10)

**Sections:** 1 Introduction and scope · 2 Solution overview (apps, licences) · 3 Business processes (to-be maps) · 4 Data model (ERD, data dictionary) · 5 User experience (forms, views, dashboards per role) · 6 Business logic (rules, BPFs, flows) · 7 Security · 8 Integrations · 9 Reports · 10 Data migration · 11 Non-functional requirements · 12 Open questions · 13 Sign-off.

**Example entry (section 6):** *FR-23 Case routing.* When a case is created with Case type = Warranty, a routing rule assigns it to the Warranty queue. Traces to US-12, BR-02. Test: TS-12.

**Requirements traceability matrix (RTM):**

| Business req | User story | FRD ref | Component | Test script | Status |
| --- | --- | --- | --- | --- | --- |
| BR-02 | US-12 | FR-23 | Routing rule “Warranty” | TS-12 | Passed |
| BR-01 | US-07 | FR-05 | Sales Pipeline dashboard | TS-07 | In test |
