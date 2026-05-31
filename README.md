# UI/UX Multi-Model Auditing — Kimi 2.5 Review Package

This folder contains the materials for Kimi 2.5 to help adapt our multi-model auditing methodology from smart contract security to UI/UX reviews.

## Background

We developed a rigorous process for multi-model security auditing through the IQC token project (see the Playbook in the research repo).

We now want to explore how to apply similar discipline, structure, and anti-pattern avoidance to auditing user interfaces and experiences.

## Package Contents

- `Kimi_2.5_UIUX_Methodology_Review_Prompt.md` — The main review prompt (ready to send to Kimi)

## Goal

Get high-quality, structured input from Kimi 2.5 on:
- How to adapt the core principles
- What a "Pain Model" / User Frustration Model should look like
- Recommended workflows for UI/UX reviews
- Severity rubrics
- How to run effective head-to-head debates in a design context
- Integration with real user research and data

## Recommended Usage

Send the prompt to Kimi 2.5 (ideally in high-rigor / master prompt mode). You can also attach or link the main Playbook for reference.

## Current Contents

- `Kimi_2.5_UIUX_Methodology_Review_Prompt.md` — Prompt sent to Kimi 2.5
- `GPT5.3_Codex_UIUX_Methodology_Review_Prompt.md` — Parallel prompt for GPT-5.3 Codex (for head-to-head)
- `raw-outputs/kimi-2.5-uiux-methodology-adaptation.md` — Kimi 2.5's full detailed response

This folder supports a head-to-head comparison between Kimi 2.5 and GPT-5.3 Codex on adapting the multi-model auditing methodology to UI/UX.

**Current status**:
- Kimi 2.5 + GPT-5.3 Codex round-1 responses archived in `raw-outputs/`
- Kimi-only debate round completed (`head-to-head-kimi-vs-codex/`) — full response archived as `kimi-debate-response-codex-sparring.md`
- Merged **UIUX_Multi_Model_Auditing_Playbook_v0.1.md** created at top level
- **Gemini 3.1 Pro (extended thinking) review completed** (`gemini-3.1-pro-review/`)
  - Full response archived as `gemini-3.1-pro-review-response.md`
  - Gemini scored v0.1 **Weak** and proposed 4 specific mandatory revisions (stronger evidence gates, predictive verification, programmatic linting, strict Pain Model provenance)

**Next**: Final synthesis into v0.2 incorporating Kimi, Codex, and Gemini inputs. The three voices are now in tension (Kimi = pragmatic flexibility, Codex = hard epistemological gates, Gemini = even stricter post-debate tightening).

See `HEAD_TO_HEAD_SETUP.md` for the full current status and next steps.

---

Part of the ongoing Immutable QC research into multi-model AI-assisted auditing.