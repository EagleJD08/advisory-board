# Advisory Board — Claude Code Plugin

**Stress-test your decisions with a 6-persona AI advisory board.**

A single plugin that takes your decision, question, or proposal and runs it through 6 independent advisors — PM, CMO, CTO, CPO, Operations, and Devil's Advocate. Each evaluates from their distinct lens. You get structured feedback from all six, plus a board synthesis that surfaces the key tension and the single question you need to answer before committing.

---

## What is Claude Code?

Claude Code is Anthropic's free CLI that runs Claude directly in your terminal. It's not a chatbot in a browser tab — it's an AI that reads your files, runs commands, and takes actions. You install it once, and then you can run any plugin from anywhere.

[Install Claude Code](https://docs.anthropic.com/claude/claude-code) — takes about 2 minutes.

---

## Install

```
/plugin marketplace add EagleJD08/advisory-board
/plugin install advisory-board@EagleJD08
```

Two commands. No Terminal required beyond what Claude Code already has.

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

## What It Does

1. **Parses your decision** — identifies decision type, stakes level, and the key assumption you're making
2. **Runs 6 advisors in parallel** — each evaluates independently, with no knowledge of what the others will say
3. **Produces structured feedback** per advisor: verdict, main concern, opportunity, key question, confidence level
4. **Synthesizes the board** — overall sentiment (Aligned / Mixed / Divided), the key tension, the one question you must answer, and the recommended next action
5. **Learns over time** — tracks which decisions you brought to the board and what the outcomes were

See [`plugins/advisory-board/examples/example-run.md`](./plugins/advisory-board/examples/example-run.md) for a full annotated run.

---

## Plugin Structure

```
advisory-board/
├── .claude-plugin/
│   └── marketplace.json                      — this repo's plugin registry
├── plugins/advisory-board/
│   ├── .claude-plugin/plugin.json            — plugin manifest
│   ├── skills/advisory-board/
│   │   ├── SKILL.md                          — the skill Claude runs
│   │   └── config.default.md                — bundled defaults for first run
│   ├── examples/example-run.md              — annotated sample output
│   └── README.md                            — plugin-level usage docs
├── README.md                                — this file
└── LICENSE                                  — MIT
```

The critical structural rule: `skills/` lives at the **plugin root**, not inside `.claude-plugin/`. This is the most common footgun when building Claude Code plugins.

**User config** (created on setup, stored locally):
```
~/.claude/data/advisory-board/config.md
```

---

## Feedback

Built this because I was making too many big decisions in an echo chamber. The Devil's Advocate alone has saved me from 3 expensive mistakes.

If you try it, I'd love to know what you think. [DM me on LinkedIn](https://www.linkedin.com/in/juanminoprio/) or open an issue.

---

## License

MIT — see [LICENSE](./LICENSE).
