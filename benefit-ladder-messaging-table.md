# Benefit Ladder Messaging Table

## Use Case
Build a complete, persona-segmented messaging architecture — the "source of truth" document that governs what your product marketing team says, to whom, in what channel, and with what proof. Structured as a messaging table that maps Core Message → Elevator Pitch → UVP → Capabilities → Proof Points → Use Cases, per persona.

## When to Use
- Before any major campaign, launch, or content program kicks off
- When messaging has diverged across sales, marketing, and product
- When onboarding a new content agency or field marketing team
- As the foundational input for a sales deck, website refresh, or email nurture build

## Required Inputs
- `[PRODUCT_NAME]` — Product or solution
- `[PERSONA_1]` — Primary persona name + one-line description (e.g., "OREN — Technical hands-on automation builder at a mid-market SaaS company")
- `[PERSONA_2]` — Secondary persona name + one-line description (e.g., "BUYER — VP of Operations or CTO who controls the budget decision")
- `[CORE_CAPABILITIES]` — 4–8 core product capabilities in plain language
- `[PROOF_POINTS]` — Customer outcomes, stats, case study results, analyst recognition
- `[COMPETITIVE_SET]` — Alternatives the segment evaluates
- `{EXISTING_MESSAGING}` — Optional: current messaging copy to audit and improve

## Expected Output
- Full messaging table per persona (Core Message / Elevator Pitch / UVP / Capabilities / Proof Points / Use Cases)
- Benefit ladder per persona (Feature → Functional Benefit → Emotional/Business Value)
- Single Purpose / Single Theme per persona
- Messaging anti-patterns to avoid ("the laundry list" flags)
- Channel-level messaging guidance

---

## The Prompt

```
You are a VP of Product Marketing building the canonical messaging architecture for [PRODUCT_NAME]. This document will serve as the "source of truth" for all content, campaigns, sales collateral, and communications for the next 12 months.

Your job is to produce a structured, rigorous messaging table — not a creative brief, not a tagline exercise, not a brand manifesto. This is an engineering document for marketing: precise, falsifiable, and directly actionable by a content writer, sales rep, or demand gen manager.

Work through each step in sequence. Apply the Benefit Ladder at every level: ground every claim in a product capability (Feature layer), connect it to a workflow or outcome improvement (Benefit layer), and ladder it up to the business or human motivation that a VP or C-suite cares about (Value layer).

---

STEP 1 — PERSONA PRESSURE TEST

Before building messaging, validate the personas you are building for.

Persona 1: [PERSONA_1]
Persona 2: [PERSONA_2]

For each persona, confirm:
1a. What is the specific "job" this persona is hired to perform in their organization? What does success look like for them, and how would their manager or stakeholders measure it?

1b. What is the primary tension this persona operates under — the competing pressures that make their job hard? Effective messaging almost always addresses a tension, not just a need.

1c. What is their relationship to the buying decision for [PRODUCT_NAME]? Are they the economic buyer, the technical evaluator, the internal champion, or an end user who influences adoption? The answer determines where in the messaging hierarchy you lead with business value vs. technical capability.

1d. What is the one thing this persona is most afraid of getting wrong? Fear-of-failure is a powerful positioning lever — but only when addressed with credibility, not just reassurance.

---

STEP 2 — BUILD THE MESSAGING TABLE (Per Persona)

For each persona, produce a complete messaging table with the following rows. Every row must ladder back to the persona's specific job, tension, and success criteria from Step 1.

CORE MESSAGE (1 sentence):
The single most important thing this persona should walk away believing about [PRODUCT_NAME] after any interaction with your marketing. This is not a slogan — it is a strategic belief state you are trying to create. It must be ownable (you can claim it), believable (they will accept it), and motivating (it connects to something they care about).

ELEVATOR PITCH (3–4 sentences):
The narrative version of the core message — the answer to "what does [PRODUCT_NAME] do and why does it matter to me?" Structured as: (1) the problem/tension, (2) the approach, (3) the outcome. No feature lists. No jargon that the persona wouldn't use themselves.

UNIQUE VALUE PROPOSITION (1 sentence):
The specific, competitive claim: what [PRODUCT_NAME] delivers for this persona that no alternative in [COMPETITIVE_SET] can match, stated in outcome terms, not capability terms.

CAPABILITY → PROOF POINT → USE CASE MAPPING (table):
For each of the [CORE_CAPABILITIES], map:
- Capability: What the product does (Feature layer — factual, demonstrable)
- Persona Benefit: What it means for this persona's workflow or outcome (Benefit layer — "what's in it for me")
- Business/Emotional Value: Why it matters at the level of organizational success, career impact, or risk management (Value layer — "why it's important to me")
- Proof Point: The specific customer outcome, stat, or third-party validation that makes this claim credible to a skeptic
- Recommended Use Case: The one scenario or customer story that best illustrates this capability for this persona — specific enough that a sales rep could reference it in a 30-minute demo

Core capabilities: [CORE_CAPABILITIES]
Proof points available: [PROOF_POINTS]

---

STEP 3 — SINGLE PURPOSE / SINGLE THEME DISCIPLINE

For each persona, identify the Single Theme — the one narrative thread that ties all capability messaging together into a coherent story.

This is the antidote to the Laundry List trap. Every campaign, piece of content, and sales conversation for this persona should be a specific expression of this single theme. Features are examples of the theme in action, not standalone selling points.

3a. State the Single Theme for [PERSONA_1] in one sentence.
3b. State the Single Theme for [PERSONA_2] in one sentence.
3c. Identify any capability claims from Step 2 that do NOT fit under these themes. Flag them as potential messaging noise — either they belong in a different persona's table, or they indicate the theme needs to be broadened.

---

STEP 4 — PROOF POINT RIGOR AUDIT

Apply the following three-part test to every proof point used in the messaging table:

TYPE TEST: Is this proof point grounded in (a) hard data / third-party research, (b) a specific, named customer outcome, or (c) a logical argument from first principles? Soft proof (e.g., "customers love X" without specifics) should be flagged and replaced or strengthened.

SPECIFICITY TEST: Is the proof point specific enough to be memorable and falsifiable? "Reduces time to value" fails this test. "Reduced onboarding time from 14 days to 3 days for [CUSTOMER TYPE]" passes.

EXCLUSIVITY TEST: Could a competitor use this exact proof point? If yes, is it being used as a POP (table stakes) or incorrectly positioned as a POD (differentiator)?

Produce a brief audit summary: list any proof points that fail the tests, and for each, recommend how to strengthen them (e.g., "add a specific customer name and metric" or "reframe as POP and pair with a stronger POD").

---

STEP 5 — CHANNEL MESSAGING GUIDANCE

For each persona, provide brief guidance on how the Core Message and Elevator Pitch should be adapted — not changed, but adapted — for the following channels:

OUTBOUND EMAIL (Subject line angle + opening hook):
The message needs to earn the open and immediately signal relevance to this persona's specific tension. No generic intros.

PAID SOCIAL / DIGITAL ADS (Single claim + visual direction):
Compress the UVP to its most arresting, single-claim form. Suggest a visual metaphor or scenario that would resonate with this persona's daily reality.

EVENT / KEYNOTE NARRATIVE (Opening statement for a 20-minute talk):
This persona is in a room full of peers. Lead with an industry insight or uncomfortable truth — not a product pitch — that makes them lean in before [PRODUCT_NAME] is even mentioned.

SALES DISCOVERY CONVERSATION (The question that opens the right conversation):
A single provocative or diagnostic question a sales rep could use to surface the exact tension that [PRODUCT_NAME] solves, without leading with a product pitch.

---

STEP 6 — MESSAGING ANTI-PATTERNS

Based on the completed messaging table, flag 3–5 specific anti-patterns the content and campaign team must avoid. These are the lazy defaults, inherited phrases, or competitive me-too claims that dilute the positioning.

For each anti-pattern:
- State what NOT to say (or the structural pattern to avoid)
- Explain why it fails — what belief state it creates vs. what it should create
- Provide a replacement example that reflects the correct messaging approach

---

FORMATTING REQUIREMENTS:
- Step 2 messaging table: one full table per persona — clearly labeled, all columns populated
- Step 4 proof point audit: table with columns — Proof Point | Type Test | Specificity Test | Exclusivity Test | Verdict | Recommendation
- Step 5 channel guidance: one section per persona, four channel sub-sections
- All prose: tight, direct, zero filler — write as if every word is competing for budget
- Total output should be comprehensive enough to hand to a content team and launch without a briefing call
```

---

## Pro Tips

**Iteration 1 — Conflict test:**
*"Where do the messaging tables for [PERSONA_1] and [PERSONA_2] contradict each other — i.e., where claiming something for one persona undermines credibility or relevance for the other? How should we resolve that tension without diluting either message?"*

**Iteration 2 — Competitive stress test:**
*"Take the UVP for [PERSONA_1] and rewrite it as if you were the CMO of [TOP COMPETITOR]. How would they attempt to claim the same space? Now revise the UVP to be more explicitly differentiated."*

**Common Failure Mode:**
Messaging tables often collapse into feature lists with benefit decorations. If the output reads like a product spec sheet with adjectives added, invoke the Value Layer hard: *"For every row in the capability table, answer this question as the persona: 'So what does this mean for my performance review at the end of the year?' If the answer isn't in the Business/Emotional Value column, rewrite it."*
