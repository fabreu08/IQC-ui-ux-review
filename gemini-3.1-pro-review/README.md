# Gemini 3.1 Pro (Extended Thinking) — Third Model Review Package

**Purpose**: Bring a strong third voice (Gemini 3.1 Pro in extended thinking mode) into the UI/UX methodology adaptation process after the Kimi 2.5 vs GPT-5.3 Codex debate round.

This follows the proven pattern from the IQC token security audit where additional high-rigor perspectives (especially after head-to-head debate) significantly improved the final synthesis.

## Current State of the Research (as of this package)

1. **Round 1** — Parallel high-rigor prompts sent to:
   - Kimi 2.5 → `../raw-outputs/kimi-2.5-uiux-methodology-adaptation.md`
   - GPT-5.3 Codex → `../raw-outputs/gpt5.3-codex-uiux-methodology-adaptation.md`

2. **Debate Round** — Budget-constrained. Kimi 2.5 was given both round-1 responses and performed a full unilateral adversarial critique of Codex using the 6-section protocol + 6-dimension rubric + 11 seeded tensions.
   - Full debate response: `kimi-debate-response-codex-sparring.md` (in sibling `head-to-head-kimi-vs-codex/` directory)

3. **Merged Playbook v0.1** — Human synthesis of the above, heavily leveraging Kimi's excellent "Final Recommendation" section while preserving Codex's operational strengths.
   - Current best artifact: `../UIUX_Multi_Model_Auditing_Playbook_v0.1.md`

## What Gemini Is Being Asked To Do

Gemini is **not** being asked to do another generic UI/UX review of alpha.immutableqc.com.

Instead, Gemini is being asked to act as a **third strong skeptic and methodologist** who:
- Has read the entire evolution (both round-1 proposals + the Kimi debate critique + the resulting merged v0.1 playbook)
- Pressure-tests the current v0.1 against the original goals (preventing vibes theater, maintaining epistemic discipline from the security playbook, practicality for a real alpha team)
- Surfaces remaining weaknesses, new anti-patterns, or blind spots that the Kimi ↔ Codex exchange missed
- Scores the current playbook using the established 6-dimension rubric
- Offers concrete improvements or alternative structures, especially on the unresolved tensions Kimi flagged

## Package Contents

- `README.md` (this file)
- `Gemini_3.1_Pro_Review_Prompt.md` — The main high-rigor prompt (optimized for extended thinking). This is what you send.
- `Process_History_Summary.md` — Concise narrative of how we got here (recommended reading before the raw documents)
- `UIUX_Multi_Model_Auditing_Playbook_v0.1.md` — The current best merged artifact (must be reviewed)
- Copies of key supporting artifacts (protocol, tensions, debate response) for self-containment

**Recommended supporting documents to have open** (all in parent or sibling directories):
- `head-to-head-kimi-vs-codex/kimi-debate-response-codex-sparring.md`
- `head-to-head-kimi-vs-codex/Shared_Debate_Protocol_and_Rubric.md`
- `head-to-head-kimi-vs-codex/Key_Tensions_Seed.md`
- Original round-1 responses in `../raw-outputs/`

## Recommended Usage (Completed)

1. Prompt sent to Gemini 3.1 Pro (Extended Thinking).
2. Full response archived as `gemini-3.1-pro-review-response.md`.
3. **Synthesis complete**: `UIUX_Multi_Model_Auditing_Playbook_v0.2.md` (top level) now incorporates Gemini's four mandatory revisions while preserving operational feasibility.

Gemini scored v0.1 as **Weak** and pushed the methodology significantly back toward stricter evidence standards (closer to Codex's original position). v0.2 reflects that pressure.

## Success Criteria for This Review

- Gemini identifies at least 2–3 genuine remaining weaknesses or new risks that the prior Kimi/Codex exchange did not surface.
- Gemini provides a clear score of the current v0.1 on the 6-dimension rubric with specific justification.
- Gemini gives actionable, concrete suggestions (not vague "consider adding X").
- The response helps us decide whether the current merged playbook is ready for real-world use or still requires material changes.

---

This package is part of the ongoing Immutable QC research into rigorous, multi-model, anti-theater approaches to auditing subjective domains (security → UI/UX).