---
name: client-brain-interview
description: Use after the brain is set up, or whenever it has gaps, to interview the business owner with high-impact questions in short rounds and save the answers into the right brain files. Starts with a 10-minute quick start of 12 questions, then optional deep-dive rounds. Saves after every round through the updater skill. Never asks for passwords or secrets.
---

# Client Brain Interview

Goal: fill the brain with the answers an AI (or a new team member) needs to do great work, with the fewest, best questions.

## Before you start

- Find the brain repo (name in project instructions, else search for `brain-` under the signed-in user). If none exists, point to `skills/client-brain-setup/SKILL.md` in `DubLow-Digital/client-second-brain-template`.
- Read the whole brain first. Work out what is empty: placeholders in `<angle brackets>`, blank table cells, services marked `Not purchased`, empty lists.
- Tell the user, in plain words, how much is filled and what the interview will cover. Never ask something the brain already answers.
- Saving uses `skills/client-brain-updater/SKILL.md` from the same template repo.

## How to run it

1. **Pick a mode.** Default is **Quick start**: 12 questions, about 10 minutes, in 3 rounds of 4. Offer **Deep dive** rounds (A to G) afterwards or if the user asks for it.
2. **Ask 3 to 4 questions at a time**, one theme per round. Use the question form if the app offers one; otherwise a short numbered list. Never dump the whole bank.
3. **Push for specifics.** Ask for real numbers, real examples, real quotes. If an answer is vague, ask one follow-up ("roughly how many a month?", "what would a customer actually say?").
4. **Allow skipping.** "Not sure" and "skip" are fine. Record the answer as `(unverified)` or add the question to `09-open-items.md` under "Waiting on client".
5. **After every round:** play back what you captured, grouped by file, in short bullets. Ask "Did I get that right?" Then save through the updater (a small commit per round) so nothing is lost if the chat ends.
6. **Keep it moving.** Do not lecture, and do not explain marketing theory unless asked.
7. **If a DubLow team member is answering on the owner's behalf,** note "per <name>" and keep the facts `(unverified)` until the owner confirms.

## Safety

- Never ask for passwords, API keys, bank or card numbers, SSNs or EINs. If the user offers one, do not store it; tell them to keep it in a password manager (and to change it if it was typed into chat).
- Do not collect customer or patient names, lists or records. Ask about customers in general terms.
- Do not give legal, tax or medical-compliance advice. Record the rules the owner states and who confirmed them.

## Quick start: the 12 high-impact questions

**Round 1: the business** (saves to `00`, `01`)
1. In one sentence: what do you sell, and who buys it?
2. What does your best customer or job look like, and what is a typical sale worth?
3. What makes people choose you over the other options? (proof, guarantee, years in business, reviews)
4. What do you never want to be known for, or never want to sell?

**Round 2: leads and goals** (saves to `01`, `02`, `03`, `09`)
5. If you could get more of ONE kind of customer in the next 90 days, which one?
6. What is your 90-day goal, as a number? (leads, booked calls, jobs, revenue)
7. How do leads reach you today, and roughly how many a month? Who answers them, how fast, and about what share become customers?
8. What has worked and not worked in your marketing so far, and roughly what do you spend a month?

**Round 3: voice and ground rules** (saves to `00`, `01`, `07`, `09`)
9. What are the top three things people worry about or ask before buying? (in their words)
10. Describe how you want to sound in three words, and name something you would never say.
11. Who approves content and campaigns, and how quickly do they usually reply?
12. Is there anything we must not say, promise or do? (industry rules, past bad experiences, off-limits services or areas)

After round 3, summarize the brain's state, update `03-status.md` with the next steps, and offer a deep dive.

## Deep dive rounds

### A. Business and offer (`00`, `01`, `02`)
- List your services or products, ranked by how much profit they make you.
- What are your prices or price ranges, and what do you offer for free or at a discount?
- Where do you serve, what are your hours, and how many jobs or customers can you handle at once?
- Which seasons are busy or slow?
- Which jobs or customers do you turn away, and why?

### B. Customers (`01`)
- Describe your ideal customer (age range, situation, what they are trying to fix).
- Describe your worst-fit customer. What goes wrong with them?
- Where do most customers come from, and how do they usually decide?
- What do customers say after they buy? Give two real compliments in their words.
- What questions do you answer on the phone again and again?

### C. Brand voice (`01`)
- What is the story of how and why you started?
- What do you believe about your industry that others get wrong?
- Which words do you use all the time, and which do you avoid?
- Name two or three brands or ads whose style you like, and say why.
- Paste two or three short lines you have written and love. Do you have photos and video of your work or team, and where are they?

### D. Marketing today (`01`, `06`, `07`)
- Where do you show up today? (website, Google Business Profile, Facebook, Instagram, email, texting, ads)
- How many reviews do you have, and what is your rating?
- Do you have an email or text list, and roughly how big is it?
- Who manages each channel now, and what tools do you use?
- How do you currently track where leads come from?

### E. Sales process (`02`, `09`)
- Walk me through what happens from first contact to paid. How long does it take?
- How do people book (phone, form, online calendar)?
- What follow-up happens if someone does not buy right away?
- Where do leads fall through the cracks today?

### F. Goals and money (`03`, `08`)
- What would make this year a clear win? What is the 12-month and 3-year picture?
- What is the single biggest thing holding the business back?
- Roughly what monthly marketing budget feels comfortable? (a range is fine)
- What would you need to see in 6 months to feel this was worth it?

### G. People and rules (`00`, `07`, `09`)
- Who is on your team, and who should the AI and any helpers talk to?
- Who has final say on money, on messaging and on legal wording?
- What consent or opt-in rules apply to texting or email for your business?
- What renewals or deadlines matter in the next 12 months (domain, licences, contracts)?

## Where answers go

| Topic | File |
|---|---|
| Who they are, people, contact preferences | `00-profile.md` |
| Offer, customers, goals, brand voice, objections, online presence | `01-business-and-brand.md` |
| Services and what is in or out of scope | `02-services-and-scope.md` |
| Current focus and next steps | `03-status.md` |
| Decisions with reasons | `05-decisions.md` |
| Systems and links | `06-contacts-and-systems.md` |
| Rules, renewals and dates | `07-compliance-and-dates.md` |
| Budget and results (ranges only) | `08-financial-snapshot.md` |
| Anything unanswered or waiting | `09-open-items.md` |

## Finish

1. Do a completeness check: list sections that are still empty.
2. Move unanswered questions into `09-open-items.md` with a suggested follow-up date.
3. Update `03-status.md` with the next three steps.
4. Add a log line: `YYYY-MM-DD | <who> | Interview | Completed <quick start / rounds> | Next: <step>`.
5. Save through the updater, then tell the user what is filled, what is open, and when to run the interview again (for example after a major change or every quarter).
