# UI/UX Multi-Model Auditing Playbook v0.1

**Title**: Adversarial UX Review — Merged Methodology  
**Version**: 0.1 (Post Kimi vs Codex Debate)  
**Date**: 2026-05-31  
**Status**: Ready for first execution on alpha.immutableqc.com (subject to Gemini 3.1 Pro review)  
**Source**: Synthesized from Kimi 2.5 round-1, GPT-5.3 Codex round-1, and Kimi's full unilateral debate response (Codex as sparring partner).

---

## Core Thesis

UI/UX auditing with frontier LLMs is epistemically fragile. Models trained on overlapping design corpora will correlate on "modern," "clean," or "intuitive" patterns even when those patterns fail real users. 

The only defense is **radical grounding + adversarial pressure + strict evidence gates**, not more models or prettier reports.

This playbook adapts the hard lessons from the IQC token security audit (Trust Model first, diminishing returns, head-to-head debate, anti-theater discipline) into the much more subjective domain of user experience.

---

## 1. Foundational Principles (Non-Negotiable)

1. **Pain Model First** — No model review begins until a versioned Pain Model exists and is attached.
2. **Behavioral Evidence Non-Negotiable Above Medium** — Opinion dressed as "High" is the dominant failure mode.
3. **Causal-Chain + Disconfirming Evidence Discipline** — Every Medium+ claim must articulate a mechanism and what would falsify it.
4. **Capability Differentiation Over Model Count** — Three similar frontier models are often worse than two differentiated ones + structured debate.
5. **Diminishing Returns Are Real** — Stop when new rounds produce mostly aesthetic churn or ungrounded hypotheses.
6. **Verification Before Prioritization** — No High/Critical finding is accepted without evidence that can be reproduced from existing data.
7. **Epistemic Humility by Design** — The process must force models (and humans) to name where they are most likely to be wrong.

---

## 2. Pain Model (Prerequisite Artifact)

**Required Structure** (frozen before any model is invoked):

- **Personas** (3–5 primary, with goals, constraints, emotional states, device/context)
- **Critical User Journeys (CUJs)** (3–5 flows where failure is business-catastrophic)
- **Success Signals** (observable, measurable behaviors that indicate completion)
- **Failure Signals** (rage clicks, backtracks, drop-offs, support themes, error rates)
- **Business Impact Mapping** (how each failure translates to activation, conversion, retention, support cost, or risk)
- **Accessibility Baseline** (WCAG 2.1 AA results + manual screen reader notes on critical flows)
- **Device / Context Matrix** (actual traffic breakdown + known constraints)

**Rule**: Any finding that cannot be mapped to a specific dimension in the current Pain Model is opinion and is rejected.

---

## 3. Claim Card Schema (Atomic Output Unit)

Every model output and every debated issue must use this structure:

| Field                        | Requirement                                      | Notes |
|-----------------------------|--------------------------------------------------|-------|
| Claim ID                    | Unique                                           | - |
| Journey / CUJ               | From Pain Model                                  | - |
| Segment + Context + State   | Specific                                         | e.g. "Novice on mobile Safari, first session, low bandwidth" |
| Symptom                     | What the user experiences                        | - |
| Mechanism                   | Why the interface produces this experience       | Causal chain |
| Observed / Hypothesized Behavior | -                                           | - |
| Evidence Refs               | Specific & reproducible                          | Query params, timestamps, transcript excerpts, replay IDs |
| Disconfirming Evidence      | What would falsify this claim                    | Required for Medium+ |
| Severity                    | Per rubric below                                 | - |
| Confidence                  | High / Moderate / Low                            | - |
| Pain Model Mapping          | Exact dimension(s)                               | Required for Medium+ |
| User Harm + Business Harm   | One sentence each                                | - |
| Verification Status         | Verified / Hypothesis / Needs Targeted Test      | - |
| Redesign Proposal Quarantine| Optional, auto-downgrades if present             | See Guardrails |

---

## 4. Severity Rubric (Merged)

**Critical**
- Irreversible harm (data loss, compliance violation, accessibility catastrophe that blocks assistive technology on a core path)
- Immediate product or legal risk
- Evidence: Strong multi-source + no viable workaround

**High**
- Critical journey + repeated failure + (business impact OR user quotes OR session recording of struggle)
- Evidence threshold: At least one strong behavioral signal from existing data

**Medium**
- Secondary journey or recoverable friction with measurable inefficiency
- Evidence: Analytics support or consistent user feedback

**Low**
- Cosmetic, inconsistency, or preference issues
- Can be heuristic-only

**Informational**
- Observations and questions for future research

**Hard Rule**: No High or Critical without at least one piece of behavioral evidence from the current evidence pack. If new research is required, the item is "Hypothesis — Defer to Post-Launch Test" and is excluded from the prioritized backlog.

---

## 5. Recommended Workflow (Minimum Viable 5-Day Track)

**Phase 0: Setup (Day 0–1)**
- Human locks scope to 3–5 critical journeys.
- Produces Pain Model v0.1 + evidence pack (analytics last 30 days, 8–12 session recordings, accessibility baseline, user quotes).
- Freezes both artifacts.

**Phase 1: Blind Model Review (Days 2–3)**
- Three models with explicit capability differentiation (strongly recommended):
  - Claude 3.5 Sonnet or equivalent: Spatial / layout / information architecture analysis
  - Kimi 2.5 or equivalent: Adversarial / hostile-user simulation
  - GPT-4o / Gemini 2.5 Pro or equivalent: Heuristic + pattern violation detection
- All receive identical Pain Model + evidence pack + screenshots.
- Output strictly in Claim Card format.
- System prompt includes: "Assume the design is hostile to user goals until proven otherwise." + banned aesthetic language list + mandatory disconfirming evidence field.

**Phase 2: Claim Normalization + Arbitration (Day 4)**
- Human (or lightweight script) deduplicates.
- Structured debate on Medium+ items:
  - Proposer (original model) states claim + evidence + causal chain.
  - Falsifier (different capability model) attacks with specific contradictory evidence from the pack or states "No strong falsification possible with current data."
  - Arbiter scores on: Evidence specificity, causal plausibility, severity fit.
- Tie-breaker checkpoint (third model or senior human): "Review only the debate record. Do not generate new findings. Flag any claims that appear to be correlated aesthetic consensus rather than grounded pain."

**Phase 3: Synthesis + Verification Gate (Day 5)**
- Human PM + Design Lead + Research (if available) review.
- Apply severity rubric + hard evidence rule.
- Produce two backlogs:
  - Verified (actionable now)
  - Hypothesis (requires new data collection)
- Epistemic Humility Check: Explicitly list the top 3 findings most likely to be wrong due to model training-data bias.
- Final sign-off.

**Stop Conditions**:
- Two consecutive rounds produce <10% net-new Medium+ claims.
- Debate devolves into aesthetic language ("cleaner," "more modern").
- >50% of Medium+ items are still Hypothesis after Phase 3.

**Full Track (when resources allow)**: Add Codex-style Week 2 targeted validation (rapid usability tests + focused analytics) before final prioritization.

---

## 6. Model Selection & Prompt Constraints

**Strongly Preferred Pattern** (capability differentiation):
- 1 spatial/layout model
- 1 adversarial/hostile simulation model
- 1 broad heuristic + pattern model

**Mandatory Prompt Constraints** (include in every invocation):
- Ban first-person preference language ("I find this confusing").
- Ban aesthetic words without evidence ("modern", "clean", "polished", "intuitive", "feels off").
- Require: "Assume the design is hostile to user goals until proven otherwise."
- Require specific, reproducible evidence references.
- Require populated "Disconfirming evidence" field for Medium+.
- Forbid redesign language in diagnosis fields (quarantine it).

---

## 7. Three (Plus Two) Mandatory Guardrails

From the Kimi debate round:

1. **Evidence Reference Specificity** — "Mixpanel" is not evidence. Exact funnel step + date range + drop percentage is.
2. **Disconfirming Evidence or Downgrade** — Empty or "nothing could falsify this" → auto-downgrade to Low.
3. **No Redesign Before Causality** — Any redesign language auto-quarantines the finding until the causal claim survives independent review.

Additional guardrails surfaced during synthesis:

4. **Field Quality Check** (arbiter / tie-breaker responsibility) — Evidence and disconfirming fields must be specific enough to reproduce. Checkbox compliance is called out and downgraded.
5. **Epistemic Humility Check** (mandatory in Phase 3) — Explicitly name the top 3 findings most vulnerable to training-data correlation bias.

---

## 8. Provenance & Limitations (v0.1)

This version is the direct product of:
- Parallel high-rigor prompts to Kimi 2.5 and GPT-5.3 Codex
- Kimi 2.5's full adversarial critique of Codex's proposal (unilateral due to cost)
- Human synthesis prioritizing operational clarity (Codex) + adversarial rigor + evidence flexibility (Kimi)

**Known Remaining Weaknesses** (as identified by Kimi in the debate):
- Still vulnerable to correlated model bias on aesthetic priors.
- Hard gates vs flexible judgment tension is not fully resolved.
- Verification timing remains resource-dependent.

This playbook is intentionally lightweight enough to run on an alpha product with imperfect analytics, while being strict enough to prevent vibes theater.

---

**Next Step**: Third-model review by Gemini 3.1 Pro (extended thinking) before first real execution.

---

*Part of the Immutable QC multi-model auditing research program.*  
*Adapted from the Multi-Model LLM Security Auditing Playbook and the IQC token security audit process.*