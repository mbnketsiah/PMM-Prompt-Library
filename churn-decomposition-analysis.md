# Churn Decomposition Analysis

## Use Case
Apply the Three Ds of Churn framework (Distribution, Decomposition, Decile) and Multiplicative Profit Decomposition to diagnose the true drivers of revenue attrition — moving beyond blunt churn rate metrics to identify the specific customer cohorts, behavioral patterns, and product/market misalignments causing preventable loss.

## When to Use
- When churn rate is above benchmark and root cause analysis is inconclusive
- Before investing in a retention campaign or CS intervention program
- During annual planning when renewal forecasting requires churn assumption inputs
- When NRR is underperforming despite healthy new business acquisition

## Required Inputs
- `[PRODUCT_NAME]` — Product or tier being analyzed
- `[CHURN_DATA]` — Summarized churn data: rate by cohort, segment, tenure, plan tier, and/or usage level (paste data or a summary)
- `[ACTIVE_CUSTOMER_COUNT]` — Current active customer count
- `[AOF]` — Average Order Frequency: how often the average customer transacts or renews in a 12-month period
- `[AOV]` — Average Order Value: average ACV or transaction value
- `[TOP_CHURN_REASONS]` — Top 3–5 stated churn reasons from exit surveys or CS offboarding notes
- `[USAGE_DATA_SUMMARY]` — What usage patterns are visible for churned vs. retained cohorts (e.g., "churned customers averaged 1.2 logins/month vs. 8.4 for retained")
- `{ONE_TO_TWO_CYCLE_DATA}` — Optional: time distribution between a customer's first and second meaningful usage event

## Expected Output
- Multiplicative Profit Decomposition model
- Distribution analysis (churn variability mapping)
- Decomposition analysis (churn by component: segment, cohort, plan, usage tier)
- Decile analysis (identification of the "Vital Few" — the top churn contributors driving disproportionate revenue loss)
- 1-to-2 Purchase/Usage Cycle analysis
- Prioritized retention intervention recommendations

---

## The Prompt

```
You are a customer analytics strategist and retention expert. Your task is to conduct a rigorous churn decomposition analysis for [PRODUCT_NAME] using the Three Ds of Churn framework, and produce a prioritized diagnosis and intervention plan.

Inputs:
- Churn data: [CHURN_DATA]
- Active customer count: [ACTIVE_CUSTOMER_COUNT]
- Average Order Frequency (AOF): [AOF]
- Average Order Value (AOV): [AOV]
- Top churn reasons (stated): [TOP_CHURN_REASONS]
- Usage data summary: [USAGE_DATA_SUMMARY]
- 1-to-2 cycle data (optional): {ONE_TO_TWO_CYCLE_DATA}

A core operating principle: the stated reason for churn is almost never the complete picture. "Too expensive" is often a rationalization for insufficient perceived value. "Not using it enough" describes a symptom, not a cause. Your analysis must get below stated reasons to behavioral and structural drivers.

Work through each step in sequence. Where data is incomplete, make explicit assumptions and flag them as hypotheses to validate.

---

STEP 1 — MULTIPLICATIVE PROFIT DECOMPOSITION

Before diagnosing churn, establish the revenue baseline using the multiplicative decomposition model.

The model: Total Revenue = Active Customers × Average Order Frequency (AOF) × Average Order Value (AOV)

1a. Calculate the current revenue baseline:
- Active Customers: [ACTIVE_CUSTOMER_COUNT]
- AOF: [AOF]
- AOV: [AOV]
- Baseline Revenue = Active Customers × AOF × AOV

1b. Calculate the revenue impact of the current churn rate:
- Using the churn data provided, calculate: Revenue at Risk = Active Customers × Churn Rate × AOV
- Express this as both an absolute dollar figure and as a percentage of baseline revenue

1c. Sensitivity analysis — which lever has the highest revenue impact?
Run three scenarios by improving each variable by 10% independently (holding the others constant):
- Scenario A: Active Customer Count +10% (net new acquisition)
- Scenario B: AOF +10% (frequency/expansion)
- Scenario C: Churn Rate reduced by 10% (retention)

Which scenario produces the highest marginal revenue gain? This determines where retention investment competes against acquisition and expansion investment on a pure ROI basis.

1d. State the strategic implication: at what churn rate does the business achieve a breakeven point where acquisition spend is no longer able to offset attrition? This is the "leaking bucket threshold."

---

STEP 2 — DISTRIBUTION ANALYSIS (The First D)

Distribution analysis asks: is churn uniformly distributed across the customer base, or is it concentrated in specific cohorts or profiles?

2a. Using the churn data provided, map the distribution of churn across the available dimensions:
- By cohort (acquisition quarter or year): is newer or older cohort churn higher?
- By segment (company size, industry, or use case): which customer profile churns most?
- By plan or pricing tier: is churn higher at a specific price point?
- By tenure: at what point in the customer lifecycle does churn peak? (Month 1–3? Month 6–12? At renewal?)

2b. Plot the distribution findings on a conceptual scale: LOW VARIANCE (churn is evenly distributed — a systemic product or market fit problem) vs. HIGH VARIANCE (churn is concentrated in specific cohorts — an addressable targeting or onboarding problem).

2c. State the diagnostic implication: what does the distribution pattern suggest about the nature of the churn problem? A systemic problem requires a different intervention than a cohort-specific one.

---

STEP 3 — DECOMPOSITION ANALYSIS (The Second D)

Decomposition analysis asks: what are the component parts of the overall churn rate, and how does each contribute?

3a. Break the overall churn rate into its component streams:
- VOLUNTARY CHURN: Customer actively chose to leave (identify the primary triggers from [TOP_CHURN_REASONS])
- INVOLUNTARY CHURN: Payment failures, expired cards, billing errors (estimate as % of total churn if data available)
- PRODUCT-LED CHURN: Churn driven by adoption gaps — customers who never reached meaningful value before their renewal date
- COMPETITIVE DISPLACEMENT: Churn driven by switching to an identified competitor

3b. For each churn component, estimate the proportion of total churn it represents. Flag any components where the data is insufficient to estimate (these are data infrastructure gaps to fix).

3c. Prioritize by impact: which component is the highest-yield target for intervention? Consider both the volume of churn it drives AND the feasibility of addressing it with available resources.

3d. Stated vs. Revealed Churn Reason Analysis:
Map each stated churn reason from [TOP_CHURN_REASONS] to a likely root behavioral driver:
- "Too expensive" → likely: insufficient perceived value (value was not demonstrated convincingly before renewal), OR: budget reallocation due to macro pressure (external, less addressable)
- "Not using it enough" → likely: activation failure (product gap or onboarding gap), OR: wrong-fit customer (ICP misalignment)
- "Missing feature X" → likely: competitive displacement risk, OR: genuine product gap for this use case
- "Poor support experience" → likely: CS capacity or process failure, addressable

For each stated reason in your data, produce: Stated Reason | Likely Root Driver | Behavioral Evidence | Addressability (HIGH/MED/LOW)

---

STEP 4 — DECILE ANALYSIS (The Third D)

Decile analysis asks: which customers are responsible for the disproportionate share of churn revenue? The Vital Few often drive 60–80% of revenue at risk despite being a minority of churning accounts.

4a. Segment churned customers into deciles by ACV (or AOV × AOF). Identify the top decile — the highest-value churned accounts.

4b. Profile the top decile: what characteristics do these highest-value churned accounts share that differentiate them from the lower-value churned accounts?
- Company size, industry, use case, acquisition channel, onboarding path, usage pattern before churn
- Time to churn from acquisition: did they churn faster or slower than average?
- Last meaningful usage event: how long before churning did they disengage from the product?

4c. The Vital Few Intervention: Given the revenue concentration in the top decile, propose a Vital Few intervention strategy — a dedicated, high-touch retention play targeted specifically at the next cohort of accounts that match this high-value churn profile, before they reach the churn decision point.

4d. Early Warning Indicator Identification: Based on the pre-churn behavioral patterns of the top decile, define 2–3 leading indicators that a currently active high-value account is entering the churn risk window. These become the triggers for proactive CS intervention.

---

STEP 5 — 1-TO-2 USAGE CYCLE ANALYSIS

The 1-to-2 cycle is the most predictive leading indicator of long-term retention. A customer who completes a second meaningful usage event within a defined window after their first is significantly more likely to habituate and renew.

Usage cycle data: {ONE_TO_TWO_CYCLE_DATA}

5a. Define the "meaningful usage event" for [PRODUCT_NAME]: what specific product action, if completed, represents genuine value realization rather than passive browsing? (If not defined, propose a definition based on the product description and usage data provided.)

5b. Analyze the 1-to-2 cycle distribution:
- What % of new customers complete the second meaningful usage event within 7 days?
- Within 14 days? Within 30 days?
- What is the correlation between 1-to-2 cycle completion time and 90-day retention rate?

5c. Identify the "activation cliff": is there a specific time window after which a customer who has not completed the 1-to-2 cycle is unlikely to retain? This is your intervention deadline — the last moment a proactive nudge can prevent churn.

5d. Design a 1-to-2 acceleration intervention: a targeted onboarding or re-engagement sequence designed to pull customers across the 1-to-2 threshold before the activation cliff.
- Trigger: what event or time-based condition launches the sequence?
- Channel: in-product notification, email, CSM outreach, or combination?
- Message: what proof of value or prompt would most effectively motivate a second usage event for this customer profile?
- Success metric: what improvement in 1-to-2 completion rate within 30 days constitutes a successful intervention?

---

STEP 6 — RETENTION INTERVENTION PRIORITY MATRIX

Synthesize all findings into a prioritized intervention plan.

For each identified churn driver (from Steps 2–5), produce:
- Intervention name and description
- Target cohort: which specific customer profile does this address?
- Expected revenue impact: estimated ARR saved if this intervention is successful
- Effort level: HIGH / MEDIUM / LOW (engineering, CS, and marketing resources required)
- Time-to-deploy: weeks until this intervention is live
- Confidence level: HIGH / MEDIUM / LOW (based on evidence quality)

Present as a priority matrix table, sorted by Expected Revenue Impact × Confidence Level.

Additionally, recommend the SINGLE highest-priority intervention — the one action the team should start on in the next two weeks — with a clear rationale for why this represents the best use of scarce retention resources.

---

STEP 7 — DATA INFRASTRUCTURE GAPS

Flag any critical data gaps that prevented full analysis and recommend the instrumentation or process changes needed to close them within 90 days.

For each gap:
- What data is missing?
- Why does it matter for churn analysis?
- How should it be captured going forward (product instrumentation, CS offboarding survey, CRM field)?
- Priority: what would this data unlock that isn't possible today?

---

FORMATTING REQUIREMENTS:
- Step 1: show all calculations explicitly, even if working from estimates
- Step 3d: structured table per stated churn reason
- Step 4: decile analysis structured as a profile block for the top decile
- Step 6: priority matrix table, sorted by impact × confidence
- Assumption flags: every assumption should be labeled [ASSUMPTION: X] inline so they are easy to identify and validate
- Total output: this is an internal analytical document — optimize for rigor and specificity, not readability for non-analysts
```

---

## Pro Tips

**Iteration 1 — Build the early warning dashboard:**
*"Using the Vital Few early warning indicators from Step 4d, write a specification for a customer health score dashboard. Define the metrics, weights, thresholds for RED/YELLOW/GREEN status, and the CSM action trigger for each status level."*

**Iteration 2 — Executive retention narrative:**
*"Summarize the churn decomposition findings in a 5-slide executive narrative structure: (1) Revenue at risk, (2) Where the churn is coming from, (3) The Vital Few, (4) The top 3 interventions, (5) What we're doing next week. Write the talking points for each slide."*

**Common Failure Mode:**
Churn analyses frequently produce a list of interventions without prioritization discipline, leading to scattered effort and no measurable impact. If Step 6 produces more than 5 interventions without a clear #1, push back: *"Force rank these interventions using a strict revenue impact × confidence level sort. If the top intervention requires more than 8 weeks to deploy, flag it and identify the fastest-to-deploy intervention that would show measurable impact within 30 days."*
