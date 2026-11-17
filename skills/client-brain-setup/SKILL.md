---
name: client-brain-setup
description: Use when someone wants to start their business second brain. Finds the public DubLow client-second-brain-template, creates a PRIVATE brain repo in the user's own GitHub account (a copy, not a fork), fills in the business name, and hands back the instructions to paste into a new Ask AI project. Run once per business. Needs GitHub connected to Ask AI.
---

# Client Brain Setup

Template repo (public, read only): `DubLow-Digital/client-second-brain-template`
Result: a private repo `<owner>/brain-<client-slug>` that becomes the business's single source of truth.

## Before you start

- Always run a fresh discovery of the GitHub connection and read each tool's schema before calling it.
- Check GitHub is connected by asking for the signed-in user. If it fails, stop and tell the user: open Connectors in Ask AI, connect GitHub, allow it to read and create repositories, then run this again. Do not continue without it.
- Speak plainly. Assume the user is not technical.

## Hard rules

1. The brain repo is always **private**. Never create it public, and never fork the template (forks of a public repo are public).
2. Never write to the template repo. It is read only for you.
3. One repo per run. If a brain repo for this business already exists, do not create another (see step 2).
4. Never put passwords, keys, tokens, SSNs, EINs, bank or card numbers anywhere in the repo.
5. Get the user's yes before creating anything.

## Steps

### 1. Gather
Ask (one short message):
- **Business name** (as customers know it).
- **Where should the repo live?** Default: the user's own GitHub account (from the signed-in user). Only use an organization if they name one they belong to.

Build the **slug** from the business name: lowercase, letters and numbers, spaces become hyphens, drop punctuation and "LLC/Inc". Example: "Glo Ocala, LLC" becomes `glo-ocala`. Repo name: `brain-<slug>`.

### 2. Check it does not exist yet
Search repositories for `brain-<slug>` under the chosen owner. If it exists, do NOT create a new one: tell the user it is already set up, give them the project instructions (step 8) for that repo, and offer the interview skill. Stop here.

### 3. Ask for approval
Show a short summary and wait for a yes:
- Repo: `<owner>/brain-<slug>`
- Visibility: **Private**
- Created from: the public DubLow template (copied, not forked)
- What gets created: 14 brain files, a meetings folder and a deliverables folder

### 4. Create the repo
Create a repository named `brain-<slug>` with private set to true and auto-initialize on (so the main branch exists). Description: `Private second brain for <Business Name>`. Set the organization field only if the user chose one.

### 5. Read the template
Read the template repo root, then the `meetings` and `deliverables` folders. Copy these files, exactly as they are:
`AGENTS.md`, `index.md`, `00-profile.md`, `01-business-and-brand.md`, `02-services-and-scope.md`, `03-status.md`, `04-log.md`, `05-decisions.md`, `06-contacts-and-systems.md`, `07-compliance-and-dates.md`, `08-financial-snapshot.md`, `09-open-items.md`, `meetings/_template.md`, `deliverables/README.md`.

Do **not** copy the template's `README.md` or the `skills/` folder. Skills stay in the template and are read live, so every brain always gets the newest version.

### 6. Fill in the basics
In the copies, replace:
- `<CLIENT NAME>` with the business name (`index.md`)
- `<client-slug>` with the slug (`index.md`, `AGENTS.md`, `06-contacts-and-systems.md`)
- `<owner>` with the repo owner (`index.md`, `AGENTS.md`, `06-contacts-and-systems.md`)
- `Brain last reviewed` in `index.md` with today's date
- The example line in `04-log.md` with: `YYYY-MM-DD | <who> | Onboarding | Created client brain from template | Next: run the interview`

Leave every other placeholder for the interview skill to fill in.

Also write a new `README.md` for the brain repo:

```
# <Business Name> — Second Brain (private)
The single source of truth about <Business Name> for people and AI. Created from the DubLow Digital client second brain template.
Skills (setup, interview, updater) are read live from DubLow-Digital/client-second-brain-template.
Start with index.md. Never store passwords, keys, or customer data here.
```

### 7. Save everything in one commit
Push all files to `main` in a single commit. Message: `Create client brain from DubLow template`.

Then list the new repo's root and confirm all files are present. Tell the user plainly if anything is missing.

### 8. Hand back the project instructions
Give the user this block with the real owner and slug filled in, and tell them to create a **new Ask AI project** and paste it into the project's instructions (this skill cannot create the project itself):

```
This business has a second brain in the private GitHub repo <owner>/brain-<slug>. It is the single source of truth.
START of every session: read index.md, 03-status.md, 09-open-items.md and the last 20 lines of 04-log.md from that repo before doing anything, then tell me in two or three sentences where things stand.
END of every session: follow the skill skills/client-brain-updater/SKILL.md in the public repo DubLow-Digital/client-second-brain-template. Show me the changes, get my yes, then save them to the brain repo.
If the brain has gaps, offer to run skills/client-brain-interview/SKILL.md from the same template repo.
Never write passwords, API keys, SSNs, full EINs, bank or card numbers, or customer or patient data into the brain.
Draft only: never send, schedule, publish or launch anything without my approval.
If the brain and my CRM disagree, trust the CRM for records and tell me about the mismatch.
```

Remind them:
- Everyone who uses the project needs GitHub connected in their own Ask AI, with access to this repo.
- If they want the DubLow Digital team to help, they add them as collaborators in the repo's GitHub settings. Do not do that for them.

### 9. Offer the interview
Say the brain is created but empty, and offer to start the interview now (`skills/client-brain-interview/SKILL.md` in the template repo). The quick start takes about 10 minutes.

## Report
Tell the user: the repo name and that it is private, how many files were created, the project instructions block, and the next step.
