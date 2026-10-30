# Data migration mapping, user guide and cutover plan (Weeks 15–16)

**Migration mapping:**

| Source column | Target table.column | Transformation | Rule |
| --- | --- | --- | --- |
| Cust_Name | Account.name | Trim spaces, title case | Required |
| Email | Contact.emailaddress1 | Lowercase | Duplicate check |
| Install_Dt | cnt_appliance.cnt_installdate | Convert to DD/MM/YYYY | Reject if blank |

**User guide:** one task per page — goal, who it's for, numbered steps with screenshots, “what if it goes wrong”.

**Cutover plan and go/no-go checklist:**

- [ ] All Must stories passed UAT and signed off
- [ ] No open Severity 1 or 2 defects
- [ ] Data migrated and reconciled (record counts match)
- [ ] Users trained and licences assigned
- [ ] Support rota and hypercare plan (2 weeks) agreed
- [ ] Rollback plan tested
- [ ] Sponsor go/no-go decision recorded
