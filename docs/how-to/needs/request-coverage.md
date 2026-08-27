---
status: needs-ui
primary: frontend
---

<!-- @frontend: mechanism confirmed by reading Align-FrontEnd's
components/need-detail-dialog.tsx (2026-08-26), not by clicking through it live.
The demo's WA_VOLUNTEER_USER account is actually a Lead Volunteer (per this repo's
CLAUDE.md and a comment in WrapAround-Testing-Suite's config/roles.ts) — a Lead
Volunteer has useCanManageCareItems()=true for their own family, so they always see
the *manager* view (the "Modify this day" card, same as an Advocate) and never the
plain-volunteer "Claimed the series" row this page describes. No base Support
Volunteer demo account exists to verify against, and this account's own schedule
had no occurrence with a live claim to click through anyway. Steps below are
accurate to the source (coverageControl() renders next to the claim holder's own
name whenever canManage is false and claim.user_id === the signed-in user's id —
see need-detail-dialog.tsx line ~303), but need a real click-through by a Support
Volunteer account before this reaches status: ready. -->

# Request coverage on a need you've claimed

**Who this is for:** Volunteer (on your own claim).
**When to use it:** You've claimed a need or a recurring slot but might not be able to
make it, and want to ask the care community for a replacement — without giving up the
slot yet.
**Before you start:** You've already [claimed](claim-a-need.md) the need or occurrence.

## Steps

1. Go to **Schedule**.
2. Click the day with the occurrence you claimed. If more than one item falls on that
   day, a short list opens first — click through to the specific occurrence to open its
   detail dialog.
3. Find your own name in the list of who's covering it. Next to it, click
   **Request coverage**.

## What you'll see

The care community is emailed that this slot needs a different volunteer. **You stay
assigned** — this only asks for backup, it doesn't remove you from the slot. If no one
steps in, you still hold it; if you can no longer do it at all, use
[Withdraw a claim](withdraw-a-claim.md) instead to release it outright.

For a recurring need, requesting coverage only affects the **date you opened** — your
assignment on every other occurrence in the series is untouched.

!!! tip "Not the same as withdrawing"
    **Request coverage** asks for backup while you keep the slot. **Withdraw** gives the
    slot up completely and returns it to the open list. Use whichever matches what you
    actually need.

## Related

- [Withdraw a claim](withdraw-a-claim.md)
- [Claim a need](claim-a-need.md)
- [Request coverage on behalf of a volunteer](../advocate/request-coverage.md) — the
  same control, used by an advocate or lead volunteer on someone else's claim.
