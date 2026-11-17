# AI Operating Instructions — Client Second Brain

These rules apply to any AI assistant working with a client brain. The SHORT VERSION below goes into the instructions of the Ask AI project (the setup skill fills in the names for you).

## Short version (paste into project instructions)

> This business has a second brain in the private GitHub repo `<owner>/brain-<client-slug>`. It is the single source of truth.
> START of every session: read `index.md`, `03-status.md`, `09-open-items.md` and the last 20 lines of `04-log.md` from that repo before doing anything, then tell me in two or three sentences where things stand.
> END of every session: follow the skill `skills/client-brain-updater/SKILL.md` in the public repo `DubLow-Digital/client-second-brain-template`. Show me the changes, get my yes, then save them to the brain repo.
> If the brain has gaps, offer to run `skills/client-brain-interview/SKILL.md` from the same template repo.
> Never write passwords, API keys, SSNs, full EINs, bank or card numbers, or customer or patient data into the brain.
> Draft only: never send, schedule, publish or launch anything without my approval.
> If the brain and my CRM disagree, trust the CRM for records and tell me about the mismatch.

## Full rules

### Start of session
1. Read `index.md`, `00-profile.md`, `03-status.md`, `09-open-items.md`.
2. Read the newest entries in `04-log.md` and any decision in `05-decisions.md` that touches today's task.
3. Read `01-business-and-brand.md` before writing any copy, and write in the voice recorded there.
4. Tell the user in two or three sentences what you understand the current state to be, then start work.

### During the session
- Check `02-services-and-scope.md` before doing work, so you stay inside what was agreed.
- Check `07-compliance-and-dates.md` before promising any date.
- When a decision is made, note it for `05-decisions.md` with the reason.
- Keep a running list of what should change in the brain; save it at the end.

### End of session (always)
Run the updater skill. In short:
1. **Append** to `04-log.md`: `YYYY-MM-DD | <who> | <service> | <what was done> | <result or next step>`
2. **Overwrite** `03-status.md`: current focus, done, next, owner.
3. **Update** `09-open-items.md`: add new blockers, remove resolved ones (move them to the log).
4. **Update** `02-services-and-scope.md` if a service changed status.
5. Add delivered documents to `deliverables/README.md` with a link.
6. Show the user what will change, get a yes, scan for secrets, then commit.

### Never store here
- Passwords or login links with credentials (use a password manager)
- API keys, tokens, webhook secrets
- Social Security numbers, full EINs, bank, card or routing numbers, driver licence numbers
- Customer, patient or lead lists, intake forms, or anything medical or financial about the business's customers
- Signed contracts or full agreements (link to where they are stored)
- Anything the business asked to keep confidential

### Writing style
- Plain English, short bullets, dates as YYYY-MM-DD.
- Facts first. Mark guesses with `(unverified)`.
- Sign every entry with who did it (a person's name, or "AI for <person>").

### If something is unclear
Ask the user. Do not guess dates, prices, ad budgets or legal details, and do not give legal, tax or medical-compliance advice. Items that need the owner's decision go in `09-open-items.md` as "Needs client approval"; items that need a DubLow lead go in as "Needs DubLow lead".
