# Quick Reference: Kimi 2.5 vs GPT-5.3 Codex — Core Positions at a Glance

Use this as a fast index while reading the full debate responses or during synthesis. Not a substitute for the primary documents.

## 1. Core Philosophy

| Aspect | Kimi 2.5 | Codex |
|--------|----------|-------|
| Opening stance on porting security playbook | "Sound instinct, but dangerous if applied uncritically" | "Bluntly... you’ll get polished nonsense" without epistemology change |
| Central metaphor | Pain Model replaces Trust Model | Pain Model replaces Threat Model; "behavioral evidence + causal confidence" replaces "exploit proof" |

## 2. Pain Model / Grounding

| Aspect | Kimi 2.5 | Codex |
|--------|----------|-------|
| Primary structure | Document-centric: Personas, CUJs, Success/Failure Signals, Business Impact, Accessibility Baseline, Device/Context (heavy tables) | Claim-oriented: Segment, Journey, Context, Failure mode (taxonomy), Observable signals, User/Business harm, Evidence refs, Confidence |
| Enforcement slogan | "If a finding cannot be mapped to a specific Pain Model dimension, it is opinion, not a finding. Full stop." | "No Pain Model mapping = not a finding. No evidence IDs = hypothesis only. No causal path = severity capped at Low." |
| Minimum pre-review artifact | 5–10 session recordings + funnel analytics + 3–5 transcripts + axe/WAVE + device matrix | Event dictionary + funnel baseline (4–8 weeks) + stratified replay sample + research excerpts + constraints log |

## 3. Severity Rubric

| Aspect | Kimi 2.5 | Codex |
|--------|----------|-------|
| Levels | Critical / High / Medium / Low / Informational | Informational / Low / Medium / High / Critical |
| High gate | "Significant friction in critical journey; measurable business impact; user quotes or A/B test" + mandatory 4-field justification | "Critical journey + repeated failure + quantified exposure + at least 2 independent evidence classes" (hard gate) |
| Critical gate | Session recording of failure or WCAG A/AA catastrophe with major business impact | "Severe/irreversible harm, systemic blocker, legal/accessibility catastrophe on core path + immediate product risk" |
| Downgrade mechanism | "If any field missing... downgrade by one level" | Auto-downgrade for missing causal chain; single screenshot cannot justify >Low |

## 4. Workflow & Debate Mechanics

| Aspect | Kimi 2.5 | Codex |
|--------|----------|-------|
| Phases | 5 phases (Pain Model construction → 2-3 model exploration → Head-to-head pressure testing → Human synthesis + verification → Diminishing returns check) | 6-phase table (Scope lock → Grounding pack → Blind passes → Claim normalization → Adversarial debate → Human verification → Synthesis) |
| Debate format | Direct model-model confrontation on specific tensions ("Defend your position using the Pain Model evidence") | Proposer / Challenger / Arbiter scoring (Evidence quality, causal plausibility, severity fit) → accept/revise/downgrade/defer-to-test |
| Model count | 2–3 max primary; optional tie-breaker asked only to evaluate debate evidence (not generate new findings) | 3 primary; 4th only for narrow specialist pass; stop on <10% net-new Medium+ over two rounds |
| Post-debate verification | Human synthesis + behavioral verification (relatively lightweight) | Explicit "Verified vs Hypothesis" split + Week 2 targeted validation + re-score + triage (fix/experiment/archive) |

## 5. Anti-Patterns (UI/UX Specific)

**Shared by both**: Vibes Consensus / Consensus Theater 2.0, Phantom Friction / Design Debt Zombie, Severity Inflation (via effort or narrative), Persona Projection, Replay Cherry-Picking, Local Optimization Trap, Documentation / Heuristic Theater, Accessibility Tokenism.

**Kimi-unique emphasis**: Designer Defensiveness (explicit new principle + "assume hostile" framing), Recency Bias (explicit counterweight questions).

**Codex-unique emphasis**: Aesthetic Absolutism (preference quarantine lane), Severity Inflation via Narrative (rubric gating), "falsifier" role as structural mitigation.

## 6. Prompt / Bias Controls

| Aspect | Kimi 2.5 | Codex |
|--------|----------|-------|
| Language bans (examples) | No "users might", no "intuitive", no "clean/modern/polished", "assume design is hostile" | Ban first-person preference ("I find this confusing"), require disconfirming evidence field, separate diagnosis from solution |
| Structural controls | Strong "hostile UX auditor" role + Pain Model mapping requirement in every finding | Claim-card schema mandatory, randomize artifact order, "no redesign before causal claim passes" |
| New principle named | "The User Is Not You", "Recency Bias Is Inevitable", "Designer Defensiveness Is Contagious" | "Segment specificity", "Journey criticality over visual salience", "Causal-chain discipline", "Reversibility-aware prioritization" |

## 7. Practical Execution

- **Kimi**: 5-day review skeleton + detailed "Ideal Prompt Package" checklist + copy-pasteable model prompt template.
- **Codex**: Explicit 10-day (Week 1 analysis + Week 2 validation) calendar plan with day-by-day tasks for alpha.immutableqc.com.

## 8. Model Self-Assessment (Round 1)

- **Kimi on Kimi**: Strong at cross-referencing heuristics with specific elements; skeptical of aesthetic claims. Weakness: may over-index on pattern consistency vs. user context.
- **Codex on Codex**: Strong at rigorous schemas, adversarial reasoning, synthesis discipline. Weakness: can over-index structure if visual artifacts are weak.

---

**Use during debate reading**: When either model claims "my version handles X better," jump to the corresponding row and see whether the debate responses actually justify that claim under the shared rubric.

**Use during synthesis**: The areas with the most divergence (T1–T11 in Key_Tensions_Seed.md) are exactly the rows where the synthesis must make a conscious, documented choice.