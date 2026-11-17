---
name: dublow-client-brain-updater
description: Use when a DubLow client's second brain has changed (or is being created) and the readable copy in SharePoint must be created or updated. Targets Documents > DubLow Company Drive > 2. Clients > <Client Folder> > Dublow Clients Brain. Never deletes files, never overwrites the append-only log, never stores secrets.
---

# DubLow Client Brain Updater

Keeps the SharePoint copy of a client's second brain in step with the working brain (the GitHub repo `DubLow-Digital/brain-<client-slug>`, or the files in the current Ask AI project).

## Where it writes (exact path)

`Documents > DubLow Company Drive > 2. Clients > <Specific Client's Folder> > Dublow Clients Brain`

- Library: the **Documents** library of the DubLow root SharePoint site (`https://dublow.sharepoint.com`).
- Drive path to use with the file tools: `DubLow Company Drive/2. Clients/<Client Folder>/Dublow Clients Brain`
- `<Client Folder>` is the client's existing folder name exactly as it appears under `2. Clients` (for example `Glo Ocala`). Never create a new client folder and never guess a spelling: list `2. Clients` and match it.
- Only write inside `Dublow Clients Brain`. Do not touch Agreements, Brand, Digital Marketing Services, Managed IT, Operations or any other folder.

## Folder layout inside `Dublow Clients Brain`

```
Dublow Clients Brain/
  index.md
  00-profile.md
  01-business-and-brand.md
  02-services-and-scope.md
  03-status.md
  04-log.md
  05-decisions.md
  06-contacts-and-systems.md
  07-compliance-and-dates.md
  08-financial-snapshot.md
  09-open-items.md
  meetings/        one file per meeting: YYYY-MM-DD-<short-title>.md
  deliverables/    README.md (index of finished documents)
```

`AGENTS.md`, `README.md` and `skills/` stay in GitHub only. They are team instructions, not client information.

## Tools

Use the DubLow 365 connector (Microsoft 365). Always run a fresh discovery first and read each tool's schema before calling it. The tools needed are: find the site and library, list a folder, read a text file, create a folder, and create or overwrite a small text file by path.

## Safety rules (read before writing)

1. **Overwrite replaces the whole file.** Writing a file by path replaces what is there. Never write a file you have not just read, unless it does not exist yet.
2. **`04-log.md` is append only.** Read the SharePoint version, keep every existing line, add the new lines at the bottom, and write the whole file back. If the SharePoint log has lines that the repo does not (someone edited in SharePoint), keep them. Never drop a line.
3. **Never delete or move files.** If something looks wrong, add it to `09-open-items.md` as a question for the team.
4. **No secrets, ever.** Before writing, scan the text for passwords, API keys, tokens, SSNs, full EINs, bank or card numbers, and client customer or patient data. If found, stop, remove it, and tell the user.
5. **Only the files that changed.** Do not rewrite untouched files; it clutters version history.
6. **Ask before the first write for a client.** Show the user the target path and the list of files to create or change, and wait for a yes. After that, updates for the same client in the same session can proceed.
7. **Small text files only.** The write tool handles text files (md). Never upload binaries, signed documents or images here.

## Procedure A: first-time setup for a client

1. Confirm the client's exact folder name with the user, then list `DubLow Company Drive/2. Clients` and find it. If it is missing, stop and ask; do not create it.
2. List the client folder. If `Dublow Clients Brain` already exists, switch to Procedure B.
3. Show the user the plan (path, folders and files) and wait for approval.
4. Create the folder `Dublow Clients Brain` inside the client folder, then `meetings` and `deliverables` inside it.
5. For each brain file (`index.md`, `00` to `09`, `deliverables/README.md`), take the filled-in version from the brain repo or project. If the client's brain is still the blank template, still create the files so the team has a place to fill in.
6. Replace the placeholders `<Client Folder>` and `<CLIENT NAME>` with the real names in the copies you write. Leave other placeholders for the team to fill.
7. Read back the folder listing and confirm every file is present.
8. Set `SharePoint last synced` in `index.md` to today's date (YYYY-MM-DD) and add a line to `04-log.md`: `YYYY-MM-DD | <who> | Onboarding | Created Dublow Clients Brain folder in SharePoint | Team can open it from the client folder`.
9. Add the SharePoint brain folder link to `06-contacts-and-systems.md` (link only).

## Procedure B: update after a work session

1. Work out which brain files changed this session. The usual set is `03-status.md`, `04-log.md`, `09-open-items.md`, and sometimes `02-services-and-scope.md`, `05-decisions.md`, `07-compliance-and-dates.md`, a new `meetings/` file, or `deliverables/README.md`.
2. List `Dublow Clients Brain` in SharePoint and read the current version of each changed file.
3. Compare to the working copy:
   - `03-status.md`: replace the SharePoint version with the new one.
   - `04-log.md`: append only, as in the safety rules.
   - Other files: if SharePoint has edits that are not in the working copy, merge them in rather than overwriting, and mention the merge to the user.
4. Write each changed file back by path. New meeting notes go in `meetings/` named `YYYY-MM-DD-<short-title>.md`.
5. Update `SharePoint last synced` in `index.md` to today's date.
6. Read back one or two files to confirm the write, and list the folder once at the end.

## Procedure C: pull SharePoint edits back into the working brain

Use when a teammate edited a file in SharePoint. Read the SharePoint file, show the user what differs from the working copy, and update the working copy only after they agree. Log it in `04-log.md`.

## After every run: report

Tell the user, in plain words:
- the exact SharePoint path used
- which files were created or updated (and which were left alone)
- anything merged, skipped or found in the safety scan
- one line added to `04-log.md` for the sync itself: `YYYY-MM-DD | <who> | Brain sync | Updated <list of files> in SharePoint | Next: <step>`

## Never

- Never write outside `Dublow Clients Brain`.
- Never delete, rename or move SharePoint files.
- Never email or share the folder with anyone.
- Never put credentials or client customer data into any brain file.
- Never send, publish or schedule client work as part of a brain update.
