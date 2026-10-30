---
status: draft
primary: frontend
last_reviewed: 2026-10-24
---

<!-- @backend: code-checked against Align-Core (canTakeOverStrandedClaim, PUT /need-claims/{id}, #467/#468):
     a non-manager can reassign a claim only to themselves, only when the holder is paused/disabled, only if
     they are on the family's care team and not suspended themselves, and a standing claim needs an
     occurrence_date (one day at a time). Human backend reviewer to confirm before status: ready. -->

# Take over a claim from a paused volunteer

**Who this is for:** Volunteers on the family's care team. Advocates, coordinators and admins who manage the family's needs can also reassign claims, and see the same button.
**When to use it:** When a need or a day of a recurring need is held by a volunteer who has been paused or disabled, so nobody is coming.
**Before you start:** You're [signed in](../account/accept-invite.md), you're on the family's care team, and your own volunteer account is active.

## Steps

1. From the main menu, open **Schedule**.
2. Find the date marked **volunteer paused** (in the calendar and day list, the line under the title reads, for example, "Sample Volunteer · volunteer paused"). It is highlighted in red. A recurring need's date list on the **Needs** page, in the claim dialog, marks the same dates **Volunteer paused — needs cover**.
3. Tap **Take over this day** on a recurring need, or **Take over** on a one-time need.
4. In the **Take over this day?** confirmation, read the details and tap **Take over this day**. Tap **Never mind** to back out (**Not yet** in the recurring-need dialog on the **Needs** page).
5. A message confirms **You've taken over this day**.

## What you'll see

- You're listed as the volunteer for that date, replacing the paused volunteer.
- On a recurring need, only that one date moves to you. Any other dates the paused volunteer holds stay theirs, so take over each date you want.

!!! note "Why these dates need cover"
    A claim held by a paused or disabled volunteer is still listed, but it no longer counts as coverage, so the need can read as **Open** again. That volunteer has lost access to the family and gets no reminders. Admins, coordinators and advocates see a red banner on the Schedule page ("N upcoming needs are claimed by a paused or disabled volunteer") and a **Needs claimed by paused volunteers** count under **What needs attention** on the advocate dashboard; the count only appears while there is something to fix.

## Related

- [Claim a need](claim-a-need.md)
- [Request coverage on a need you've claimed](request-coverage.md)
- [View the calendar](../schedules/view-calendar.md)
