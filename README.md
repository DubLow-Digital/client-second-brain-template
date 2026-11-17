# Client Second Brain — Template (by DubLow Digital)

A free, public template for giving your business an **AI second brain**: one private GitHub repo that holds everything an AI assistant needs to know about your business, so it stops asking the same questions and starts doing useful work.

No downloads. No installs. You need two things: a free GitHub account and Ask AI with GitHub connected.

## Start here (3 steps)

1. **Connect GitHub** to your Ask AI (Connectors). Allow it to read and create repositories.
2. **Paste this into Ask AI** and press send:

   > Set up my business second brain. Read the skill at `DubLow-Digital/client-second-brain-template`, file `skills/client-brain-setup/SKILL.md`, and follow it step by step.

3. It creates a **private** repo called `brain-<your-business>` in your GitHub account, gives you project instructions to paste into a new Ask AI project, and then interviews you with high-impact questions to fill the brain in.

After that, in your project, just work normally. At the end of a session the AI saves what it learned into your brain repo.

## Joining an existing brain (teammates and helpers)

Use this if someone else already created the brain and you are **joining it**: a teammate, a helper, or the DubLow Digital team. Do **not** run the setup prompt above; that would create a second, empty brain.

**Before you start**

1. Ask the brain's owner to add your GitHub username as a collaborator on their private `brain-<business>` repo (repo Settings → Collaborators), then accept the invite from your email or GitHub notifications.
2. Connect **your own GitHub** to **your own Ask AI** (Connectors). Allow it to read repositories (and to write, if you will be saving updates).
3. Get the exact repo name from the owner, for example `glo-ocala-owner/brain-glo-ocala`.

**Paste this into Ask AI** (replace the repo name) and press send:

> Connect me to an existing second brain. The brain is the private GitHub repo `<owner>/brain-<business>`. Do this: (1) Check you can read that repo with my connected GitHub. If you cannot, tell me exactly what access I need to ask the owner for, and stop. (2) Read `index.md`, `03-status.md` and `09-open-items.md` from that repo and tell me in three sentences where things stand. (3) Read the short version in `AGENTS.md` of `DubLow-Digital/client-second-brain-template`, fill in this brain's repo name, and give me the finished text to paste into the instructions of a new Ask AI project. Do not change anything in the repo.

**Then**

- Create a **new Ask AI project** and paste the instructions it gave you.
- Start a chat inside that project. It will read the brain at the start of every session and, at the end, offer to save what it learned (after showing you the changes and getting your yes).
- If the brain is mostly empty, say "run the interview skill" and it will use `skills/client-brain-interview/SKILL.md` from this template.

Everything the AI learns is saved to the one shared brain repo, so every teammate's project stays in sync.

## How it works

| Piece | Where it lives | What it does |
|---|---|---|
| This template | `DubLow-Digital/client-second-brain-template` (public) | The blank brain and the skills. Never holds anyone's private info. |
| Your brain | `<you>/brain-<business>` (**private**, in your GitHub) | Your single source of truth. A copy of this template, filled in. |
| Your Ask AI project | In Ask AI | Short instructions that point the AI at your brain. |
| The skills | `skills/` in this template, read live | Setup, updating and interviewing. Improve them here once and everyone gets the new version. |

Your brain is a **copy**, not a fork. Forks of a public repo are public; your brain must stay private.

## The three skills

| Skill | Run it when | What it does |
|---|---|---|
| `skills/client-brain-setup/SKILL.md` | Once, to start | Creates your private brain repo from this template and hands you the project instructions |
| `skills/client-brain-interview/SKILL.md` | After setup, and whenever the brain has gaps | Asks high-impact questions in short rounds and saves the answers in the right files |
| `skills/client-brain-updater/SKILL.md` | End of every work session | Saves status, log, decisions and open items to your repo, after showing you what will change |

## What is in a brain

| File | Purpose | Updated |
|---|---|---|
| `AGENTS.md` | Rules the AI follows: read first, write last, what never goes in | Rarely |
| `index.md` | Map of the brain, read first | When files are added |
| `00-profile.md` | Who you are, key people, services | Onboarding, then as it changes |
| `01-business-and-brand.md` | Offer, customers, brand voice, online presence | As it changes |
| `02-services-and-scope.md` | Every service: status, owner, dates | Whenever a service moves |
| `03-status.md` | Where things stand RIGHT NOW and what is next | Every session (overwrite) |
| `04-log.md` | Dated history of work (append only) | Every session (append) |
| `05-decisions.md` | Decisions made and why | When a decision is made |
| `06-contacts-and-systems.md` | Where things live: CRM, domains, profiles (links only) | When systems change |
| `07-compliance-and-dates.md` | Registrations, renewals, campaign dates | When dates are set or met |
| `08-financial-snapshot.md` | Billing and results picture, no card or bank numbers | Monthly |
| `09-open-items.md` | Waiting-on, blockers, questions | Every session |
| `meetings/_template.md` | Copy for each meeting or call | Per meeting |
| `deliverables/README.md` | Index of finished documents with links | When a document is delivered |

## Golden rules

- **Never store secrets.** No passwords, API keys or tokens, no SSNs, no full EINs, no bank or card numbers. Write pointers instead, e.g. "EIN on file with the accountant".
- **No customer or patient data.** Contact lists, intake forms and similar stay in your CRM or business systems.
- **Your CRM stays the source of truth for contact and opportunity records.** The brain holds context around them.
- **`04-log.md` is append only. `03-status.md` is overwritten** each session.
- **Draft-only by default.** The AI never sends, schedules, publishes or launches anything without your approval.
- Keep your brain repo **private**. If you want the DubLow Digital team to help, add them as collaborators yourself in GitHub settings.

## For the template maintainers

- Keep this repo **public** with the **Template repository** setting on.
- Never put client information in this repo.
- Skills are read live by every user, so edit them carefully and keep each one self-contained.
