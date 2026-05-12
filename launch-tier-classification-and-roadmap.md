# Launch Tier Classification & 16-Week Roadmap

## Use Case
Classify an upcoming product release into the correct launch tier (T1/T2/T3), calibrate resource investment accordingly, and generate a phase-gated 16-week roadmap with DACI ownership, channel mix, and Balanced Scorecard metrics appropriate for that tier.

## When to Use
- At the start of any launch planning cycle, before resource allocation decisions are made
- When multiple releases are queued and the PMM team needs to triage investment across a portfolio
- When a launch is being over-resourced (treated as T1 when it's T2) or under-resourced (T1 scope, T3 budget)
- When a new PMM joins a team and needs to build a launch framework from scratch

## Required Inputs
- `[RELEASE_NAME]` — Name of the product, feature, or update being launched
- `[RELEASE_DESCRIPTION]` — 2–3 sentence description of what is changing and for whom
- `[TARGET_SEGMENT]` — Primary audience for this release
- `[BUSINESS_CONTEXT]` — Why this release exists (e.g., "Responds to competitive pressure from X," "Unlocks new segment Y," "Reduces churn driver Z")
- `[AVAILABLE_RESOURCES]` — Marketing headcount, estimated budget range, partner/agency support available
- `[DACI_TEAM]` — Names and functions available to support the launch
- `[LAUNCH_WINDOW]` — Target launch date or quarter

## Expected Output
- Tier classification with scoring rationale
- Resource calibration guidance per tier
- Full 16-week phase-gated roadmap
- DACI ownership table
- Balanced Scorecard with tier-appropriate metrics
- Go/No-Go gate criteria for each phase

---

## The Prompt

```
You are a seasoned Product Marketing Director who has overseen 30+ product launches across B2B SaaS companies at multiple growth stages. Your task is to classify the following release and produce a calibrated launch plan that matches resource investment to strategic impact.

Release: [RELEASE_NAME]
Description: [RELEASE_DESCRIPTION]
Target segment: [TARGET_SEGMENT]
Business context: [BUSINESS_CONTEXT]
Available resources: [AVAILABLE_RESOURCES]
DACI team: [DACI_TEAM]
Launch window: [LAUNCH_WINDOW]

A foundational principle of this work: most launches are over-complicated and under-resourced at the same time — too much process applied to a Tier 3 release, and too little strategic rigor applied to a Tier 1. The tier classification is the most consequential decision you will make. Get it wrong and every downstream decision is miscalibrated.

Work through each section sequentially. Show your scoring rationale in full — tier classification decisions are frequently contested in cross-functional planning, and your reasoning must be defensible to a CMO and CPO.

---

SECTION 1 — TIER CLASSIFICATION SCORING

Evaluate [RELEASE_NAME] against the following five dimensions. Score each dimension 1–3 (1 = low, 3 = high). The total score determines the tier.

DIMENSION 1 — MARKET IMPACT (1–3):
Does this release change the competitive dynamics of the category? Score 3 if it introduces a genuinely new capability that no competitor currently offers and that a target buyer would switch vendors to access. Score 1 if it closes a feature gap that peers already have.

DIMENSION 2 — SEGMENT EXPANSION (1–3):
Does this release unlock access to a meaningfully new customer segment, buyer persona, or use case? Score 3 if it enables entry into a segment the product was previously unable to serve. Score 1 if it serves the existing core segment with an incremental improvement.

DIMENSION 3 — REVENUE POTENTIAL (1–3):
What is the realistic incremental revenue impact in the 12 months following launch? Score 3 if this release is expected to be a primary driver of a significant new ARR cohort. Score 1 if it primarily protects existing revenue (churn reduction) or is a retention play.

DIMENSION 4 — STRATEGIC URGENCY (1–3):
How time-sensitive is this launch? Score 3 if a competitor has announced something similar and delay materially harms competitive positioning. Score 1 if the timing is internally driven and the market is not expecting this.

DIMENSION 5 — INTERNAL COMPLEXITY (1–3):
How many cross-functional teams must be coordinated to execute this launch? Score 3 if it requires deep alignment across Product, Sales, CS, Legal, and external partners simultaneously. Score 1 if it can be executed primarily within the marketing function.

SCORING RUBRIC:
- Total 12–15: TIER 1 — Game-changing. Maximum resource investment. CEO/CMO visibility. Full 16-week runway required.
- Total 8–11: TIER 2 — Significant. Focused investment with prioritized channels. 8–10 week timeline typically sufficient.
- Total 4–7: TIER 3 — Incremental. Lightweight execution. Release notes, internal comms, and a targeted email campaign may be sufficient.

Produce a scoring table with your scores per dimension, total score, tier classification, and a 2–3 sentence executive justification for the classification.

---

SECTION 2 — RESOURCE CALIBRATION BY TIER

Based on the tier classification, produce a resource calibration recommendation.

If TIER 1:
- Recommended marketing FTE allocation (dedicated vs. partial support)
- Budget range as % of annual marketing budget (provide a benchmark range)
- Channels that MUST be activated vs. channels that are optional for this tier
- Executive involvement requirements (e.g., CMO keynote, PR push, analyst briefings)
- Minimum runway before launch date (weeks of preparation required)

If TIER 2:
- Same structure as above, calibrated for a focused but not full-scale effort
- Which T1 activities can be reasonably cut for a T2 launch without materially harming outcomes?

If TIER 3:
- Minimum viable launch checklist: what must be done, and what is waste for this tier?
- Internal vs. external communication ratio: what proportion of effort goes inward (sales enablement, CS training) vs. outward (demand gen, PR)?
- Warning: flag any indicators in the release description that might suggest this is being classified too conservatively (i.e., a T1 release being treated as T3 because of resource constraints — this is a risk, not a solution)

---

SECTION 3 — 16-WEEK PHASE-GATED ROADMAP

Construct a 16-week roadmap calibrated to the classified tier. Each phase has an explicit go/no-go gate — a set of criteria that must be met before the team moves forward. Treat these gates as non-negotiable; a common failure mode is launching before internal readiness is achieved.

PHASE 1 — STRATEGIC FOUNDATION (Weeks 1–4)
Key activities:
- Launch tier confirmed and socialized with exec sponsor
- DACI ownership table finalized and signed off
- Positioning statement drafted and aligned with Product
- Target segment (Segment of One) defined with firmographic + behavioral criteria
- SMART objectives written and approved by Approver

Go/No-Go Gate 1 criteria (ALL must be true):
□ Positioning statement approved by CMO/VP Marketing
□ DACI ownership table signed off by all Contributors
□ SMART objectives approved and entered into reporting dashboard
□ Launch tier confirmed by exec sponsor

PHASE 2 — CONTENT AND ENABLEMENT BUILD (Weeks 5–9)
Key activities:
- Hero asset produced (e.g., product video, whitepaper, ROI calculator — specify for this tier/segment)
- Supporting content calendar built and briefed
- Sales battlecard and launch FAQ distributed to field
- Demo narrative updated to reflect new release
- Customer reference program: 2–3 referenceable customers confirmed for launch

Go/No-Go Gate 2 criteria:
□ Hero asset QA'd and approved
□ Sales team has received launch enablement session (live or recorded)
□ At least 2 customer references confirmed and briefed
□ Funnel audit (Leaky Pipe) completed — highest drop-off stage identified and fix-first plan confirmed

PHASE 3 — PRE-LAUNCH ACTIVATION (Weeks 10–12)
Key activities:
- Outbound prospecting sequences activated for target segment
- Paid media campaigns built and staged (not live — pending launch date)
- PR / analyst briefings executed under embargo
- Partner co-marketing confirmed and assets delivered
- Internal launch readiness review: all go/no-go criteria from Gates 1–2 verified

Go/No-Go Gate 3 criteria:
□ Paid campaigns approved and staged
□ PR outreach completed (confirm embargo lift date matches launch date)
□ Sales pipeline report showing target accounts engaged pre-launch
□ All launch assets live in internal content hub and accessible to field

PHASE 4 — LAUNCH WEEK (Week 13)
Key activities:
- Coordinated announcement: press release, email, social, exec blog post — same-day
- Sales activation: AE outreach to target accounts triggered on Day 1
- SDR sequences flipped to launch messaging
- Paid surge budget deployed
- Real-time monitoring: daily metric check against SMART objectives

PHASE 5 — POST-LAUNCH OPTIMIZATION (Weeks 14–16)
Key activities:
- 1-to-2 usage milestone report: identify activated users who have not returned; trigger re-engagement
- Win/loss debrief: first 20 launch-influenced deals reviewed
- Messaging refinement based on field and customer feedback
- Reporting: launch performance dashboard presented to INFORMED stakeholders
- Retrospective: what worked, what didn't, what changes to the launch playbook for next time

---

SECTION 4 — DACI OWNERSHIP TABLE

Using [DACI_TEAM], assign ownership for each phase and key deliverable. Produce a table with columns:
Phase | Deliverable | Driver | Approver | Contributors | Informed

Flag any gaps — roles in the DACI model that are unfilled given the available team. For each gap, recommend whether to (a) pull in an additional resource, (b) reassign an existing team member, or (c) descope the deliverable for this launch tier.

---

SECTION 5 — BALANCED SCORECARD

Define the measurement framework appropriate for the classified tier.

TIER 1 SCORECARD (Full suite):
- Sales: Pipeline generated ($), win rate in target segment (%), new ACV from launch cohort
- Marketing: Product Penetration Rate (% of target segment accounts activated), Feature Adoption Rate, 1-to-2 Usage Cycle (days)
- Product: Time-to-Value (days), Activation Funnel Completion Rate (%), Day-30 Retention (%)

TIER 2 SCORECARD (Focused):
- Reduce to the 3–4 metrics most predictive of success for this release type and segment
- Justify which T1 metrics have been deprioritized and why

TIER 3 SCORECARD (Lightweight):
- 2–3 metrics maximum: typically Feature Adoption Rate, internal enablement completion (sales team trained), and one customer-facing signal (NPS delta or support ticket reduction)

For the classified tier, produce:
- The specific metrics that will be tracked
- The target for each metric (tied to SMART objectives from Section 1)
- The data source and measurement cadence
- The "red flag" threshold that triggers a launch intervention or escalation

---

SECTION 6 — TIER CLASSIFICATION CHALLENGE PROTOCOL

Because tier classification is often contested, produce a brief "challenge protocol" document:

6a. What are the top 2–3 arguments a product manager or exec might make to UPGRADE this launch to a higher tier? (e.g., "This is actually category-defining because...")

6b. What are the top 2–3 arguments they might make to DOWNGRADE it? (e.g., "This is actually a T3 because the segment is too small to justify...")

6c. How would you adjudicate each argument? What additional data or criteria would you request before changing the classification?

This section exists because tier disagreements are a common source of cross-functional conflict. Surface the debate now rather than after budget decisions are made.

---

FORMATTING REQUIREMENTS:
- Section 1: scoring table + written justification
- Section 3: phase structure with explicit go/no-go gates formatted as checklists
- Section 4: DACI table with gap analysis
- Section 5: metrics table appropriate for classified tier
- All output should be immediately usable as a working document — no summaries or placeholders
```

---

## Pro Tips

**Iteration 1 — Portfolio prioritization:**
If running multiple launches simultaneously, prompt: *"Run the tier classification scoring for each of the following [N] releases: [LIST]. Produce a comparative scoring table and recommend how to sequence the launches and allocate shared resources across the portfolio."*

**Iteration 2 — Downgrade audit:**
*"We currently have this classified as [TIER]. Play devil's advocate: make the strongest possible case that this should be classified as [LOWER TIER] and that we are over-investing. What would we cut, and what is the risk of cutting it?"*

**Common Failure Mode:**
Teams frequently let organizational politics drive tier classification upward — every PM wants their release treated as T1. If the scoring produces T2 or T3 but stakeholders push back, use Section 6 directly: *"The product team is arguing this should be T1 because of [REASON]. Score their argument against the classification criteria and recommend how to respond."*
