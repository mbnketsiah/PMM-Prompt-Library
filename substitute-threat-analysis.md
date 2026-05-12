# Substitute Threat Analysis

## Use Case
Identify and prioritize non-obvious threats to market share — the substitutes, workarounds, and adjacent solutions that your target segment uses instead of buying your product. Map the conditions under which a buyer defects to each substitute, and produce counter-positioning strategy for each.

## When to Use
- When win rates are declining but you can't find a named competitor to blame
- When "no decision" or "status quo" appears frequently in loss analysis
- When entering a new segment where the buying behavior is unfamiliar
- During any positioning refresh where you want to pressure-test your differentiation

## Required Inputs
- `[YOUR_PRODUCT]` — Product or feature name
- `[TARGET_SEGMENT]` — Primary ICP with firmographic and behavioral detail
- `[THE_JOB]` — The specific functional outcome your product is hired to perform (one sentence, verb-forward)
- `[YOUR_PRICE_POINT]` — Approximate ACV or monthly cost (used to calibrate rational defection scenarios)
- `[TOP_WIN_LOSS_THEMES]` — 3–5 recurring themes from recent loss calls or CRM loss reason data
- `{KNOWN_SUBSTITUTES}` — Optional: substitutes you already suspect (the model will add to this list)

## Expected Output
- Comprehensive substitute register with defection trigger mapping
- Rational buyer defection model per substitute
- Counter-positioning language for each major substitute threat
- Prioritized action list for product and marketing to close the gaps

---

## The Prompt

```
You are a B2B product marketing strategist specializing in competitive displacement and market structure analysis. Your task is to conduct a thorough substitute threat analysis for [YOUR_PRODUCT], which targets [TARGET_SEGMENT].

The job [YOUR_PRODUCT] is hired to perform: [THE_JOB]

Approach this analysis with first-principles thinking. The goal is to surface threats that would not appear on a standard competitive landscape slide — the substitutes, workarounds, and inertia forces that quietly erode market share without showing up in a win/loss CRM field.

Work through the following steps in sequence. Reason explicitly before concluding.

---

STEP 1 — RETHINK THE CATEGORY BOUNDARIES

Before identifying substitutes, challenge the category definition itself.

1a. How does [TARGET_SEGMENT] mentally frame the problem that [YOUR_PRODUCT] solves? Is it primarily a technology problem, a workflow problem, a headcount problem, or a risk management problem? The answer determines what they consider a legitimate substitute.

1b. What would a budget holder in [TARGET_SEGMENT] write on a purchase order to expense [YOUR_PRODUCT]? How they categorize the spend reveals the alternative budget lines they might raid instead — and therefore the substitutes that compete for the same dollars.

1c. Apply the JTBD substitution heuristic: "On the day before [TARGET_SEGMENT] decided to evaluate [YOUR_PRODUCT], what were they already doing to get [THE_JOB] done?" List every plausible answer, including partial solutions and manual workarounds.

---

STEP 2 — BUILD THE SUBSTITUTE REGISTER

Identify and catalog all meaningful substitutes across five categories:

CATEGORY A — MANUAL WORKAROUNDS
Tools or behaviors that deliver a "good enough" version of the job without dedicated software. Examples: spreadsheets, internal wikis, email threads, Notion databases, Airtable configurations.

CATEGORY B — ADJACENT SOFTWARE ALREADY IN THE STACK
Products the segment already pays for that could be stretched to partially perform [THE_JOB]. For each, assess: what percentage of [THE_JOB] could a resourceful power user accomplish with existing tooling?

CATEGORY C — HUMAN-POWERED ALTERNATIVES
Consultants, agencies, freelancers, or additional headcount that deliver the outcome without a SaaS purchase.

CATEGORY D — INTERNAL BUILD
The decision to solve this with internal engineering resources rather than buying a vendor solution. When is this rational? What company profile makes this likely?

CATEGORY E — STATUS QUO / DO NOTHING
The inertia option. Under what specific conditions is a rational buyer better off with the status quo than with [YOUR_PRODUCT] at [YOUR_PRICE_POINT]? Be honest — this is not always irrational.

For each substitute identified, produce:
- Substitute name/description
- The buyer profile most likely to choose this over [YOUR_PRODUCT]
- The specific trigger condition — what has to be true for a buyer to rationally defect to this substitute
- The "switch cost" that works in [YOUR_PRODUCT]'s favor — what they lose by not using a dedicated solution
- Threat level: HIGH / MEDIUM / LOW, with a one-sentence rationale

---

STEP 3 — CROSS-REFERENCE WITH LOSS DATA

Loss data: [TOP_WIN_LOSS_THEMES]

3a. Map each loss theme to its most likely substitute category from Step 2. For example, "too expensive" maps to Status Quo or Manual Workaround; "already have a solution" maps to Adjacent Software.

3b. Identify the substitute that is most likely driving your losses but is NOT being captured in your current CRM loss reason taxonomy. What is the hidden competitor that no one is naming?

3c. Flag any loss themes that suggest the market is not yet ready to buy — i.e., where the Jobs-to-be-Done insight is that buyers are still in the "workaround phase" and haven't yet experienced enough pain to trigger a formal evaluation.

---

STEP 4 — RATIONAL DEFECTION MODELING

For the top 3 highest-threat substitutes identified in Step 2, build a rational defection model:

For each substitute:
4a. Under what specific conditions (company size, team maturity, budget cycle, prior tech investments) does choosing this substitute over [YOUR_PRODUCT] represent a rational, defensible decision — even to a sophisticated buyer?

4b. What is the "moment of truth" — the specific pain event or milestone — that tips a buyer from the substitute to actively evaluating [YOUR_PRODUCT]? This is the trigger you should be marketing against.

4c. What is the one thing [YOUR_PRODUCT] would need to demonstrate, prove, or change to make the switch from this substitute feel obviously worth it? Frame this as a proof requirement, not a feature request.

---

STEP 5 — COUNTER-POSITIONING STRATEGY

For each of the top 3 substitute threats, produce:

5a. A one-sentence "substitute reframe" — positioning language that acknowledges the substitute as a legitimate starting point, then pivots to why it breaks down at scale, complexity, or risk. Do NOT disparage the substitute — validate it first, then illustrate the ceiling.

Example structure: "[SUBSTITUTE] is the right call when [CONDITION X]. Where it breaks down is [SPECIFIC FAILURE MODE] — and that's the moment [YOUR_PRODUCT] pays for itself."

5b. A content or channel recommendation: what type of asset (comparison page, ROI calculator, case study structure, event talk, sales play) would most effectively intercept a buyer who is currently in the substitute-evaluation mindset?

5c. An internal trigger for your sales team: the qualifying question or discovery prompt that surfaces this substitute usage early in a sales conversation, before the prospect has anchored on the substitute as their solution.

---

STEP 6 — PRIORITIZED ACTION LIST

Synthesize findings into a prioritized action list across three workstreams:

PRODUCT: What capability gaps, onboarding improvements, or pricing structures would reduce defection to the top substitutes?

MARKETING: What messaging, content, or channel investments would most efficiently intercept buyers in the substitute consideration phase?

SALES ENABLEMENT: What discovery prompts, objection scripts, or proof assets does the field need to displace the top substitutes in active deals?

Rank each action by: Impact (HIGH/MED/LOW) × Feasibility (HIGH/MED/LOW) × Time-to-Deploy (weeks). Present as a prioritized table.

---

FORMATTING REQUIREMENTS:
- Step 2 substitute register: structured table format
- Step 4 defection models: one structured block per substitute, clearly labeled
- Step 6 action list: table with columns — Action | Workstream | Impact | Feasibility | Time-to-Deploy
- Prose sections: tight, specific, no filler language
- Avoid generic B2B advice — every insight must be specific to [TARGET_SEGMENT] and [THE_JOB]
```

---

## Pro Tips

**Iteration 1 — Build a discovery script:**
After running the full analysis, prompt: *"Based on the top 3 substitute threats, write a 5-question discovery sequence a sales rep could use in the first 20 minutes of a demo call to diagnose which substitute the prospect is currently using and how embedded they are in it."*

**Iteration 2 — Build a comparison landing page brief:**
*"Using the substitute reframe language from Step 5a, write a content brief for a '[YOUR_PRODUCT] vs. [SUBSTITUTE]' comparison page. Include the narrative arc, 3 proof points, and a CTA hypothesis."*

**Common Failure Mode:**
Models often underweight the "Do Nothing" option. If the output treats status quo as obviously inferior, push back: *"Steelman the case for staying with the status quo for [SPECIFIC BUYER PROFILE]. Under what conditions is not buying [YOUR_PRODUCT] the correct decision, and what does that tell us about who we should NOT be targeting?"*
