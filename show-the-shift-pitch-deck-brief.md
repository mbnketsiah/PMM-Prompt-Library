# Show the Shift Pitch Deck Brief

## Use Case
Write a narrative brief for a B2B sales pitch deck using the "Show the Shift" framework — a structure that opens with a transformative shift in the prospect's world before introducing a single product feature. Reduces Decision Latency by making the business case inevitable before the product is mentioned.

## When to Use
- Building or rebuilding a core sales deck for a new segment, launch, or rebrand
- When the existing deck opens with a company overview or feature list (the most common failure mode)
- When win rates are strong in discovery but drop at the presentation stage
- When the deck needs to work both in a live demo setting and as a leave-behind for async stakeholder review

## Required Inputs
- `[PRODUCT_NAME]` — Your product
- `[TARGET_PERSONA]` — The primary audience for this deck (economic buyer vs. technical evaluator vs. end-user champion)
- `[THE_SHIFT]` — The transformative market or operational shift happening in the prospect's world (e.g., "The rise of AI agents is eliminating the workflow automation category as they knew it")
- `[THE_PROBLEM]` — The specific problem this shift creates for [TARGET_PERSONA] that old approaches can't solve
- `[YOUR_APPROACH]` — How [PRODUCT_NAME] addresses the problem — one sentence, outcome-oriented
- `[PROOF_POINTS]` — 3–5 specific customer outcomes, metrics, or case study results
- `[DESIRED_OUTCOME]` — What you want the prospect to DO after seeing this deck (book a trial, approve a POC, escalate to exec sponsor)
- `{COMPETITIVE_CONTEXT}` — Optional: competitive alternatives the deck should implicitly or explicitly position against

## Expected Output
- Full narrative arc (slide-by-slide brief)
- Slide titles and talking point summaries
- Hero story recommendation
- Anti-patterns audit (what to remove from the current deck)
- Async vs. live use guidance

---

## The Prompt

```
You are a Senior Product Marketing Manager and sales narrative architect. Your task is to write a complete pitch deck narrative brief for [PRODUCT_NAME] targeting [TARGET_PERSONA], using the "Show the Shift" framework.

The "Show the Shift" principle: a great B2B sales narrative does not start with the product. It starts with a shift — a change in the world that is creating a new problem for the prospect. The product is introduced not as a collection of features, but as the natural, inevitable response to that shift. By the time the product appears in the deck, the audience should already be nodding at the problem — and relieved that a solution exists.

Key inputs:
- The shift: [THE_SHIFT]
- The problem this creates: [THE_PROBLEM]
- Your approach: [YOUR_APPROACH]
- Proof points: [PROOF_POINTS]
- Target persona: [TARGET_PERSONA]
- Desired action: [DESIRED_OUTCOME]
- Optional competitive context: {COMPETITIVE_CONTEXT}

Design principles:
1. DECISION LATENCY REDUCTION: Every slide must move the prospect closer to a decision. Remove any slide that exists for the presenter's ego, the company's history, or a feature that doesn't directly address [THE_PROBLEM].
2. SINGLE THEME: The entire deck must be a specific expression of one narrative thread. Every slide asks and answers the same question from a different angle: "Why is the old way broken, and why is [PRODUCT_NAME] the right response to the shift?"
3. EMOTION BEFORE LOGIC: Open with a shift that creates urgency or anxiety before introducing any rational solution. System 1 (emotion) must be engaged before System 2 (rational evaluation) can close the deal.
4. THE GUARDIAN: Every word, example, and proof point in this deck should be defensible by the product team, credible to a skeptical CFO, and consistent with the brand's positioning statement.

Work through each section sequentially. For each slide, provide: the slide title, the narrative purpose, the talking point summary (what the presenter says), the single most important visual direction, and the transition into the next slide.

---

SECTION 1 — THE NARRATIVE ARC (Pre-Deck)

Before building the slide brief, architect the narrative arc. A "Show the Shift" deck follows a specific emotional and logical progression:

ACT 1 — THE WORLD HAS CHANGED (Slides 1–3):
Open with an undeniable truth about the prospect's world that they already believe. This is not your opinion — it is an observation about a market, technology, or operational shift that the prospect is already living through. The goal is to create immediate relevance and a sense of "this deck is about me."

ACT 2 — THE PROBLEM THIS CREATES (Slides 4–6):
Name the specific problem the shift creates for [TARGET_PERSONA]. Be precise — not "companies are struggling with efficiency" but "teams like yours are now managing 3× the workflow complexity with the same headcount, and the tools they built the last decade weren't designed for this." The goal is recognition, not education.

ACT 3 — WHY THE OLD APPROACH FAILS (Slides 7–8):
Introduce the "villain" — the incumbent approach or category that used to solve this problem but is now inadequate. Do not name a competitor by name; instead, describe the approach and its failure mode. The goal is to create dissatisfaction with the status quo without triggering defensiveness.

ACT 4 — A NEW APPROACH EXISTS (Slides 9–11):
Introduce [PRODUCT_NAME] as the logical response to everything established in Acts 1–3. The product should feel inevitable at this point — the prospect should be leaning forward, not skeptical. Lead with the approach and the outcome, not the features.

ACT 5 — PROOF IT'S REAL (Slides 12–14):
Deliver proof. Customer stories, metrics, and third-party validation. The goal is to shift from intellectual acceptance ("this makes sense") to emotional conviction ("I believe this works for people like me").

ACT 6 — THE CLEAR NEXT STEP (Slide 15):
Ask for one thing. The desired outcome is [DESIRED_OUTCOME]. Make the ask direct, low-friction, and connected to the narrative: "Given what we've walked through today, the obvious next step is [specific action]. Here's what that looks like..."

For each act, confirm: does the narrative logic of [THE_SHIFT], [THE_PROBLEM], and [YOUR_APPROACH] support this arc? Flag any gaps or places where additional proof or context is needed.

---

SECTION 2 — SLIDE-BY-SLIDE BRIEF

Write the complete slide brief using the arc from Section 1. For each slide:

SLIDE [N]: [TITLE]
- NARRATIVE PURPOSE: Why this slide exists in the sequence. What belief state should the prospect hold after seeing this slide?
- TALKING POINTS: What the presenter says (not a script — key points, in priority order, that can be delivered in 60–90 seconds)
- VISUAL DIRECTION: The single strongest visual concept for this slide. Priority: data visualization > customer quote > product screenshot > stock concept art. Never a bullet list.
- TRANSITION: The one sentence that bridges from this slide to the next, maintaining narrative momentum

Mandatory slides to cover:
1. Opening hook / The Shift (NOT a company overview or agenda)
2. Market evidence for the shift (data-backed)
3. The prospect's world before — the tension they live in every day
4. The problem stated precisely (the "job" this deck is hired to solve)
5. Why the current approach breaks down at scale/complexity
6. The insight: what would have to be true to solve this correctly
7. The [PRODUCT_NAME] approach (one-sentence framing before any features)
8. Core capability 1 — tied directly to the problem from Slide 4
9. Core capability 2 — tied to a specific workflow or outcome
10. Core capability 3 — the "wow" moment — the capability that changes the conversation
11. Customer story — [HERO STORY RECOMMENDATION: see Section 3]
12. Metric proof slide — 3–5 quantified outcomes, no vague percentages
13. Social proof panel — logos, G2 badges, analyst recognition
14. The "why now" urgency slide — what is the cost of inaction?
15. CTA — [DESIRED_OUTCOME], specific and frictionless

---

SECTION 3 — HERO STORY RECOMMENDATION

The customer story slide is the most persuasive slide in the deck if chosen correctly, and the least persuasive if chosen incorrectly. The right story is not the biggest logo — it is the story that most closely mirrors [TARGET_PERSONA]'s situation, problem, and desired outcome.

Based on [PROOF_POINTS], recommend:

3a. The ideal hero story profile: what type of company, use case, and buyer persona would create the strongest "that's us" recognition moment for [TARGET_PERSONA]?

3b. Narrative arc for the hero story (3-part structure):
- BEFORE: The specific problem this customer faced (should echo [THE_PROBLEM] exactly)
- APPROACH: Why they chose [PRODUCT_NAME] and what the implementation looked like (short — this is not a case study, it is a proof point)
- AFTER: The specific, quantified outcome (if available) or the qualitative shift in how their work operates

3c. The "pull quote": the one sentence from this customer that, if put on a slide in large type, would make [TARGET_PERSONA] say "I want that." Write a template for the quote if you don't have a real one yet — mark it [PLACEHOLDER: confirm with customer reference team].

---

SECTION 4 — ANTI-PATTERNS AUDIT

List the 7 most common pitch deck failure modes — and for each, assess whether the current brief for [PRODUCT_NAME] risks falling into this trap.

ANTI-PATTERN 1 — THE COMPANY HISTORY SLIDE:
Opening with "Founded in [year], we are a [adjective] company serving [N] customers." Why it fails: the prospect does not care about your company's history until they care about your company's solution. If the deck opens here, move it to an appendix or eliminate it.

ANTI-PATTERN 2 — THE FEATURE AVALANCHE:
Listing every product capability without a through-line. Why it fails: features are only meaningful in the context of a specific problem. Every feature slide must be introduced with "Because [THE_PROBLEM], you need [capability]."

ANTI-PATTERN 3 — THE VAGUE PROOF:
"Customers see 3× improvement in efficiency." Why it fails: specificity creates credibility. Replace with: "Customers like [COMPANY TYPE] reduced [specific metric] from [X] to [Y] within [N] days of deployment."

ANTI-PATTERN 4 — THE SILENT COMPETITION:
Pretending no alternatives exist. Why it fails: sophisticated buyers have already evaluated your competitors. A deck that doesn't acknowledge competitive context feels naïve. The alternative: implicitly position against the approach (Act 3), not the vendor by name.

ANTI-PATTERN 5 — THE WEAK CTA:
Ending with "Any questions?" or a logo slide. Why it fails: Decision Latency requires a specific ask. End with [DESIRED_OUTCOME] framed as the natural conclusion of the narrative: "Based on everything we've discussed, the next step is [specific, low-friction action]."

ANTI-PATTERN 6 — THE ASYNC FAILURE:
Building a deck that only works with a live presenter. Why it fails: most decks are forwarded to stakeholders who were not in the room. Every slide must communicate its message without audio — titles must be claims, not topics; visuals must tell the story without caption.

ANTI-PATTERN 7 — THE BRAND DRIFT:
Language or claims in the deck that deviate from the approved positioning statement, messaging hierarchy, or proof point inventory. Why it fails: inconsistency is a credibility signal to buyers. The rep sounds like they work at a different company than the website.

For each anti-pattern: confirm whether the brief above risks this failure mode, and if so, specify the correction.

---

SECTION 5 — ASYNC VS. LIVE USE GUIDANCE

This deck needs to work in two contexts: as a LIVE presentation with a rep walking through it, and as an ASYNC leave-behind forwarded to stakeholders who were not in the room.

For each context, provide:

LIVE USE:
- Which slides should be skipped or condensed for a 20-minute demo slot?
- Which slides are presenter-dependent (require the rep's narrative to work) and must be preceded by a verbal setup?
- Where is the natural "pause and ask a discovery question" moment in the flow?

ASYNC USE:
- Which slides require additional context (a text annotation, a caption, or a longer title) to make sense without audio?
- What is the minimum viable deck for async (the slides that MUST be included if you cut everything else)?
- Recommend a cover message template for when a rep sends this deck after a first call: what 3–4 sentences should accompany the deck to prime the reader before they open it?

---

FORMATTING REQUIREMENTS:
- Section 2 slide briefs: one labeled block per slide with all four sub-sections
- Section 4 anti-patterns: structured analysis with explicit verdict per anti-pattern (AT RISK / CLEAR / FLAGGED FOR REVIEW)
- Section 5: two clearly separated sections for each use context
- Total output: this is a full production brief — a content team should be able to build the deck from this document without a briefing call
```

---

## Pro Tips

**Iteration 1 — Executive version:**
*"Build a compressed version of this narrative arc for a 5-slide executive summary deck — designed for a 10-minute C-suite slot where the goal is to get approval for a formal evaluation, not to close a deal. Which 5 slides survive the cut, and how does the CTA change?"*

**Iteration 2 — Video script:**
*"Using the narrative arc from Section 1, write a 90-second video script for a prospect-facing explainer video. The video should work without the deck — it is the pre-meeting hook that gets a cold prospect to book a demo."*

**Common Failure Mode:**
The "Show the Shift" framework requires that the shift in Act 1 be genuinely undeniable — something the prospect already believes, not something you are trying to convince them of. If The Shift sounds like a vendor claim rather than a market observation, the entire narrative loses credibility. Test it with: *"Would a journalist at [industry trade publication] write an article about this shift without mentioning [PRODUCT_NAME]? If not, the shift is actually a product claim in disguise — reframe it."*
