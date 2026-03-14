# Skill 02 — Cold Email Drafting

Framework: Signal → Problem → Proof → Ask (SPPA)
Use when: you have a scored prospect list and want first-touch emails.
Input: outputs/<client>/<date>-prospect-research.csv + BATTLECARD.md + ASSETS.md
Output: one draft email per company, ready for review
Runtime: 10–20 minutes for 20 emails

---

## The SPPA Framework

Signal: open with a specific, researched observation about their company.
Problem: connect that signal to the exact problem your product solves.
Proof: one concrete proof point — a number, a customer, a result.
Ask: one clear, low-friction next step. Never two asks in one email.

## Prompt

Read these files:
- outputs/<client>/<date>-prospect-research.csv
- BATTLECARD.md
- ASSETS.md
- clients/<client>/icp.md

Task:
For each company with Status = INCLUDE, draft one cold email.

Rules:
- Subject line: specific, no clickbait, under 8 words
- Email body: under 100 words
- Line 1 must reference the specific signal from the research CSV
- Line 2–3: connect signal to the problem we solve (use BATTLECARD.md)
- Line 4: one proof point (use BATTLECARD.md proof points)
- Line 5: one ask from ASSETS.md offer library
- No "I hope this finds you well"
- No "I wanted to reach out"
- No "leading provider of"
- Write in the voice defined in ASSETS.md
- Address the primary buyer defined in BATTLECARD.md

For each draft include:
Company | Recipient Title | Subject Line | Email Body | Signal Used | Offer Used

Export: write to outputs/<client>/<today>-cold-emails-draft.csv

Do not send. Export drafts only. I will review before anything goes out.
