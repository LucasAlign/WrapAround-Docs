---
status: needs-ui
primary: frontend
---

# Add parent or child information

**Who this is for:** Advocate
**When to use it:** To add a parent/caregiver or a child to a family's household record.
**Before you start:** The family must be served by your church.

<!-- @frontend: on the live demo (2026-08-17, DemoAdvocate), the family's Household
section — both in the read-only Overview and inside Edit Details — only shows the
EXISTING parents/children (with two unlabeled icon buttons per row, likely edit-only)
and a "Send Account Setup Emails" button. No visible "Add Parent" / "Add Child" control
was found on the family detail page itself, which conflicts with the "Add" buttons in
families-modals.tsx's HouseholdManager component. Possibilities: (a) this control is
gated to Admin/Coordinator only and not exposed to Advocate despite ADVOCATE_ROLE.md
saying advocates manage "parents, children", (b) it's reached through a different flow
this pass didn't find, or (c) it isn't wired up yet for this role. Needs a real
walkthrough with someone who knows the current UI before this doc's steps are trustworthy. -->

## Steps

1. Open the family's **Household** section (Overview tab).
2. *(Unconfirmed)* Locate the add control for a parent or child.
3. Fill in the fields — name, phone, email for a parent; name, birthdate, and relationship for a child.
4. Save.

## What you'll see

The new parent or child appears in the Household list.

!!! tip "Want to give a parent portal access?"
    Adding a parent here only records their information — it doesn't create their WrapAround login. See [Invite a family's parents](invite-a-familys-parents.md) for that.

## Related

- [Invite a family's parents](invite-a-familys-parents.md)
- [How to view child information](view-child-information.md)
