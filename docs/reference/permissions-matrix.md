---
status: needs-review
primary: backend
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
| See **one** family (assigned / own) | ✓ | ✓ | ✓ ᵃ | ✓ | ✓ |
| Browse & claim needs | ✓ | ✓ | ✓ | ✓ | — |
| Create / remove needs | ✓ | ✓ | ✓ | Lead ᵇ | — |
| View the schedule | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Messaging within a circle | ✓ | ✓ | ✓ | ✓ | ✓ ᶜ |
| Manage families, volunteers, churches | ✓ | ✓ | their church ᵃ | — | — |
| Invite / onboard people | ✓ | ✓ | ✓ | — | — |
| View the audit log | ✓ | ✓ | — | — | — |

**✓** = allowed · **—** = not available

- **ᵃ** Across each family their church serves.
- **ᵇ** A **Lead Volunteer** can create/remove needs within their one family.
- **ᶜ** Within their own family's circle: a read-only calendar and a "Message Team" thread.
