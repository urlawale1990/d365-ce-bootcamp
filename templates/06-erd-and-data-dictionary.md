# ERD and data dictionary (Week 7)

**ERD notation:** boxes = tables, lines = relationships, crow's foot = many. Standard tables shown in grey, custom in blue.

**Contoso ERD in words:** Account 1:N Contact · Account 1:N Appliance · Appliance 1:N Service Contract · Appliance 1:N Case · Case N:1 Contact.

| Table | Column | Type | Required | Description |
| --- | --- | --- | --- | --- |
| Appliance (cnt_appliance) | Serial number | Text (50) | Yes | Manufacturer serial, unique |
| Appliance | Install date | Date only | Yes | Used for warranty calculation |
| Appliance | Account | Lookup (Account) | Yes | Owner of the appliance |
| Service Contract | End date | Date only | Yes | Triggers renewal reminder |
