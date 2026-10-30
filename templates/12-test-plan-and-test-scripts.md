# Test plan and test scripts (Week 14)

**Test plan sections:** scope, test types (unit, system, UAT, regression), environments, entry/exit criteria, roles, defect severity levels, schedule.

| Script | Story | Step | Expected result | Actual | Pass/Fail |
| --- | --- | --- | --- | --- | --- |
| TS-12 | US-12 | 1. Create case, type Warranty, save | Case appears in Warranty queue | As expected | Pass |
| TS-12 | US-12 | 2. Change type to Repair | Case moves to Repair queue | Stayed in Warranty | Fail — defect BUG-31 |

Test cases and defects (BUG-31) tracked in Azure DevOps, linked to US-12.
