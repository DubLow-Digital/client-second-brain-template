# DubLow Client Second Brain — Template

The shared memory for ONE DubLow Digital client. Anyone on the team (and their AI) reads it before working and updates it after working, so every project, sub-account and person stays in sync.

## How the brain is stored

Each client's brain lives in two places that must match:

| Place | What it is | Used for |
|---|---|---|
| GitHub repo `DubLow-Digital/brain-<client-slug>` | The working copy, created from this template | Fast reads and writes by the team and AI |
| SharePoint folder (see below) | The readable copy the whole team can open | Day-to-day reference, linked from the client's folder |

**SharePoint brain folder (exact path):**

`Documents > DubLow Company Drive > 2. Clients > <Specific Client's Folder> > Dublow Clients Brain`

(Browser address: `https://dublow.sharepoint.com/Shared Documents/DubLow Company Drive/2. Clients/<Client Folder>/Dublow Clients Brain`)

The procedure for keeping the SharePoint folder up to date is in `skills/dublow-client-brain-updater/SKILL.md`.

## How to use this template

1. Click **Use this template** on GitHub and create a new **private** repo named `brain-<client-slug>` (example: `brain-glo-ocala`).
2. Fill in `00-profile.md` first, then `02-services-and-scope.md`.
3. Paste the short version at the top of `AGENTS.md` into the instructions of every AI project that touches this client.
4. Create the `Dublow Clients Brain` folder inside the client's folder in SharePoint and sync the brain files into it using the updater skill.
5. Link finished documents from `deliverables/README.md`. The documents themselves stay in the client's SharePoint folders (Brand, Digital Marketing Services, Managed IT, Operations, Agreements).

## What is in here

| File | Purpose | Who updates it |
|---|---|---|
| `AGENTS.md` | Rules the AI follows: read first, write last, what never goes in | Rarely (company-wide) |
| `index.md` | Map of the brain, read first | When files are added |
| `00-profile.md` | Who the client is, key people, services bought | Onboarding, then as it changes |
| `01-business-and-brand.md` | Offer, customers, brand voice, online presence | As it changes |
| `02-services-and-scope.md` | Every DubLow service: status, owner, dates | Whenever a service moves |
| `03-status.md` | Where things stand RIGHT NOW and what is next | Every work session (overwrite) |
| `04-log.md` | Dated history of work done (append only) | Every work session (append) |
| `05-decisions.md` | Decisions made and why | When a decision is made |
| `06-contacts-and-systems.md` | Where things live: CRM sub-account, domains, profiles, SharePoint, Notion (links only) | When systems change |
| `07-compliance-and-dates.md` | Registrations, renewals and campaign dates, and who handles each | When dates are set or met |
| `08-financial-snapshot.md` | Billing and retainer picture, no card or bank numbers | Monthly |
| `09-open-items.md` | Waiting-on-client, blockers, questions | Every work session |
| `meetings/_template.md` | Copy for each meeting or call | Per meeting |
| `deliverables/README.md` | Index of finished documents with SharePoint links | When a document is delivered |
| `skills/dublow-client-brain-updater/SKILL.md` | How to update the client's SharePoint brain folder | Rarely |

## Golden rules

- **Never store secrets here.** No passwords (those live in the DubLow password manager), no API keys or tokens, no SSNs, no full EINs, no bank or card numbers. Write pointers instead, e.g. "EIN on file in SharePoint > Agreements".
- **No client customer or patient data.** Contact lists, intake forms and similar stay in the CRM or the client's SharePoint Operations folder.
- **The CRM stays the source of truth for contact and opportunity records.** This brain holds context and knowledge around them.
- **`04-log.md` is append only.** Add lines at the bottom, never edit old ones. That keeps two people from overwriting each other.
- **`03-status.md` is overwritten** each session so it always shows the current picture.
- **Draft-only by default.** Nothing is sent, scheduled, published or launched for a client without a person's approval.
- Keep entries short, dated (YYYY-MM-DD) and signed with who did the work.
