# Prompt for GPT-5.3 Codex — Adapting Multi-Model Auditing to UI/UX

You are operating at maximum rigor, skepticism, and methodological precision.

## Context

Over the past several months, we developed a structured multi-model methodology for security auditing of smart contracts (documented in the "Multi-Model LLM Security Auditing Playbook").

The full playbook is available here:  
https://github.com/fabreu08/IQC-token-research/blob/main/research/Multi-Model-LLM-Security-Auditing-Playbook.md

We are now exploring how to adapt this same disciplined approach to **UI/UX auditing** of the current Immutable QC product (alpha.immutableqc.com and related interfaces).

This is not a casual "give me some UX feedback" request. We want to port the core philosophy, anti-pattern avoidance, and process discipline from security auditing into the much more subjective domain of interface and experience design.

## Your Task

Provide a high-signal, structured response on how to best adapt the multi-model auditing methodology for UI/UX work.

Address the following areas directly and rigorously:

### 1. Core Principles Adaptation
- Which principles from the security playbook transfer cleanly to UI/UX?
- Which principles break or become dangerous if applied without modification?
- What new principles must be introduced specifically for design and user experience reviews?

### 2. The "Pain Model" (Threat Model Equivalent)
Define what a proper "User Pain / Frustration Model" should contain for a product like Immutable QC.
- What dimensions are most important?
- How should it be constructed before any model review begins?
- How does it prevent models from giving ungrounded aesthetic or opinion-based feedback?

### 3. Recommended Workflow
Propose a practical, repeatable workflow for running multi-model UI/UX reviews, modeled on the security process but adapted for subjectivity and human-centered data.
Include thoughts on:
- Optimal number of models and when to stop
- Role and format of head-to-head debates in a UI/UX context
- How and when to incorporate real user research, analytics, session recordings, and prototypes
- Synthesis and final output standards

### 4. Severity / Impact Rubric
Design a clear, defensible severity framework for UI/UX issues that minimizes subjectivity while remaining practical for product decisions.
- How do we distinguish between taste, preference, and actual usability or business impact?
- What evidence thresholds should be required for High and Critical ratings?

### 5. Anti-Patterns Specific to UI/UX
Identify the UI/UX-specific versions of the anti-patterns we saw in security reviews (Consensus Theater, Phantom Findings, Severity Inflation, etc.).
- What new failure modes are likely to appear in interface and experience reviews?

### 6. Model Selection & Collaboration Strategy
- Which current frontier models (including yourself) tend to be strongest or weakest at grounded UI/UX critique?
- Is a head-to-head debate format still the highest-leverage collaboration method, or is a different structure better for design work?
- What specific instructions or constraints should be given to models to counteract common biases (recency bias, designer defensiveness, projection of their own "user" experience, etc.)?

### 7. Grounding & Verification Standards
- What artifacts and data must be provided as context before models are allowed to critique?
- What strict rules should be enforced to prevent models from generating ungrounded opinions?
- How do we force models to tie every Medium+ claim to specific behavioral evidence or established standards (heuristics, accessibility, etc.)?

### 8. Practical Execution Plan
If we wanted to run the first serious multi-model UI/UX review of the current alpha.immutableqc.com experience in the next 1–2 weeks, what would the ideal prompt package, process, and stop conditions look like?

---

## Output Instructions

Respond in a clear, structured, high-signal format. Use sections and tables where they increase clarity.

Be direct and unsentimental. We are not looking for encouragement or high-level platitudes. We want the same level of methodological rigor and pressure-testing you applied during the Trust Model and contract reviews.

If something from the security playbook does not translate well, say so explicitly and explain why, along with what should replace it.

You may reference the full Playbook linked above for context.

---

Ready when you are. Provide your most rigorous analysis.