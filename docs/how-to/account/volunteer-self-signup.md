---
status: needs-ui
primary: frontend
---

<!-- @frontend: confirmed 2026-08-26 against Align-FrontEnd (VOLUNTEER_ROLE.md and the
route table in App.tsx) that there is no self-service volunteer signup path in the
shipped app today. VOLUNTEER_ROLE.md is explicit: "The `/invite-register`,
`/invite/:token` and `/volunteer-register` routes were all removed as dead
Express-era paths." Onboarding is invite-only — an admin or advocate must call
POST /onboarding/invite before a volunteer account can exist at all. This page
documents that fact rather than fabricating steps for a flow that doesn't exist.
If self-service volunteer signup ships later (mirroring the family flow at
/family-signup — see docs/how-to/account/../../get-started/families.md), replace
this page's content with real steps and screenshots, move it to
status: needs-review, and update get-started/volunteers.md to link to it instead
of accept-invite.md as the only path in. -->

# Sign up as a volunteer

**Who this is for:** Anyone who wants to volunteer with WrapAround.
**When to use it:** You're looking for a "create your own volunteer account" option.
**Before you start:** Nothing.

## There's no self-service volunteer signup today

WrapAround doesn't have a public "sign up as a volunteer" page. Volunteer accounts are
created by **invitation only** — a program coordinator or your church's advocate has to
add you first, and WrapAround emails you an invite to set your password and get started.

If you want to volunteer:

1. **Contact your church's advocate or the program office** and ask to be added as a
   volunteer.
2. Once they've entered your information, you'll get an **invite email**. Follow it to
   set your password and sign in.
   → [Accept your invite & sign in](accept-invite.md)

!!! tip "Families are different"
    Foster/adoptive families *can* create their own account without an invite. If you
    meant to register your family rather than volunteer, see
    [Getting started for families](../../get-started/families.md).

## Related

- [Accept your invite & sign in](accept-invite.md)
- [Get started as a Volunteer](../../get-started/volunteers.md)
