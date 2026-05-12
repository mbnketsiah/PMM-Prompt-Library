# Big Bang Launch Plan

## Use Case
Generate a full end-to-end launch plan for a major product release — built on Big Bang Launch methodology — with SMART objectives, DACI ownership, a Leaky Pipe funnel audit, and a Balanced Scorecard. Designed to drive 25%+ penetration and 30%+ adoption within a defined target segment within 90 days.

## When to Use
- Tier 1 launches: game-changing product developments, major platform expansions, or category-creation moments
- Any launch where the goal is rapid penetration into a defined "Segment of One"
- When you need to build cross-functional alignment with a single artifact
- When leadership wants a launch plan that ties channel investments to measurable business outcomes

## Required Inputs
- `[PRODUCT_OR_FEATURE]` — What is being launched
- `[LAUNCH_DATE]` — Target GA date
- `[TARGET_SEGMENT]` — The "Segment of One" — the single, most strategically important segment for this launch
- `[SEGMENT_SIZE]` — Approximate number of addressable accounts or users in the target segment
- `[SMART_OBJECTIVE]` — Your hypothesis on the primary launch objective (the model will refine it)
- `[CORE_VALUE_CLAIM]` — The single most important thing the segment should believe after the launch
- `[DACI_TEAM]` — Names and roles for Driver, Approver, Contributor, Informed
- `[CURRENT_FUNNEL_DATA]` — Conversion rates at each stage, if available (Awareness → Trial → Adoption → Paid)
- `{COMPETITIVE_CONTEXT}` — Optional: key competitive dynamics that should shape launch timing or messaging

## Expected Output
- SMART objectives (refined)
- DACI ownership map
- Leaky Pipe funnel audit with fix-first prioritization
- 16-week integrated channel roadmap
- Balanced Scorecard metrics
- 1-to-2 usage cycle definition and measurement plan

---

## The Prompt

```
You are a Senior VP of Product Marketing architecting a Tier 1 product launch. Your task is to build a complete, execution-ready Big Bang Launch Plan for [PRODUCT_OR_FEATURE], targeting [TARGET_SEGMENT].

A Big Bang Launch is a high-velocity, integrated sprint designed to create a sharp awareness and adoption spike within a defined segment — not a slow ramp. Every decision in this plan should be optimized for speed-to-penetration, not broad awareness. Think surgical, not broadcast.

Work through each section in sequence. Do not skip the funnel audit — it is the most common source of launch failure and is non-negotiable.

---

SECTION 1 — LAUNCH CLASSIFICATION AND STRATEGIC FRAMING

1a. TIER CLASSIFICATION: Classify this launch using the standard three-tier framework:
- Tier 1: Game-changing development — new category, fundamental capability shift, or major competitive displacement
- Tier 2: Significant enhancement — meaningful new feature or persona expansion with moderate market impact
- Tier 3: Incremental improvement — quality-of-life update or minor feature addition

Based on [PRODUCT_OR_FEATURE] and [TARGET_SEGMENT], assign a tier and justify the classification in 2–3 sentences. The tier determines resource intensity, executive visibility, and channel investment for the plan that follows.

1b. STRATEGIC FRAMING: In 3–4 sentences, frame why this launch matters NOW. What is the market timing argument? What competitive window does this launch exploit or defend? What is the cost of a slow or poorly executed launch?

1c. SEGMENT OF ONE DEFINITION: Sharpen the target segment definition into a "Segment of One" — a description specific enough that a sales rep, demand gen manager, and content writer would all identify the same type of prospect from it.

Target segment: [TARGET_SEGMENT]
Segment size: [SEGMENT_SIZE]

Include: firmographic profile (company size, industry, tech stack indicators), behavioral profile (what they are actively doing that signals readiness to buy), and psychographic profile (what they care about, what they fear, and what success looks like for them personally).

---

SECTION 2 — SMART OBJECTIVES

Refine the following launch objective into a SMART format and expand into a full objective set.

Input objective: [SMART_OBJECTIVE]

Produce three layered SMART objectives for this launch:

PRIMARY OBJECTIVE (Penetration): "Achieve [X]% product penetration in [TARGET_SEGMENT] by Day [N] post-launch."
— Define penetration as: % of addressable accounts in the segment that have completed at least one meaningful product action (define the action).

SECONDARY OBJECTIVE (Adoption / Habituation): "Drive [X]% of penetrated accounts to the 1-to-2 usage milestone within [N] days of first use."
— The 1-to-2 usage milestone is defined as: a user who has completed a second meaningful usage event after their first, indicating the beginning of habituation.

TERTIARY OBJECTIVE (Revenue / Conversion): "Convert [X]% of active users in the segment to [paid/upgraded tier] within [N] days."

For each objective: state the metric, the measurement methodology, the data source, and the owner.

---

SECTION 3 — DACI OWNERSHIP MAP

Using the team provided, build a DACI ownership map for the full launch lifecycle. Assign roles with enough specificity that accountability is unambiguous at each phase.

Team: [DACI_TEAM]

DACI definitions for this context:
- DRIVER: The single person who owns the end-to-end launch execution. They make day-to-day decisions, unblock the team, and are accountable for the metrics.
- APPROVER: The executive who must sign off on positioning, messaging, launch gate criteria, and major investment decisions. One person only.
- CONTRIBUTORS: The functional leads who deliver specific workstreams (Product, Demand Gen, Content, Sales, CS). Each contributor owns a defined deliverable set.
- INFORMED: Stakeholders who need visibility but do not have decision rights (Legal, Finance, Exec team outside the Approver).

Produce a DACI table with columns: Phase | Decision / Deliverable | Driver | Approver | Contributors | Informed

Cover the following phases: (1) Pre-Launch Build (weeks 1–8), (2) Launch Week Execution, (3) Post-Launch Optimization (weeks 10–16).

---

SECTION 4 — THE LEAKY PIPE AUDIT (Non-Negotiable)

Current funnel data: [CURRENT_FUNNEL_DATA]

This is the most important section of the plan. Do not start optimizing top-of-funnel awareness until you have diagnosed and prioritized the leaks in the existing funnel. Adding water to a leaky pipe is waste.

4a. MAP THE FUNNEL: Plot the current conversion rates at each stage:
Awareness (Reached) → Consideration (Engaged) → Trial/Demo (Activated) → Adoption (Active User) → Conversion (Paid/Expanded)

For each stage transition, calculate the drop-off rate. If data is unavailable for any stage, flag the data gap as a risk and make an assumption with explicit reasoning.

4b. IDENTIFY THE BIGGEST LEAK: Which stage transition has the highest drop-off rate? This is your highest-priority fix — regardless of how tempting it is to build more top-of-funnel awareness.

4c. ROOT CAUSE HYPOTHESIS: For the biggest leak, generate 3 plausible root cause hypotheses. For each, identify the leading indicator you would monitor to confirm or refute it, and the fix you would test first.

4d. FIX-FIRST PRIORITIZATION: Before allocating any launch budget to new awareness channels, mandate a fix-first investment in closing the biggest leak. State specifically: what fix, what investment level (time/resource), and what improvement in conversion rate would constitute success within 30 days.

4e. SYNERGY EFFECT PLANNING: Once the biggest leak is addressed, identify the multi-channel mix that will create the highest integrated impact for this launch. For [TARGET_SEGMENT], which combination of channels creates the compounding effect — i.e., where exposure in Channel A materially increases conversion in Channel B?

---

SECTION 5 — 16-WEEK INTEGRATED CHANNEL ROADMAP

Build a week-by-week (condensed into phases) channel activation roadmap for the 16 weeks surrounding the [LAUNCH_DATE].

PHASE 1 — INTERNAL READINESS (Weeks 1–6, pre-launch):
- Sales enablement: battlecard, objection scripts, demo narrative, launch FAQ
- Internal alignment: launch brief distributed, DACI confirmed, success metrics socialized
- Content pipeline: hero asset produced, supporting content calendar confirmed
- Beta / customer reference program: which existing customers will be public advocates at launch?

PHASE 2 — PRE-LAUNCH DEMAND CREATION (Weeks 7–10):
- Outbound prospecting sequences activated for [TARGET_SEGMENT]
- Analyst/press briefings scheduled and executed
- Community seeding: where does [TARGET_SEGMENT] gather? Seed the conversation before the announcement.
- Partner co-marketing: any distribution leverage available?

PHASE 3 — LAUNCH WEEK (Weeks 11–12):
- Announcement sequence: press release, email blast, social posts, exec blog post — coordinated same-day release
- Event or virtual launch moment (if applicable)
- Sales activation: SDR sequences flipped to launch messaging, AE outreach to target accounts triggered
- Paid amplification: surge budget deployed for maximum signal density in the launch week

PHASE 4 — POST-LAUNCH OPTIMIZATION (Weeks 13–16):
- 1-to-2 usage milestone monitoring: identify users who activated but have not returned; trigger re-engagement sequence
- Win/loss cadence established: debrief on first 20 deals influenced by launch messaging
- Messaging refinement: update positioning and proof points based on first-month feedback
- Reporting: weekly dashboard sent to INFORMED stakeholders with actuals vs. SMART objectives

For each phase, specify: channels activated, owner (from DACI), key deliverable, and go/no-go gate criteria before moving to the next phase.

---

SECTION 6 — BALANCED SCORECARD

Define the measurement framework across three dimensions. Replace any broad brand metrics with launch-specific leading indicators.

SALES METRICS (Commercial outcomes):
- Metric 1: Pipeline influenced by launch in [TARGET_SEGMENT] ($) — target and timeframe
- Metric 2: Win rate for deals where launch messaging was used vs. baseline — target improvement
- Metric 3: ACV of first cohort of accounts acquired through launch

MARKETING METRICS (Activation and penetration):
- Metric 1: Product Penetration Rate — % of target segment accounts that have activated the product within 60 days
- Metric 2: Feature Adoption Rate — % of activated accounts using the core differentiating capability within 30 days
- Metric 3: 1-to-2 Usage Cycle — median time from first to second meaningful usage event (target: under 7 days)

PRODUCT METRICS (Time-to-Value):
- Metric 1: Time-to-Value (TTV) — time from sign-up to first meaningful outcome (target: under 7 days)
- Metric 2: Activation Funnel Completion Rate — % of new users who complete the defined activation sequence
- Metric 3: Retention at Day 30 — % of activated users still active at the 30-day mark

For each metric: define the measurement methodology, data source, reporting cadence, and threshold for a launch "red flag" that triggers an intervention.

---

SECTION 7 — RISK REGISTER

Identify the top 5 risks to launch success and for each:
- Risk description (specific, not generic)
- Probability: HIGH / MEDIUM / LOW
- Impact: HIGH / MEDIUM / LOW
- Pre-mortem: If this launch fails, which of these risks is most likely to be the cause?
- Mitigation action: what do you do before launch to reduce the probability?
- Contingency plan: what do you do if it happens anyway?

---

FORMATTING REQUIREMENTS:
- Section 3 DACI: structured table
- Section 4 funnel: data visualized as a stage-by-stage conversion waterfall in text format
- Section 5 roadmap: phase-by-phase table with columns — Phase | Channel | Owner | Key Deliverable | Gate Criteria
- Section 6 scorecard: three-section table, one per dimension
- Section 7 risk register: table format
- Total output: this should be long enough to be a real working document — do not abbreviate for the sake of brevity
```

---

## Pro Tips

**Iteration 1 — Sales play extraction:**
*"Based on the launch plan, write a sales play for the launch week — a specific sequence of touchpoints an AE should execute in the 10 business days following launch announcement to activate the top 25 target accounts. Include messaging guidance and talk tracks."*

**Iteration 2 — Executive summary:**
*"Write a one-page executive summary of this launch plan for a CMO and CFO who have 5 minutes. Lead with the business case, the SMART objectives, and the top 3 risks. No channel detail."*

**Common Failure Mode:**
Launch plans without a Leaky Pipe audit consistently over-invest in awareness and under-invest in conversion. If the model skips the audit or treats it as secondary, force it back: *"Do not proceed to the channel roadmap until you have identified the single highest-drop-off funnel stage and specified the fix-first investment that addresses it."*
