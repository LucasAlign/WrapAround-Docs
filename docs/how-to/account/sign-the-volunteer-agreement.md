---
status: draft
primary: frontend
last_reviewed: 2026-11-02
---

# Sign the volunteer agreement

**Who this is for:** Volunteers, lead volunteers, and advocates.
**When to use it:** The first time you sign in after your program publishes a volunteer agreement, and again whenever it publishes a new version.
**Before you start:** You've [accepted your invite and signed in](accept-invite.md).

When your program has a volunteer agreement in place, WrapAround shows it to you before
anything else. You can't open the rest of the app until you sign it, and that includes the
onboarding steps if you haven't finished them yet.

<!-- @backend: confirm the roles that must sign. The frontend gate (isVolunteerAgreementRole) covers volunteer, lead_volunteer and church_advocate, and exempts admins, families, and anyone acting as an advocate. Align-Core's POST /agreements/{id}/sign for the volunteer audience should be checked for the same scope. -->

## Steps

1. Sign in. If you need to sign, WrapAround opens the **Volunteer agreement** screen, headed
   "Please review and sign before continuing."
2. Read the agreement. Scroll inside the text box to reach the end.
3. Select **Review & sign**.
4. In the **Confirm your signature** dialog, check the details that will be recorded with
   your signature: **Signed by**, **Email**, **Agreement** (title and version), and **Date**.
5. Select **I agree & sign**. To change your mind, select **Go back**.

## What you'll see

WrapAround records your signature and takes you to **Onboarding** if you haven't finished
it, or to your **dashboard** if you have. You also get a "for your records" email with the
text you signed, as a PDF and in the message.

If you finish onboarding by signing, you don't need a separate step to mark it complete.

!!! tip "Don't want to sign yet?"
    Select **Back — I don't want to sign yet**. This signs you out, because you can't use
    WrapAround without signing. Sign in again when you're ready.

!!! note "If something goes wrong"
    - **We couldn't load the volunteer agreement.** Select **Try again**.
    - **Couldn't record signature.** Try again. If a newer version was published while you
      were reading, WrapAround reloads it so you sign the current one.
    - If you already signed this version, WrapAround takes you straight on.

!!! info "No agreement published?"
    If your program hasn't published a volunteer agreement, you won't see this screen.

## Related

- [Accept your invite & sign in](accept-invite.md)
- [Sign up as a volunteer](volunteer-self-signup.md)
- [Manage family agreements](../admin/family-agreements.md)
