# Rule 03 — The Drafts Gate

Purpose:
Ensure nothing is sent, published, or submitted without human review.

The rule:
Claude never sends emails. Claude never submits forms.
Claude never pushes data to external tools directly.

All output from Skill 02 and Skill 03 is saved to /outputs/ as a draft CSV.
All output from Skill 04 is saved to /clients/ as a markdown file.

The only exception is explicit instruction:
"You have permission to push this to [tool] via MCP."

Why this matters:
MCP tools give Claude the ability to interact with external systems.
Without this rule, an agent with Clay MCP and email MCP access
could theoretically research, enrich, and send — without a human in the loop.
That is not the system we are building.

Human review is the last gate. Always.

Add this to CLAUDE.md:
"All output is saved as drafts. Do not push to external tools,
send emails, or submit data anywhere unless explicitly instructed
in this session with the words: 'You have permission to push.'"
