# How To Documents:

_Copied from Google Drive doc "Important help documents"
(https://docs.google.com/document/d/1RCyshgxLsDer3Z1XYaMTOXEnDLNd6eV5mWlohGcJZ_w/edit) on
2026-08-16. This is the planning list of help documents needed to support rollout —
not a published guide itself. Work off this copy; the source-of-truth for what the app
actually does is the frontend/backend repos, not this list (see CLAUDE.md)._

# How To Documents:

## General

  - How to login
  - How to sign up as a volunteer
  - How to self register as a family
  - How to modify personal notification settings
  - How to modify personal profile
  - How to complete personal training
  - How to sign up as a volunteer
  - How to RSVP for a scheduled group training event

## Users:

### As admin:

  - How to create new admin user
  - How to modify an admin user
  - How to remove an admin user

<!-- end list -->

  - How to create new Coordinator
  - How to modify a Coordinator

<!-- end list -->

  - How to assign an individual Coordinator to a county.& consequences

<!-- end list -->

  - How to remove a Coordinator

<!-- end list -->

  - How to create new Advocate
  - How to modify a Advocate

<!-- end list -->

  - How to change advocate training status - link (see training management)
  - How to change advocate church assignment & consequences
  - How to assign an advocate to an individual family - Shared (see Family onboarding)

<!-- end list -->

  - How to Remove an Advocate

<!-- end list -->

  - How to create new volunteer
  - How to modify a volunteer

<!-- end list -->

  - How to change volunteer's training status - link (see training management)
  - How to change volunteer's church assignment & consequences
  - How to change volunteer's family assignment & consequences

<!-- end list -->

  - How to remove a volunteer

### As Advocate:

  - How to onboard a new volunteer \< walk volunteer through self registry and selecting the correct church.
  - How to view volunteer details

### As Lead Volunteer:

  - How to view volunteer details \< Verified live 2026-08-17: Lead Volunteers get a Volunteers nav tab, but it's the same full "Volunteers & Advocates" directory an Admin/Advocate sees (all volunteers/advocates, filterable by church/family/status) — not scoped to just their own family's teammates as first assumed.
  - **Known bug, do not document as a feature:** this directory shows a "Create New User" button to Lead Volunteers. Clicking it and submitting returns a Forbidden error — confirmed by a real Lead Volunteer user 2026-08-17. The button should not be visible to this role. Flag for @frontend; don't write a "how to create a user as a Lead Volunteer" doc.

## Family

  - Shared explanation of all family profile entries.

### As Admin/Coordinator role

  - How to create a new family.

<!-- end list -->

  - Explain that your work is saved while working on creating a new family. This data is saved until you clear it, or close your tab.

<!-- end list -->

  - How to modify family

<!-- end list -->

  - How to change Serving church & consequences
  - How to manage care team
  - How to assign a volunteer as Lead to a family.
  - How to manually add an Advocate to a family.- Shared
  - How to manage needs - link (See Needs)

<!-- end list -->

  - How to "activate" a new family

### As an Advocate

  - How to modify a family's profile
  - How to modify a family's care team
  - How to add Parents/Care giver information
  - How to invite a family's parents (create their portal login)
  - How to assign a volunteer as Lead to a family.
  - How to view child information
  - How to view individually assigned advocates per family

### As Lead Volunteer

  - How to view your assigned family's details \< Read only per Actions list (family bio, photo, parents/children roster on the Families page & dashboard card).

### As Self registered family

  - How to self register as a family.
  - What to expect.

## Needs

### Recurring needs and coverage

#### For admin/lead role

  - How to create recurring needs ie. Weekly meal deliveries

<!-- end list -->

  - How to cover a single day in a recurring need
  - How to switch volunteers from one recurring need to another. Ie. Moving one volunteer from 1st week to 3rd week.

#### For Advocate\&Lead volunteer role

  - How to create a one time need
  - How to create a recurring need
  - How to assign a volunteer to a need
  - How to assign a volunteer to cover a single day of a recurring need
  - How to change volunteer assignments on recurring needs
  - How to view schedule
  - How to request coverage on behalf of a volunteer

#### For Volunteer role

  - How to Claim a need
  - How to request coverage for a single occurrence(day) of a recurring need.
  - How to view your schedule

#### For Family role

  - How to view your needs schedule.

## Messaging

#### For Advocate role

  - How to start a message thread
  - How to reply to a message & read receipts

#### For Volunteer role

  - How to start a message thread \< Verified live 2026-08-17: a "New Conversation" control is available, opening a Family Members picker. This corrects an earlier assumption (from VOLUNTEER_ROLE.md) that volunteers can only reply, not start threads.
  - How to reply to a message & read receipts

## Churches & Counties

### As Admin

  - How to Create a new church
  - How to modify a church

<!-- end list -->

  - How to change which county a church is in.
  - Changing Church contact details

<!-- end list -->

  - How to remove a church & consequences

<!-- end list -->

  - How to create a new County
  - How to modify a county

<!-- end list -->

  - How to assign Coordinators to a county.& consequences

<!-- end list -->

  - How to remove a county

## Training Management & Training

### As Admin:

  - How to modify volunteer/advocate training status

<!-- end list -->

  - How to create new Training module
  - How to modify Training module

<!-- end list -->

  - How to make a training module mandatory

<!-- end list -->

  - How to remove Training module
  - How to re-order Training modules

<!-- end list -->

  - How to view group trainings
  - How to start a new group training
  - How to Join/Manage a live group training
  - How to view attendees of a group training

### As advocate:

  - How to start group training event
  - How to Join/Manage a live group training
  - How to view attendees of a group training

### As Volunteer/Lead Volunteer:

  - How to join a group training session with a session code \< Verified live 2026-08-17: the Training page shows "Have a session code? Join a group training session," which opens a page with a **Session code** field, or lets you pick a session from an "Active in your community" list if any are running — no code needed for those. Volunteers and Lead volunteers can only join a session an advocate is hosting; they cannot start/host one (host controls are advocate/admin-only per the frontend's isHostEligible check).

## Admin Management (Can only be run as an admin/coordinator)

  - Users - Link (See users)
  - Family Agreements

<!-- end list -->

  - How to view Signed Agreements
  - How to print Signed Agreement
  - How to view current Agreement
  - How to view old agreement
  - How to modify current Agreement
  - How to create a new Agreement

<!-- end list -->

  - Reference Data

<!-- end list -->

  - Explain Reference tables

<!-- end list -->

  - Support Types
  - Volunteer Status
  - Child Relationships
  - Family Status
  - User Types
  - Home Types
  - Family Structures
  - Agencies
  - Languages

<!-- end list -->

  - How to modify reference type

<!-- end list -->

  - How to make a support type require or not require childcare approval
  - How to modify Family Status' lifecycle category & consequences
  - How to Add a value to a reference table
  - How to Remove a value from a reference table & consequences
  - How to Modify the value in a reference table & consequences

<!-- end list -->

  - How to use the audit log.

## Reports (Can only be run as an admin/coordinator)

  - How to run a report
  - How to export a report
  - How to customize a report
  - How to export a report (PDF/CSV/Print)
  - How to share a report
  - How to import a shared report

# General How-To documents

# How to login

1.  Navigate to the specific tenant URL your organization has been provided
    1.  Example: demo.wraparound.lucasalign.com
    2.  Other tenants will be {tenant}.wraparound.lucasalign.com
2.  Click "sign in"
3.  If you have created a user account with a google account, you can use the social login "Sign in with Google" button to sign in.
4.  You can also enter your email address and password, and click "Sign in"

# How to accept your invite (for Advocates/Volunteers invited by staff)

_Stub — needs full write-up. Applies to anyone created by an Admin or Advocate via the
onboarding invite flow (as opposed to self-registration): they receive a temporary
password and must set their own password on first sign-in._

# How to sign up as a volunteer

1.  Navigate to the specific tenant URL your organization has been provided
    1.  Example: demo.wraparound.lucasalign.com
    2.  Other tenants will be {tenant}.wraparound.lucasalign.com
        1.  This tenant URL should be findable on your organization's website.
2.  Click "sign in"
3.  At the bottom of the sign in prompt, click "Create an account"
4.  Enter the following
    1.  Email address (Use a gmail account to be able to use google social login if desired)
    2.  Full name
    3.  A secure password
        1.  Required to be 8 characters long.
        2.  Requires a number
        3.  Requires a uppercase letter
        4.  Requires the use of a special character
    4.  Confirm the password you have just typed.
    5.  Click "Sign up"
5.  You will be sent an email with a code to verify your email account.
6.  Enter the code and click "Confirm account"
7.  You will be prompted to complete your volunteer profile
8.  Select your attending church if present in the drop down list, otherwise leave blank. If your church isn't present in the list that means this organization doesn't have any official relationship with your church. Talk to your church leaders and put them in contact with this organization. You can still serve with no church selected.
9.  Enter your mailing address.
10. Click Save and Continue
11. Next Steps are to complete your training.

# How to self register as a family

This guide assumes you as a parent in a family wish to sign up to receive care from an organization.

1.  The organization you wish to self register with should have their family registration link posted on their website. It should look similar to this demo.wraparound.lucasalign.com/family-signup
2.  Enter your full name in "Parent's Full Name"
3.  "Family / household name" is used as an identifier for your family. We recommend you use your full name as opposed to just your surname to avoid duplicate family names. (This value automatically fills
4.  Enter your email address, This will be used for your login and for contact info. (using a @gmail address allows you to make use of google social login)
5.  Entering a phone number will assist in allowing the organization to contact you.
6.  Select the county in which you live, This will ensure you are paired with the correct county coordinator to facilitate your onboarding. If your county is not listed that means the organization doesn't currently serve your county. Feel free to reach out to the organization to request additional information.
7.  Create a password
    1.  Required to be 8 characters long.
    2.  Requires a number
    3.  Requires a uppercase letter
    4.  Requires the use of a special character
8.  Confirm that password.
9.  Click "Create Account"
10. You will be prompted to verify you email address
    1.  Copy the code from your email and paste it into the prompt
    2.  Click Confirm & continue
11. Registration is complete. An automatic email will be sent to your county coordinator including you to help facilitate the start of communication. Your coordinator will reach out to start the on-boarding process and help walk your through the rest of the process..
12. If you wish to pre-fill as much information as possible, you can.
13. You will first need to review the Family Participation Agreement
    1.  If you agree, click "Review & Sign"
        1.  This will display a prompt showing your information and any relevant details, review to make sure they are correct. If there is something wrong, wait for your coordinator to contact you and mention it to them. Click "Go back"
    2.  Click "I agree & sign"
14. You will be taken to an onboarding screen that will allow you to pre-fill all of the on-boarding details. A coordinator will review these details with you during your on-boarding call.
    1.  See Family profile break down for explanation of all of these values. - Link \< \*\*\*\* Needs to be attached \*\*\*\*
15. After pre-filling any details you wish, click "Save my information"
16. Signing in will bring you back to this page, until your family status has been updated.

# How to modify personal notification settings

1.  After signing in click on your picture/user Initial in the top right, or bottom left of the screen.
2.  Scroll down to the Notifications panel
3.  Toggle on or off any notification that you do not wish to receive via email.
4.  Click "Save Changes"

# How to view and use your notifications

Not built yet. Confirmed live in the demo (2026-08-17): the Notifications page exists in
nav but reads "In-app notifications coming soon." Hold this doc until the feature ships —
same status as "How to RSVP for a scheduled group training event."

# How to modify personal profile

1.  After signing in click on your picture/user Initial in the top right, or bottom left of the screen.
2.  Modify any available options. Email and Role can not be modified.
3.  Click "Save Changes"

# How to complete personal training

1.  After signing in as a volunteer or advocate who hasn't completed their training you will be immediately redirected to the training page.
2.  If you are not redirected, locate and click on the "Training" option in the left hand bar.
3.  You will be shown all of the training modules.
4.  Un-Available training modules are greyed out.
5.  Click on the start button next to any available training module to begin it.
6.  Click start on the video or navigate to the external training resource.
7.  When the video or external training resource is complete, you will automatically be marked complete on that module.
8.  Click "Back to Training" to go back to the available modules.
9.  As you complete training modules, the next module will become available.
10. Once your training is complete a serving advocate or coordinator will need to assign you to a family to serve. If you have completed your training and are excited to start serving, please reach out to your organization or your local coordinator to find ways that you can help immediately.

# How to RSVP for a scheduled group training event

Not built yet.

# Users, How-To documents

## Users

### As admin:

  - How to create new admin user
  - How to modify an admin user
  - How to remove an admin user

<!-- end list -->

  - How to create new Coordinator
  - How to modify a Coordinator

<!-- end list -->

  - How to assign an individual Coordinator to a county.& consequences

<!-- end list -->

  - How to remove a Coordinator

<!-- end list -->

  - How to create new Advocate
  - How to modify a Advocate

<!-- end list -->

  - How to change advocate training status - link (see training management)
  - How to change advocate church assignment & consequences
  - How to assign an advocate to an individual family - Shared (see Family onboarding)

<!-- end list -->

  - How to Remove an Advocate

<!-- end list -->

  - How to create new volunteer
  - How to modify a volunteer

<!-- end list -->

  - How to change volunteer's training status - link (see training management)
  - How to change volunteer's church assignment & consequences
  - How to change volunteer's family assignment & consequences

<!-- end list -->

  - How to remove a volunteer

### As Advocate:

  - How to onboard a new volunteer \< walk volunteer through self registry and selecting the correct church.
  - How to view volunteer details

### As Lead Volunteer:

  - How to view volunteer details \< Verified live 2026-08-17: Lead Volunteers get a Volunteers nav tab, but it's the same full "Volunteers & Advocates" directory an Admin/Advocate sees (all volunteers/advocates, filterable by church/family/status) — not scoped to just their own family's teammates as first assumed.
  - **Known bug, do not document as a feature:** this directory shows a "Create New User" button to Lead Volunteers. Clicking it and submitting returns a Forbidden error — confirmed by a real Lead Volunteer user 2026-08-17. The button should not be visible to this role. Flag for @frontend; don't write a "how to create a user as a Lead Volunteer" doc.

# Family, How-To documents

## Family

  - Shared explanation of all family profile entries.

### As Admin/Coordinator role

  - How to create a new family.

<!-- end list -->

  - Explain that your work is saved while working on creating a new family. This data is saved until you clear it, or close your tab.

<!-- end list -->

  - How to modify family

<!-- end list -->

  - How to change Serving church & consequences
  - How to manage care team
  - How to assign a volunteer as Lead to a family.
  - How to manually add an Advocate to a family.- Shared
  - How to manage needs - link (See Needs)

<!-- end list -->

  - How to "activate" a new family

### As an Advocate

  - How to modify a family's profile
  - How to modify a family's care team
  - How to add Parents/Care giver information
  - How to invite a family's parents (create their portal login)
  - How to assign a volunteer as Lead to a family.
  - How to view child information
  - How to view individually assigned advocates per family

### As Lead Volunteer

  - How to view your assigned family's details \< Read only per Actions list (family bio, photo, parents/children roster on the Families page & dashboard card).

### As Self registered family

  - How to self register as a family.
  - What to expect.

# Needs, How-To documents

## Needs

### Recurring needs and coverage

#### For admin/lead role

  - How to create recurring needs ie. Weekly meal deliveries

<!-- end list -->

  - How to cover a single day in a recurring need
  - How to switch volunteers from one recurring need to another. Ie. Moving one volunteer from 1st week to 3rd week.

#### For Advocate\&Lead volunteer role

  - How to create a one time need
  - How to create a recurring need
  - How to assign a volunteer to a need
  - How to assign a volunteer to cover a single day of a recurring need
  - How to change volunteer assignments on recurring needs
  - How to view schedule
  - How to request coverage on behalf of a volunteer

#### For Volunteer role

  - How to Claim a need
  - How to request coverage for a single occurrence(day) of a recurring need.
  - How to view your schedule

#### For Family role

  - How to view your needs schedule.

# Messaging, How-To documents

## Messaging

#### For Advocate role

  - How to start a message thread
  - How to reply to a message & read receipts

#### For Volunteer role

  - How to start a message thread \< Verified live 2026-08-17: a "New Conversation" control is available, opening a Family Members picker. This corrects an earlier assumption (from VOLUNTEER_ROLE.md) that volunteers can only reply, not start threads.
  - How to reply to a message & read receipts

# Churches & Counties, How-To documents

## Churches & Counties

### As Admin

  - How to Create a new church
  - How to modify a church

<!-- end list -->

  - How to change which county a church is in.
  - Changing Church contact details

<!-- end list -->

  - How to remove a church & consequences

<!-- end list -->

  - How to create a new County
  - How to modify a county

<!-- end list -->

  - How to assign Coordinators to a county.& consequences

<!-- end list -->

  - How to remove a county

# Training Management & Training, How-To documents

## Training Management & Training

### As Admin:

  - How to modify volunteer/advocate training status

<!-- end list -->

  - How to create new Training module
  - How to modify Training module

<!-- end list -->

  - How to make a training module mandatory

<!-- end list -->

  - How to remove Training module
  - How to re-order Training modules

<!-- end list -->

  - How to view group trainings
  - How to start a new group training
  - How to Join/Manage a live group training
  - How to view attendees of a group training

### As advocate:

  - How to start group training event
  - How to Join/Manage a live group training
  - How to view attendees of a group training

### As Volunteer/Lead Volunteer:

  - How to join a group training session with a session code \< Verified live 2026-08-17: the Training page shows "Have a session code? Join a group training session," which opens a page with a **Session code** field, or lets you pick a session from an "Active in your community" list if any are running — no code needed for those. Volunteers and Lead volunteers can only join a session an advocate is hosting; they cannot start/host one (host controls are advocate/admin-only per the frontend's isHostEligible check).

# Admin Management, How-To documents

## Admin Management (Can only be run as an admin/coordinator)

  - Users - Link (See users)
  - Family Agreements

<!-- end list -->

  - How to view Signed Agreements
  - How to print Signed Agreement
  - How to view current Agreement
  - How to view old agreement
  - How to modify current Agreement
  - How to create a new Agreement

<!-- end list -->

  - Reference Data

<!-- end list -->

  - Explain Reference tables

<!-- end list -->

  - Support Types
  - Volunteer Status
  - Child Relationships
  - Family Status
  - User Types
  - Home Types
  - Family Structures
  - Agencies
  - Languages

<!-- end list -->

  - How to modify reference type

<!-- end list -->

  - How to make a support type require or not require childcare approval
  - How to modify Family Status' lifecycle category & consequences
  - How to Add a value to a reference table
  - How to Remove a value from a reference table & consequences
  - How to Modify the value in a reference table & consequences

<!-- end list -->

  - How to use the audit log.

# Reports, How-To documents

## Reports (Can only be run as an admin/coordinator)

  - How to run a report
  - How to export a report
  - How to customize a report
  - How to export a report (PDF/CSV/Print)
  - How to share a report
  - How to import a shared report

# Actions that can be taken

# Actions that can be taken

## Admin (Admin/Coordinator):

  - Create/modify/remove:
    - Admins
    - Coordinators
    - Advocates
      - Training status
      - Church Assignment
      - Individual family Assignments
    - Volunteers
      - Training Status
      - Church Assignment
      - Family Assignment
    - Families
      - Profile
      - Family needs/schedule
      - Care Team
      - Advocates
      - Serving Church assignment
    - Churches
      - Church details
      - County assignment
    - Counties
      - County details
    - Reports
      - Run reports
      - Customize reports
      - Export reports
      - Share reports
      - Import shared reports
    - Admin data
      - Family Agreements
      - Reference Data
    - Training Management
      - Training Modules
      - Group Training
      - Volunteer training

## Advocate (Advocate access is based on which church they serve, and any individual family assignments)

  - Read/Write
    - Personal Details
    - Serving Church details \< should this be a thing? Advocates able to change contact information for the church they serve?
    - Family

<!-- end list -->

  - Family profile
    - Excepting child information.
  - Care team
  - Create Family users
  - A Family's Needs and Schedule

<!-- end list -->

  - Messaging
  - Training
    - Complete personal training
    - Create and lead Group training sessions

<!-- end list -->

  - Read Only
    - Family
      - Child information
      - Advocate assignment
    - Volunteers
      - Volunteer profile

## Volunteer (Volunteer access is scoped by which family they are assigned to, A volunteer can serve multiple families)

### Lead volunteer

  - Read/Write
    - Family needs/schedule
    - Messaging
    - Training
      - Complete personal training
  - Read Only
    - Family details
    - Volunteer details

### Support volunteer

  - Read/Write
    - Needs
      - Claiming Family need
      - Requesting need coverage
    - Messaging
    - Training
      - Complete personal training
