# Three Cs Competitive Audit

## Use Case
Generate a rigorous, board-ready competitive landscape analysis using the Three Cs Model — synthesizing Consumer needs, Competitor offerings, and Company capabilities into an actionable strategic map.

## When to Use
- Ahead of a product launch or major positioning refresh
- During annual planning or strategy cycles
- When a new entrant is disrupting your category
- Before a pricing or packaging decision

## Required Inputs
Before running this prompt, gather:
- `[YOUR_PRODUCT]` — Product or feature name
- `[TARGET_SEGMENT]` — Your primary ICP (e.g., "Mid-market RevOps teams at B2B SaaS companies with 200–1,000 employees")
- `[COMPETITOR_LIST]` — 3–6 named competitors you want analyzed
- `[YOUR_KEY_CAPABILITIES]` — 4–6 bullet points on what your product does best
- `[RECENT_MARKET_SIGNALS]` — Any known competitor funding rounds, hires, product announcements, or job postings
- `{CUSTOMER_FEEDBACK_THEMES}` — Optional: top 3–5 themes from recent win/loss calls or G2/Capterra reviews

## Expected Output
- Competitor triage table (Direct / Indirect / Potential)
- Points of Parity (POP) and Points of Difference (POD) matrix
- Substitute threat register
- Strategic vulnerability assessment
- Recommended focus areas for positioning and product roadmap

---

## The Prompt

```
You are a Senior Director of Product Marketing with 15 years of experience in B2B SaaS competitive strategy. Your task is to produce a rigorous competitive audit for [YOUR_PRODUCT], targeting [TARGET_SEGMENT].

Work through this analysis step by step, using the Three Cs Model as your structural backbone. Do not skip steps. Show your reasoning at each stage before drawing conclusions.

---

STEP 1 — CONSUMER LAYER: Identify Unmet and Under-served Needs

Before analyzing any competitor, establish the demand-side foundation.

1a. Define the primary "job" the target segment is hiring a solution like [YOUR_PRODUCT] to perform. Apply a Jobs-to-be-Done lens: what functional outcome are they trying to achieve, what emotional friction are they trying to eliminate, and what social signal does using this type of solution send within their organization?

1b. Identify the top 3 criteria this segment uses to evaluate solutions in this category. Rank them by decision weight (what they say they care about vs. what actually drives their final vendor decision based on behavioral evidence, not survey data).

1c. Flag any unmet needs that no current solution in the market adequately addresses. These are your whitespace opportunities.

---

STEP 2 — COMPETITOR LAYER: Triage and Assess the Competitive Set

Using the competitor list below, classify each competitor into one of three tiers:
- DIRECT: Competes for the same customer, solving the same job, with a comparable approach
- INDIRECT: Solves a related job or targets an adjacent segment, but overlaps materially at the margin
- POTENTIAL: Not currently a direct threat, but their trajectory, funding, or hiring patterns suggest they could enter your space within 18 months

Competitor list: [COMPETITOR_LIST]
Recent market signals: [RECENT_MARKET_SIGNALS]

For each competitor, produce:
- Tier classification (Direct / Indirect / Potential) with a one-sentence rationale
- Their core value claim as a customer would articulate it (not how they market themselves — how a satisfied customer would describe why they chose them)
- Their primary Points of Parity with [YOUR_PRODUCT] — the "must-have" category features they deliver
- Their primary Points of Difference — the unique claims they make that justify a price premium or preference
- One "black box" weakness: a known or inferable gap in their product, GTM, or support model that your team could exploit

For the Potential tier competitors, additionally assess: What is the one market signal (a specific job posting type, a partnership announcement, a product category expansion) that would confirm they are about to enter your space? Define the tripwire.

---

STEP 3 — SUBSTITUTE ANALYSIS: Look Beyond the Defined Category

The most dangerous competitors are often not on any analyst's radar. Apply substitute analysis: what else does [TARGET_SEGMENT] "hire" to do the same job, even if it's not a software product?

Consider:
- Manual workarounds (spreadsheets, internal wikis, Slack threads)
- Adjacent software they already pay for that partially does this job
- Consulting or agency services that deliver the outcome without a SaaS tool
- Doing nothing (status quo inertia as a competitive force)

For each substitute identified, assess:
- Why a rational buyer might choose it over [YOUR_PRODUCT]
- What would need to be true for them to switch to a dedicated solution
- How [YOUR_PRODUCT]'s positioning should preemptively address this

---

STEP 4 — COMPANY LAYER: Honest Capability Assessment

Assess [YOUR_PRODUCT]'s actual capabilities against the competitive set. Do not default to marketing language — this is an internal strategic document.

Company capabilities: [YOUR_KEY_CAPABILITIES]
Optional customer feedback: {CUSTOMER_FEEDBACK_THEMES}

4a. Produce a POP/POD matrix:
- Points of Parity with the category (what you must have to be taken seriously): list each one and confirm whether [YOUR_PRODUCT] meets the threshold
- Points of Difference (what only you can credibly claim): list each one, and for each, state the evidence or proof point that substantiates it — logical argument, third-party data, or direct customer testimony

4b. Identify your most defensible competitive moat. This is the one capability that would be hardest for a well-funded competitor to replicate within 12 months, and why.

4c. Identify your most critical vulnerability — the one area where a competitor could legitimately out-position you if they chose to attack it directly.

---

STEP 5 — SYNTHESIS: Strategic Implications

Synthesize your findings into three concrete strategic recommendations:

5a. POSITIONING PRIORITY: Based on the POP/POD analysis and whitespace opportunities, what is the one positioning angle that (a) no current competitor owns and (b) maps directly to an unmet or under-served customer need? State it as a draft positioning claim in plain language.

5b. COMPETITIVE RESPONSE MODELING: For your #1 Direct competitor, predict their most likely counter-move if [YOUR_PRODUCT] aggressively pursues the positioning angle from 5a. What would they do, and how should the team prepare?

5c. FACTOR MARKET WATCH LIST: List 3 specific signals (job postings, partnership types, product release patterns) you would monitor over the next 90 days to detect competitive movement before it becomes a public threat.

---

FORMATTING REQUIREMENTS:
- Output Step 2 as a structured table with columns: Competitor | Tier | Core Value Claim | POPs | PODs | Black Box Weakness
- Output Step 4a as a two-column table: POP/POD | Evidence/Proof Point
- All other sections in structured prose with clear headers
- Total length: comprehensive but tight — prioritize specificity over exhaustiveness
- Avoid the Monopoly Fallacy: every strategic recommendation must account for how a rational competitor would respond
```

---

## Pro Tips

**Iteration 1 — Sharpen the substitute analysis:**
After the initial output, follow up with: *"For the [SPECIFIC SUBSTITUTE] you identified, write a two-sentence objection-handling response I could use in a sales call when a prospect says they'd rather use [substitute] than buy [YOUR_PRODUCT]."*

**Iteration 2 — Stress-test the PODs:**
Ask: *"For each Point of Difference you listed, steelman the case that this is actually a Point of Parity — i.e., that a sophisticated buyer would consider this table stakes, not a differentiator. Which ones survive the steelman test?"*

**Common Failure Mode:**
If the model produces generic competitive analysis (e.g., "Competitor X is strong in enterprise"), push back with: *"Rewrite the competitive assessment using only claims that could be falsified with evidence. Remove all assertions that a competitor's marketing team would also claim about themselves."*
