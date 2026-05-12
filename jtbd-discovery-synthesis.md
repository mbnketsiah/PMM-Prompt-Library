# JTBD Discovery Synthesis

## Use Case
Synthesize qualitative customer research — interviews, win/loss calls, NPS verbatims, support tickets, sales call recordings — into a rigorous Jobs-to-be-Done framework. Output a JTBD map, persona refinements, and a product/messaging recommendation set grounded in behavioral evidence rather than stated preferences.

## When to Use
- After a batch of customer discovery or win/loss interviews
- When building or validating a new ICP definition
- Before a messaging refresh or positioning project
- When churn or adoption data doesn't match your product's stated value prop

## Required Inputs
- `[PRODUCT_NAME]` — Your product
- `[RESEARCH_INPUT]` — Paste or summarize your raw research: interview transcripts, key quotes, win/loss themes, NPS verbatims, support ticket patterns, or sales call notes
- `[TARGET_SEGMENT]` — The customer segment this research represents
- `[RESEARCH_VOLUME]` — How many customers/calls/data points does this synthesize? (Helps calibrate confidence levels)
- `{PRIOR_PERSONA_DEFINITION}` — Optional: existing ICP or persona documentation to pressure-test

## Expected Output
- Jobs Map (Functional / Emotional / Social jobs by customer type)
- Behavioral insight synthesis (what customers do vs. what they say)
- JTBD-aligned product/messaging recommendations
- Confidence-scored findings
- Ethnographic observation notes (flags where stated preferences likely diverge from actual behavior)

---

## The Prompt

```
You are a customer insights strategist and qualitative researcher. Your task is to synthesize the following research data using the Jobs-to-be-Done framework, and produce a structured insight report that directly informs product roadmap priorities and marketing positioning decisions.

Product: [PRODUCT_NAME]
Target segment represented in this research: [TARGET_SEGMENT]
Research volume: [RESEARCH_VOLUME]
Optional existing persona: {PRIOR_PERSONA_DEFINITION}

Research input (quotes, themes, call notes, tickets, verbatims):
[RESEARCH_INPUT]

A core operating principle for this analysis: BEHAVIOR OVER ATTITUDE. What customers say they want is frequently different from what they actually do. Weight behavioral evidence — usage patterns, switching behavior, workaround adoption, and churn triggers — more heavily than stated preferences or survey responses. When these diverge, flag the divergence explicitly.

Work through each step in sequence. Apply "eyes of innocence" — approach this data as if seeing this customer's world for the first time, without the bias of your product's existing framing.

---

STEP 1 — RAW SIGNAL CLASSIFICATION

Before interpreting the research, classify the raw inputs.

1a. Separate the inputs into three buckets:
- BEHAVIORAL EVIDENCE: Things customers were observed doing, or reported doing, in the context of getting a job done (usage patterns, workarounds, switching events, help-seeking behaviors)
- ATTITUDINAL DATA: Things customers said they think, feel, prefer, or want (satisfaction scores, feature requests, stated priorities)
- OUTCOME DATA: Measurable results customers achieved or failed to achieve while using [PRODUCT_NAME] or alternatives

1b. For any attitudinal data that contradicts the behavioral evidence, flag it explicitly as a "stated vs. revealed preference divergence." These divergences are often the most strategically valuable signals in qualitative research — they indicate where your messaging may be landing differently than intended, or where customers have rationalized a behavior post-hoc.

1c. Rate the overall research quality: given [RESEARCH_VOLUME] data points, what is the appropriate confidence level for the insights that follow? Flag any significant gaps in the research sample (e.g., no churned customers represented, all inputs from a single industry vertical, no input from the economic buyer persona).

---

STEP 2 — JOBS-TO-BE-DONE MAP

Apply the JTBD framework to synthesize the behavioral and attitudinal evidence into a structured jobs map.

For [TARGET_SEGMENT], identify and map the jobs at three levels:

FUNCTIONAL JOBS (the practical task):
What specific task or workflow is the customer trying to complete when they "hire" a product like [PRODUCT_NAME]? Functional jobs are verb-forward and outcome-oriented. Example: "Consolidate competitive intelligence from multiple sources into a shareable briefing document before a sales call."

List 3–5 functional jobs, ranked by frequency of evidence in the research data.

EMOTIONAL JOBS (the feeling they're seeking):
What emotional state does successfully completing the functional job create or protect? What anxiety or discomfort does it eliminate? Emotional jobs explain why customers feel strongly about solutions that technically do the same thing as competitors.

List 2–3 emotional jobs with direct evidence from the research.

SOCIAL JOBS (the signal they send):
How does using [PRODUCT_NAME] — or the outcome it produces — affect how the customer is perceived by their peers, manager, or organization? Social jobs explain why certain features become "must-haves" even when they don't improve functional performance (e.g., the ability to share a well-formatted output that looks credible in a leadership meeting).

List 1–2 social jobs with evidence.

For each job at each level:
- State the job in the customer's own language where possible (use direct quotes from the research)
- Identify the "success criteria" — what does the customer use as evidence that the job was done well?
- Identify the "failure mode" — what would have to happen for the customer to feel the job was done badly?
- Identify the "switch trigger" — what specific experience or event leads a customer to start evaluating alternatives or workarounds?

---

STEP 3 — ETHNOGRAPHIC OBSERVATION LAYER

Apply an ethnographic lens: look for patterns in how customers actually apply [PRODUCT_NAME] in their daily lives that your product team may not have anticipated.

3a. UNINTENDED USE CASES: Are there jobs customers are using [PRODUCT_NAME] to do that were not part of the original product vision? These represent either (a) expansion opportunities the roadmap should pursue, or (b) misuse patterns that are creating support burden or churn.

3b. WORKAROUND PATTERNS: Where are customers using [PRODUCT_NAME] plus something else (a spreadsheet, a Slack channel, a manual process) to complete a job that the product should theoretically handle alone? Each workaround is a product gap signal — but it's also a messaging signal (the product is being positioned as doing something it doesn't fully deliver).

3c. "BRIGHT SPOT" BEHAVIOR: Which customers are getting the most value from [PRODUCT_NAME]? What do they do differently in the first 14 days of use that predicts long-term retention? These behaviors are your onboarding and activation targets.

3d. LANGUAGE AUDIT: How do customers describe the problem [PRODUCT_NAME] solves — in their own words, not yours? Extract 3–5 verbatim phrases or vocabulary patterns from the research. These are the words your messaging should adopt, not your product team's internal terminology.

---

STEP 4 — STATED VS. REVEALED PREFERENCE ANALYSIS

This is the highest-value section of the analysis. For each major divergence identified in Step 1b, apply full analytical treatment.

For each divergence:
4a. State what customers SAY they want (attitudinal preference).
4b. State what the behavioral evidence shows they actually DO (revealed preference).
4c. Formulate a hypothesis that explains the gap. Is this a rationalization? A social desirability bias? A genuine unarticulated need? A feature they think they want but would never use?
4d. State the strategic implication: does this change (a) the product roadmap priority, (b) the messaging and positioning, (c) the sales discovery approach, or (d) the success metric definition?

---

STEP 5 — PERSONA PRESSURE TEST

Compare the findings from Steps 2–4 against the existing persona definition (if provided):

{PRIOR_PERSONA_DEFINITION}

5a. What does this research CONFIRM about the existing persona definition? State the evidence.

5b. What does this research CHALLENGE or CONTRADICT? For each challenge, assess: is this a signal that the persona needs to be updated, or is it noise from an outlier cohort?

5c. What does this research REVEAL that was ABSENT from the prior persona? New pain points, unaddressed jobs, unexpected decision-making triggers, or demographic/behavioral characteristics the existing persona missed?

5d. Produce a "delta report": a concise summary of the specific updates you recommend making to the persona definition, with evidence cited for each change.

If no prior persona is provided, produce a first-draft persona definition grounded entirely in the research evidence.

---

STEP 6 — ACTIONABLE RECOMMENDATIONS

Synthesize the JTBD analysis into a prioritized recommendation set across three workstreams.

PRODUCT RECOMMENDATIONS:
For each identified job gap or unintended use case, produce:
- Recommendation: what capability or experience change would address this job more completely?
- Evidence basis: which specific research signals support this recommendation?
- Confidence level: HIGH / MEDIUM / LOW, based on the volume and quality of supporting evidence
- Priority rationale: why this, why now?

MESSAGING RECOMMENDATIONS:
For each language pattern and JTBD insight, produce:
- What messaging change is indicated? (specific claim to add, modify, or remove)
- Which channel or touchpoint should be updated first?
- The JTBD-aligned framing: "When [CUSTOMER TYPE] is [FUNCTIONAL JOB], they need to feel [EMOTIONAL JOB] and be seen as [SOCIAL JOB]. Our current messaging addresses __ of these three levels. Here is the gap."

SALES DISCOVERY RECOMMENDATIONS:
For each switch trigger and stated vs. revealed preference divergence, produce:
- A discovery question that would surface this trigger in a live sales conversation
- The probe follow-up that gets below the surface-level stated preference to the real job
- The signal to listen for that indicates this is a high-fit prospect vs. a wrong-fit evaluation

---

FORMATTING REQUIREMENTS:
- Step 2 Jobs Map: three-section structure (Functional / Emotional / Social), each job as a labeled block
- Step 4: one structured analysis block per divergence
- Step 6: three clearly labeled sections with individual recommendation blocks
- Confidence levels: stated explicitly for every major finding (HIGH = 3+ independent data points; MEDIUM = 2 data points; LOW = 1 data point or inference)
- Verbatim customer language: use quotes wherever available — label them with source type (e.g., "Win call," "NPS verbatim," "Support ticket")
```

---

## Pro Tips

**Iteration 1 — Build an interview guide:**
*"Based on the research gaps identified in Step 1c, write a 10-question discovery interview guide designed to fill those gaps. Structure it so the first 5 minutes build rapport and surface the functional job, and the next 20 minutes probe the emotional and social layers and the stated vs. revealed preference divergences."*

**Iteration 2 — Activation sequence design:**
*"Based on the 'Bright Spot' behaviors identified in Step 3c, design a 14-day new user activation sequence that steers new users toward those behaviors. Specify the trigger, the message, the channel, and the desired action for each touchpoint."*

**Common Failure Mode:**
JTBD analysis frequently stays at the functional level because emotional and social jobs are harder to surface from notes and transcripts. If Step 2 produces only functional jobs, push back: *"For each functional job you identified, ask: 'What would the customer feel — specifically — if they failed to complete this job?' The answer is the emotional job. Now find the evidence for it in the research."*
