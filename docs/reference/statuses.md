---
status: needs-review
primary: backend
last_reviewed: 2026-10-21
---

<!-- @backend verified 2026-08-28 against KeyFam-infrastructure: "Care Requested / Needs
Vetting" and "Prospect" are real, hardcoded-by-name backend gates (the API looks them up
by that exact string), confirming this page's two "the system enforces this gate"
claims. The "Other common values" lists are appropriately hedged as non-exhaustive and
weren't independently re-verified this pass — the dev instance was unreachable to pull
the live reference-data list. -->

# Statuses explained

Many records in WrapAround carry a **status** that tracks where they are in their lifecycle.
Statuses are managed lists — program staff can adjust the available options — so the live
list you see in the app is always the source of truth. Below are the standard values and
the few that drive how the system behaves.

## Family status

Tracks where a family is in the care journey.

- **Care Requested / Needs Vetting** — where a newly self-registered family starts. Staff
  must review and approve the family before it becomes active. *(The system enforces this
  gate, so this status matters.)*

Other common values include *Applicant*, *Active – Awaiting serving Church*,
*Active / Being served*, *On Hold*, and *Closed*.

## Volunteer status

Tracks where a volunteer is in their journey.

- **Prospect** — where a new or just-invited volunteer starts.

Other common values include *Equipped / Waiting*, *Serving*, *Taking a Break*,
*No Longer Serving*, and *Pending team placement*.

Behind the scenes each volunteer status can carry a **category** — *intake*, *active*,
*paused*, or *disabled* — set by an admin. The system acts on the category, not the status
wording, so a status can be renamed freely. A status with no category is treated as active.

- **Paused** and **disabled** volunteers lose access to their families' and church's data,
  can't send or receive messages, stop getting notification emails, and can't be assigned
  to needs.
- Moving a volunteer into a **disabled** status also turns off their sign-in; moving them
  out turns it back on.
- New volunteers start in the *intake* category (by default the **Prospect** status).

<!-- @backend verified 2026-10-21 against Align-Core #455 (volunteer_status.category,
migration aligncore/034): effects above match utils/volunteer-status.ts, messaging,
notify.ts and the volunteers handler. Which role may change the category/status is not
asserted here — confirm before marking ready. -->

## Where statuses come from

Statuses are reference lists kept centrally and editable by staff, so treat the app's
current list as authoritative. Two values are special because the system acts on them:
**Care Requested / Needs Vetting** gates a family's approval, and **Prospect** is the
starting point for a new volunteer.
