---
status: needs-review
primary: frontend
---

<!-- @frontend verified 2026-08-27 end-to-end live on the dev instance, using a real
throwaway account carried through every step: registration, the emailed 6-digit code,
the participation-agreement signature, and the resulting dashboard while the family sits
in Care Requested / Needs Vetting. Corrected: the post-signature dashboard does NOT show
an advocate, volunteers, needs, or schedule yet (those only appear once staff activate
the family and assign a serving church) — pre-activation it shows the vetting-status
banner, a "Your county coordinators" contact card, and an editable "About your family"
profile form. Also confirmed there is no returning-family sign-in path in this app: the
site's one "Sign in" button goes through the staff/volunteer Cognito hosted UI, while
families authenticate through a separate SDK-based flow that only the signup page itself
calls (lib/cognito-family.ts). That is almost certainly why a previously-registered demo
family account can't sign back in through "Sign in" — it's a product gap, not a bad demo
account. Flagging for the backend/frontend teams rather than fixing in docs. -->

# Getting started for families

If you're a foster or adoptive parent, WrapAround is where your **care circle** comes
together — the advocate and volunteers helping your family. You'll see **your own family**
only.

## Your first day, step by step

WrapAround is one of the few roles that **doesn't require a staff invite** — you can
register yourself.

1. **Register your family.** Go to the family signup page (your local program can give
   you the link) and fill in the **Request a care community** form: your name as the
   primary parent, a family/household name (it starts prefilled with your name — change
   it if you'd rather use something else), your email, a US phone number, and your
   **county**. Set a password, agree to the Terms of Service and Privacy Policy, and
   click **Create account**.

   ![The family registration form — Parent's full name, Family/household name, Email, Phone, County, Password, and the Terms of Service/Privacy Policy agreement.](img/fam-signup-form-desktop.png)

2. **Confirm your email.** WrapAround emails you a 6-digit code. Enter it on the
   **Confirm your email** screen and continue — this signs you in automatically.

   ![Confirm your email screen with a 6-digit Confirmation code field.](img/fam-signup-confirm-desktop.png)

3. **Sign the participation agreement.** Before you can reach your dashboard, you're
   asked to review and sign your program's active **participation agreement**. Read it,
   click **Review & sign**, check the identity details shown (name, family, email, phone,
   agreement version, date), and click **I agree & sign**.

   ![The Participation agreement screen with the agreement text and a Review & sign button.](img/fam-agreement-gate-desktop.png)

   ![The Confirm your signature dialog, showing the signer's details and an "I agree & sign" button.](img/fam-agreement-sign-dialog-desktop.png)

4. **Land on your dashboard.** Right after signing, your family is in **Care Requested /
   Needs Vetting** — so what you see is a status banner, your **county coordinators'**
   contact details, and an editable **About your family** profile (preferred language,
   preferences, family bio, church, and how volunteers can help). Take a few minutes to
   fill this in; it helps staff place you.

   ![Your dashboard right after signing — the vetting-status banner, county coordinators, and an About your family form.](img/fam-dashboard-desktop.png)

   Your full circle — an assigned **advocate**, **volunteers**, **needs**, and a
   **schedule** — appears once staff review your request and activate your family with a
   serving church.
   → [View your family](../how-to/family/view-your-family.md)

!!! tip "Already have an account?"
    If your family was set up by staff instead of self-registering, you'll get an invite
    email instead of using the signup form — see
    [Accept your invite & sign in](../how-to/account/accept-invite.md).

!!! warning "No way back in if you close the tab before signing in elsewhere"
    Registering yourself signs you in automatically, but there's currently no separate
    "sign in" path built for returning families — the site's one Sign In button is for
    staff and volunteers. If you get signed out, contact your program; don't create a
    second account with the same email.

!!! note "Care Requested / Needs Vetting"
    Right after signing the agreement, your family starts in a **vetting** status while
    your program reviews your request. An advocate or coordinator moves you forward from
    there.

## What you can do

WrapAround gives you a window into your own care circle:

- See your family's circle — your advocate and the volunteers helping you.
- See the **needs** raised for your family and who's helping with each.
- See your family's **schedule**.

Creating needs, claiming tasks, and managing the schedule are handled by your advocate,
program staff, and volunteers — so you can stay focused on your family.

New here? Start with [What is WrapAround?](../concepts/what-is-wraparound.md).
