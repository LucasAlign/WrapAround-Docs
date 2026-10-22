---
status: needs-review
primary: backend
last_reviewed: 2026-10-22
---

<!-- @backend verified 2026-10-22 against Align-Core: family and volunteer gates key off the admin-assigned
`category` flag (community_status / volunteer_status, #99, #455), not the status name. -->

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

- **Prospect** — where a new or just-invited volunteer starts (the status flagged as the
  *intake* category).

Other common values include *Equipped / Waiting*, *Serving*, *Taking a Break*,
*No Longer Serving*, and *Pending team placement*.

Each volunteer status carries a hidden **category** that staff assign — *intake*, *active*,
*paused*, or *disabled* — and the system acts on the category, not on the status text, so
renaming a status is safe. A status with no category is treated as active.

- **Paused** or **disabled** volunteers lose access to their families' and church's data,
  can't send or receive messages, stop receiving notification emails, and can't be assigned
  to needs.
- Moving a volunteer into **disabled** also turns off their sign-in; moving them out turns
  it back on.

## Where statuses come from

Statuses are reference lists kept centrally and editable by staff, so treat the app's
current list as authoritative. The system acts on a status's hidden category rather than its name: a family status in the
*vetting* category gates a family's approval, and the volunteer status in the *intake*
category is the starting point for a new volunteer.
