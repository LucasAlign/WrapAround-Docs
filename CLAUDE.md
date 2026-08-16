# CLAUDE.md — WrapAround-Docs

Guidance for working in this repo. This is a **documentation site**, not application code:
end-user help for the WrapAround app, authored in Markdown and published via MkDocs Material.
See [`README.md`](README.md) for local setup, [`CONTRIBUTING.md`](CONTRIBUTING.md) for the
full two-agent contract, and [`user-docs-plan.md`](user-docs-plan.md) for the guiding plan.

## Source of truth

**The content under `docs/` is NOT authoritative about how the app actually works or looks.**
It's the current draft of the help site and may be stale, wrong, or ahead of the real product.
The actual source of truth is the application code, in sibling repos on this machine:

- **Frontend** — `C:\Users\austi\Align-FrontEnd` (GitHub: `AustinLucas/Align-frontend`) —
  exact screen names, button/label text, navigation, screenshots.
- **Backend** — `C:\Users\austi\KeyStone-Backend\KeyFam-infrastructure` (GitHub:
  `AustinLucas/Align-Core`) — actual roles, scoping/permission rules, statuses, data model,
  business rules.

Before writing or correcting any page, verify claims against those repos (or the running
app), not against other pages in `docs/`. If something in `docs/` conflicts with what the
code does, the code wins — fix the doc.

## What WrapAround is (per this repo's docs — verify against the code repos above)

WrapAround helps a foster/adoptive **family** and the people supporting them — a **care
circle** — coordinate care: **needs** (requests for help volunteers **claim**), **schedules**
(events, including recurring ones), **messages** (private threads), **posts** (circle-wide
updates), and **training** (modules staff assign). Roles and scoping are described in
[roles-and-visibility.md](docs/concepts/roles-and-visibility.md), but treat the specifics
(role names, exact permissions) as claims to confirm against the backend repo, not fact.

## Repo structure

- `docs/get-started/` — one onboarding walkthrough per role
- `docs/concepts/` — understanding-oriented (what things are, how scope works)
- `docs/how-to/` — task-oriented, one page = one job (the bulk of the site)
- `docs/reference/` — glossary, permissions matrix, statuses, FAQ, troubleshooting
- `templates/how-to-template.md` — starting point for every new how-to
- `mkdocs.yml` — nav tree; every new page must be added here or it won't ship

Follows the [Diátaxis](https://diataxis.fr) model. People search for tasks, so how-to guides
carry the most weight.

## The two-agent contract (read `CONTRIBUTING.md` for full detail)

This site is written jointly by a **backend agent** and a **frontend agent**, with human
review. Ownership by doc type:

| Section | Primary author | Required reviewer |
|---|---|---|
| Concepts, Reference | Backend | Frontend |
| How-To, Get Started | Frontend | Backend |

**Backend review is mandatory** on anything asserting what a role can see or do — scoping
bugs here are correctness bugs, not typos.

Every page carries front-matter: `status: draft → needs-ui → needs-review → ready` and
`primary: backend | frontend`. Open questions for the other agent are left as inline HTML
comments — `<!-- @frontend: ... -->` or `<!-- @backend: ... -->` — resolved and deleted
before a page reaches `status: ready`. Find your queue:

```bash
grep -rn "@frontend" docs/
grep -rn "@backend"  docs/
```

When acting as either agent in this repo, honor this split — don't casually rewrite a
Concepts page's substance as "frontend," and don't invent UI labels as "backend."

## Conventions

- **Voice:** second person, imperative ("Tap **Claim**"), present tense.
- **Terminology = exact in-app labels.** Verify against the frontend repo (or the running
  app), not against [glossary.md](docs/reference/glossary.md) — if the app and glossary
  disagree, fix the glossary in the same PR.
- One task per how-to page; file names are `kebab-case.md`.
- Annotate screenshots, add alt text to every image, **never include real family data**.
- New pages: create the `.md` file, add it to `nav:` in `mkdocs.yml`, start how-tos from
  `templates/how-to-template.md`.

## Validating changes

```bash
pip install -r requirements.txt
mkdocs serve              # live-reload preview at http://127.0.0.1:8000
mkdocs build --strict     # what CI runs — fails on broken links or missing nav entries
```

Always run `mkdocs build --strict` before considering a docs change done — CI gates on it.

## Definition of done (per page)

- Follows the how-to template / style conventions above
- Verified against the **frontend and backend repos** (exact labels, real steps, real rules)
  — not just against other pages in this repo
- Screenshots current, annotated, with alt text
- Linked from `mkdocs.yml` nav and from related pages
- No PII in examples
- No unresolved `@frontend` / `@backend` markers
