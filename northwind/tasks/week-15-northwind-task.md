# Week 15 Northwind task: legacy data migration and a receptionist user guide

**Due:** Sat 27 February (see [due dates](README.md#due-dates)) · **Technique:** [Week 15 Contoso lab](../../labs/week-15-contoso-lab.md)

## The brief

Northwind's old records are messy. Migrate 300 of them cleanly, without duplicates, and write a guide good enough that a receptionist can complete a booking without help.

## Client material

- `data/northwind-legacy-contacts.xlsx`: 300 legacy records, released by your trainer in the [client pack](../README.md) this week
- [Data migration, user guide and cutover template](../../templates/13-data-migration-mapping-user-guide-and-cutover-plan.md)

## Deliver

1. A **mapping sheet**: source column → target table and column → transformation rule.
2. A **cleansing log** of every decision about bad data.
3. **Duplicate detection rules** set up before import.
4. The records **imported**, with record counts reconciled against the source.
5. A **receptionist user guide**: one task per page with screenshots, including how to complete a booking.

## Pass checks

- [ ] No duplicates after import.
- [ ] Record counts match the source, minus rejects you've explained.
- [ ] A classmate completes a booking using only your guide.
- [ ] No medical notes were imported.

## Hints

- Clean in Excel before importing, and write down why you changed each thing.
- What will you do with records that have no email or a date you can't read?
