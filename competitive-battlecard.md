# Competitive Battlecard

## Use Case
Build a kill-sheet-grade competitive battlecard — the internal sales weapon that empowers reps to displace a specific competitor in active deals. Goes beyond feature comparison to deliver: attack lines, trap questions, objection scripts, Win/Loss pattern analysis, and a "defend your turf" response playbook.

## When to Use
- When a specific competitor appears repeatedly in deal notes or CRM competitive fields
- After a cluster of losses to the same vendor (pattern analysis needed)
- When onboarding new AEs or SDRs who need competitive context fast
- Before a sales kickoff or competitive training session

## Required Inputs
- `[YOUR_PRODUCT]` — Your product/solution
- `[COMPETITOR_NAME]` — The specific competitor this battlecard targets
- `[YOUR_KEY_STRENGTHS]` — 4–6 areas where you demonstrably outperform this competitor
- `[COMPETITOR_KNOWN_WEAKNESSES]` — What you know or can infer about their gaps (product, support, pricing, roadmap)
- `[TYPICAL_DEAL_SCENARIO]` — The deal context where this competitor most often appears (e.g., "Competitive displacement — prospect currently using [competitor]," or "Head-to-head evaluation in mid-market")
- `[WIN_LOSS_PATTERNS]` — Recurring themes from deals won and lost against this competitor
- `[TARGET_PERSONA]` — The buyer or champion persona this battlecard is written for
- `{COMPETITOR_PUBLIC_CLAIMS}` — Optional: paste their website copy, G2 page, or sales deck claims you want to counter

## Expected Output
- One-paragraph "elevator" competitive summary for quick deal context
- POD/POP battle map
- Attack playbook: trap questions and discovery lines
- Defense playbook: how to respond when they attack you
- Objection handling scripts (top 3)
- Win/Loss pattern analysis with recommended plays
- "Never say this" guardrails

---

## The Prompt

```
You are a Senior Product Marketing Manager and competitive intelligence expert. Your task is to build a production-grade competitive battlecard that arms sales reps with everything they need to win in a head-to-head evaluation against [COMPETITOR_NAME].

Your product: [YOUR_PRODUCT]
Competitor: [COMPETITOR_NAME]
Deal context: [TYPICAL_DEAL_SCENARIO]
Target sales persona using this card: [TARGET_PERSONA]
Your known strengths: [YOUR_KEY_STRENGTHS]
Competitor known weaknesses: [COMPETITOR_KNOWN_WEAKNESSES]
Win/Loss patterns: [WIN_LOSS_PATTERNS]
Optional competitor claims: {COMPETITOR_PUBLIC_CLAIMS}

Design principles for this battlecard:
1. COMMERCIAL VELOCITY — every element must reduce Decision Latency for the buyer. No philosophical positioning. Every line should either help the rep accelerate the deal or prevent it from stalling.
2. BRAND CONSISTENCY — the rep using this card should be "singing from the same hymn book" as every other customer-facing touchpoint. The language here should match the website, the pitch deck, and the NPS follow-up email.
3. EXPLOIT THE BLACK BOX — the most effective competitive positioning exploits specific, verifiable weaknesses in the competitor's product or GTM model, not generic claims of superiority.
4. VALIDATE BEFORE YOU ATTACK — sophisticated buyers are suspicious of salespeople who disparage competitors. Every attack line must first acknowledge why the prospect might have reasonably put [COMPETITOR_NAME] on their list.

Work through each section. For sections that require inference (where hard data is unavailable), mark inferences explicitly as [INFERRED FROM: source].

---

SECTION 1 — QUICK BRIEF (For reps in a 2-minute context window)

1a. WHO IS [COMPETITOR_NAME]?
Two sentences: what they sell, who they primarily target, and what they're known for in the market. Written for a rep who has never heard of them and is about to walk into a call.

1b. WHY DOES [YOUR_PRODUCT] WIN?
One sentence. The single clearest reason a rational buyer chooses [YOUR_PRODUCT] over [COMPETITOR_NAME] in the deal context described. No hedging.

1c. WHY DOES [YOUR_PRODUCT] LOSE?
One sentence. The single most common reason [COMPETITOR_NAME] beats you. Say it clearly — a rep who doesn't know this is going to be blindsided. Honest assessment only.

1d. DEAL SIGNAL: When does [COMPETITOR_NAME] appear in a deal?
What trigger or conversation topic indicates the prospect has [COMPETITOR_NAME] on their shortlist? (e.g., "Prospect mentions X capability as a must-have," or "They've been using [competitor] for X use case and are evaluating an upgrade.") This is the rep's early warning signal.

---

SECTION 2 — POD / POP BATTLE MAP

For each of [YOUR_KEY_STRENGTHS], classify the competitive dynamic:

POINT OF DIFFERENCE (POD): A capability, outcome, or experience that [YOUR_PRODUCT] delivers and [COMPETITOR_NAME] demonstrably cannot match. These are your attack vectors.

POINT OF PARITY (POP): A capability both products deliver to an acceptable threshold. These are not selling points — they are "table stakes" claims that level the playing field. Reps should acknowledge POPs calmly and not over-claim here.

COMPETITOR STRENGTH ACKNOWLEDGMENT: Where [COMPETITOR_NAME] is genuinely strong. Acknowledge these proactively in the rep's discovery approach — buyers respect salespeople who are honest about competitive trade-offs.

Produce a three-column table:
Capability | Competitive Dynamic (POD / POP / Competitor Strength) | Sales Guidance (how to position this capability in a live conversation)

---

SECTION 3 — THE ATTACK PLAYBOOK

The goal of the Attack Playbook is to surface [COMPETITOR_NAME]'s weaknesses without triggering buyer defensiveness. The technique: use diagnostic questions that lead the prospect to discover the gap themselves.

3a. TOP 3 TRAP QUESTIONS
These are discovery questions designed to expose [COMPETITOR_NAME]'s most significant weaknesses. Each question should:
- Sound like genuine discovery, not a competitive gotcha
- Surface a pain point that [COMPETITOR_NAME] cannot address and [YOUR_PRODUCT] can
- Be answerable by the prospect from their own experience — not require them to know [COMPETITOR_NAME]'s product deeply

For each trap question:
- The question (verbatim, as the rep would ask it)
- Why it works: what gap does this surface, and why does [COMPETITOR_NAME] fail on this dimension?
- The bridging statement: how the rep pivots from the prospect's answer to a [YOUR_PRODUCT] proof point

3b. THE TIMING ATTACK
If [COMPETITOR_NAME] has known weaknesses in roadmap delivery, release cadence, or execution speed, provide a line of attack that positions [YOUR_PRODUCT] as the lower-risk choice from a timeline and reliability perspective.

3c. THE TOTAL COST ATTACK (if applicable)
If [COMPETITOR_NAME]'s true cost of ownership is higher than the headline price (e.g., implementation costs, professional services requirements, seat minimums, support tier costs), provide the math and the line: "The sticker price is only part of the story. Here's what most [COMPETITOR_NAME] customers don't factor in until they're already signed..."

---

SECTION 4 — THE DEFENSE PLAYBOOK

[COMPETITOR_NAME] has a sales team too. They have their own battlecard with attacks against [YOUR_PRODUCT]. This section prepares reps for those attacks.

4a. THE TOP 3 ATTACKS [COMPETITOR_NAME] RUNS AGAINST [YOUR_PRODUCT]
Based on [WIN_LOSS_PATTERNS] and known competitor positioning, identify the three most common attacks [COMPETITOR_NAME]'s reps use in competitive deals.

For each attack:
- The attack (as [COMPETITOR_NAME]'s rep would phrase it, or as a prospect would relay it)
- Why the prospect might find it compelling — acknowledge the grain of truth if one exists
- The reframe response: how to address it without becoming defensive (structure: acknowledge → reframe → proof point)
- The one thing the rep must NEVER say in response (the defensive reaction that makes things worse)

4b. THE PROOF POINT ARSENAL
For each major competitive attack from 4a, identify the strongest proof point available:
- Customer reference or case study
- Third-party validation (analyst, review site, benchmark)
- Product demonstration moment (the specific feature or flow that proves the reframe claim)

---

SECTION 5 — OBJECTION HANDLING SCRIPTS

Write three full objection handling scripts for the most common deal-blocking objections in [COMPETITOR_NAME] competitive deals.

Script format: Empathy → Reframe → Proof → Close

For each objection:
OBJECTION: [The exact words a prospect uses]
EMPATHY OPENER: Acknowledge the concern without capitulating. The prospect's concern is reasonable — start there.
REFRAME: Shift the frame of the objection. What's the question they should actually be asking?
PROOF POINT: The specific, credible evidence that resolves the reframed question.
SOFT CLOSE: A question that moves the conversation forward without pressure.

REQUIRED OBJECTIONS TO COVER:
1. "[COMPETITOR_NAME] already has [specific capability]. Why would we switch?"
2. "Your pricing is higher than [COMPETITOR_NAME]."
3. "[COMPETITOR_NAME] is the industry standard / everyone uses them."

---

SECTION 6 — WIN/LOSS PATTERN ANALYSIS

Win/Loss data: [WIN_LOSS_PATTERNS]

6a. WINNING PATTERN: When [YOUR_PRODUCT] beats [COMPETITOR_NAME], what are the 2–3 conditions that are almost always present? (e.g., "We win when the prospect has experienced a specific failure with [COMPETITOR_NAME]," or "We win when the champion is [specific persona type].")

6b. LOSING PATTERN: When [COMPETITOR_NAME] beats [YOUR_PRODUCT], what are the 2–3 conditions most predictive of a loss? Be specific and honest.

6c. THE DEAL YOU SHOULD WALK AWAY FROM: Based on the losing pattern, define the deal profile — specific indicators that a prospect is unlikely to choose [YOUR_PRODUCT] over [COMPETITOR_NAME] regardless of the rep's effort. Time saved by disqualifying early is time that can be invested in winnable deals.

6d. THE PLAY TO RUN: For each winning condition identified in 6a, write the specific sales play — the sequence of discovery questions, proof moments, and stakeholder actions — that consistently produces a win. This is the repeatable playbook, not generic advice.

---

SECTION 7 — BRAND GUARDRAILS: WHAT NEVER TO SAY

List 5–7 phrases or claims the sales team must never use when positioning against [COMPETITOR_NAME]. For each, explain the risk it creates and provide the approved alternative.

Categories to cover:
- Claims that are factually unverifiable and create legal or credibility risk
- Claims that are true but will trigger defensiveness or sympathy for [COMPETITOR_NAME]
- Claims that are generic and make the rep sound like every other vendor's sales team
- Claims that deviate from the approved messaging hierarchy and create brand inconsistency

Format: NEVER SAY: "[PHRASE]" → WHY: [RISK] → INSTEAD SAY: "[APPROVED ALTERNATIVE]"

---

FORMATTING REQUIREMENTS:
- Section 1: four tight labeled blocks — usable as a cheat sheet printed on one page
- Section 2: structured three-column table
- Section 3 trap questions: one structured block per question
- Sections 4 and 5: structured blocks per attack / objection with labeled sub-sections
- Section 7: the Never/Why/Instead format — one line per guardrail
- Total card: complete enough to be the only document a rep needs for a competitive deal, but tight enough to actually be read
```

---

## Pro Tips

**Iteration 1 — SDR-specific version:**
*"Create a shortened version of this battlecard for SDRs. Focus on: the one-sentence win reason, the deal signal (when does [COMPETITOR_NAME] come up), 2 trap questions for discovery calls, and the top objection response. Limit to one printed page."*

**Iteration 2 — Proof point sourcing:**
*"For each proof point referenced in the battlecard, write a brief that specifies what evidence would fully substantiate it — the exact type of customer story, metric, or third-party source needed. This becomes the brief for the customer marketing team to fill."*

**Common Failure Mode:**
Battlecards frequently age out — [COMPETITOR_NAME] releases new features, hires new leadership, or changes pricing, and the card becomes a liability rather than an asset. Add a maintenance protocol: *"Add a 'Last Reviewed' date field and a review trigger: 'This card should be reviewed whenever a rep loses a deal to [COMPETITOR_NAME] for a reason not covered here.' What are the 3 questions a rep should answer in a post-loss debrief to flag a card update?"*
