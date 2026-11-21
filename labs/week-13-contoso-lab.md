# Week 13 lab: Power Apps for technicians

You build a canvas app for Contoso engineers, then bring it into the Contoso Service model-driven app. Work inside the **Contoso Configuration** solution.

---

## Saturday 6 February: the technician canvas app (about 50 minutes)

### Step 1 — Prepare the data

1. In the solution, **Case → Columns → + New column:** `Repair photo`, data type **Image**. **Save**.
2. Make sure at least 3 **active** cases are owned by you (the person who will test the app), each linked to an appliance.

### Step 2 — Create the app

1. In the solution: **New → App → Canvas app**. Name: `Contoso Technician`. Format: **Phone**. **Create**.
2. **Data → Add data → Dataverse:** add **Cases** and **Appliances**.

### Step 3 — Screen 1: today's jobs

1. Insert a **vertical gallery** named `galJobs`. Set **Items**:

   ```
   Filter(Cases, Owner.'Primary Email' = User().Email, Status = 'Status (Cases)'.Active)
   ```

2. In the gallery template, show **Case Title**, the customer name and the appliance name:

   ```
   ThisItem.'Case Title'
   ThisItem.Customer.'Account Name'
   ThisItem.Appliance.Name
   ```

3. Insert a title label at the top: `Today's jobs`.

If you see a delegation warning (blue underline), that's fine for a small test dataset. Discuss what it would mean with 50,000 cases.

### Step 4 — Screen 2: job details

1. **New screen → Blank**. Name it `scrJob`. On `galJobs`, set **OnSelect** to `Navigate(scrJob)`.
2. Insert a **Display form**, data source **Cases**, Item = `galJobs.Selected`. Show Case Title, Customer, Appliance, Description, Priority.
3. Add a **Back** icon with OnSelect `Back()`.

### Step 5 — Mark complete and take a photo

1. Insert a **Camera** control named `camRepair` (on desktop it uses your webcam).
2. Insert a button **Save photo**, OnSelect:

   ```
   Patch(Cases, galJobs.Selected, {'Repair photo': camRepair.Photo}); Notify("Photo saved", NotificationType.Success)
   ```

3. Insert a button **Mark complete**, OnSelect:

   ```
   Patch(Cases, galJobs.Selected, {Description: galJobs.Selected.Description & " — completed on site"}); Notify("Marked complete", NotificationType.Success); Back()
   ```

4. **Save**, **Publish**, and test it with **Play** (and on your phone with the Power Apps mobile app if you have it).

### Saturday checks

- [ ] The gallery shows only your active cases.
- [ ] Selecting a job opens its details.
- [ ] Save photo stores the image on the case (check the case in Customer Service Hub).
- [ ] Mark complete adds “completed on site” to the description.

---

## Sunday 7 February: into the model-driven app, custom pages and portals (about 60 minutes)

### Step 1 — Add a custom page to the Contoso Service app

1. In the solution: **New → App → Page** (custom page). Name: `Technician jobs`.
2. Rebuild the jobs gallery on it (copy the gallery from Contoso Technician, or rebuild with the same Items formula).
3. **Save** and **Publish**.
4. Open the **Contoso Service** app in the designer → **+ Add page → Custom page → Use an existing page → Technician jobs**. Add it to the **Service** group. **Save** and **Publish**.
5. Play the model-driven app and open **Technician jobs** from the navigation.

### Step 2 — Embed on a form (demo or try it)

On the **Appliance** main form, the trainer shows how a canvas component or custom page can sit inside a form, and when that's worth the extra complexity compared with a subgrid.

### Step 3 — Power Pages overview (trainer demo, 15 minutes)

Watch the trainer create a Power Pages site from a template and show how a customer could log a case or read knowledge articles. Discuss: what would Contoso's landlords want on a portal? What security does it need?

### Step 4 — A change request (consultant practice, 15 minutes)

Write change request **CR-04 Add “Priority customer” flag to cases**: impact (Case form, routing rules, SLA), effort, risk and decision. Use the [configuration log and change request template](../templates/11-configuration-log-and-change-request.md).

### Sunday checks

- [ ] The Technician jobs custom page opens inside the Contoso Service app.
- [ ] You can say when to use a canvas app, a custom page or a model-driven form.
- [ ] CR-04 is written with impact, effort and a decision.

---

## Homework

Polish the technician app: a nicer gallery, an edit form so the engineer can update the description, and the photo capture working on your phone.
