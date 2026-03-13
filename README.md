# gtm-agent-repo
The Claude Code GTM Agent Starter Pack

The complete folder structure, prompts, and operating rules
from the Claude Code GTM Agent Starter Pack.

Full guide: [wojciech.io/claude-code-vs-clay](https://wojciech.io/claude-code-vs-clay)

---

## What's inside

### Core context files
- `CLAUDE.md` — agent operating manual, behavior and output rules
- `BATTLECARD.md` — product knowledge, proof points, objection handling
- `ASSETS.md` — offer library, voice, tone, sequence rules

### Client memory
- `clients/_template/` — ICP, signals, disqualifiers, past win patterns

### Skills (copy-paste research and outreach prompts)
- `01-prospect-research` — scored account list from scratch
- `02-cold-email-drafting` — SPPA framework emails, under 100 words
- `03-followup-sequence` — 3-step sequence, Email 2 and Email 3
- `04-executive-dossier` — deep research on one decision maker
- `05-anti-sales-filter` — quality check before Clay enrichment

### Rules (guardrails for the agent)
- `batch-gate` — validate 10 before running 50
- `locked-files` — protect core context from silent drift
- `drafts-gate` — nothing sends without human approval

### MCP config
- `plugins/gtm-tools/.mcp.json` — Brave Search, Firecrawl, Exa

---

## How to use

1. Fork this repo
2. Copy `CLAUDE.md`, `BATTLECARD.md`, `ASSETS.md` to your Claude Code project root
3. Install MCP tools (see guide)
4. Fill `clients/_template/` for your first client
5. Run Skills in order: 01 → 05 → 02 → 03
6. Enrich only PASS accounts in Clay

---

Built by [Wojciech Łuszczyński](https://wojciech.io)
