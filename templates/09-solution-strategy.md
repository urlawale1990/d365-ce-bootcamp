# Solution strategy (Week 11)

| Decision | Contoso choice | Reason |
| --- | --- | --- |
| Publisher and prefix | Contoso Home Services, prefix cnt_ | Every custom component identifiable |
| Solutions | ContosoCore (tables, security), ContosoSales, ContosoService | Smaller deployments, clear ownership |
| Dev environment | Unmanaged only | Only place customisations are made |
| Test / Prod | Managed only | Clean upgrades and uninstall |
| Versioning | Major.Minor.Build.Revision, e.g. 1.2.0.0 | Clear release history |
| Patches | Avoided; full upgrades instead | Simpler for a small team |
