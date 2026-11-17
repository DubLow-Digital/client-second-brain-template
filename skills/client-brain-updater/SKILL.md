---
name: client-brain-updater
description: Use at the end of a work session, or whenever new information should be saved, to update the business's private brain repo on GitHub (status, log, decisions, open items, services, meetings, deliverables). Shows the changes first, scans for secrets, then commits. Never deletes files, never touches other repos.
---

# Client Brain Updater

Keeps the business's private brain repo (`<owner>/brain-<slug>`) current. The repo is the single source of truth.

## Before you start

- Run a fresh discovery of the GitHub connection and read each tool's schema before calling it.
- Find the brain repo: use the name in the project instructions. If there is none, search repositories for `brain-` under the signed-in user; if there are several, ask which one. If there are none, point the user to `skills/client-brain-setup/SKILL.md` in `DubLow-Digital/client-second-brain-template`.

## Hard rules

1. **Only the brain repo.** Never write to the template repo or any other repo.
2. **Never delete files.** Never make the repo public.
3. **`04-log.md` is append only.** Read the current file, keep every line, add new lines at the bottom.
4. **`03-status.md` is overwritten** with the current picture.
5. **No secrets or customer data.** No passwords, API keys, tokens, SSNs, full EINs, bank or card numbers; no customer, patient or lead lists. If the user says one, leave it out and tell them.
6. **Facts only.** Mark guesses `(unverified)`. Never invent dates, amounts or decisions.
7. **Show, then save.** Get the user's yes before the first commit of the session.

## Start of session (reading)

Read from the brain repo: `index.md`, `00-profile.md`, `03-status.md`, `09-open-items.md`, the last 20 lines of `04-log.md`, and any entry in `05-decisions.md` that touches today's task. Tell the user in two or three sentences where things stand. Read `01-business-and-brand.md` before writing any copy.

## End of session (saving)

### 1. Work out what changed
Go through the session and list, per file:

| File | Change |
|---|---|
| `04-log.md` | One or more new lines: `YYYY-MM-DD | <who> | <service> | <what was done> | <result or next step>` |
| `03-status.md` | New summary, working on now, done recently, next up (in order), waiting on, risks |
| `09-open-items.md` | Add new blockers; move resolved ones to the log |
| `02-services-and-scope.md` | Status or dates, only if a service moved |
| `05-decisions.md` | New decision with date, reason, options, decided by |
| `07-compliance-and-dates.md` | New or completed dates (note how completion was confirmed) |
| `06-contacts-and-systems.md` | New links or systems (links only) |
| `00` / `01` / `08` | New facts learned about the business, brand or billing |
| `meetings/YYYY-MM-DD-<short-title>.md` | New file from `meetings/_template.md` if a meeting happened |
| `deliverables/README.md` | One row per finished document, with its link |
| `index.md` | Update `Brain last reviewed` to today |

Only include files that actually change.

### 2. Show and ask
Show the user a short table of files and what changes. Ask for a yes. Take edits if they want any.

### 3. Prepare the new file contents
Read each changed file fresh from the repo right before writing (someone may have edited it). Then:
- `04-log.md`: existing content plus new lines at the bottom.
- `03-status.md`: full replacement.
- Everything else: edit the current content; do not drop anything you were not asked to change.

### 4. Scan for secrets
Run the secret scan on the new contents. If it finds anything, remove it, tell the user, and scan again before saving.

### 5. Commit once
Save all changed files in a **single commit** to `main`. Message: `YYYY-MM-DD <who>: <short summary>`.
If the save fails because a file changed in the meantime, read the file again, merge your change once, and retry once. If it still fails, stop and tell the user plainly.

### 6. Confirm
Read back the commit or the changed files. Tell the user which files were updated and that nothing else was touched. Say plainly if anything could not be saved.

## If new info arrives mid-session
Save small facts at the next natural pause rather than waiting, using the same steps. Never save in silence: the user always sees the change table first.

## Never
- Never save without showing the changes first.
- Never overwrite `04-log.md`.
- Never store credentials or customer data.
- Never send, publish or schedule client work as part of a brain update.
