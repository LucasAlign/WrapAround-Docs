---
status: needs-review
primary: frontend
---

# Accept your invite

**Who this is for:** Advocate (also applies to Volunteers invited directly by an Admin or Advocate)
**When to use it:** The first time you sign in, after program staff or an advocate has created your account.
**Before you start:** You need the invite email sent to the address staff used to create your account.

<!-- @backend verified 2026-08-27: onboarding invites use Cognito AdminCreateUser with a
temporary password; the auth stack sets no TemporaryPasswordValidityDays override, so the
Cognito default of 7 days applies. -->

!!! note "Use your temporary password within 7 days"
    The temporary password in your invite email expires after **7 days**. If it's expired,
    you don't need a new invite — on the sign-in screen, choose **Forgot your password?**
    and follow the steps to set your own password, using the same email the invite was
    sent to.

## Steps

1. Open the invite/welcome email and find your **temporary password**.
2. Go to your organization's WrapAround sign-in page and choose **Sign in**.

    ![WrapAround sign-in form with email address and password fields](img/accept-your-invite-signin-desktop.png)

3. Enter the email address the invite was sent to, and the temporary password.
4. When prompted, set a new permanent password: at least 8 characters, including a number, an uppercase letter, and a special character.
5. Sign in again with your new password.

## What you'll see

If you haven't completed your assigned training yet, you're taken straight to **Training**. Once training is complete, you land on your normal dashboard — for an Advocate, this is **Managed Care Communities**, showing the families your church serves.

!!! tip "Not sure which email to use?"
    Invites always go to the exact address staff entered when creating your account. If sign-in fails, double check you're using that address, not a personal alternate.

## Related

- [How to complete personal training](../training/modules-and-progress.md)
- [Troubleshooting](../../reference/troubleshooting.md)
