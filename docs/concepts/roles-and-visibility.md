---
status: needs-review
primary: backend
---

<!-- @frontend verified 2026-08-28: filled in the Family row's "What they typically do"
column (previously blank in effect — it just repeated the "Sees" claim) with what a
family can actually do: view-only needs/schedule plus messaging. Lead Volunteer's "extra
abilities... such as creating or removing needs" confirmed against hooks/use-user.tsx's
useCanManageCareItems, which explicitly excludes "volunteer" and "family" roles but not
"lead_volunteer". Cross-referenced with the corrected reference/permissions-matrix.md. -->

# Roles & who sees what

WrapAround is built around one rule: **you only see the families you're responsible for.**
Your role decides how wide that reach is. This is enforced by the server on every
request — it isn't just hidden in the interface.

The names below are the labels shown on your role badge in the app.

## The roles

| Role | Sees | What they typically do |
|---|---|---|
| **Central Admin** (program staff) | **Every** family and all data | Set up and manage everything; full access |
| **Coordinator Admin** | **Every** family (same access as Central Admin) | Admin-level access, focused on managing their county |
| **Church Advocate** | Every family served by **their church** | Coordinate care across their church's families |
| **Support Volunteer** | **One** family — the one they're assigned to | Claim needs, keep an eye on the schedule, message the team |
| **Family** | **Their own** family only | View their own needs and schedule, message the team; can't create or manage needs |

## How your scope is decided

- **Admins and Coordinators** aren't scoped — they see all families.
- **Advocates** are scoped to their **church**: they can see every family whose *serving
  church* is theirs. An advocate isn't tied to a single family.
- **Volunteers** are scoped to the **one family** they're assigned to. A volunteer cannot
  see another family's needs, schedule, messages, or posts.
- **Families** (self-registered parents) are scoped to **their own family record** only.

> **Lead Volunteer.** A volunteer can be marked as the **Lead Volunteer** for their family.
> Leads get extra abilities *within that one family* — such as creating or removing needs —
> but they're still limited to that single family like any other volunteer.

## Why it works this way

Family information is sensitive. The rule that a volunteer only ever sees their own family
is enforced in the backend on every request, so it holds no matter what any screen happens
to show.
