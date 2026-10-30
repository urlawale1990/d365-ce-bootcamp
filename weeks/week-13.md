# Week 13 — Power Apps

- Saturday: model-driven app design in depth, app designer, security on apps; canvas app intro. Guided lab: a canvas app for technicians to log appliance visits.
- Sunday: embed the canvas app in a model-driven form; custom pages overview; Power Pages overview for customer portals.
- Reading: *Create a canvas app*; *Model-driven app design*.
- Homework: polish the technician app with a gallery, form and photo capture.


### Microsoft Learn modules (in the bootcamp collection)

- [Build a model-driven app](https://learn.microsoft.com/training/modules/build-model-driven-app/) — module
- [Build a canvas app](https://learn.microsoft.com/training/modules/build-canvas-app/) — module

## Consultant workshop (Sunday, last 40 minutes)

- **Skill:** Configuration management
- **Activity:** Configuration log; change requests and impact analysis; working with developers on gaps
- **Deliverable:** Configuration log + 1 change request

Use the matching template in [templates](../templates/README.md).

## What good looks like (Contoso example)

This example uses Contoso, not Northwind, so you see the standard expected without being given the answer.

**Contoso example — technician app:** a gallery of today's cases for the signed-in technician; a **Mark complete** button using
`Patch(Cases, ThisItem, {Description: ThisItem.Description & " — completed on site"})`;
a camera control to attach a photo of the repair.

**Contoso example — change request:** CR-04 “Add *Priority customer* flag to cases” · Impact: Case form, routing rules, SLA · Effort: 2 days · Risk: low · Decision: approved for release 1.2.

**Why this is good:** the app shows only what the technician needs, and the change request states impact and effort before anything is built.

## Northwind capstone (complete during the week)

- **Task:** Build a canvas app for receptionists to check in patients; log all configuration and raise 1 change request
- **Deliver:** Canvas app embedded in the model-driven app + config log + CR
- **Acceptance check:** App writes to Dataverse; CR includes impact and effort

Client material is in [northwind](../northwind/README.md). Demo-ready by Saturday: 2–3 learners present each week.
