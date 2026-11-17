# AI Operating Instructions — DubLow Client Second Brain

These instructions apply to any AI assistant working on a DubLow Digital client. Paste the SHORT VERSION into each project's instructions.

## Short version (paste into project instructions)

> This client has a second brain in the GitHub repo `DubLow-Digital/brain-<client-slug>`, mirrored in SharePoint at Documents > DubLow Company Drive > 2. Clients > <Client Folder> > Dublow Clients Brain.
> START of every session: read `index.md`, `03-status.md`, `09-open-items.md` and the last 20 lines of `04-log.md` before doing anything.
> END of every session: append a dated entry to `04-log.md`, overwrite `03-status.md` with the current picture, update `09-open-items.md` and `02-services-and-scope.md` if anything changed, then sync the changed files to the SharePoint brain folder using the `dublow-client-brain-updater` skill.
> Never write passwords, API keys, SSNs, full EINs, bank or card numbers, or client customer data into the brain. Link to SharePoint or the CRM instead.
> Draft only: never send, schedule, publish or launch anything for the client without a person's approval.
> If the brain and the CRM disagree, trust the CRM for records and tell the user about the mismatch.

## Full rules

### Start of session
1. Read `index.md`, `00-profile.md`, `03-status.md`, `09-open-items.md`.
2. Read the newest entries in `04-log.md` and any decision in `05-decisions.md` that touches today's task.
3. Read the client's Brand Voice and Identity document (linked in `01-business-and-brand.md`) before writing any copy.
4. Tell the user in two or three sentences what you understand the current state to be, then start work.

### During the session
- Check `02-services-and-scope.md` before doing work, so you stay inside what the client bought.
- Check `07-compliance-and-dates.md` before promising any date (A2P status, domain renewals, campaign dates).
- When a decision is made, write it to `05-decisions.md` with the reason.

### End of session (always)
1. **Append** to `04-log.md` using this format: `YYYY-MM-DD | <who> | <service> | <what was done> | <result or next step>`
2. **Overwrite** `03-status.md`: current focus, what is done, what is next, who owns it.
3. **Update** `09-open-items.md`: add new blockers, remove resolved ones (move them to the log).
4. **Update** `02-services-and-scope.md` if a service changed status.
5. If a document was delivered, add it to `deliverables/README.md` with its SharePoint location.
6. **Sync to SharePoint:** follow `skills/dublow-client-brain-updater/SKILL.md` so the Dublow Clients Brain folder matches the repo.

### Never store here
- Passwords or login links with credentials (password manager only)
- API keys, tokens, webhook secrets
- Social Security numbers, full EINs, bank, card or routing numbers, driver licence numbers
- Client customer, patient or lead lists, intake forms, or anything medical or financial about the client's customers
- Signed contracts or full agreements (SharePoint > Agreements, link to them)
- Anything the client asked us to keep confidential

### Writing style
- Plain English, short bullets, dates as YYYY-MM-DD.
- Facts first. Mark guesses with `(unverified)`.
- Sign every entry with who did it (a person's name, or "AI for <person>").

### If something is unclear
Ask the user. Do not guess dates, prices, ad budgets or legal details, and do not give legal, tax or medical-compliance advice. Items that need the client's decision go in `09-open-items.md` as "Needs client approval"; items that need a DubLow lead go in as "Needs DubLow lead".
