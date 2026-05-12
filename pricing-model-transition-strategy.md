# Pricing Model Transition & Migration Strategy

## Use Case
Design a structured, risk-managed strategy for migrating from a legacy pricing model (typically seat-based or flat-fee) to a value-aligned model (usage-based, outcome-based, or hybrid) — including cohort impact analysis, revenue bridge modeling, customer communication architecture, and a behavioral economics layer that reduces perceived price pain during the transition.

## When to Use
- Moving from seat-based pricing to usage- or outcome-based
- When a legacy pricing model is suppressing NRR and creating "all-you-can-eat" customers who pay flat fees but consume disproportionate resources
- When a competitor's pricing blunder has opened a window to reposition your model as the market standard
- When AI infrastructure costs (inference, compute, tokens) are scaling faster than revenue under a flat pricing structure
- When enterprise customers are demanding outcome-based commercial models and the current model can't accommodate them

## Required Inputs
- `[PRODUCT_NAME]` — Product or solution undergoing pricing migration
- `[CURRENT_MODEL]` — Existing pricing model in detail (e.g., "$500/seat/month, flat, all features included")
- `[PROPOSED_MODEL]` — The target pricing model (e.g., "Usage-based at $X per task resolved, with a BETTER/BEST tier overlay")
- `[CUSTOMER_COHORT_DATA]` — Summary of current customer base segmented by usage level and ACV (e.g., "Top 20% of accounts = 65% of revenue; bottom 40% = 8% of revenue")
- `[COGS_PRESSURE]` — The cost driver forcing the model change (e.g., "AI inference costs rising 30% YoY; flat pricing creating negative margin on high-usage accounts")
- `[NEXT_BEST_ALTERNATIVE]` — Competitor or substitute the customer would evaluate if pricing change triggers evaluation
- `[MIGRATION_TIMELINE]` — Target window for full migration (e.g., "New customers on new model from Q3; existing customers migrated by end of Q4")
- `[CHURN_TOLERANCE]` — The maximum acceptable churn (in ARR %) from the migration
- `{LEGACY_TENSION_SIGNALS}` — Optional: any existing customer complaints, competitor moves, or market signals that indicate pricing dissatisfaction
- `{WIN_LOSS_PRICE_DATA}` — Optional: how price comes up in win/loss analysis currently

## Expected Output
- Current model diagnosis and legacy tension assessment
- Revenue bridge model (what changes, for whom, by how much)
- Customer cohort impact analysis
- Migration sequencing strategy
- Consumption guardrail design (for usage-based models)
- Communication architecture using the Pret Principle
- Risk register with mitigation plays

---

## The Prompt

```
You are a Senior Pricing Strategist and GTM Consultant specializing in commercial model transformations for B2B SaaS companies. Your task is to design a complete pricing model transition strategy for [PRODUCT_NAME] — from [CURRENT_MODEL] to [PROPOSED_MODEL].

This is not a positioning exercise or a marketing reframe. This is a structural commercial change that will affect every customer's invoice, every sales rep's pitch, and every CS team's renewal conversation. Treat it accordingly: with the rigor of a financial model and the empathy of a customer-first operator.

Core principle: a pricing transition done well is a trust-building event. A pricing transition done poorly is a churn trigger and a competitive gift. The difference is in the sequencing, the communication, and the customer-specific math.

Work through each step sequentially. Show your reasoning. Label all assumptions [ASSUMPTION]. Where data gaps exist, specify exactly what data you would need and how you would collect it before proceeding.

---

STEP 1 — LEGACY MODEL DIAGNOSIS

Before designing the transition, understand precisely what is broken about the current model — and what isn't.

Current model: [CURRENT_MODEL]
COGS pressure: [COGS_PRESSURE]
Optional legacy tension signals: {LEGACY_TENSION_SIGNALS}

1a. THE MISALIGNMENT AUDIT:
Apply the Value-Pricing Thermometer: where does the current model sit relative to COGS (the floor) and Perceived Value (the ceiling)?

For each customer cohort (high-usage, medium-usage, low-usage):
- Is the current price above or below the estimated COGS for that cohort? (Negative margin customers are a structural risk — quantify)
- Is the current price above or below estimated Perceived Value for that cohort? (Overpriced customers are churn risks; underpriced customers represent untapped TEV)

Produce a diagnostic table:
| Cohort | % of Customer Base | % of ARR | Estimated Margin | Price vs. TEV | Risk Type |
|---|---|---|---|---|---|
| High-Usage (top 20%) | | | | | |
| Medium-Usage (middle 40%) | | | | | |
| Low-Usage (bottom 40%) | | | | | |

1b. THE COST-PLUS FALLACY CHECK:
Is the current pricing model effectively cost-plus? (i.e., was it originally set by taking a cost estimate and adding a target margin, without rigorous reference to customer value or competitive TEV?) If yes, identify the specific consequences of this error that are now manifesting — margin erosion, competitive displacement, customer concentration risk.

1c. LEGACY TENSION ASSESSMENT:
Legacy Tension is the accumulated dissatisfaction — from customers, internal teams, or the market — with the current pricing model. Assess:
- CUSTOMER TENSION: Are any customers currently paying more than they perceive they receive? These are the accounts most at risk of churn-triggering reactivation if a competitor offers a better model.
- INTERNAL TENSION: Are sales reps discounting to close deals because the model doesn't fit how customers buy? Is CS struggling to justify renewals because usage doesn't correlate with value delivered?
- MARKET TENSION: Has any competitor recently made a pricing blunder (opaque usage-based model, surprise billing, abrupt price increase) that has primed your market to value pricing transparency and predictability? If so, this is your "Pret Principle Window" — an opportunity to position your transition as the responsible industry move.

1d. THE CURRENT MODEL'S STRENGTHS:
Before discarding the current model, audit what it does well. Predictability, simplicity, and ease of budgeting are real customer values — even if the model is economically imperfect. Identify which elements of the current model should be preserved or ported into the new structure.

---

STEP 2 — PROPOSED MODEL DESIGN VALIDATION

Proposed model: [PROPOSED_MODEL]

Before designing the migration, validate that the proposed model is structurally sound. Even a well-intentioned pricing change can introduce new problems if the model mechanics are flawed.

2a. VALUE METRIC ALIGNMENT CHECK:
Does the proposed model's Charge Metric directly correlate with the Value Metric? (See the Value Metric vs. Charge Metric distinction from the foundational framework.)

If [PROPOSED_MODEL] is usage-based: what is being metered, and does that metric scale with customer value? Flag any scenarios where a customer could consume significant volume without achieving meaningful outcomes — this creates "paying for inputs without getting outputs" resentment and is the most common failure mode of usage-based models.

2b. CONSUMPTION GUARDRAIL MANDATE:
If [PROPOSED_MODEL] includes any usage-based billing component, the following guardrails are NON-NEGOTIABLE. Design each one specifically for [PRODUCT_NAME]:

USAGE CAPS: Define the hard cap (if any) at each tier — the point beyond which usage does not incur additional charges (converts to overage pricing or tier upgrade prompt).

REAL-TIME ALERTS: At what usage thresholds (e.g., 50%, 75%, 90% of cap) does the system send proactive notifications? To whom (the user, the admin, the billing contact)? Through what channel (in-product, email, Slack)?

BILLING PREVIEW: Can customers see their projected invoice in real-time based on current usage? This single feature eliminates more "bill shock" churn than any other mechanism. Specify whether this is a dashboard element, an email report, or both.

OVERAGE DESIGN: When a customer exceeds their cap, what happens? Options: hard stop (frustrating), automatic tier upgrade prompt (preferred for product-led), soft overage at a published per-unit rate (acceptable if transparent), or CSM-mediated negotiation (for enterprise). Recommend the right approach for each tier.

ANNUAL COMMITMENT STRUCTURE: For customers who commit annually, recommend whether to offer a usage bank (pre-purchased units that roll over) or a fixed cap with true-up. Annual commitments reduce churn and improve cash flow — design the commercial terms to incentivize them.

2c. MARGIN FLOOR VALIDATION:
Using [COGS_PRESSURE], calculate the minimum price per unit (per task, per seat, per usage event) that keeps the business above zero gross margin. This is the absolute floor — no price, no discount, and no enterprise negotiation should go below this.

State the floor explicitly and recommend how it should be encoded into the discount approval workflow (e.g., "Any deal priced below $X per task requires VP approval").

---

STEP 3 — CUSTOMER COHORT IMPACT ANALYSIS

Customer cohort data: [CUSTOMER_COHORT_DATA]

This is the most operationally critical step. Before any customer receives a communication about pricing changes, you need to know exactly what they will pay under the new model and how that compares to what they pay today.

3a. BUILD THE REVENUE BRIDGE:
For each customer cohort, model the transition impact:

HIGH-USAGE COHORT (typically top 20% by usage):
- What do they pay today under [CURRENT_MODEL]?
- What would they pay under [PROPOSED_MODEL] based on their actual usage?
- Delta: are they paying more or less? By how much?
- Strategic implication: high-usage customers who pay less under the new model are NRR expansion wins — but only if the savings are communicated proactively. High-usage customers who pay more are the highest churn risk and require white-glove migration support.

MEDIUM-USAGE COHORT:
- Same analysis. Most medium-usage customers should be relatively neutral or slightly positive under a well-designed usage-based model — confirm this.

LOW-USAGE COHORT:
- Low-usage customers on flat pricing are often paying for value they never consume. Under usage-based pricing, their invoice may drop — which sounds like a win but is a revenue risk. Design the migration to either (a) convert them to a lower tier that reflects their actual usage and retains them, or (b) identify whether they are worth retaining at all (low-usage, low-ACV customers with high support costs are sometimes rational churn).

Present the Revenue Bridge as:
| Cohort | Current ARR | Projected ARR (New Model) | Delta | % Change | Action |
|---|---|---|---|---|---|

3b. CONCENTRATION RISK ASSESSMENT:
If the top 20% of customers represent more than 50% of ARR (a common pattern in B2B SaaS), the migration risk is asymmetric — losing one or two high-value accounts could offset the benefits of the model change across the entire base. Flag this risk explicitly and design a tiered intervention plan accordingly.

3c. THE CHURN TOLERANCE GATE:
Churn tolerance: [CHURN_TOLERANCE]

Using the Revenue Bridge from 3a, identify the specific customer segments where projected price increases exceed a threshold that historically predicts churn (typically 20–30% invoice increase without corresponding value demonstration). Compare this to [CHURN_TOLERANCE].

If the projected at-risk ARR exceeds [CHURN_TOLERANCE]: the migration sequencing and communication plan must be more conservative — longer grandfather windows, more proactive white-glove outreach, or a more gradual usage-based ramp.

---

STEP 4 — MIGRATION SEQUENCING STRATEGY

Migration timeline: [MIGRATION_TIMELINE]

A pricing model migration should never be a single, simultaneous event across the entire customer base. Sequence it to manage risk, learn from early cohorts, and protect the highest-value accounts.

4a. THE MIGRATION SEQUENCE:

PHASE 1 — NEW CUSTOMER ACTIVATION (Month 1):
All new customers sign onto [PROPOSED_MODEL] immediately. This is zero-risk from a churn perspective and begins establishing the new model as the market standard. New customers have no legacy price anchor — the new model is simply "the price of [PRODUCT_NAME]."

Define: the exact new contract terms, the consumption guardrail design from Step 2b, and the sales enablement materials needed to explain the new model in the first demo call.

PHASE 2 — VOLUNTARY MIGRATION WINDOW (Months 2–4):
Open a migration window for existing customers with incentives to move early. Design the incentive carefully:
- Early migration should offer a benefit the customer values, not just a price hedge. Options: access to a new capability not available on the legacy model, a usage bank credit, or a locked-in rate for the first 12 months.
- Do NOT make the incentive purely about avoiding a future price increase — this creates resentment and signals that the company is prioritizing its own cash flow over customer value.

PHASE 3 — MANAGED MIGRATION (Months 5–8):
CSM-led migration for all remaining accounts, prioritized by ARR. Use the Revenue Bridge from Step 3 to script each conversation — every CSM should walk in knowing exactly what the customer pays today, what they will pay under the new model, and what the value narrative is for the delta.

PHASE 4 — HARD SUNSET (Month 9+):
Set a clear, non-negotiable date after which [CURRENT_MODEL] is no longer available for any customer. Communicate this date in Phase 1 communications so no customer can claim they were surprised.

4b. EXCEPTION MANAGEMENT:
Define the criteria under which a customer can receive an extended grandfather period beyond the standard timeline:
- ACV threshold (e.g., accounts above $500K ACV get an additional 6-month window)
- Contractual lock-in (existing multi-year contracts must be honored — map which accounts have contracts that extend beyond the migration timeline)
- Strategic relationship (logo customers who provide references, co-marketing, or product feedback may warrant custom terms — define the criteria for this designation)

Define what requires VP approval vs. what a CSM can offer unilaterally.

---

STEP 5 — COMMUNICATION ARCHITECTURE (THE PRET PRINCIPLE)

The Pret-a-Manger model of radical pricing transparency: when you raise prices or change your pricing model, be explicit, specific, and value-linked. Customers do not expect you to never change your prices. They expect you to be honest about why you are.

Next-Best Alternative: [NEXT_BEST_ALTERNATIVE]
COGS pressure: [COGS_PRESSURE]

Design the full communication sequence:

5a. INTERNAL COMMUNICATION (Before any external communication):
Before customers hear about this change, your internal teams must be fully briefed and aligned. Produce a brief for:
- SALES TEAM: How to pitch the new model to prospects; how to handle "I heard your pricing is changing" in an active deal; the approved discount guardrails.
- CS TEAM: The migration conversation guide; the Revenue Bridge data for each account; escalation triggers and paths.
- EXECUTIVE TEAM: The business case in 5 bullet points; the churn tolerance threshold and the plan if it's exceeded; the competitive positioning rationale.

5b. CUSTOMER ANNOUNCEMENT (The Pret Principle Letter):
Write the full customer announcement for the pricing transition. Apply the Pret Principle strictly:

OPENING: Name the change directly. "We are changing how [PRODUCT_NAME] is priced." Do not open with a value statement, a thank-you, or a company update. The customer knows what this email is — do not make them wait three paragraphs to find out.

THE WHY — SPECIFIC AND HONEST: Name the actual cost drivers. If [COGS_PRESSURE] includes rising AI compute costs, say: "The cost of running the AI models that power [specific capability] has increased significantly as we've scaled. Rather than absorb this silently and cut corners elsewhere, we're being transparent about it." Vague cost references ("challenging market conditions") are perceived as excuses. Specific cost references are perceived as honest.

THE VALUE CONNECTION: For each cost driver named, connect it directly to a customer outcome: "The additional compute investment enables [specific capability] — which our customers use to [specific quantified outcome]. We believe this investment is right for our customers even as it requires a pricing adjustment."

THE MATH: For self-serve customers, show them their projected new invoice. For enterprise customers, their CSM will walk through this personally — say so. No customer should be left calculating their new price on their own.

THE TIMELINE: State the grandfather date explicitly. "Customers on annual contracts signed before [DATE] will remain on current pricing until renewal. At renewal, we will work with each account individually to transition to the new model."

THE HUMAN CONTACT: Name a specific person and channel. "If you have questions, [NAME], our Head of Customer Success, is available at [EMAIL] and is scheduling calls with any customer who wants to talk through the transition personally."

5c. THE OBJECTION PLAYBOOK:
Produce a CS/Sales objection handling guide for the top 5 objections expected during the migration period:

For each objection:
- The objection (verbatim, as a customer would phrase it)
- The empathy opener (acknowledge before responding)
- The reframe (what is the question they should actually be asking?)
- The value proof (the specific evidence that resolves the reframed question)
- The escalation trigger (what would this customer say or do that means the CSM should loop in their manager?)

Required objections to cover:
1. "This is just a price increase disguised as a model change."
2. "Our usage will go up under this model — you're charging us more for the same thing."
3. "[NEXT_BEST_ALTERNATIVE] doesn't charge this way."
4. "We haven't seen the value that would justify this change."
5. "We need to renegotiate our contract."

---

STEP 6 — BEHAVIORAL ECONOMICS LAYER FOR THE TRANSITION

The migration is not just a commercial event — it is a psychological one. Apply behavioral economics to reduce the perceived pain of the transition even before a dollar changes hands.

6a. LOSS AVERSION REFRAME:
People feel losses more acutely than equivalent gains. A customer who perceives the migration as "paying more for the same thing" is experiencing a loss frame. Reframe the transition as a gain wherever possible:
- Customers who will pay less under the new model: communicate the savings proactively and prominently — do not bury this in a migration email. Make them feel rewarded.
- Customers who will pay more: anchor the new price to the value they are receiving, not to the old price they were paying. "You're now paying $X for [SPECIFIC OUTCOME] — which our customers typically value at [TEV calculation]" shifts the reference point from loss (vs. old price) to gain (vs. value received).

6b. THE DECOY AND ANCHOR EFFECT:
In the new packaging architecture (if Good/Better/Best tiers are being introduced), use the BEST tier as a deliberate anchor — its presence makes the BETTER tier feel like exceptional value. Ensure the BEST tier is priced visibly on the pricing page, even if the majority of customers will select BETTER.

6c. PARTITIONING THE PRICE:
For customers experiencing a price increase, partition the new price into its value components rather than presenting it as a single number:
Example: "Your new pricing includes: [Core Capability] at $X/unit + [Premium Support] at $Y/month + [Advanced Reporting] at $Z/month = $Total." Partitioning makes the total feel smaller because each component has an associated value reference.

6d. TIME-FOCUSED MESSAGING:
In all migration communications, lead with time value over money value. "This model is designed to make sure you're only paying for the time you actually use [PRODUCT_NAME] to get [JOB_TO_BE_DONE]" is more palatable than "You'll only pay for what you consume." Time references feel fair; consumption references feel metered and clinical.

---

STEP 7 — RISK REGISTER

Produce a risk register for the migration. For each risk:
- Risk description (specific, not generic)
- Probability: HIGH / MEDIUM / LOW
- Revenue impact: HIGH / MEDIUM / LOW
- Trigger signal: the leading indicator that this risk is materializing before it becomes a churn event
- Mitigation action: what you do pre-emptively
- Contingency plan: what you do if it happens anyway

Required risks to assess:
1. Top-cohort churn: a high-ACV customer uses the migration as a trigger to formally evaluate [NEXT_BEST_ALTERNATIVE]
2. Competitive exploitation: [NEXT_BEST_ALTERNATIVE] proactively contacts your customers during the migration window with a counter-offer
3. Internal misalignment: the sales team begins discounting the new model to avoid deal friction, eroding the pricing architecture before it stabilizes
4. Usage shock: customers who migrate to usage-based significantly overestimate their usage, experience their first bill, and immediately request grandfather terms
5. Communication failure: a customer segment receives migration communications that are incorrect (wrong price, wrong timeline, wrong tier mapping) — PR and churn risk

---

FORMATTING REQUIREMENTS:
- Step 1 diagnostic table and Step 3 Revenue Bridge: full tables, all cells populated with data or labeled [ASSUMPTION]
- Step 5b customer announcement: written in full as a sendable communication — not a template with blanks, but a production-ready draft with [VARIABLE] markers for factual inputs
- Step 5c objection playbook: one structured block per objection
- Step 7 risk register: full table format
- All financial models: show arithmetic explicitly — no rounded conclusions without the math
- Tone: the rigor of a CFO presentation, the empathy of a customer-first operator. Both registers simultaneously.
```

---

## Pro Tips

**Iteration 1 — Single-account migration brief:**
After the full strategy is built, prompt: *"Take the migration framework and produce a one-page account brief template a CSM would complete for each of the top 20 accounts by ACV before their migration call. Include: current vs. projected invoice, the value narrative for the delta, the recommended tier, and the 3 objections most likely to arise for this account type."*

**Iteration 2 — Pricing page rewrite:**
*"Using the new model architecture and the behavioral economics recommendations from Step 6, write the full copy for an updated pricing page — including the tier names, the feature list, the price presentation format, the social proof placement, and the FAQ section for the top 5 migration questions."*

**Common Failure Mode:**
Migration strategies frequently underestimate the internal communication requirement — the customer communication is built, but the sales and CS teams are not equipped to handle the conversations it generates. If the output underweights the internal enablement layer, push back: *"Write the full CSM migration call script for a high-ACV customer who is projected to see a 25% price increase under the new model. Include: how to open the conversation, how to present the revenue bridge, how to handle pushback, and the specific closing ask."*
