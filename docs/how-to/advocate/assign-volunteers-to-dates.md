---
status: draft
primary: frontend
last_reviewed: 2026-11-09
---

# Assign volunteers to several dates of a recurring need

**Who this is for:** Advocates and lead volunteers
**When to use it:** To put one or more care-team volunteers onto many dates of a recurring need in one pass, instead of covering each day separately.
**Before you start:** Pick the family in **Select Family** on the **Needs** page. The family needs at least one recurring need with open dates in the next 120 days.

## Steps

1. Open **Needs** from the navigation.
2. Click **Assign Volunteers to Dates** above the board.
3. Choose a recurring need, then click **Next**. A need with no room left shows **No open dates** and can't be chosen. If the family has none, the dialog says "This family has no recurring needs to assign."
4. Choose who will cover it, then click **Next**.
5. Choose the dates. Each date shows how many people are already signed up, for example "1 of 2 covered". Dates that are already covered can't be selected. **Select all open dates** picks every open date, and **Clear all** unselects them.
6. Click **Assign N dates** (**Assign 1 date** when you picked one).
7. Read the results, then click **Done**. Each date shows **Assigned**, **Already assigned**, **Skipped: already covered** or **Failed**.

Use **Back** to change an earlier choice before you assign.

## What you'll see

The dialog lists dates for the next 120 days. Existing claims are never overwritten: a volunteer who already holds a date shows **Already assigned**, and a date that filled up in the meantime shows **Skipped: already covered**.

## Related

- [Assign a volunteer to a need](assign-a-volunteer-to-a-need.md)
- [Cover a single day of a recurring need](cover-a-single-day.md)
- [See what each volunteer has committed to](view-volunteer-commitments.md)

<!-- @backend: confirm who may create need claims for other volunteers across multiple dates; the frontend shows the button only to church advocates and lead volunteers (not admins or coordinators), and falls back to single claims if the batch endpoint (Align-Core#363) is unavailable. -->
