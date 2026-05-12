# Positioning Statement Generator

## Use Case
Generate a rigorous, strategically defensible brand positioning statement — built on the standard academic format — complete with Reasons to Believe (RTB), competitive context, and a benefit-laddered rationale. This is an internal strategic document, not consumer-facing copy.

## When to Use
- Repositioning an existing product for a new segment or use case
- Launching a new product or major feature tier
- When messaging has drifted and the team needs to re-anchor on a canonical positioning
- Before building any messaging architecture, sales deck, or campaign brief

## Required Inputs
- `[PRODUCT_NAME]` — The product or solution being positioned
- `[TARGET_MARKET]` — Precise segment definition (firmographic + behavioral + psychographic)
- `[COMPETITIVE_SET]` — The specific alternatives this segment evaluates (named competitors + substitutes)
- `[UNIQUE_VALUE_CLAIM]` — Your hypothesis on the one thing only you can credibly claim
- `[REASONS_TO_BELIEVE]` — 3–5 proof points: data, customer outcomes, technical differentiators, awards
- `{CURRENT_POSITIONING_DRAFT}` — Optional: existing positioning language to stress-test or improve

## Expected Output
- Final positioning statement in standard format
- Benefit ladder (Feature → Benefit → Value)
- RTB validation scorecard
- Common failure modes flagged
- Draft tagline directions (clearly labeled as external-facing, separate from the internal statement)

---

## The Prompt

```
You are a Chief Marketing Officer and positioning strategist with deep expertise in B2B SaaS brand architecture. Your task is to develop a rigorous brand positioning statement for [PRODUCT_NAME] and validate it against the highest standards of positioning science.

This is an internal strategic document — a compass for the marketing and product organization, not a consumer-facing slogan. Treat it accordingly: prioritize strategic clarity over creative flair.

Work through each step sequentially. Show your reasoning process, including where you considered and rejected alternatives.

---

STEP 1 — ESTABLISH THE STRATEGIC CONTEXT

Before writing any positioning language, set the foundation.

1a. Confirm the target market definition. Evaluate the following segment definition against three criteria: (1) Is it specific enough to be actionable — could a sales rep identify a qualifying prospect from this description alone? (2) Is it large enough to be a viable business? (3) Is it behaviorally coherent — do members of this segment share similar buying triggers, success criteria, and switching costs?

Target market: [TARGET_MARKET]

Flag any weaknesses in this definition and recommend refinements if needed.

1b. Define the frame of reference — the competitive category or "mental shelf" where [PRODUCT_NAME] will live in the target market's mind. This is not a product category from an analyst report; it is how the buyer mentally groups the alternatives they consider. What is the frame of reference for [PRODUCT_NAME]?

1c. Articulate the single most important insight about what [TARGET_MARKET] fundamentally wants that the competitive set fails to fully deliver. This is the strategic opening that [PRODUCT_NAME] must own.

---

STEP 2 — DRAFT THE POSITIONING STATEMENT

Using the standard positioning statement format, produce three candidate positioning statements for [PRODUCT_NAME]:

Standard Format:
"For [TARGET MARKET], [PRODUCT_NAME] is the only [FRAME OF REFERENCE] that [UNIQUE VALUE CLAIM] because [REASONS TO BELIEVE]."

Inputs:
- Competitive set: [COMPETITIVE_SET]
- Unique value claim hypothesis: [UNIQUE_VALUE_CLAIM]
- Reasons to believe: [REASONS_TO_BELIEVE]
- Optional existing draft: {CURRENT_POSITIONING_DRAFT}

For each of the three candidates:
- Write the full positioning statement
- Label the strategic emphasis: (a) category leadership, (b) differentiated approach, or (c) segment specificity
- Identify what this version wins on and what it concedes

---

STEP 3 — BENEFIT LADDER VALIDATION

For the strongest candidate from Step 2, build out a full benefit ladder to ensure the positioning claim connects all the way from product reality to human motivation.

RUNG 1 — FEATURE LAYER ("What's in it?"): 
List the 3 core product capabilities that substantiate the positioning claim. These are observable, demonstrable product facts.

RUNG 2 — FUNCTIONAL BENEFIT LAYER ("What's in it for me?"):
For each feature, articulate the direct functional benefit — the task it makes easier, faster, or less error-prone for the user.

RUNG 3 — EMOTIONAL/BUSINESS VALUE LAYER ("Why does it matter?"):
For each functional benefit, articulate the deeper business or emotional value it delivers — the outcome that gets a VP or C-suite out of bed: risk reduction, revenue growth, career safety, competitive advantage, or organizational reputation.

Present this as a three-column table: Feature | Functional Benefit | Business/Emotional Value

---

STEP 4 — RTB VALIDATION SCORECARD

Evaluate the Reasons to Believe for the recommended positioning statement against five criteria. Score each RTB on a 1–3 scale (3 = strong).

Criteria:
- CREDIBILITY: Would a skeptical buyer find this believable without further research?
- VERIFIABILITY: Can this claim be independently confirmed or demonstrated?
- RELEVANCE: Does this proof point directly address a criterion the target segment uses to evaluate vendors?
- EXCLUSIVITY: Could a direct competitor make the exact same claim with equal validity?
- DURABILITY: Is this a structural advantage or a temporary lead that a well-funded competitor could close within 12 months?

Reasons to Believe: [REASONS_TO_BELIEVE]

Flag any RTBs that score below 2 on Exclusivity or Durability — these are the claims most likely to erode under competitive pressure.

---

STEP 5 — FAILURE MODE AUDIT

Stress-test the recommended positioning statement against four common positioning failure modes:

5a. THE LAUNDRY LIST TRAP: Does the positioning statement try to claim more than one differentiated benefit? If so, force a choice — which single claim is most defensible and most motivating to [TARGET_MARKET]?

5b. THE ASPIRATIONAL GAP: Is the Unique Value Claim something [PRODUCT_NAME] actually delivers today, or is it aspirational? If aspirational, flag this as a risk and recommend either adjusting the claim or identifying the roadmap milestone that closes the gap.

5c. THE COMPETITOR CLAIM TEST: Run each element of the positioning statement through this filter: "Could [TOP COMPETITOR] say the exact same thing?" If yes, the element is a Point of Parity, not a Point of Difference. Flag any POPs masquerading as PODs.

5d. THE INTERNAL ALIGNMENT TEST: Would the product team, sales team, and customer success team all recognize this positioning statement as an accurate description of what [PRODUCT_NAME] is and does? If not, identify the most likely point of internal disagreement and recommend how to resolve it.

---

STEP 6 — FINALIZED DELIVERABLES

6a. RECOMMENDED POSITIONING STATEMENT: Present the final, refined positioning statement incorporating all feedback from Steps 3–5.

6b. EXECUTIVE RATIONALE: A 3–4 sentence explanation of why this positioning was chosen over the alternatives — written for a CMO or VP of Marketing who needs to sell this internally.

6c. TAGLINE DIRECTIONS (clearly labeled as EXTERNAL-FACING COPY, separate from the internal positioning statement): 
Generate 3 candidate tagline directions that translate the positioning into consumer-facing language. For each, identify the emotional register it plays in (e.g., aspiration, confidence, urgency, empowerment) and the scenario where it would perform best (e.g., paid media, event keynote, product UI).

6d. MESSAGING GUARDRAILS: 3–5 explicit instructions for the content and campaign team. What this positioning statement explicitly permits them to claim, and what it explicitly prohibits (the "and never say this" list).

---

FORMATTING REQUIREMENTS:
- Step 2 candidates: clearly numbered and labeled
- Step 3 benefit ladder: three-column table
- Step 4 RTB scorecard: table with scores per criterion
- Step 5 failure modes: structured prose, one section per failure mode
- Step 6: clearly delineated sections with bold headers
- Total tone: strategic and precise — this is a C-suite document, not a creative brief
```

---

## Pro Tips

**Iteration 1 — Competitive pressure test:**
*"Take the recommended positioning statement and imagine the CMO of [TOP COMPETITOR] has just seen it. Write a one-paragraph response from their perspective — how would they attempt to neutralize or undercut this positioning, and how should we preemptively address that counter?"*

**Iteration 2 — Persona-specific translation:**
*"Translate the recommended positioning statement into persona-specific value propositions for (a) the economic buyer [e.g., CFO/VP], (b) the technical evaluator, and (c) the end user/champion. Each should ladder back to the core positioning but lead with the benefit most relevant to that person's success criteria."*

**Common Failure Mode:**
The model may produce positioning statements that are internally consistent but competitively soft — claiming differentiation on attributes that all serious competitors also possess. If the output reads like it could describe any product in the category, invoke the Exclusivity test explicitly: *"For the recommended positioning statement, name three competitors who could legitimately make the exact same claim. If any exist, the POD needs to be sharpened."*
