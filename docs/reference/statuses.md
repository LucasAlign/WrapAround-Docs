---
status: needs-review
primary: backend
last_reviewed: 2026-11-24
---

<!-- @backend verified 2026-10-22 against Align-Core: family and volunteer gates key off the admin-assigned
`category` flag (community_status / volunteer_status, #99, #455), not the status name.
Re-verified 2026-11-24 against Align-Core #552: the family agreement gate now fires on
entering care (target not vetting/inactive, previous status vetting/inactive or none),
not on leaving vetting (requiresSignedAgreement in handlers/people/index.ts). -->

# Statuses explained

Many records in WrapAround carry a **status** that tracks where they are in their lifecycle.
Statuses are managed lists — program staff can adjust the available options — so the live
list you see in the app is always the source of truth. Below are the standard values and
the few that drive how the system behaves.

## Family status

Tracks where a family is in the care journey.

- **Care Requested / Needs Vetting** — where a new family starts. Staff review and approve
  the family before it moves into care.

A family in an intake (*vetting*) or *inactive* status can't be moved into care (an
*active*, *building* or uncategorized status) until a parent has signed the current
participation agreement. The system enforces this. Moving a family to an *inactive*
status never needs a signature, so a family that drops out of intake can be closed
without signing.

Other common values include *Applicant*, *Active – Awaiting serving Church*,
*Active / Being served*, *On Hold*, and *Closed*.

Staff also assign each family status a **category** — *vetting*, *building*, *active*, or
*inactive* — and the app colours the status badge by that category, not by the status text.
*Building* is the stage after a family is approved and has signed the participation
agreement but before its care circle is assembled. A status with no category shows a
neutral badge.

## Volunteer status

Tracks where a volunteer is in their journey.

- **Prospect** — where a new or just-invited volunteer starts (the status flagged as the
  *intake* category).

Other common values include *Equipped / Waiting*, *Serving*, *Taking a Break*,
*No Longer Serving*, and *Pending team placement*.

Behind the scenes each volunteer status can carry a **category** — **Intake**, **Active**,
**Paused**, or **Disabled** — set on the status under **Add/Remove Reference Data** in the
admin area. The system acts on the category, not the status wording, so a status can be
renamed freely. A status with no category shows as **Informational** and is treated as active.

- **Paused** and **disabled** volunteers (and advocates) lose access to their families' and church's data,
  can't send or receive messages, stop getting notification emails, and can't be assigned
  to needs. When they open the app they see a full-page **Your account is paused** (or
  **Your account is disabled**) screen with a **Sign out** button, telling them their advocate
  or coordinator needs to move them out of that status.
- Moving a volunteer into a **disabled** status also turns off their sign-in; moving them
  out turns it back on.
- New volunteers start in the *intake* category (by default the **Prospect** status).

![Admin Management, Add/Remove Reference Data tab, Volunteer Status list showing Intake, Active, Paused and Disabled category badges.](../assets/screens/statuses/volunteer-status-categories.png)

<!-- @backend verified 2026-10-21 against Align-Core #455 (volunteer_status.category,
migration aligncore/034): effects above match utils/volunteer-status.ts, messaging,
notify.ts and the volunteers handler. Which role may change the category/status is not
asserted here — confirm before marking ready. -->

## Where statuses come from

Statuses are reference lists kept centrally and editable by staff, so treat the app's
current list as authoritative. The system acts on a status's category rather than its name: the participation-agreement
check runs when a family moves from a *vetting* or *inactive* status into care, and the
volunteer status in the *intake* category is the starting point for a new volunteer.
