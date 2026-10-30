# Security design and role matrix (Week 8)

**Business units:** Contoso (root) → North, South. **Teams:** Sales North, Sales South, Service Desk.

| Role | Account | Opportunity | Case | Appliance | Notes |
| --- | --- | --- | --- | --- | --- |
| Salesperson | Read org, write user | Create/write user | Read BU | Read BU | Cannot delete |
| Sales Manager | Write BU | Write BU | Read BU | Read BU | Approves discounts |
| Service Agent | Read org | None | Create/write BU | Write BU | Contract value field secured |
| System Customiser | Consultant only | | | | Dev environment only |
