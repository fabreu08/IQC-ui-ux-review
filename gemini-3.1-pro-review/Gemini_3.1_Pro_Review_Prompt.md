# PROMPT FOR GEMINI 3.1 PRO (EXTENDED THINKING MODE)

**You are operating at maximum rigor, skepticism, and methodological precision — the same standard used in the highest-signal phases of the IQC token security audit.**

You are being brought in as the **third strong voice** after a full Kimi 2.5 vs GPT-5.3 Codex debate round on adapting the multi-model LLM security auditing playbook to UI/UX work.

---

## Your Role in This Process

You are **not** here to do another UI/UX critique of alpha.immutableqc.com.

You are here as a **methodological reviewer and tie-breaker / additional skeptic** who has the benefit of seeing the entire evolution:

- Two independent high-rigor round-1 proposals (Kimi 2.5 and GPT-5.3 Codex)
- A full adversarial head-to-head debate (Kimi critiquing Codex unilaterally using the exact 6-section protocol + 6-dimension rubric + 11 seeded tensions)
- The resulting human-synthesized "best current artifact" (Playbook v0.1)

Your job is to pressure-test the current merged playbook, the debate process itself, and the remaining unresolved tensions — with fresh eyes and no loyalty to either prior proposal.

---

## Documents You Must Read (All Provided in This Package or Immediate Parent Directories)

1. **Primary Object of Review** (read this first and most carefully):
   - `../UIUX_Multi_Model_Auditing_Playbook_v0.1.md`

2. **The Debate That Produced It**:
   - `head-to-head-kimi-vs-codex/kimi-debate-response-codex-sparring.md` (Kimi's full 6-section unilateral critique + self-updates + merged recommendation)

3. **Supporting Context** (read for grounding):
   - `Process_History_Summary.md` (this directory)
   - `head-to-head-kimi-vs-codex/Shared_Debate_Protocol_and_Rubric.md`
   - `head-to-head-kimi-vs-codex/Key_Tensions_Seed.md`
   - Both original round-1 responses:
     - `../raw-outputs/kimi-2.5-uiux-methodology-adaptation.md`
     - `../raw-outputs/gpt5.3-codex-uiux-methodology-adaptation.md`

You have the full history. Use it.

---

## Specific Tasks (Structure Your Response Exactly This Way)

### Section 1: Overall Assessment of the Current v0.1 Playbook
One tight paragraph:
- Is the merged playbook a genuine improvement over either round-1 proposal, or did synthesis dilute the strongest elements of both?
- What is its single highest-leverage strength?
- What is its single highest-leverage remaining weakness or risk?

### Section 2: Scoring the v0.1 Playbook on the 6-Dimension Rubric
Use the exact rubric from `Shared_Debate_Protocol_and_Rubric.md`:

For each of the 6 dimensions, give:
- **Score**: Strong / Adequate / Weak
- 2–4 sentence justification with specific references to the v0.1 text
- The most important concrete improvement you would make

Dimensions:
1. Fidelity to Security Playbook Anti-Pattern Defenses
2. Resistance to Subjectivity Creep (UI/UX Specific)
3. Actionability & Operational Clarity for a Real Product Team
4. Severity / Impact Calibration Rigor
5. Debate & Synthesis Mechanics
6. Grounding & Verification Loop Strength

**Overall Score** for v0.1 (binding constraint = weakest dimension).

### Section 3: Attack on the Three Unresolved Tensions Kimi Explicitly Flagged

Kimi (after the debate) named these as still genuinely open:

**T-A**: Hard gates vs. flexible judgment on evidence for High/Critical (Codex's "2 classes" risk of false negatives vs Kimi's more flexible OR logic risking inflation).

**T-B**: Correlated model bias on aesthetic / design priors — neither proposal has a robust solution when all strong models share similar training data.

**T-C**: Realistic verification loop timing for teams that will never run a full "Week 2" targeted validation phase.

For **each** of these three:
- State which side (or synthesis) the current v0.1 landed on.
- Explain why you believe that landing is still insufficient or dangerous.
- Propose a concrete mechanism, rule, prompt constraint, or process change that would meaningfully improve it (not just "be more careful").

### Section 4: New Risks or Anti-Patterns You See in the v0.1 or the Overall Approach

The Kimi debate surfaced three new ones (Claim-Card Completeness Theater, Falsifier Role Capture, Week 2 Skipped / Vocabulary Theater).

Name any **additional** ones you see that the prior exchange missed. For each:
- Name it
- Describe the failure mode in practice on an alpha product
- Give the specific mitigation you would add to the playbook or prompts

### Section 5: Direct Commentary on the Debate Process Itself

The security audit reached some of its best insights during head-to-head debate between strong skeptics.

In this UI/UX case we only had a unilateral (Kimi-only) debate because of cost.

- How much signal do you believe was lost by not having Codex actually respond?
- Does the current merged v0.1 feel like it has the "sharp edges" that come from real adversarial exchange, or does it feel like a polite compromise?
- Would you recommend we still run the original two-way cross-critique prompts when funding appears, or is the current artifact good enough that the marginal value is low?

### Section 6: Final Recommendation — Ship, Revise, or Start Over?

Given everything you have read:

**Option A**: The current v0.1 is good enough to run on alpha.immutableqc.com as the first real multi-model UI/UX audit (with only minor wording tweaks).

**Option B**: The playbook needs material changes in 2–4 specific areas before it is safe to run (list them with proposed fixes).

**Option C**: The entire approach still carries too much residual "polished nonsense" risk and we should pause methodology work and go straight to running real user research + manual expert review instead of multi-model LLM work.

Choose one and defend it ruthlessly with reference to the documents.

---

## Additional Instructions (Extended Thinking Mode)

- Think step by step. Show your reasoning on the hard calls (especially the three unresolved tensions).
- Be as direct and unsentimental as Kimi was in its debate response. Politeness has no value here.
- When you criticize the current v0.1, quote specific sections or guardrails.
- When you praise something, explain the mechanism that makes it work (not just "this feels better").
- If you believe Gemini-class models have particular strengths or blind spots that make them especially useful (or dangerous) in this kind of methodological review, name them explicitly.

---

**Send your full structured response following the 6 sections exactly.**

No preamble outside the required sections.

This is high-stakes work. The quality of your review will directly determine whether the first real UI/UX audit we run on alpha.immutableqc.com is rigorous or just expensive theater.

---

*Package prepared 2026-05-31. Part of the Immutable QC multi-model auditing research program.*