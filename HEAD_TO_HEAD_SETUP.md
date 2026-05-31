# UI/UX Methodology Head-to-Head: Kimi 2.5 vs GPT-5.3 Codex

## Purpose

This package is set up for a direct head-to-head comparison between two strong models on the topic of adapting the multi-model LLM auditing methodology (originally developed for smart contract security) to UI/UX auditing.

## Models

- **Kimi 2.5** (with agents / master prompt configuration)
- **GPT-5.3 Codex**

**Status (updated)**: 
- Both round-1 responses received and archived.
- Debate round completed in **Kimi-only mode** (Codex response used as static sparring partner).
- Merged Playbook v0.1 produced from the debate.
- **Gemini 3.1 Pro (extended thinking) review completed**. Full response archived in `gemini-3.1-pro-review/gemini-3.1-pro-review-response.md`.
- Gemini scored v0.1 as **Weak** (binding constraints: Severity Rigor + Verification Loop) and proposed 4 mandatory revisions leaning heavily toward stricter evidence gates (closer to Codex's original position).
- Synthesis phase now active to produce v0.2 incorporating all three voices.

## Prompts

Both models have been given parallel, high-rigor prompts asking them to adapt the existing security auditing playbook to UI/UX work.

- `Kimi_2.5_UIUX_Methodology_Review_Prompt.md`
- `GPT5.3_Codex_UIUX_Methodology_Review_Prompt.md`

The prompts are intentionally similar in structure and demands so that differences in response quality, rigor, and insight can be compared fairly.

## Status: Debate Package Adapted for Kimi-Only Execution

**Debate round materials** in `head-to-head-kimi-vs-codex/` (updated for budget):

- `README.md` (now documents Kimi-only mode)
- `Shared_Debate_Protocol_and_Rubric.md` (unchanged — still governs the critique)
- `Key_Tensions_Seed.md` (11 high-signal seeded tensions — unchanged)
- `Kimi_Debate_Round_Prompt.md` — **Active single prompt for this round** (Kimi critiques Codex's full text + self-updates + produces merged recommendation)
- `Prompt_Kimi_Critiques_Codex.md` and `Prompt_Codex_Critiques_Kimi.md` — Archived two-way versions (not sent)
- `Synthesis_Template.md` (used after Kimi delivers; Codex original text serves as the second "voice")
- `Quick_Reference_Side_by_Side.md` (navigation aid)

## Recommended Process (Kimi-Only — Current Budget)

1. **Execute the debate (single high-rigor call)**:
   - `Kimi_Debate_Round_Prompt.md` is now **fully self-contained** (both round-1 texts pre-embedded in the placeholders).
   - Copy the entire prompt file and send it to Kimi 2.5 in highest-rigor / master-prompt configuration.
   - Archive reply as `kimi-debate-response-codex-sparring.md`

2. **Synthesize** using `Synthesis_Template.md` (human first pass; Codex's original document stands in for the missing reciprocal response).

3. **Produce** the unified `UIUX_Multi_Model_Auditing_Playbook.md` + supporting templates.

4. **Run the first real audit** of alpha.immutableqc.com once a proper behavioral evidence pack exists.

When funding arrives, the two-way cross-critique prompts remain available for a future higher-signal round.

## Goal

Produce a practical, battle-tested adaptation of the methodology that can be used to run rigorous, multi-model reviews of the current alpha.immutableqc.com UI/UX (and future interfaces). The debate round exists specifically to surface weaknesses that parallel reviews miss — exactly as the Opus 4.7 vs Kimi 2.5 security head-to-head did.

---

Part of the Immutable QC multi-model auditing research initiative.