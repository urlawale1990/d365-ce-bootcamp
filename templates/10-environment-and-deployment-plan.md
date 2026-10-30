# Environment and deployment plan (Week 12)

| Environment | Type | Purpose | Who has access |
| --- | --- | --- | --- |
| Contoso-Dev | Sandbox | Build and unit test | Consultants |
| Contoso-Test | Sandbox | System test and UAT | Testers, key users |
| Contoso-Prod | Production | Live use | All users |

**Deployment checklist:** solution version increased → export managed from Dev → environment variables and connection references set → import to Test via pipeline → smoke test → UAT sign-off → deploy to Prod out of hours → post-deployment checks → release notes sent. **Rollback:** keep the previous managed version; reimport if the smoke test fails.
