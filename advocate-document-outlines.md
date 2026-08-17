# Advocate document outlines

Working draft: simple step-by-step outlines for every how-to document tagged for the
**Advocate** role in [`important-help-documents.md`](important-help-documents.md), plus
the two general-but-advocate-critical items (accepting a staff-sent invite, using
notifications) that were added as gaps.

**Grounding:** button/screen labels below were pulled directly from
`C:\Users\austi\Align-FrontEnd\artifacts\wraparound\src` (not guessed) — see the file/line
noted under each doc. Anything not yet confirmed is marked `@frontend`. These are outlines
only — expand each into a full how-to (template in `templates/how-to-template.md`) with
screenshots before publishing.

Status: draft outlines, not yet verified against a live walkthrough of the app.

---

## Onboarding & Account

### How to onboard a new volunteer (as an Advocate)
*Source: `pages/volunteers-modals.tsx` ("Invite New User" modal → "Create User"), backend
`onboarding/index.ts` (advocates may only invite the Volunteer role).*

1. Go to **Volunteers**.
2. Click **Invite New User**.
3. Enter the volunteer's name and email address.
4. Confirm the role is set to **Volunteer** (advocates can't invite any other role — the option won't be offered).
5. Click **Create User**.
6. Tell the volunteer to check their email for a temporary password and to expect the account-setup steps in [How to accept your invite](#how-to-accept-your-invite-staff-invited-users).

**What you'll see:** the new volunteer appears in the Volunteers list with a **Prospect** status until they complete training.

### How to view volunteer details
*Source: `pages/volunteer-profile.tsx`.*

1. Go to **Volunteers**.
2. Click a volunteer's name to open their profile.
3. Review **Overview** (status, assigned family/families, training progress), **Details**, and **Training & Certs** tabs.

**What you'll see:** training modules marked Completed/In progress, and whether the volunteer's account is Approved.

### How to accept your invite (staff-invited users)
*Applies to Advocates and Volunteers created by an Admin/Advocate via "Invite New User" —
distinct from the self-registration flow. `@frontend`: confirm the exact first-sign-in
screen text/flow (temp password → forced reset).*

1. Open the invite/welcome email and note the temporary password.
2. Go to the tenant sign-in URL and choose **Sign in**.
3. Enter your email and the temporary password.
4. When prompted, set a new permanent password (8+ characters, a number, an uppercase letter, a special character).
5. Sign in with your new password.
6. If you're an Advocate or Volunteer who hasn't completed training, you'll be redirected straight to **Training**.

**What you'll see:** your role-specific dashboard once training is complete (Advocates: "Managed Care Communities"; Volunteers: Training first, then their assigned family).

### How to view and use your notifications
*Confirmed live in the demo (2026-08-17): the **Notifications** nav item exists (own page,
own icon, separate from the Email settings panel), but the page itself reads: "In-app
notifications coming soon — Real-time in-app notifications are planned for a future
release. You'll receive updates here when someone posts a need, schedule change, or
community announcement." **Not built yet** — same status as "How to RSVP for a scheduled
group training event." Don't write this doc until the feature ships.*

**Related:** [How to modify personal notification settings](how-to/account/manage-notification-emails.md)

---

## Family

### How to modify a family's profile
*Source: `pages/family-detail.tsx` ("Edit Details" → "Save Changes").*

1. Go to **Families** and open the family.
2. Click **Edit Details**.
3. Update the editable fields (Administrative Details: Serving Church, Attending Church, Address, County, Status, etc.).
4. Click **Save Changes**.

**What you'll see:** the updated details reflected immediately on the family's Overview tab.

### How to modify a family's care team
*Source: `pages/family-detail.tsx` ("Remove from care team", volunteer show/hide controls).*

1. Open the family and scroll to the care team / volunteers section.
2. Click **Show all volunteers** to see everyone eligible, or **Show assigned volunteers** to see who's currently on the team.
3. Add or remove volunteers as needed; click **Remove from care team** to take someone off.

**What you'll see:** the care team list updates immediately; removed volunteers no longer see this family.

**Related:** [How to assign a volunteer as Lead to a family](#how-to-assign-a-volunteer-as-lead-to-a-family)

### How to add Parents/Care giver information
*Source: `pages/families-modals.tsx` (`HouseholdManager`: "Add" [Parent/Child], "Save").*

1. Open the family and go to the **Household** section.
2. Click **Add** next to Parent (or Child).
3. Fill in name, phone, email, and other fields as applicable.
4. Click **Save**.

**What you'll see:** the new parent/child appears in the Household list.

### How to invite a family's parents (create their portal login)
*Source: `pages/family-detail.tsx` line ~1200: "Send Account Setup Emails" button (visible to Admin/Advocate); confirm dialog "Send account setup emails?" → "Send Email(s) (N)". Backend: `POST /onboarding/families/{id}/invite-parents`.*

1. Open the family and go to the **Household** section.
2. Click **Send Account Setup Emails** (only shown if at least one parent has an email on file).
3. Review the list of parents who will receive an invite — parents who already have an account are skipped automatically.
4. Click **Send Email(s) (N)** to confirm.
5. Review the results: each parent shows **Email sent**, **Email failed**, **Already has an account**, or **No email on file**.

**What you'll see:** parents with a delivered email get a temporary password and can sign in via [How to accept your invite](#how-to-accept-your-invite-staff-invited-users).

### How to assign a volunteer as Lead to a family
*Source: `pages/family-detail.tsx` ("Lead volunteer for this family" toggle).*

1. Open the family's care team section.
2. Find the volunteer in the list.
3. Toggle **Lead volunteer for this family** on for that volunteer.

**What you'll see:** the volunteer is now flagged as Lead and gains the ability to create/remove needs for this one family.

**Related:** [Roles & who sees what](docs/concepts/roles-and-visibility.md)

### How to view child information
*Source: `pages/families-modals.tsx` (Household list, Child entries — Birthdate, relationship, etc.).*

1. Open the family and go to **Household**.
2. Locate the child in the list.
3. Click into the child's entry to see details (birthdate, relationship, etc.).

**What you'll see:** read-only or editable child details depending on your permissions.

### How to view individually assigned advocates per family
*Source: `pages/family-detail.tsx` ("Assign Advocate", "Unassign advocate", "Show all advocates").*

1. Open the family and locate the Advocate section.
2. Click **Show all advocates** to see the full list, or view the currently assigned advocate(s) directly.

**What you'll see:** which advocate(s), beyond the default church-wide access, are individually tied to this family.

---

## Needs

### How to create a one time need
*Source: `components/need-modal.tsx` ("Post a Need" → "Post Need").*

1. Go to **Needs** (or open the family and go to its Needs tab).
2. Click **Post a Need**.
3. Select the family (if not already scoped), need type, and date/time.
4. Fill in the description.
5. Click **Post Need**.

**What you'll see:** the need appears on the Needs board as **Unassigned** until a volunteer claims it or you assign one.

### How to create a recurring need
*Source: `components/need-modal.tsx` (weekday selector, First/Second/Third/Fourth/Fifth/Last position picker, "Post Need").*

1. Click **Post a Need**.
2. Toggle on **Recurring**.
3. Choose the recurrence pattern (specific weekdays, e.g. Mon/Wed/Fri, or a monthly position like "Second Tuesday").
4. Set the start date/time and, if applicable, an end date.
5. Click **Post Need**.

**What you'll see:** the need appears on the schedule on every date the recurrence rule produces, initially **Unassigned**.

### How to assign a volunteer to a need
*Source: `components/need-assignee-picker.tsx`.*

1. Open the need (from the Needs board or the family's Needs tab).
2. Open the assignee picker.
3. Select a volunteer from the list.

**What you'll see:** the need shows the assigned volunteer's name instead of **Unassigned**.

### How to assign a volunteer to cover a single day of a recurring need
*Source: `components/recurring-needs-panel.tsx`.*

1. Open the recurring need's schedule view.
2. Locate the specific occurrence (date) that needs coverage.
3. Use the assignee picker for that single occurrence — this does not change the assignment on other occurrences.

**What you'll see:** only the selected date shows the new volunteer; the rest of the series is unaffected.

### How to change volunteer assignments on recurring needs
*Source: `components/recurring-needs-panel.tsx`.*

1. Open the recurring need's schedule view.
2. Find the occurrence(s) whose assignment you want to change.
3. Reassign to a different volunteer, or clear the assignment back to **Unassigned**.

**What you'll see:** the schedule reflects the new assignment(s) for the affected date(s) only.

### How to view schedule
*`@frontend`: confirm exact nav label — likely the family's "Schedule" tab per `pages/family-detail.tsx` line 866.*

1. Open a family and click the **Schedule** tab (or go to the top-level Schedule/calendar view).
2. Browse by day/week/month.

**What you'll see:** needs and recurring events plotted on the calendar, each showing its assigned volunteer or **Unassigned**.

### How to request coverage on behalf of a volunteer
*Confirmed live in the demo (2026-08-17, signed in as DemoAdvocate) — Khoury Family →
Schedule → Aug 18 → "Weekly Wednesday dinner" occurrence claimed by Elias Haddad. Source:
`components/need-detail-dialog.tsx` (issue #215). This broadcasts that a claimed slot
needs a **different** volunteer, without removing the current one — a separate control
from "Excuse from this day" / "Replace," which frees or fills the slot outright. Offered
to a manager (Admin/Advocate/Lead Volunteer) **or** the volunteer who holds the claim — so
an advocate can raise this on a volunteer's behalf if the volunteer hasn't or can't.*

1. Go to **Schedule**.
2. Click the day containing the volunteer's occurrence (a small day-summary popover opens if there's more than one item that day).
3. Click the specific occurrence (e.g. "Weekly Wednesday dinner") to open its detail dialog.
4. Under **Modify this day**, find the volunteer's name next to the assigned occurrence.
5. Click **Request coverage** (icon button, tooltip: "Email the care community that this slot needs a different volunteer").

**What you'll see:** the dialog also shows **Replace** (swap in a specific volunteer immediately), **Excuse from this day** (frees the slot, can't be undone), **Reschedule**, and volunteers-needed +/-. Request coverage is the non-destructive option — it notifies the community by email while leaving the volunteer assigned; use it when you want to ask around before actually pulling them off the slot. Everything in this dialog applies to this one date only — the note "Changes here only apply to this day. To edit the schedule... for every date, modify the series" links out to series-level edits.

**Related:** [How to assign a volunteer to cover a single day of a recurring need](#how-to-assign-a-volunteer-to-cover-a-single-day-of-a-recurring-need)

---

## Messaging

### How to start a message thread
*Source: `pages/messages.tsx` ("New conversation" → "Direct message"/"Group conversation" → "Start Chat").*

1. Go to **Messages**.
2. Click **New conversation**.
3. Choose **Direct message** or **Group conversation**.
4. Select the recipient(s) — Volunteers, Family Members, etc.
5. Click **Start Chat**.

**What you'll see:** the new thread opens and you can begin typing.

### How to reply to a message & read receipts
*Source: `pages/messages.tsx` (conversation list, message thread view).*

1. Go to **Messages** and select the conversation.
2. Type your reply and send it.
3. Note the read indicator next to your message once the recipient has opened the thread.

**What you'll see:** a read receipt is not confirmation the request was handled — only that the message was seen.

**Related:** [Replies & read receipts](docs/how-to/messaging/reply-read-receipts.md)

---

## Training

### How to start group training event
*Source: `pages/training-session-create-modal.tsx` ("Create session"), `pages/training-session-host.tsx` ("Start session").*

1. Go to **Training** (Advocates see the group-session management view, not a personal module list).
2. Click **Create session**.
3. Choose the training track/module and any session settings.
4. Click **Start session** when ready to begin.

**What you'll see:** a join code/link to share with attendees, and the session marked **Live**.

### How to Join/Manage a live group training
*Source: `pages/training-session-host.tsx` ("Mark complete", "Complete for group", "End session"), `pages/training-session-join.tsx` ("Join").*

1. From **Training**, open the active session (or share the join code/link so attendees can click **Join**).
2. As host, walk attendees through the module content.
3. Use **Mark complete** for an individual or **Complete for group** to mark everyone present as complete.
4. Click **End session** when finished.

**What you'll see:** the session moves from **Live** to ended; completions are recorded on each attendee's training progress.

### How to view attendees of a group training
*Source: `pages/training-session-host.tsx` (attendee list alongside Mark complete/Remove controls).*

1. Open the live or completed session.
2. Review the attendee list.
3. Use **Remove** to drop an attendee who joined in error, if needed.

**What you'll see:** each attendee's completion status (Required/Optional module, completed or not).

---

## Open questions to resolve before publishing

- `@frontend`: confirm exact nav path/label for "Schedule" outside a single family's tab (top-level calendar?).
- `@frontend`: confirm the Notifications panel's exact icon/location, separate from notification email settings.
- `@backend`/`@frontend`: confirm whether "How to view child information" is truly identical for Advocate vs Admin, or whether any fields are restricted per `ADVOCATE_ROLE.md`'s "every family served by their church" scope note.
