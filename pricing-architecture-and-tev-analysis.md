# Pricing Architecture & True Economic Value Analysis

## Use Case
Build a rigorous, value-anchored pricing strategy from first principles — calculating True Economic Value (TEV), identifying the optimal Value Metric vs. Charge Metric, designing a Good/Better/Best packaging architecture, and producing a behavioral optimization layer that reduces the Pain of Paying without discounting.

## When to Use
- Launching a new product or feature and setting price for the first time
- Repositioning pricing to move away from cost-plus or seat-based legacy models
- When gross margin is healthy but perceived value is low and conversion is suffering
- Before entering a new segment where willingness-to-pay is unknown
- When a competitor has made a pricing blunder and a market window has opened

## Required Inputs
- `[PRODUCT_NAME]` — Product or feature being priced
- `[NEXT_BEST_ALTERNATIVE]` — What the customer would use or do if your product didn't exist (named competitor, internal build, manual workaround, or status quo)
- `[NBA_PRICE]` — The price or cost of the Next-Best Alternative (annual or monthly)
- `[PERFORMANCE_DIFFERENTIAL]` — How your product outperforms the NBA on the dimensions that matter to the buyer (quantified where possible)
- `[COGS_PER_UNIT]` — Variable cost of delivering the product (e.g., AI inference cost per task, per seat, per GB)
- `[JOB_TO_BE_DONE]` — The specific outcome the customer is hiring the product to achieve (verb-forward, one sentence)
- `[CURRENT_PRICING_MODEL]` — Existing model if applicable (e.g., flat seat-based at $X/seat/month)
- `[TARGET_SEGMENT]` — The primary ICP for this pricing exercise
- `{USAGE_DATA}` — Optional: distribution of usage across current customer base (high/medium/low usage cohorts)
- `{WIN_LOSS_PRICE_FEEDBACK}` — Optional: what buyers say about price in win/loss calls

## Expected Output
- Value Metric vs. Charge Metric recommendation
- TEV calculation with economic justification
- Good/Better/Best packaging architecture
- Behavioral pricing optimization layer
- Pricing floor and ceiling analysis
- Risk and communication plan

---

## The Prompt

```
You are a Senior Pricing Strategist and GTM Consultant with deep expertise in B2B SaaS and AI product monetization. Your task is to produce a complete pricing architecture for [PRODUCT_NAME], grounded in value economics — not cost-plus intuition.

A foundational rule for this entire analysis: KILL THE COST-PLUS FALLACY. At no point should price be derived by taking [COGS_PER_UNIT] and adding a margin percentage. Cost is the floor — it tells you where you cannot go. Value is the ceiling — it tells you where you can go. Everything between the floor and ceiling is a strategic decision, not an arithmetic one.

Work through each step in sequence. Show your reasoning explicitly at every stage. Where data is unavailable, make explicit assumptions labeled [ASSUMPTION] and state what you would need to validate them.

---

STEP 1 — VALUE METRIC DISCOVERY

Before setting any price, identify what the customer actually values — and separate that from what you will bill them for. These are often different things, and confusing them is one of the most common pricing errors in B2B SaaS.

Product: [PRODUCT_NAME]
Job to be done: [JOB_TO_BE_DONE]
Target segment: [TARGET_SEGMENT]

1a. VALUE METRIC IDENTIFICATION:
The Value Metric is the unit of benefit — the thing that scales in the customer's mind as they get more value from the product. It is the answer to: "As the customer gets more out of this product, what goes up?"

Evaluate the following candidate value metrics for [PRODUCT_NAME]:
- Outcome-based: the actual result achieved (e.g., tickets resolved, leads converted, hours saved)
- Usage-based: the volume of product consumed to achieve outcomes (e.g., API calls, tasks run, documents processed)
- Seat-based: the number of people accessing the product
- Capacity-based: the scale of what the product manages (e.g., number of workflows, data volume)

For each candidate, score it on three dimensions (1–3 scale):
- ALIGNMENT: Does price go up as customer value goes up? (3 = perfectly aligned)
- INTELLIGIBILITY: Can the customer easily understand and predict their bill? (3 = fully transparent)
- SCALABILITY: Does this metric grow with the customer's business in a way that expands revenue naturally? (3 = strong NRR engine)

Recommend the optimal Value Metric for [PRODUCT_NAME] and justify it.

1b. CHARGE METRIC SELECTION:
The Charge Metric is what actually appears on the invoice. It may or may not match the Value Metric.

Critical note for AI products: if [PRODUCT_NAME] is AI-powered, the compute cost is denominated in tokens, API calls, or inference runs — but customers almost never value tokens. They value outcomes. Billing for tokens when the value is outcomes creates misalignment, erodes trust, and attracts "bill shock" complaints.

For [PRODUCT_NAME], recommend the Charge Metric and explain:
- How it maps to the Value Metric (ideally, they are the same or tightly correlated)
- Whether there is a gap between what customers value and what you will bill them for — and if so, how to bridge that gap in packaging and communication
- If usage-based: mandate the inclusion of usage caps, overage alerts, and billing threshold notifications to prevent bill shock. Specify the exact design of these guardrails.

---

STEP 2 — TRUE ECONOMIC VALUE (TEV) CALCULATION

TEV is the maximum rational price a buyer would pay before switching to the Next-Best Alternative. It is the economic ceiling of your pricing power. Every price you set should be justified relative to TEV.

Formula: TEV = NBA Price + Performance Differential Value − Switching Cost

Inputs:
- Next-Best Alternative: [NEXT_BEST_ALTERNATIVE]
- NBA Price: [NBA_PRICE]
- Performance Differential: [PERFORMANCE_DIFFERENTIAL]
- Current pricing model (for switching cost reference): [CURRENT_PRICING_MODEL]

2a. NBA COST ANALYSIS:
What does the Next-Best Alternative actually cost the customer — in total? Consider:
- Direct price (the invoice they pay [NEXT_BEST_ALTERNATIVE])
- Indirect costs: implementation, training, maintenance, integration, internal FTE time to manage it
- Failure costs: what happens when the NBA fails to do the job well? What is the cost of that failure?

State the fully-loaded NBA cost. This is always higher than the headline price — make the math explicit.

2b. PERFORMANCE DIFFERENTIAL VALUATION:
Where [PRODUCT_NAME] outperforms the NBA, quantify the value of that differential in dollar terms.

Performance differential inputs: [PERFORMANCE_DIFFERENTIAL]

For each differential advantage, express it as a dollar value using one or more of these methods:
- TIME VALUE: If [PRODUCT_NAME] saves X hours per week vs. the NBA, calculate: Hours Saved × Fully-Loaded Hourly Cost of the Role Affected
- ERROR RATE REDUCTION: If [PRODUCT_NAME] reduces errors vs. the NBA, calculate: Error Frequency × Average Cost Per Error
- REVENUE IMPACT: If [PRODUCT_NAME] generates additional revenue vs. the NBA, calculate: Revenue Uplift × Customer's Average Margin
- RISK REDUCTION: If [PRODUCT_NAME] reduces a compliance, security, or operational risk, calculate: Probability of Risk Event × Cost of Risk Event

Sum all differential values to produce the Total Performance Differential ($).

2c. TEV CALCULATION:
TEV = [NBA_PRICE (fully-loaded)] + [Total Performance Differential] − [Switching Cost Estimate]

Present the TEV as a range (low/mid/high) based on assumptions about differential magnitude and switching costs.

2d. PRICE POSITIONING WITHIN THE TEV RANGE:
The Value-Pricing Thermometer: your price must sit between [COGS_PER_UNIT] (the floor — your incentive to sell) and TEV (the ceiling — the customer's rational limit).

COGS floor: [COGS_PER_UNIT]
TEV ceiling: [calculated above]

Recommend where within this range to set the price — and justify the positioning strategically:
- Pricing close to TEV: maximizes revenue per customer, requires high marketing support to demonstrate the differential, and risks being perceived as aggressive
- Pricing well below TEV: maximizes adoption speed and competitive displacement, sacrifices margin, and may signal lower quality
- The Goldilocks zone: typically 50–70% of TEV for B2B SaaS — enough to capture significant value while leaving the customer feeling they "won" the negotiation

State the recommended price point and the strategic rationale.

---

STEP 3 — PACKAGING ARCHITECTURE (GOOD / BETTER / BEST)

A single price point is a missed opportunity. A tiered packaging architecture serves multiple segments simultaneously, anchors perception of value at the top, and allows customers to self-select into the tier that fits their maturity and budget.

3a. ANCHOR, FLAGSHIP, ENTRY TIER DESIGN:

BEST (Anchor / Enterprise Tier):
Purpose: This tier exists primarily to make the middle tier look reasonable. It is also the aspirational destination for high-value customers. Price it at or near TEV — it should feel "expensive but worth it" to the most sophisticated buyers.
- What capabilities does this tier include that no other tier offers?
- What is the pricing mechanism (flat enterprise contract, usage-based with high cap, outcome-based)?
- What "white glove" service elements (dedicated CSM, SLA guarantees, custom integrations) justify the premium?

BETTER (Flagship / Growth Tier):
Purpose: This is where the majority of ARR will come from. It should be priced at the Goldilocks zone within the TEV range — compelling value, healthy margin.
- What capabilities does this tier include?
- What are the natural upgrade triggers from the Entry tier? (i.e., the moments when a customer on the Entry tier will feel they need to move up)
- What is the price, and how does it relate to the TEV calculation from Step 2?

GOOD (Entry / Land Tier):
Purpose: Designed to remove friction from initial purchase, get customers into the product, and begin the habituation process. Priced to be a "no-brainer" relative to the NBA — a rational, low-risk first step.
- What is the minimum viable capability set for a customer to achieve their first meaningful outcome?
- What are the deliberate limitations that make the Entry tier feel complete but not sufficient for growth? (e.g., seat caps, usage limits, feature gates)
- Is this tier freemium, paid-low, or trial-gated?

3b. PACKAGING TABLE:
Produce a three-column packaging table:
| | GOOD | BETTER | BEST |
|---|---|---|---|
| Price | | | |
| Charge Metric | | | |
| Core Capabilities | | | |
| Key Limitations | | | |
| Upgrade Trigger | | | |
| Target Buyer | | | |

3c. DEMOGRAPHIC AND TRANSACTION-BASED CUSTOMIZATION:
Beyond the tier structure, recommend 2–3 customization levers:
- DEMOGRAPHIC: Segment-specific pricing (e.g., startup program, nonprofit pricing, academic tier)
- TEMPORAL: Early commitment discounts (annual vs. monthly differential — recommend the % gap that maximizes annual contract conversion without training customers to wait)
- VOLUME: Usage-based overage design — how should price per unit change as usage scales? (linear, stepped, declining — and why)

---

STEP 4 — BEHAVIORAL PRICING OPTIMIZATION

Price is not just a number — it is a psychological signal. The same price communicated differently produces materially different conversion rates. This step applies behavioral economics to reduce the Pain of Paying without changing the price itself.

4a. CHARM PRICING VS. ROUND PRICING:
The choice between $99 and $100 is not arbitrary — it is a System 1 vs. System 2 decision.

- For RATIONAL / HIGH-STAKES purchases (large B2B contracts, enterprise tiers, multi-year commitments): use round numbers. Round numbers feel considered and fair. $50,000/year communicates confidence. $49,999 communicates desperation.
- For TRANSACTIONAL / SELF-SERVE purchases (SMB, PLG, freemium-to-paid conversion): use charm digits ($X9, $X7). The left-digit anchoring effect is real and documented — $97/month is perceived as meaningfully less than $100/month even when the rational difference is negligible.

Apply the correct tactic to each tier in the [PRODUCT_NAME] packaging architecture. Justify each choice.

4b. CURRENCY SYMBOL AND PRESENTATION:
- For HEDONIC / EXPERIENCE-ORIENTED contexts (where the product is pleasurable to use): remove the dollar sign where design allows. Studies show that removing the "$" reduces the Pain of Paying by reducing the salience of the financial transaction.
- For UTILITARIAN / ROI-ORIENTED contexts (where the buyer is calculating a business case): keep the currency symbol and pair the price with a ROI framing — the symbol anchors the comparison: "$X per month vs. $Y you're currently losing to [the problem]."

Which context applies to [PRODUCT_NAME] for [TARGET_SEGMENT]? Apply accordingly.

4c. TIME VS. MONEY FRAMING:
Research by Mogilner & Aaker shows that "time spent" messaging outperforms "money saved" messaging for products where the emotional connection matters.

- If [PRODUCT_NAME] is positioned as a capability enhancer (makes the user feel more skilled, autonomous, or effective): lead with time — "Save 6 hours a week" outperforms "Save $1,200/month" even when they are mathematically equivalent.
- If [PRODUCT_NAME] is positioned as a pure cost reduction tool: lead with money — "Reduce your [expense category] by 40%" — and pair it with the TEV calculation.

Recommend the primary framing for each tier and persona, and write a sample pricing page headline for the flagship tier.

4d. PARTITIONING AND PAIN REDUCTION:
For high-price tiers, recommend whether to partition the price (show the per-seat, per-outcome, or per-day equivalent alongside the annual price) to reduce the psychological magnitude of the number.

Example: "$120,000/year" is psychologically heavy. "$10,000/month" is lighter. "$329/day" is lighter still — and if [THE_JOB] saves more than $329/day of value, the anchor inverts: the price becomes cheap relative to the value reference.

Design the optimal price presentation format for each tier.

---

STEP 5 — MULTIPLICATIVE PROFIT DECOMPOSITION

Before finalizing the pricing recommendation, stress-test it against the full profit model.

Formula: Profit = # Active Customers × AOF (Average Order Frequency) × AOV (Average Order Value) × Average Margin

5a. MODEL THE CURRENT STATE:
Using the current pricing model ([CURRENT_PRICING_MODEL]) and any available data, estimate the current Profit = Customers × AOF × AOV × Margin.

5b. MODEL THE RECOMMENDED STATE:
Using the new pricing architecture from Steps 2–3, model the expected impact on each variable:
- Does the new pricing model increase or decrease the total addressable customer count? (Might decrease if price rises — quantify the expected conversion rate impact)
- Does the new pricing model increase AOF? (E.g., usage-based pricing increases "order frequency" as customers consume more)
- Does the new pricing model increase AOV? (The primary goal — TEV-anchored pricing should expand AOV materially)
- Does the new pricing model increase margin? (By moving away from cost-plus, margin should improve even if per-unit cost stays the same)

5c. THE 1% PRICE INCREASE RULE:
Calculate: what is the net income impact of a 1% price increase vs. a 20% volume increase, holding all other variables constant?

For most B2B SaaS businesses, a 1% price increase produces 2–4× the net income improvement of a 20% volume increase. State the math for [PRODUCT_NAME] explicitly. This is the business case for value pricing over growth-at-any-cost pricing.

5d. SENSITIVITY ANALYSIS:
Run three scenarios:
- BEAR: New pricing underperforms — conversion rate drops 15%, but AOV increases as modeled. Net impact on profit?
- BASE: New pricing performs as modeled. Net impact?
- BULL: New pricing outperforms — segment responds strongly to TEV framing, conversion holds, AOV increases. Net impact?

---

STEP 6 — RISK MITIGATION AND COMMUNICATION PLAN

6a. PRICING CHANGE RISK ASSESSMENT (if applicable):
If this is a pricing change from [CURRENT_PRICING_MODEL], assess:
- LEGACY TENSION: Are there existing customers who will experience a price increase? Estimate the churn risk by cohort (high-usage customers may welcome usage-based pricing; low-usage customers may feel penalized).
- COMPETITIVE RESPONSE: How will [NEXT_BEST_ALTERNATIVE] likely respond to your pricing move? If you raise price and they hold, you may lose price-sensitive deals. If you move to outcome-based and they don't, you gain a positioning advantage.
- CHANNEL CONFLICT: Does the new pricing model create tension with existing resellers, partners, or integrators who have margin expectations built on the old model?

6b. THE PRET PRINCIPLE — RADICAL TRANSPARENCY COMMUNICATION:
When communicating any price change to existing customers, follow the Pret-a-Manger model: be explicit, specific, and value-linked. Euphemisms like "price optimization" or "tier restructuring" breed resentment. Directness builds trust.

Write a template customer communication for the pricing change (if applicable) that:
- Opens by naming the change directly: "We are increasing the price of [PRODUCT_NAME]." No euphemisms.
- Cites specific, named cost drivers — if compute costs have risen, say so. If staff investment has increased, name it. Vague justifications feel like excuses; specific ones feel honest.
- Links each cost driver back to customer value: "The additional compute investment enables [specific capability improvement] that our customers use to [specific outcome]."
- Provides a grandfather window: a specific date before which existing customers can lock in current pricing or transition terms. State the window clearly.
- Closes with a direct invitation to discuss: name a specific person or team the customer can contact, not a generic support email.

6c. WHITE GLOVE INTERVENTION PLAN:
For the top 20% of customers by ARR who will be affected by any pricing change:
- Define the proactive outreach sequence (who reaches out, when, through what channel)
- Define the negotiation guardrails (what discount or grandfather term is acceptable; what signals that a customer is at churn risk vs. negotiating as a habit)
- Define the escalation path (at what ACV threshold does a pricing negotiation escalate from CSM to VP/C-suite?)

---

FINAL OUTPUT: PRICING FRAMEWORK SUMMARY TABLE

Produce a one-page summary table:

| Element | Recommendation | Rationale |
|---|---|---|
| Value Metric | | |
| Charge Metric | | |
| TEV (range) | | |
| Price Floor (COGS) | | |
| Recommended Price Point | | |
| Good Tier | | |
| Better Tier | | |
| Best Tier | | |
| Primary Behavioral Tactic | | |
| Framing (Time vs. Money) | | |
| Communication Approach | | |

---

FORMATTING REQUIREMENTS:
- All calculations in Step 2 and Step 5: show the arithmetic explicitly — no black-box conclusions
- Step 3 packaging table: full table, all cells populated
- Step 6b communication template: written in full, ready to adapt and send
- Assumptions: labeled [ASSUMPTION] inline throughout
- Tone: this is a document for a CMO and CFO — strategic rigor, no filler, every recommendation defensible under financial scrutiny
```

---

## Pro Tips

**Iteration 1 — Competitive pricing pressure test:**
After the full output, prompt: *"[NEXT_BEST_ALTERNATIVE] just announced a 20% price cut. Walk through how each element of the pricing architecture should — and should not — respond. Which elements are resilient to competitive price pressure, and which are exposed?"*

**Iteration 2 — Packaging page copy:**
*"Using the Good/Better/Best architecture and the behavioral optimization recommendations, write the full copy for a SaaS pricing page — including tier names, feature bullets, price presentation, and the CTA for each tier. Apply the correct charm vs. round pricing and time vs. money framing."*

**Common Failure Mode:**
The model may default to cost-plus reasoning when COGS data is provided — treating the margin above COGS as the natural price. If this happens, invoke the TEV anchor explicitly: *"The COGS figure is only relevant as a floor. Rebuild the price recommendation starting from the TEV ceiling and working down to the strategic positioning point — not up from cost."*
