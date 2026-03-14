# Rule 01 — The Batch Gate

Purpose:
Prevent Claude from researching, enriching, or drafting at full scale
before you have validated the approach on a small batch.

The rule:
When running any Skill for the first time on a new client or new ICP,
cap the first run at 10 companies.

Review the 10 before proceeding to full scale.

What to check in the review:
- Are the signals real and verifiable?
- Is the ICP score accurate based on your judgment?
- Does the "Why Now" sentence make sense?
- Would you actually send this to these companies?

If 7 out of 10 pass your gut check: run full scale.
If fewer than 7 pass: update icp.md or signals.md and re-run the batch of 10.

Never enrich 50 records before validating 10.
Never send 50 emails before validating 10.

Add this instruction to any Skill prompt when running for the first time:
"Run this workflow for the first 10 companies only.
Stop and wait for approval before continuing."
