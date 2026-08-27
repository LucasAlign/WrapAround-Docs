---
status: needs-review
primary: frontend
---

<!-- @frontend verified live 2026-08-27, comparing DemoAdvocate against DemoAdmin on the
same family (Khoury Family): Admin sees "Add parent" / "Add child" controls in the
Household section (12 buttons on the family page as Advocate vs. 27 as Admin, including
these two); Advocate sees neither, in either the read-only Overview or Edit Details. This
resolves the earlier open question on this page — it's a genuine role gate, not a missed
control. Contradicts ADVOCATE_ROLE.md's claim that advocates manage a family's "parents,
children"; that claim is stale for this specific action. See
docs/how-to/admin/families-and-people.md for the real (Admin/Coordinator-only) steps. -->

# Add parent or child information

**Who this is for:** Advocate (read this to understand why you can't do this — the
action itself is Admin/Coordinator-only).
**When to use it:** You need a parent or child added to a family's household record.
**Before you start:** Nothing — but see below before looking for a button that isn't there.

## Advocates can't add a parent or child directly

Unlike editing a family's profile or managing its care team, adding a parent or child to
the Household is **not available to Advocates** — the control simply doesn't appear,
even on families your church serves and even while you're already editing that family's
details.

## What to do instead

1. Contact your program's Admin or Coordinator.
2. Give them the parent or child's details (name, and for a parent, phone/email if you
   have them).
3. They'll add the record — see [Manage families & people](../admin/families-and-people.md#add-a-parent-or-child-to-a-family-admincoordinator-only)
   for the steps they'll follow.

## What you can do

- [View child information](view-child-information.md) already on file.
- [Invite a family's parents](invite-a-familys-parents.md) to create their own portal
  login, once they're already listed as parents on the family.
- [Modify a family's profile](modify-a-familys-profile.md) for everything else Advocates
  *can* edit.

## Related

- [Manage families & people](../admin/families-and-people.md) (Admin/Coordinator)
- [Invite a family's parents](invite-a-familys-parents.md)
- [View child information](view-child-information.md)
