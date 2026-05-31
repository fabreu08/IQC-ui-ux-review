# Prompt for Kimi 2.5 — Adapting Multi-Model Auditing to UI/UX

You are operating in your highest-rigor, most skeptical, and methodologically precise mode.

## Context

Over the past months, we developed a structured multi-model approach to security auditing (documented in the "Multi-Model LLM Security Auditing Playbook" — link below). This process involved multiple rounds of reviews, head-to-head debates (especially between you and Opus 4.7), synthesis documents, and heavy emphasis on avoiding common failure modes such as:

- Consensus theater
- Phantom findings
- Severity inflation
- Lack of grounding / verification
- Diminishing returns from additional models

The full playbook is here:  
https://github.com/fabreu08/IQC-token-research/blob/main/research/Multi-Model-LLM-Security-Auditing-Playbook.md

We also developed a rigorous Trust Model process as a prerequisite for any credible analysis.

## The New Challenge

We now want to adapt this same disciplined, multi-model methodology to **UI/UX auditing** of the current Immutable QC product (alpha.immutableqc.com and related interfaces).

UI/UX review has different characteristics than smart contract security auditing:
- Much higher subjectivity
- Strong dependence on user personas and context
- Different "ground truth" (user testing, analytics, behavioral data, accessibility standards, etc.)
- Different failure modes (vibes-based feedback, recency bias, designer defensiveness, etc.)

## Your Task

Please provide a high-signal, structured response on how to best adapt the multi-model auditing methodology for UI/UX work.

Please address the following areas directly:

### 1. Core Principles Adaptation
Which principles from the security playbook transfer well to UI/UX?  
Which ones need significant modification or replacement?  
What new principles would you add specifically for design and user experience reviews?

### 2. The "Pain Model" (equivalent of Threat Model)
How should we structure a "User Frustration / Pain Model" for a product like Immutable QC?  
What are the key dimensions we should capture (personas, critical journeys, success/failure signals, business impact, etc.)?

### 3. Recommended Workflow
Propose a practical workflow for running multi-model UI/UX reviews, drawing from what worked (and what didn't) in the security process.  
Include thoughts on:
- Number of models and when to stop
- Role of head-to-head debates in a design context
- How to incorporate real user data / research / prototypes
- Synthesis approach

### 4. Severity / Impact Rubric for UI/UX
Design a clear, usable severity framework for UI/UX issues that reduces subjectivity while remaining practical.  
How should we distinguish between "I don't like this design" vs. "This is actively harmful to the user experience or business goals"?

### 5. Anti-Patterns Specific to UI/UX
What forms do "consensus theater," "phantom findings," and "severity inflation" take when reviewing interfaces and user flows?

### 6. Model Selection & Collaboration
Which models (including yourself) tend to be strongest at UI/UX critique?  
Would a head-to-head format between two strong models still be valuable here, or does UI/UX benefit from a different collaboration structure?

### 7. Grounding & Verification
How do we force models to ground their feedback in evidence rather than taste?  
What kinds of artifacts (user quotes, session recordings, analytics, prototypes, accessibility reports, etc.) should be provided as context?

### 8. Practical Starting Point
If we wanted to run a first serious multi-model UI/UX review of the current alpha.immutableqc.com experience next week, what would the ideal prompt package and process look like?

---

Please be direct, structured, and as ruthless as you were in the previous Trust Model and contract reviews. We are not looking for validation — we are looking for the next level of methodological clarity.

You can reference the full playbook and previous documents in the research repo as needed.

Ready when you are.