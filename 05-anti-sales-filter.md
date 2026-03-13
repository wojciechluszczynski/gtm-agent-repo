# Skill 05 — Anti-Sales Filter

Use when: you have a list of INCLUDE companies and want a final quality check
before enrichment and outreach.
Input: outputs/<client>/<date>-prospect-research.csv
Output: same CSV with PASS / HOLD / DROP added + reason
Runtime: 5–10 minutes for 50 accounts

Purpose:
Most prospect lists contain 20–30% of accounts that look right on paper
but will waste enrichment credits and sender reputation.
This filter catches them before they enter Clay.

---

## Prompt

Read:
- outputs/<client>/<date>-prospect-research.csv
- clients/<client>/disqualifiers.md
- BATTLECARD.md

Task:
For each company with Status = INCLUDE, apply the Anti-Sales Filter.

Filter criteria — flag DROP if any of these are true:
1. Company is a direct competitor (check BATTLECARD.md)
2. Company is currently a customer (if customer list provided)
3. Company has a public statement against our category or approach
4. Glassdoor or news indicates severe internal instability
   (mass layoffs, CEO change, acquisition in progress, legal issues)
5. Company raised funding but is burning fast with no GTM motion visible
6. ICP score is 7 but based on only one weak signal with no corroboration

Flag HOLD if:
- Timing is likely wrong (just raised, just went through restructuring,
  just launched new product — may be heads-down for 60–90 days)
- Decision maker role is vacant (no VP or Director in the target function)

Flag PASS if:
- None of the above apply
- Score is 7 or above with at least 2 verified signals

Output format:
Add three columns to the CSV:
Filter Status (PASS / HOLD / DROP) | Filter Reason | Recommended Action

Export: write to outputs/<client>/<today>-filtered-list.csv

Only PASS accounts should proceed to Clay enrichment.
