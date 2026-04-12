# Example Run — Advisory Board

**Input:**
```
/advisory-board:advisory-board Should I launch a paid tier at $29/month now, or wait until I hit 500 free users?
```

**Decision parsed:**
- Type: Strategic + Resource
- Stakes: High (pricing shapes growth trajectory and trust)
- Key assumption: That free users want a paid tier at all

---

**PM ADVISOR** — Prioritization & Sequencing
Verdict: Launching paid now is defensible only if you've talked to 10+ free users and at least 3 expressed willingness to pay.
Main concern: You're sequencing the monetization conversation before you have enough signal — 500 users is arbitrary, but it's not zero.
Opportunity: Early pricing signals are actually data — even failed conversions tell you what the product needs to be worth.
Key question: Of your current free users, how many have told you (unprompted) that they'd pay for this?
Confidence in this direction: Medium — depends entirely on the answer above.

---

**CMO ADVISOR** — Audience & Positioning
Verdict: $29/month is a number, not a positioning — what does paid unlock, and is that story compelling enough to pay for?
Main concern: Paid tiers without a clear "this is what you get" story feel like a tax on existing users, not an upgrade.
Opportunity: The moment you introduce a paid tier is the moment you define what this product is really for — use that moment deliberately.
Key question: What does a paid user get that a free user doesn't — and can you explain it in one sentence that makes them feel stupid for NOT upgrading?
Confidence in this direction: Low until the value differentiation story is sharper.

---

**CTO ADVISOR** — Technical Feasibility & Leverage
Verdict: $29/month SaaS infrastructure is a weekend build if you use Stripe + a simple entitlement check — don't let the tech be the reason you delay.
Main concern: The real cost isn't the payment flow, it's customer support overhead once people are paying — churn questions, billing issues, refund requests.
Opportunity: Shipping a paid tier forces you to decide what's actually worth building — it's a natural product prioritization tool.
Key question: What does your support load look like at 50 paying customers — have you modeled that?
Confidence in this direction: High — this is not a technical bottleneck.

---

**CPO ADVISOR** — Product-Market Fit
Verdict: Wait. Not because 500 is the magic number, but because you haven't described what problem the paid tier solves that the free tier doesn't.
Main concern: Paid tiers on products that don't yet have a clear job-to-be-done tend to create churn, not revenue — users pay, don't find the value, and leave with a bad impression.
Opportunity: If you run 5 customer interviews this week and 3 people say "I'd pay for [specific thing]" — that's your paid tier feature. Then launch immediately.
Key question: What's the job a paying customer is hiring this product to do that they can't hire the free version for?
Confidence in this direction: Low — more interviews first.

---

**OPERATIONS ADVISOR** — Execution Risk
Verdict: Launching paid now adds customer support, billing, and retention loops to your plate — make sure you have capacity before creating a new obligation.
Main concern: Every paying customer creates a support relationship. At your stage, 20 paying customers asking questions each week could consume 30% of your time.
Opportunity: A small cohort of 10-20 paying customers is actually the best product feedback you'll ever get — they tell you the truth.
Key question: What's your current weekly time allocation — how many hours can you realistically dedicate to customer success for paying users?
Confidence in this direction: Medium — depends on your capacity.

---

**DEVIL'S ADVOCATE** — Independent Director
Verdict: You're not ready, and the 500-user threshold is a psychological safety blanket — you'll find a reason to push it to 1000.
Main concern: The real reason you're asking this question is that you're afraid the product isn't valuable enough to charge for. That fear is worth examining directly rather than hiding behind a number.
Opportunity: The fastest way to find out if your product is worth paying for is to ask someone to pay for it tomorrow. The answer will be clarifying.
Key question: If your best free user said "I'd never pay for this," what would you do — and have you asked them?
Confidence in this direction: Low — this feels like a delay tactic dressed as a strategy question.

---

**BOARD SYNTHESIS**
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Overall sentiment: Divided — the board agrees pricing is not the bottleneck, but is split on whether you have enough customer signal to act responsibly.

Key tension: CTO and Devil's Advocate say ship now (the delay is psychological, not tactical). CPO and CMO say wait until you have a clearer value differentiation story. PM is the swing vote — and their position depends on whether free users have expressed intent to pay.

Confidence breakdown:
  High: 1 advisor (CTO)
  Medium: 2 advisors (PM, Operations)
  Low: 3 advisors (CMO, CPO, Devil's Advocate)

The question you MUST answer before moving forward:
→ Have you talked to 5+ free users about the value they get — and specifically asked whether they'd pay, and for what?

Recommended next action:
→ Run 5 customer conversations this week with your most active free users. Ask: "What would make this worth $29/month to you?" If 3 out of 5 give you the same answer — that's your paid tier. Launch the following week.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

*Tip: Run `/advisory-board:advisory-board setup` to tune your board to your specific company, stage, and goals (2 min). A calibrated board gives sharper advice.*
