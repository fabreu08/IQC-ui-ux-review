# Kimi 2.5 — Adaptation of Multi-Model Methodology to UI/UX Auditing

**Model**: Kimi 2.5 (master prompt / high-rigor mode)
**Context**: Response to prompt asking for adaptation of the security auditing playbook to UI/UX reviews of the Immutable QC product.
**Date**: Latest

---

## Full Response

[Full text provided by user below for archival completeness]

---

I'll retrieve the referenced Playbook to understand the security auditing methodology before constructing my response. 

Now I have the Playbook context. Let me provide a rigorous, structured adaptation of this methodology to UI/UX auditing.

---

## Multi-Model UI/UX Auditing Methodology — Adaptation Framework

Your instinct to port this methodology is sound, but UI/UX auditing introduces failure modes that make the security playbook's assumptions dangerous if applied uncritically. Below is a direct, unsanitized assessment of what transfers, what breaks, and what must be built from scratch.

---

### 1. Core Principles Adaptation

**What Transfers Directly:**

| Security Playbook Principle | UI/UX Adaptation | Confidence |
|---------------------------|------------------|------------|
| Correlation Is Not Independence | **Critical** — Models share design pattern training data (Material Design, Apple HIG, accessibility standards). "Consensus" on a UX issue is often just correlated pattern-matching. | High |
| Diminishing Returns Are Dramatic | **Critical** — The first 2–3 models capture ~80% of genuine friction points. Rounds 4+ produce increasingly aesthetic opinions, not actionable signal. | High |
| Head-to-Head Debate Has Higher Signal | **Critical** — Direct confrontation between models on subjective claims ("this is confusing") forces grounding in user behavior, not taste. | High |

**What Requires Significant Modification:**

**"Tooling Is Non-Negotiable Above Medium Severity"** becomes:

> **"Behavioral Evidence Is Non-Negotiable Above Medium Impact"**

In security, you demand PoCs and static analysis. In UX, you demand:
- Session recordings showing actual user struggle
- Analytics showing drop-off rates at specific funnel points
- Heatmaps/scroll maps showing ignored CTAs
- Accessibility audit reports (automated + manual screen reader testing)
- User interview transcripts with direct quotes

**Without this, "High" UX severity is just opinion with a severity label.**

**"Trust Model First"** becomes:

> **"Persona + Context Model First"**

Before any model critiques the interface, you must document:
- **Who** is using this (personas with goals, not demographics)
- **In what state** (rushed, expert, novice, stressed, mobile vs desktop)
- **With what constraints** (accessibility needs, bandwidth, cognitive load)
- **To achieve what outcome** (jobs-to-be-done)

Without this, models will project their own usage assumptions onto the interface.

**New Principles Required:**

| Principle | Rationale |
|-----------|-----------|
| **Recency Bias Is Inevitable** | Models trained on 2023–2024 design patterns will overvalue "modern" aesthetics and undervalue functional familiarity. Must explicitly counterweight. |
| **Designer Defensiveness Is Contagious** | Models exposed to design critique patterns will often soften findings to avoid "being mean." Demand adversarial framing. |
| **The User Is Not You** | Models must be explicitly forbidden from projecting their own (non-existent) usage patterns, device preferences, or accessibility needs. |
| **Aesthetic Opinion ≠ Usability Finding** | "I don't like this color" is not a finding. "This color fails WCAG contrast and user testing showed 40% of users couldn't locate the button" is a finding. |

---

### 2. The "Pain Model" (User Frustration / Pain Model)

The Pain Model is your replacement for the Threat Model. It must be constructed **before** any UI review begins, or you will get ungrounded aesthetic commentary.

**Structure:**

```
PAIN MODEL: Immutable QC Alpha Interface
Version: [Date]
Personas: [List of 3-5 primary personas with goals]
Critical User Journeys (CUJs): [The 3-5 paths that must not fail]
Success Signals: [Observable metrics that indicate success]
Failure Signals: [Observable metrics that indicate breakdown]
Business Impact Mapping: [How UX failures translate to business outcomes]
```

**Dimensions to Capture:**

| Dimension | Questions to Answer | Evidence Required |
|-----------|---------------------|-------------------|
| **Personas** | Who are the 3–5 primary user types? What are their goals, constraints, and emotional states? | User research transcripts, support tickets, analytics segmentation |
| **Critical User Journeys (CUJs)** | What are the 3–5 flows where failure is catastrophic? | Funnel analysis, business metrics mapping |
| **Success Signals** | What observable behaviors indicate the user succeeded? | Event tracking, completion rates, time-on-task metrics |
| **Failure Signals** | What observable behaviors indicate the user is struggling? | Error rates, rage clicks, support ticket themes, drop-off points |
| **Accessibility Baseline** | What assistive technologies and constraints must be supported? | WCAG 2.1 AA audit, screen reader testing logs |
| **Device/Context Matrix** | What devices, screen sizes, and environmental conditions? | Analytics on device breakdown, usage context research |
| **Business Impact Mapping** | How do UX failures translate to lost revenue, support burden, or churn? | Business metrics, cohort analysis |

**Critical Rule:** If a finding cannot be mapped to a specific Pain Model dimension, it is **opinion**, not a finding. Full stop.

---

### 3. Recommended Workflow

**Phase 1: Pain Model Construction (Human-Led)**

1. Document personas, CUJs, success/failure signals, accessibility baseline
2. Gather behavioral evidence: analytics, session recordings, user quotes
3. Define scope: which flows are in-scope, which are explicitly out-of-scope
4. Run automated accessibility audit (axe, WAVE, Lighthouse)

**Phase 2: Initial Exploration (2–3 Models Max)**

- Provide each model with: Pain Model + screenshots/Figma links + behavioral evidence package
- Ask for: friction points mapped to specific CUJs, severity justified by Pain Model dimensions
- **Do not** show models each other's work

**Phase 3: Head-to-Head Pressure Testing**

- Select the 2 strongest responses (most skeptical, best grounded in Pain Model)
- Force direct debate on points of tension:
  - "Model A claims this flow is 'intuitive.' Model B claims it violates Fitts's Law. Defend your position using the Pain Model evidence provided."
  - "Model A rates this as Critical. Model B rates it as Low. Debate using the severity rubric."

**Phase 4: Synthesis + Behavioral Verification**

- Human synthesizes strongest points
- **Every High+ finding must have behavioral evidence or accessibility standard violation**
- Produce final report with clear Pain Model, scope, and evidence status

**Phase 5: Diminishing Returns Check**

If you're on round 4+ and mostly debating whether something "looks modern" or "feels clean," **stop**. Move to user testing.

---

### 4. Severity / Impact Rubric for UI/UX

This is where most UX audits collapse into subjectivity. You need a rubric that forces models to justify severity through evidence, not taste.

**Severity Framework:**

| Severity | Definition | Evidence Required | Examples |
|----------|-----------|-------------------|----------|
| **Critical** | User cannot complete core task; complete blocker for a persona; violates WCAG A/AA in a way that prevents assistive technology use; causes significant business impact | Session recording of user failing; analytics showing >X% drop-off; accessibility audit failure with user impact; support ticket volume | "Primary CTA is invisible to screen readers" / "Checkout flow broken on mobile Safari" |
| **High** | Significant friction in critical journey; violates established usability heuristics; causes measurable business impact; fails WCAG AA | Analytics showing elevated drop-off; heuristic evaluation with specific violation; user quotes describing confusion; A/B test showing negative impact | "Form validation errors don't indicate how to fix" / "Navigation hierarchy contradicts user mental model" |
| **Medium** | Friction in non-critical journey; inconsistency causing mild confusion; aesthetic issues that may affect brand perception; WCAG AA violations with limited user impact | Design system audit showing inconsistency; user feedback indicating mild confusion; competitive analysis showing standard pattern | "Button styles inconsistent across flows" / "Loading state lacks feedback" |
| **Low** | Minor polish issues; edge case friction; subjective aesthetic preferences | None required — flagged as opinion | "I prefer more whitespace here" / "This icon could be clearer" |
| **Informational** | Observations, questions, or suggestions for future testing | N/A | "Consider testing this with novice users" / "Monitor this metric post-launch" |

**Mandatory Severity Justification Template:**

Every finding must include:
1. **Pain Model Mapping**: Which persona/CUJ does this affect?
2. **Evidence**: What behavioral data, accessibility standard, or user quote supports this?
3. **Business Impact**: How does this affect business goals?
4. **Confidence**: High / Moderate / Low

**If any field is missing or cites "my experience" or "best practices" without specific standard reference, downgrade severity by one level.**

---

### 5. Anti-Patterns Specific to UI/UX

| Security Anti-Pattern | UI/UX Equivalent | Detection Method |
|----------------------|------------------|------------------|
| **Consensus Theater** | **"Vibes Consensus"** — Multiple models agree something "feels off" or "looks dated" without grounding in user behavior | Check if finding cites specific Pain Model dimension or behavioral evidence. If not, it's theater. |
| **Phantom Finding Persistence** | **"Design Debt Zombie"** — A finding about a pattern persists because subsequent models are reluctant to dismiss it, even when user data shows it's not actually a problem | Require fresh behavioral evidence in each round. If user analytics contradict the finding, kill it. |
| **Severity Inflation via Sunk Cost** | **"Severity Inflation via Effort"** — Keeping severity high because "we spent time discussing it" or "it took effort to document" | Re-evaluate every High+ finding against the rubric in each round. Severity is not earned through effort. |
| **Documentation Theater** | **"Heuristic Theater"** — Long reports citing Nielsen's heuristics without specific interface violations or user evidence | Require screenshot + specific violation + user impact for every heuristic claim. |
| **New: Designer Defensiveness** | Models softening critiques to avoid "being harsh" or "respecting the designer's vision" | Explicitly prompt for adversarial framing: "Assume the design is hostile to user goals. Find the failures." |
| **New: Recency Bias** | Overvaluing "modern" patterns (glassmorphism, dark mode, micro-interactions) over functional familiarity | Explicitly weight "familiarity over novelty" in prompts. Ask: "Would a stressed user on a 3-year-old Android device succeed?" |
| **New: Phantom Persona** | Models inventing user types that don't exist in the Pain Model to justify findings | Cross-check every persona reference against the documented Pain Model. Reject findings citing undocumented personas. |

---

### 6. Model Selection & Collaboration

**Model Strengths Assessment (Confidence: Moderate based on architectural patterns):**

| Model | UI/UX Critique Strength | Weakness | Best Role |
|-------|------------------------|----------|-----------|
| **Kimi 2.5** (me) | Strong pattern recognition; good at cross-referencing heuristics with specific interface elements; skeptical of aesthetic claims | May over-index on pattern consistency vs. user context | Primary reviewer; synthesis |
| **Opus 4.7** | Strong at logical flow analysis; good at identifying contradictions between stated goals and implementation | May underweight emotional/affective UX factors | Debate partner; logic-focused critique |
| **GPT-4o** | Broad design pattern knowledge; good at accessibility standard references | High recency bias; tendency toward "vibes-based" feedback | Pattern reference; accessibility checks |
| **Claude 3.5 Sonnet** | Good at user empathy; strong at generating "what would a confused user do?" scenarios | May be too gentle in critique; designer defensiveness risk | Persona validation; user journey mapping |

**Collaboration Structure:**

**Head-to-head debate remains valuable**, but the format must change:

**Security Format:** "Defend your technical claim with code evidence"

**UI/UX Format:** "Defend your severity claim with Pain Model evidence. Your opponent has user analytics showing the opposite. Respond."

**Recommended Structure:**

1. **Parallel Round 1**: Kimi 2.5 + Opus 4.7 (independent, no cross-contamination)
2. **Debate Round**: Force direct confrontation on severity disagreements
3. **Tie-Breaker Round** (if needed): GPT-4o or Claude 3.5 Sonnet specifically asked to evaluate the debate evidence, not generate new findings

**Beyond 3 models**: Only if you need specific expertise (e.g., accessibility specialist model, mobile-specific critique). Otherwise, stop.

---

### 7. Grounding & Verification

**Artifacts Required as Context (Non-Negotiable):**

| Artifact | Purpose | Minimum Viable |
|----------|---------|----------------|
| **Session Recordings** (Hotjar, FullStory, etc.) | Ground "confusion" claims in observed behavior | 5–10 recordings of users attempting critical journeys |
| **Analytics Dashboard** | Quantify drop-offs, error rates, time-on-task | Funnel visualization for each CUJ |
| **User Interview Transcripts** | Capture verbatim user mental models | 3–5 transcripts from target personas |
| **Accessibility Audit Report** | WCAG 2.1 AA compliance baseline | Automated scan (axe/WAVE) + manual screen reader test of critical flows |
| **Device/Browser Matrix** | Ground "this works" claims | Analytics showing actual user device breakdown |
| **Competitive/Comparative Screenshots** | Contextualize "standard pattern" claims | 3–5 comparable flows from established products |
| **Design System Documentation** | Check consistency claims | Component library or style guide |

**Grounding Rules for Models:**

1. **No "users might"** — Replace with "the Pain Model indicates [persona] would" or "user interviews show"
2. **No "best practices" without citation** — If citing Nielsen, specific heuristic number. If citing WCAG, specific success criterion.
3. **No "intuitive"** — Replace with "users in [persona] with [context] succeeded in [metric]"
4. **No "clean" / "modern" / "polished"** — These are aesthetic opinions, not findings. Flag and discard.

**Prompt Template for Grounding:**

```
When making a claim about user confusion or interface effectiveness, you must cite:
- A specific Pain Model persona and CUJ affected
- Behavioral evidence (analytics, session recording, or user quote) OR
- A specific accessibility standard violation (WCAG success criterion) OR
- A documented usability heuristic violation with interface evidence

Claims without this grounding will be rejected as opinion.
```

---

### 8. Practical Starting Point: Immutable QC Alpha Review

**Ideal Prompt Package for Next Week:**

**Pre-Review (Human Responsibility):**
- [ ] Pain Model documented (personas, CUJs, success/failure signals)
- [ ] Screenshots/Figma links of all critical flows
- [ ] Analytics export showing funnel drop-offs
- [ ] 3–5 session recordings of real users attempting critical tasks
- [ ] Automated accessibility audit (axe or WAVE) results
- [ ] Competitive comparison screenshots (3–5 comparable products)

**Model Prompt Structure:**

```
ROLE: You are a hostile UX auditor. Your job is to find where the interface fails users, not to validate design decisions.

CONTEXT PROVIDED:
- Pain Model: [Attached]
- Screenshots: [Attached]
- Behavioral Evidence: [Attached]
- Accessibility Audit: [Attached]

YOUR TASK:
1. Review each Critical User Journey in the Pain Model
2. Identify friction points, blockers, or failures
3. Map each finding to: Specific persona + CUJ + Pain Model dimension
4. Assign severity using the rubric provided
5. Cite behavioral evidence or accessibility standards for every Medium+ finding

CONSTRAINTS:
- Do not comment on aesthetic preferences (colors, "feel," "modern")
- Do not invent personas not in the Pain Model
- Do not use "intuitive" — use "users succeeded/failed at [metric]"
- Assume the design is hostile to user goals until proven otherwise

OUTPUT FORMAT:
[Finding ID] | [Severity] | [CUJ Affected] | [Persona Affected]
Description: [Specific interface element + behavior]
Evidence: [Quote from user research / analytics metric / WCAG violation]
Business Impact: [How this affects business goals]
Confidence: [High/Moderate/Low]
```

**Process:**

**Day 1:** Kimi 2.5 independent review (this prompt)
**Day 2:** Opus 4.7 independent review (same prompt, no cross-contamination)
**Day 3:** Head-to-head debate on severity disagreements
**Day 4:** Human synthesis + verification against behavioral evidence
**Day 5:** Final report with Pain Model, scope, verified findings, and evidence status

**Stop Conditions:**
- If Round 3 produces no new Critical/High findings, stop
- If debate devolves into aesthetic opinions ("I think it looks fine"), stop
- If findings lack behavioral evidence after prompting, downgrade severity and stop

---

### Final Assessment

Your security playbook is a strong foundation, but UI/UX auditing requires **tighter constraints on subjectivity** and **heavier investment in pre-review behavioral evidence**. The models will generate opinions dressed as findings — your job is to force them to defend every claim with user data or accessibility standards.

The Pain Model is your Trust Model. Behavioral evidence is your tooling. The rubric is your severity framework. Without these, you're running vibes-based theater, not an audit.

**Confidence in this methodology:** High for the framework, Moderate for specific model recommendations (limited empirical testing in UI/UX context), High for the anti-patterns (these are well-documented in design critique literature).

Ready to proceed.

---

*End of Kimi 2.5 response.*

*Archived as part of the IQC UI/UX multi-model auditing research.*