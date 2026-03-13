# Skill 01 — Prospect Research

Use when: you need a scored account list from scratch.
Input: client folder with icp.md, signals.md, disqualifiers.md, examples.md
Output: scored CSV ready for Clay enrichment
Runtime: 15–25 minutes for 50 accounts

---

## Prompt

Read these files before starting:
- clients/<client>/icp.md
- clients/<client>/signals.md
- clients/<client>/disqualifiers.md
- clients/<client>/examples.md
- BATTLECARD.md

Task:
Find up to 50 companies that match this ICP in [target geography].

Research each company using:
1. Company website — homepage, careers page, about page, press page
2. Crunchbase — funding stage, headcount, investors, recent rounds
3. LinkedIn — leadership, job postings, headcount changes
4. Recent news — Google News, TechCrunch, or relevant industry publications

For each company produce this exact output:

Company | Website | Country | Employees (estimate) |
Funding Stage | ICP Score (1–10) | Signals Found |
Signal Sources (URLs) | Why Now (1 sentence) |
Fit to BATTLECARD (1 sentence) | Status

Scoring rules:
- 7–10 = INCLUDE
- 5–6 = BORDERLINE — state what is missing
- 1–4 = EXCLUDE — state the disqualifier

Evidence rules:
- Every signal must have a source URL
- No URL = signal does not count
- Signals older than 6 months = label OLD and reduce score by 1

Progress: show a one-line update every 10 companies.

Export: write CSV to outputs/<client>/<today>-prospect-research.csv
