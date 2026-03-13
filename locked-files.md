# Rule 02 — The Locked Files Rule

Purpose:
Prevent Claude from modifying core context files during a session.

The rule:
The following files are READ-ONLY during any research or drafting session:
- CLAUDE.md
- BATTLECARD.md
- ASSETS.md
- clients/<client>/icp.md
- clients/<client>/signals.md
- clients/<client>/disqualifiers.md

Claude may read these files. Claude may not edit, overwrite, or append to them
unless you explicitly say: "You have permission to update [filename]."

Why this matters:
Claude will sometimes try to "improve" your ICP or signals mid-session.
If it overwrites icp.md with its own interpretation, your next session starts
with corrupted context. This rule prevents silent drift.

Add this reminder to CLAUDE.md:
"Never modify files listed in rules/locked-files.md unless
the user explicitly grants permission for that specific file in this session."
