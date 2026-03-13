# Skill 03 — 3-Step Follow-Up Sequence

Use when: Email 1 was sent, no reply after 4+ days.
Input: outputs/<client>/<date>-cold-emails-draft.csv + BATTLECARD.md + ASSETS.md
Output: Email 2 and Email 3 drafts per prospect
Runtime: 10–15 minutes for 20 sequences

---

## Sequence logic

Email 2 (day 5–7 after Email 1):
- Different angle from Email 1
- New proof point or customer story
- Same ask as Email 1 OR softer ask (e.g. "worth a quick read?")
- Maximum 80 words

Email 3 (day 11–14 after Email 1):
- Pattern interrupt — shorter, more direct
- Close the loop: "Should I close your file?" or similar
- Give them an easy out — this reduces friction and sometimes triggers replies
- Maximum 50 words

---

## Prompt

Read these files:
- outputs/<client>/<date>-cold-emails-draft.csv
- BATTLECARD.md
- ASSETS.md

Task:
For each company in the draft CSV, write Email 2 and Email 3.

Rules for Email 2:
- Do not repeat the same signal as Email 1
- Use a different proof point from BATTLECARD.md
- Under 80 words
- Same voice as Email 1

Rules for Email 3:
- Under 50 words
- One sentence acknowledging they may not be the right fit right now
- One clear close — make it easy to say "not now" or "yes let's talk"
- No new information, no new proof points

Output format:
Company | Email 2 Subject | Email 2 Body | Email 3 Subject | Email 3 Body

Export: write to outputs/<client>/<today>-sequence-drafts.csv

Do not send. Export drafts only.
