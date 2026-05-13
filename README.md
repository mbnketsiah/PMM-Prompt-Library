**PMM-Prompt-Library**

Open-Source AI Prompt Frameworks for Senior Product Marketers
Project Description

The PMM-Prompt-Library is a curated, open-source collection of production-grade AI prompts engineered specifically for senior product marketing managers. Every prompt is grounded in established marketing theory — the Three Cs Model, Jobs-to-be-Done, the Benefit Ladder, Big Bang Launch methodology, and more — and structured using Chain-of-Thought (CoT) reasoning to produce strategic outputs, not generic content.

This is not a “ChatGPT tips” repo. This is a practitioner’s toolkit built for marketers operating at the intersection of strategy, data, and execution.

Why This Exists

Most AI prompt libraries are built for generalists. They produce fluffy outputs that sound smart but require complete rewrites before they’re usable in a boardroom, a sales kickoff, or a product launch.

Senior PMMs need prompts that:

Force structured reasoning — not just a list of ideas, but a defensible strategic framework
Embed domain theory — positioning science, competitive response modeling, JTBD, launch tiering
Produce board-ready outputs — messaging tables, battlecards, DACI ownership maps, research synthesis
Save 6–10 hours per deliverable — not 20 minutes on a blog post
This library is the result of distilling real PMM workflows — competitive audits, launch plans, sales enablement kits, and customer research programs — into repeatable, AI-executable frameworks.

Table of Contents

Project Description
Why This Exists
Folder Structure
How to Use
Prompt Index
Competitive Intelligence
Messaging & Positioning
Launch Planning
Customer Research
Sales Enablement
Contributing
License
Folder Structure

PMM-Prompt-Library/
│
├── README.md
│
├── competitive-intel/
│   ├── three-cs-competitive-audit.md
│   └── substitute-threat-analysis.md
│
├── messaging/
│   ├── positioning-statement-generator.md
│   └── benefit-ladder-messaging-table.md
│
├── launch-plans/
│   ├── big-bang-launch-plan.md
│   └── launch-tier-classification-and-roadmap.md
│
├── customer-research/
│   ├── jtbd-discovery-synthesis.md
│   └── churn-decomposition-analysis.md
│
└── sales-enablement/
    ├── competitive-battlecard.md
    └── show-the-shift-pitch-deck-brief.md
├── pricing/
│   ├── pricing-architecture-and-tev-analysis.md
│   └── pricing-model-transition-strategy.md
 
How to Use

Each prompt file contains:

Context Block — What you need to provide before running the prompt (your product, segment, data)
The Prompt — A long-form, Chain-of-Thought structured prompt ready to paste into Claude, GPT-4, or Gemini
Expected Output — A description of the deliverable the prompt produces
Pro Tips — Iteration instructions and common failure modes to avoid
Quickstart

Navigate to the folder matching your current workstream (e.g., /launch-plans)
Open the relevant .md file
Copy the prompt from the Markdown code block
Fill in the [BRACKETED VARIABLES] with your actual inputs
Paste into your preferred LLM
Iterate using the Pro Tips section
Variable Convention

All required inputs are marked with [BRACKETS]. Optional context enhancements are marked with {CURLY BRACES}.

[REQUIRED_INPUT]       → Must be filled in before running
{OPTIONAL_CONTEXT}     → Improves output quality but not required
 
Prompt Index

Competitive Intelligence

File	Use Case	Key Frameworks
three-cs-competitive-audit.md	Full competitive landscape analysis	Three Cs Model, POP/POD, Resource Equivalence
substitute-threat-analysis.md	Identify non-obvious threats to market share	Substitute Analysis, JTBD, Factor Market Signals
Messaging & Positioning

File	Use Case	Key Frameworks
positioning-statement-generator.md	Generate a brand positioning statement with RTB	Brand Positioning Statement format, Benefit Ladder
benefit-ladder-messaging-table.md	Build a full messaging architecture by persona	Messaging Hierarchy, POP/POD, Proof Point Rigor
Launch Planning

File	Use Case	Key Frameworks
big-bang-launch-plan.md	End-to-end launch plan for a major release	Big Bang Launch, SMART Objectives, Leaky Pipe Audit
launch-tier-classification-and-roadmap.md	Tier a release and build a 16-week roadmap	Launch Tiering (T1/T2/T3), DACI, Balanced Scorecard
Customer Research

File	Use Case	Key Frameworks
jtbd-discovery-synthesis.md	Synthesize qualitative research through a JTBD lens	Jobs-to-be-Done, Ethnographic Empathy, Behavior vs. Attitude
churn-decomposition-analysis.md	Diagnose churn drivers and prioritize retention levers	3 Ds of Churn, Multiplicative Profit Decomposition, 1-to-2 Purchase Cycle
Sales Enablement

File	Use Case	Key Frameworks
competitive-battlecard.md	Build a kill-sheet-grade battlecard for sales	Win/Loss Hypothesis, Commercial Velocity, Brand Consistency
show-the-shift-pitch-deck-brief.md	Write a pitch deck narrative brief that converts	Show the Shift Framework, Decision Latency, Benefit Ladder
Contributing

Pull requests are welcome. To contribute a new prompt:

Fork the repo
Create a branch: git checkout -b prompt/your-prompt-name
Follow the prompt file template (see any existing file for structure)
Submit a PR with a one-paragraph description of the use case and frameworks referenced
Please ensure all prompts are tested against at least one major LLM before submission.

License

MIT License. Use freely, attribution appreciated.

Built for PMMs who operate at the senior level. If you find this useful, star the repo and share it with your marketing org.
