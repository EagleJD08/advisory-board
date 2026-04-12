# Advisory Board

**Stress-test your decisions with a 6-persona AI advisory board.**

Advisory Board takes your decision, question, or proposal and runs it through 6 independent advisors — PM, CMO, CTO, CPO, Operations, and Devil's Advocate. Each evaluates from their distinct lens. You get structured feedback from all six, plus a board synthesis that surfaces the key tension and the single question you need to answer before committing.

---

## Install

Two commands in Claude Code. No Terminal required.

```
/plugin marketplace add EagleJD08/advisory-board
/plugin install advisory-board@EagleJD08
```

Don't have Claude Code yet? It's a free CLI that runs Claude directly in your terminal. [Install it here](https://docs.anthropic.com/claude/claude-code) — takes 2 minutes.

---

## Usage

```
/advisory-board:advisory-board Your decision or question here
```

**First run** uses bundled generic board members — no setup needed. Works immediately.

**To personalize** (recommended after your first run):

```
/advisory-board:advisory-board setup
```

This walks you through 5 questions and calibrates the board to your specific company, stage, and goals. A board that knows your context gives sharper, more specific advice.

**To update:**

```
/plugin update advisory-board@EagleJD08
```

---

## What It Does

1. **Parses your decision** — identifies decision type (strategic, resource, product, execution), stakes level, and the key assumption you're making
2. **Runs 6 advisors in parallel** — each evaluates independently, with no knowledge of what the others will say
3. **Produces structured feedback** per advisor: verdict, main concern, opportunity, key question, confidence level
4. **Synthesizes the board** — overall sentiment (Aligned / Mixed / Divided), the key tension, the one question you must answer, and the recommended next action
5. **Learns over time** — tracks which decisions you brought to the board and what the outcomes were

---

## The Board

| Seat | Lens | Challenge Style |
|------|------|-----------------|
| **PM Advisor** | Prioritization & sequencing | Asks "compared to what?" on every recommendation |
| **CMO Advisor** | Audience & positioning | Asks "why would someone care?" relentlessly |
| **CTO Advisor** | Technical feasibility & leverage | Cuts through hype; strong on build-vs-buy |
| **CPO Advisor** | Product-market fit | Jobs-to-be-done framing; allergic to assumptions |
| **Operations Advisor** | Execution risk | Turns every plan into a risk matrix |
| **Devil's Advocate** | Independent Director | Presents the strongest possible case against your plan |

---

## Board Setup

The opt-in `/advisory-board:advisory-board setup` flow asks 5 questions:

1. Your name
2. Company/project name + one sentence on what it does
3. Stage: Idea / Early / Growing / Scaling
4. Your biggest challenge or constraint right now
5. Your goals for the next 90 days

From your answers, Claude calibrates 6 board personas to your specific context — adjusting their framing, examples, and challenge style to your industry, stage, and stated challenges. Your config is saved to `~/.claude/data/advisory-board/config.md` and updated after every session.

---

## Output Format

```
PM ADVISOR — Prioritization & Sequencing
Verdict: [1 sentence overall take]
Main concern: [the risk they'd push on hardest]
Opportunity: [what they'd be excited about]
Key question: [the one thing you need to answer]
Confidence: [High / Medium / Low] — [reason]

[... 5 more advisors ...]

BOARD SYNTHESIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Overall sentiment: [Aligned / Mixed / Divided] — [1 sentence]
Key tension: [what advisors disagree on]
Confidence breakdown: High: X | Medium: X | Low: X
The question you MUST answer: → [synthesized from the board]
Recommended next action: → [1-2 sentences]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

See [`examples/example-run.md`](examples/example-run.md) for a full annotated run.

---

## Files

```
plugins/advisory-board/
├── .claude-plugin/plugin.json          — plugin manifest
├── skills/advisory-board/
│   ├── SKILL.md                        — the skill (what Claude runs)
│   └── config.default.md              — bundled defaults for first run
├── examples/example-run.md            — annotated sample output
└── README.md                          — this file
```

**User config** (created on setup, stored locally):
```
~/.claude/data/advisory-board/config.md
```

---

## When to Use It

- Before committing to a new project or pivot
- When a decision feels obvious but something feels off
- When you're building in isolation and need outside perspective
- Before a big investment of time, money, or reputation
- Any time you catch yourself saying "I'm pretty sure this is right"

---

## Feedback

Built this because I was making too many big decisions in an echo chamber. The Devil's Advocate alone has saved me from 3 expensive mistakes.

If you try it, I'd love to know what you think. [DM me on LinkedIn](https://www.linkedin.com/in/juanminoprio/).
