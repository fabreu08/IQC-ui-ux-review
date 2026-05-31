# Post-Debate Synthesis Template
## UI/UX Multi-Model Auditing Playbook v0.1 (Draft)

**Inputs to this synthesis**:
- Kimi 2.5 original methodology adaptation (`../raw-outputs/kimi-2.5-uiux-methodology-adaptation.md`)
- GPT-5.3 Codex original methodology adaptation (`../raw-outputs/gpt5.3-codex-uiux-methodology-adaptation.md`)
- Kimi's debate response to Codex (`kimi-debate-response-to-codex.md`)
- Codex's debate response to Kimi (`codex-debate-response-to-kimi.md`)
- This template (filled by human + optional neutral arbiter model)

**Output goal**: A single, executable v0.1 playbook + supporting artifacts (Pain Model template, Claim Card schema, Debate Protocol v2, Severity Rubric v2, Prompt Package) that is tighter and better defended than either original proposal.

---

## Section 0: Synthesis Meta-Assessment

**Completed by**: [Human name / date]

1. Which 4-6 dimensions showed the strongest convergence between the two models after debate? (List with 1-sentence evidence from the debate responses.)

2. Which 2-4 tensions remain genuinely unresolved or represent legitimate trade-offs rather than one side being clearly superior? (Name the tension + the concrete product/operational implication of choosing each side.)

3. Did either model surface a new anti-pattern risk in the other's proposal (or the naive combination) that was not visible in round 1? If yes, how is it mitigated in this synthesis?

4. Overall verdict on whether the post-debate synthesis crosses the "epistemology change" threshold both models flagged:
   - [ ] Yes — this version is meaningfully harder to turn into vibes theater than either source proposal.
   - [ ] Partial — still requires 2-3 additional guardrails (list them).
   - [ ] No — we are still mostly doing sophisticated prompt engineering.

---

## Section 1: Core Principles (Merged)

**From both proposals + debate pressure**:

List the final 6-8 principles that survived. For each:
- One-sentence statement
- Source (Kimi / Codex / both / new from debate)
- The specific anti-pattern it is intended to block
- The enforcement mechanism (prompt language / schema field / human gate / rubric gate)

Example entry:
- **Pain Model First (non-negotiable prerequisite)** — Source: both + debate consensus. Blocks: Phantom Persona, persona projection, ungrounded aesthetic claims. Enforcement: No model review may begin until a versioned Pain Model artifact exists and is attached; any finding without explicit mapping to it is auto-rejected as opinion.

---

## Section 2: Pain Model / Grounding Pack Specification (Final)

**Chosen structure** (merge or select winner + refinements from debate):

Provide the exact field list / schema that will be used for the alpha.immutableqc.com audit.

Include:
- Required vs optional fields
- Versioning and freezing rules
- Minimum viable evidence pack that must accompany it before models are invoked (session replays count, analytics window, user quote minimum, accessibility baseline, etc.)

**Rationale for choices made** (especially where Kimi and Codex diverged): 2-3 sentences.

---

## Section 3: Claim Card Schema (Final)

**The atomic unit** that every model output and debate contribution must produce.

Define the exact fields (building on Codex's proposal + Kimi's justification template + any debate refinements):

- Claim ID
- Journey / CUJ
- Segment + Context + State
- Symptom (what the user sees/experiences)
- Mechanism (why the interface produces that experience)
- Observed / Hypothesized Behavior
- Evidence IDs (with types)
- Counter-evidence / Disconfirming evidence (required)
- Severity (using final rubric)
- Confidence
- Pain Model mapping (required for Medium+)
- Causal chain to user harm + business harm (one sentence each)
- Verification status (Hypothesis / Needs specific test / Verified by existing data / Verified by new test)
- Proposed next action (experiment / fix / monitor / archive) — only after causal claim passes

**Any fields that were debated and ultimately removed or added**: note them.

---

## Section 4: Severity / Impact Rubric v0.2 (Final)

**The scale** (5 levels, names + definitions).

**Hard gates** for High and Critical (these are pass/fail before severity label can be assigned).

**Justification template** that must be filled for every Medium+ claim (can be the merged version of Kimi's 4-field + Codex's exposure/quantification requirements).

**Downgrade rules** (what triggers automatic downgrade).

**Distinction between "taste / preference" and "impact"** (final language).

**Note any remaining disagreement** from the debate that the synthesis team consciously chose one side on, and why.

---

## Section 5: Workflow + Phases (Final)

**The 5-7 phase sequence** a team will actually follow for the alpha.immutableqc.com audit.

For each phase:
- Objective
- Inputs (exact artifacts)
- Who does it (human / models / both)
- Outputs (exact artifacts + quality gates)
- Estimated effort (for a small team)
- Stop / go criteria to next phase

Include explicit points where "evidence pack is incomplete → do not proceed to model review" and "debate produced X unverified High claims → mandatory targeted validation loop before prioritization".

**Calendar view** (optional but recommended for the first real run): 8-10 working day version tailored to current maturity of Immutable QC analytics + research.

---

## Section 6: Debate + Arbitration Protocol v2 (Final)

**The exact format** that will be used for the first real UI/UX audit head-to-head.

- Number of primary models
- Blind pass rules
- Claim normalization step (yes/no + who owns)
- Debate mechanics (direct confrontation vs. proposer/challenger/arbiter; who can serve as arbiter)
- Scoring dimensions for the arbiter (if any)
- What happens to claims that do not survive debate
- Role of any tie-breaker / specialist model

**Rationale** for the chosen format vs. the alternative proposed in debate.

---

## Section 7: Anti-Patterns + Guardrails (Final Consolidated List)

**UI/UX-specific anti-patterns** that made it into the final playbook, with the specific countermeasure for each (prompt language, schema requirement, human process gate, or post-audit check).

Include any new ones surfaced during the Kimi ↔ Codex debate that neither had named in round 1.

---

## Section 8: Model Selection & Prompt Constraints (Final)

**Recommended primary 2-3 models** for the first real run + rationale.

**Specialist passes** (when to add a 4th).

**Prompt-level constraints** that are mandatory in every model invocation (merged strongest language bans + schema requirements + adversarial framing from both + debate).

**Example starter prompt** (the one a human will actually copy-paste for the alpha review, with [PAIN MODEL] and [EVIDENCE PACK] placeholders).

---

## Section 9: Grounding, Verification & Stop Conditions (Final)

**Minimum evidence requirements** before any claim graduates from "model hypothesis" to "audit backlog item".

**Verification loop** after debate (what additional data collection is mandatory vs. optional).

**Quantitative + qualitative stop rules** for additional model rounds (e.g., "<10% net-new Medium+ claims across two consecutive rounds + no change to top 5 prioritized items").

**Diminishing returns / aesthetic drift detector** language.

---

## Section 10: Execution Package for alpha.immutableqc.com (First Real Run)

Checklist of artifacts that must exist before the first model is invoked:

- [ ] Pain Model v0.1 (frozen)
- [ ] Evidence Index with IDs and access instructions
- [ ] Severity Rubric v0.2 printed and agreed by product/design/research
- [ ] Claim Card template in the shared workspace
- [ ] Audit Charter (scope, non-scope, primary journeys ranked by business risk, constraints)
- [ ] Current Figma / production screenshots annotated with state notes
- [ ] Accessibility baseline (automated + at least one manual screen reader pass on critical flows)
- [ ] Three model prompts (primary reviewer, challenger, arbiter) with placeholders filled
- [ ] Human owner for each phase + decision rights

**Week-by-week plan** (condensed from the debate's concrete proposals).

**Owner** for the first full execution.

**Date** of planned kickoff.

---

## Section 11: Open Questions / Known Weaknesses of This v0.1

Even after the debate and synthesis, what are the 2-4 things we are least confident will work in practice on a real alpha product with imperfect data? These become the explicit hypotheses the first execution will test.

---

## Section 12: Sign-off

**Synthesized by**: ___________________________ Date: ________

**Reviewed by (optional neutral model or second human)**: ___________________________ Date: ________

**Approved for first execution on alpha.immutableqc.com**: [ ] Yes  [ ] With the following three mandatory modifications: ...

---

**End of Synthesis Template**

After this document is filled, the next deliverable is the clean, standalone `UIUX_Multi_Model_Auditing_Playbook.md` (extracted from the filled template + all supporting one-pagers: Pain Model blank, Claim Card blank, Debate Protocol v2 one-pager, etc.).

This template exists to force the synthesis step to be as disciplined as the debate that preceded it.