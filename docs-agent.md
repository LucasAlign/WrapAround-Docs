# Docs agent runbook

Instructions for the nightly docs agent (scheduled task, midnight ET). A human reviews and merges
every PR it opens. Read `CLAUDE.md` and `CONTRIBUTING.md` first — their rules apply in full.

## Repos

| Repo | Use |
|---|---|
| `LucasAlign/WrapAround-Docs` | the help site — the only repo you write to |
| `AustinLucas/Align-FrontEnd` | exact labels, screens, routes, navigation |
| `AustinLucas/Align-Core` | roles, scoping, statuses, business rules |
| `LucasAlign/BackEnd-FrontEnd-Refrences` | API + DB reference |
| `LucasAlign/Wraparound-testing-Suite` | login + `npm run screenshot` against **dev** |

Clone any that are missing, then `git pull --ff-only` each. Never push to the code repos.

## Run procedure

**0. Gate.** If any open PR in WrapAround-Docs has the `docs-agent` label, stop now. No work, no PR.

**1. Clean up leftovers.** If `.docs-agent/created.json` lists items, try to delete them in dev
(they were created by an earlier run). Keep any that still fail.

**2. Sync drift.** List commits merged to `main` in Align-Core and Align-FrontEnd since
`.docs-agent/state.json` → `lastRun`. For each user-visible change (labels, routes, nav, roles,
permissions, statuses, new features), find the affected pages (`grep` the label/route) and fix them.

**3. Advance.** Pick up to **3** pages with `status: needs-review` (prefer pages touched by step 2,
then how-tos, then oldest). For each:
- verify every claim against code (frontend for labels/steps, backend for who-can-do-what);
- resolve `@frontend` / `@backend` markers the code answers; leave the rest;
- set `status: ready` only when the Definition of Done in `CLAUDE.md` is fully met **and** the page
  makes no role/permission claim; otherwise leave it at `needs-review`.

**4. New page.** At most **1**: a user-facing feature with no help page (from step 2 or
`user-docs-plan.md`). Start from `templates/how-to-template.md`, add it to `nav:` in `mkdocs.yml`,
set `status: draft`.

**5. Live verify + screenshots (best effort).** For pages touched in steps 2–4:
- write a `shots.json` (format in `Wraparound-testing-Suite/src/screenshot.ts`) that logs in as
  the page's role and walks its steps, one `shot` per step;
- run `npm run screenshot -- shots.json --out <docs>/docs/assets/screens/<page-slug>` in the suite
  (needs the `WA_*` env vars; set `WA_CHROMIUM_PATH=/opt/pw-browsers/chromium`);
- use `highlight` on the control each step tells the reader to tap;
- embed with alt text: `![Alt text.](../../assets/screens/<page-slug>/<shot>.png)`;
- if the live app disagrees with the page, fix the page; if it disagrees with the **code**, flag it
  in the PR instead of guessing;
- if login, network or a step fails, keep going without that shot and list it in the PR.

Roles: `admin`, `coordinator`, `advocate`, `volunteer`, `family`. The demo volunteer is a **lead**
on one family and **support** on another: switch family to capture either view. The demo family
account has not signed the participation agreement, so its post-agreement screens can't be captured.

**6. Validate.** `pip install -r requirements.txt && mkdocs build --strict` must pass. Fix or revert
whatever breaks it.

**7. Clean up.** Delete everything you created in dev this run (step 5). Write whatever couldn't be
deleted to `.docs-agent/created.json` (otherwise `[]`). Update `state.json` → `lastRun` (now, ET)
and `lastCommits` (head SHAs you synced to).

**8. Publish.** If no page changed, open no PR and exit (state isn't saved, so the next run simply
re-checks the same window — harmless). Otherwise branch
`docs-agent/YYYY-MM-DD` from `main`, commit `docs: nightly docs-agent update (YYYY-MM-DD)`, push,
open a PR labelled `docs-agent` with the body below.

## PR body

```
## Drift fixed
- <code repo commit/PR> → <page>: <what changed>
## Pages advanced
- <page>: <old status> → <new status>
## New pages
- <page>
## Screenshots
- captured: <n> · skipped: <page/shot — reason>
## Needs a human
- permission/scope claims to confirm (backend review)
- markers the code couldn't answer
- code vs live-app disagreements
- dev data left behind (if any)
```

## Rules

- **Code wins.** Never cite other `docs/` pages as evidence. Quote UI labels exactly from frontend
  source; never invent them.
- **Size cap:** about 10 changed pages per PR, so review takes minutes. Screenshots don't count.
- **Never** merge, push to `main`, or touch the code repos.
- **Dev data:** you may create data in dev to stage tutorials. Mark it: put `[docs-agent]` in a
  title or notes field where one exists, and record each created item (type, id, role used) in
  `.docs-agent/created.json` as you go. Never edit or delete data you didn't create. Dev email
  notifications are suppressed (`notificationsDisabled` defaults on for dev).
- **Screenshot data:** content must be plausible (real-looking needs, dates, schedules, messages).
  Names, emails and phone numbers must be **obviously fake**: `Sample Volunteer`, `Test Parent`,
  `jane.example@example.com`, `555-0100`. Mask (`mask` in the shot step) anything that looks like
  a real person's details.
- No secrets in commits, PRs or logs.
