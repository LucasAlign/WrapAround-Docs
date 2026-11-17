---
status: needs-review
primary: backend
last_reviewed: 2026-11-17
---

# Roles & permissions matrix

What each role can see and do. Visibility is enforced by the server on every request — see
[Roles & who sees what](../concepts/roles-and-visibility.md) for how scope is decided.

The in-app role badges read **Central Admin**, **Coordinator Admin**, **Church Advocate**,
**Support Volunteer** / **Lead Volunteer**, and **Family**.

<!-- @frontend verified 2026-08-27 against Align-FrontEnd's hooks/use-user.tsx
(useCanManageCareItems explicitly returns false for both "volunteer" and "family"
roles) and pages/family.tsx (the family dashboard shows an embedded read-only Schedule
and a "Message Team" button, but no "Post a Need" control anywhere reachable by that
role). Corrected: Family cannot create or remove needs — that cell was wrong. -->

| Capability | Admin | Coordinator | Advocate | Volunteer | Family |
|---|:---:|:---:|:---:|:---:|:---:|
| See **all** families | ✓ | ✓ | — | — | — |
| See families at **their church** | ✓ | ✓ | ✓ | — | — |
| See **their** families (assigned / own) | ✓ | ✓ | ✓ ᵃ | ✓ | ✓ |
| Browse & claim needs | ✓ | ✓ | ✓ | ✓ | — |
| Create / remove needs | ✓ | ✓ | ✓ | Lead ᵇ | — |
| View the schedule | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Messaging within a circle | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Manage families, volunteers, churches | ✓ | ✓ | their church ᵃ | — | — |
| Invite / onboard people | ✓ | ✓ | ✓ | — | — |
| View the audit log | ✓ | ✓ | — | — | — |
| Change a user's role | ✓ | ✓ ᵈ | — | — | — |
| Create & publish training events | ✓ | — ᵉ | — | — | — |
| RSVP to a training event | — | — | ✓ | ✓ | — |

**✓** = allowed · **—** = not available

- **ᵃ** Across each family their church serves.
- **ᵇ** A **Lead Volunteer** can create/remove needs for the families they lead.
- **ᶜ** Within their own family's circle: a read-only calendar and a "Message Team" thread.
- **ᵈ** Within a tier only (Admin ↔ Coordinator, or Advocate ↔ Volunteer / Lead Volunteer),
  never on their own account or a family account. Only an Admin can make someone an Admin
  or change an Admin's role. See [Change a user's role](../how-to/admin/change-a-users-role.md).
- **ᵉ** The **Events** tab under **Training Management** is shown to Central Admins only.

<!-- @backend: the training-events API (/training/events) also accepts Coordinators; the
frontend hides the Events tab from them (Align-FrontEnd #831). Confirm the matrix should
follow the UI. -->
