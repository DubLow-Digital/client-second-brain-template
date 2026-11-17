# Client Second Brain — Template

The shared memory for ONE Whitelow Legacy Group client. Anyone on the team (and their AI) reads it before working and updates it after working, so every project, sub-account and person stays in sync.

## How to use this template

1. Click **Use this template** on GitHub and create a new **private** repo named `brain-<client-slug>` (example: `brain-dublow-company-dr`).
2. Fill in `00-profile.md` first, then `02-services-and-scope.md`.
3. Paste the contents of `AGENTS.md` (the short version at the top) into the instructions of every AI project that touches this client.
4. Link finished documents from `deliverables/README.md`. Files themselves stay in SharePoint: Whitelow Legacy Group > Clients > <Client Name>.

## What is in here

| File | Purpose | Who updates it |
|---|---|---|
| `AGENTS.md` | Rules the AI follows: read first, write last, what never goes in | Rarely (company-wide) |
| `index.md` | Map of the brain, read first | When files are added |
| `00-profile.md` | Who the client is, key people, services bought | Onboarding, then as it changes |
| `01-business-and-brand.md` | Offer, customers, brand voice, website | As it changes |
| `02-services-and-scope.md` | Every Whitelow service: status, owner, dates | Whenever a service moves |
| `03-status.md` | Where things stand RIGHT NOW and what is next | Every work session (overwrite) |
| `04-log.md` | Dated history of work done (append only) | Every work session (append) |
| `05-decisions.md` | Decisions made and why | When a decision is made |
| `06-contacts-and-systems.md` | Where things live: CRM, SharePoint, QuickBooks (links only) | When systems change |
| `07-compliance-and-dates.md` | Deadlines and who handles each | When dates are set or met |
| `08-financial-snapshot.md` | Plain-English money picture, no account numbers | Monthly |
| `09-open-items.md` | Waiting-on-client, blockers, questions | Every work session |
| `meetings/_template.md` | Copy for each meeting or call | Per meeting |
| `deliverables/README.md` | Index of finished documents with SharePoint links | When a document is delivered |

## Golden rules

- **Never store secrets here.** No passwords (those live in Keeper), no SSNs, no full EINs, no bank or card numbers, no driver licence numbers. Write pointers instead, e.g. "EIN on file in SharePoint > Formation".
- **The CRM stays the source of truth for contact and opportunity records.** This brain holds context and knowledge around them.
- **`04-log.md` is append only.** Add lines at the bottom, never edit old ones. That keeps two people from overwriting each other.
- **`03-status.md` is overwritten** each session so it always shows the current picture.
- Keep entries short, dated (YYYY-MM-DD) and signed with who did the work.
