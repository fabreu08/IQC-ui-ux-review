# UI/UX Multi-Model Auditing Playbook v0.2

**Title**: Adversarial UX Review — Final Synthesized Methodology  
**Version**: 0.2 (Post Gemini 3.1 Pro Review)  
**Date**: 2026-05-31  
**Status**: Recommended for first execution on alpha.immutableqc.com  
**Inputs**: 
- Kimi 2.5 round-1
- GPT-5.3 Codex round-1
- Kimi 2.5 unilateral debate response (Codex sparring)
- Gemini 3.1 Pro extended thinking review

---

## Executive Summary of Evolution

**v0.1** (post Kimi debate) was criticized by Gemini 3.1 Pro as having traded too much epistemological rigor for operational convenience. Gemini scored it **Weak** (binding constraints: Severity Rigor and Verification Loop) and accused it of re-opening the door to severity inflation and "Vocabulary Theater."

**v0.2** incorporates Gemini's core critique while preserving practicality for a real alpha team with imperfect data. The major shifts from v0.1:

- Hardened evidence gates for High severity (moved closer to Codex + Gemini position)
- Added mandatory "Predictive Validation" for any claim marked Verified
- Made several guardrails programmatic rather than human/LLM-dependent
- Strengthened Pain Model provenance requirements

This version represents the current best attempt at balancing **"we have limited data"** with **"we will not lower the standard just because data is limited."**

---

## 1. Foundational Principles (Hardened in v0.2)

1. **Pain Model First + Provenance** — No review begins until a versioned Pain Model with explicit data citations exists.
2. **Multi-Source Threshold for High** — High severity now requires at least two independent validation nodes (behavioral signal + surviving adversarial falsification attempt).
3. **Predictive Validation for "Verified"** — Nothing is marked Verified on the basis of existing data alone. The model must predict currently unmeasured behavior that is then confirmed.
4. **Capability Differentiation + Contrastive Prompting** — Three differentiated models + mandatory defense of the status quo on every claim.
5. **Programmatic Guardrails** — Several anti-theater rules are now enforced by length, structure, and pre-arbitration linting rather than model judgment.
6. **Diminishing Returns + Stop Conditions** remain unchanged.

---

## 2. Pain Model Requirements (v0.2 Strengthening)

Every entry in the Pain Model (Personas, CUJs, Failure Signals, etc.) **must** include a "Data Provenance" citation:

- Specific support ticket cluster ID / CRM segment / revenue metric / analytics query
- Or explicit note: "Expert hypothesis — pending validation"

**Rule**: If more than 30% of the Pain Model lacks hard provenance citations, Phase 1 (model review) is blocked. LLMs may not be used to generate the initial Pain Model without these citations.

---

## 3. Claim Card Schema (v0.2 Additions)

Added two new required fields:

- **Falsification Attempt Result** (from the adversarial model pass)
- **Predictive Validation Statement** (required for any claim the team wants to mark "Verified")

---

## 4. Severity Rubric (v0.2 — Major Change)

**Critical** — Unchanged (irreversible harm + strong multi-source evidence)

**High** (Strengthened)
- Critical journey + repeated failure pattern
- **AND** at least one concrete behavioral signal from existing data
- **AND** survives an explicit adversarial falsification attempt by a second model (the "Two-Node Falsification" rule from Gemini)

If a critical journey has insufficient instrumentation (no two independent behavioral signals available), the **maximum** severity any model finding in that journey can receive is **Medium** ("Data-Deficit Downgrade").

**Medium / Low / Informational** — Unchanged from v0.1

---

## 5. Workflow (v0.2 — Verification Hardened)

**Phase 0: Setup** (unchanged but with provenance enforcement)

**Phase 1: Blind Model Review** (added)
- Every Medium+ claim must also generate a "Contrastive Defense": a rigorous argument for why the current design may actually be optimal for the persona in the Pain Model.

**Phase 2: Arbitration** (added)
- Programmatic pre-linting: Any Claim Card with a Disconfirming Evidence field < 25 words or missing explicit Pain Model mapping is auto-rejected before human/arbiter sees it.
- Tie-breaker model receives only raw Claim Card + Falsifier attack + evidence pack (identity-blind).

**Phase 3: Synthesis + Verification Gate** (Major Change)
- Two backlogs are produced:
  - **Actionable** (High/Critical that passed all gates)
  - **Requires Predictive Validation** (everything else that reached Medium+)

**No finding may be labeled "Verified" during Day 5 synthesis** unless:
- The proposing model made a specific, testable prediction about currently unmeasured user behavior, **and**
- The team subsequently instrumented and confirmed that prediction within 48–72 hours.

This directly implements Gemini's "Predictive Analytics Gate."

---

## 6. Guardrails (v0.2 — Programmatic Enforcement Added)

**Unchanged from v0.1**:
1. Evidence Reference Specificity
2. Disconfirming Evidence or Downgrade
3. No Redesign Before Causality (Redesign Proposal Quarantine)

**Strengthened in v0.2**:
4. **Programmatic Linting** — Guardrails 2 and 4 are now enforced by automated checks (word count + structure) before any human or model sees the cards.
5. **Epistemic Humility + Contrastive Prompting** — Every Medium+ claim must include both the attack on the design *and* a serious defense of the current implementation.

---

## 7. Model Roles (v0.2 Refinement)

Recommended differentiated roles remain the same, with one addition:
- One model is explicitly assigned the **Contrastive Defense** role on every claim (this can rotate or be a fourth lightweight pass).

---

## 8. Decision Log: How v0.2 Responded to Gemini's 4 Mandatory Revisions

| Gemini Recommendation | Decision in v0.2 | Rationale |
|-----------------------|------------------|---------|
| 1. Reinstate Hard Evidence Gates (Data-Deficit Downgrade) | **Adopted** (with slight softening) | High now requires behavioral signal + surviving adversarial falsification. Pure "OR" logic removed. |
| 2. Kill Post-Hoc Verification (Predictive Analytics Gate) | **Adopted** | "Verified" status now requires the model to predict something new that is then measured. This is the single biggest hardening from v0.1. |
| 3. Programmatic Epistemic Enforcement | **Adopted** | Pre-arbitration linting + minimum word counts for Disconfirming Evidence fields added. |
| 4. Mandate Pain Model Provenance | **Adopted** | Phase 0 now has an explicit block if provenance is insufficient. LLM-generated Pain Models without citations are banned. |

---

## 9. Remaining Known Limitations (v0.2)

Even after incorporating Gemini's feedback, two structural tensions remain:

- **Resource Reality vs Epistemic Ideal**: The Predictive Validation requirement adds friction. Teams that truly cannot instrument anything new will be forced to treat almost everything as "Requires Predictive Validation."
- **Correlated Model Bias**: Contrastive prompting and capability differentiation help but do not eliminate shared training data priors. The process now forces models to argue *against* their own aesthetic priors, which is the best mitigation we have found so far.

---

## 10. Recommendation for First Execution

**Run v0.2 on alpha.immutableqc.com**, with the following explicit caveats documented in the project charter:

- The team commits to the Predictive Validation step for any claim they want to treat as high-confidence.
- If instrumentation cannot be added quickly, the output will be a high-quality **Hypothesis backlog** rather than a Verified one — and that is acceptable.

This version is materially stricter than v0.1 while remaining executable.

---

**Next Step**: When funding allows, run the original two-way Kimi ↔ Codex cross-critique prompts on this v0.2 artifact for a final pressure test before wider use.

---

*Part of the Immutable QC multi-model auditing research program.*  
*This version represents the synthesis of Kimi 2.5, GPT-5.3 Codex, and Gemini 3.1 Pro (extended thinking) perspectives.*