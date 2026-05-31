# Shared Debate Protocol + Scoring Rubric
## Kimi 2.5 vs GPT-5.3 Codex — UI/UX Methodology Adaptation

**Version**: 0.1 (for this head-to-head round)  
**Date**: Immediate  
**Goal**: Maximum signal. No vibes consensus. No politeness theater. Force each proposal to survive direct adversarial scrutiny from the other strong skeptic.

---

## Core Rules (Non-Negotiable for Both Models)

1. **You are debating the methodology, not performing a UI review.** Do not generate new findings about alpha.immutableqc.com. Stay strictly on the proposals themselves.

2. **Direct address.** Speak to the other model by name where your positions diverge. "Codex, your claim-card schema introduces X risk that my approach avoids because..." or "Kimi, your 5-phase workflow under-specifies Y operational gate that my 6-phase version handles by..."

3. **Cite specific text.** Every major critique must reference paragraph, section, or table from the opponent's exact response (e.g., "In Codex §4 Severity scale, the 'Medium' threshold requires 'two independent evidence types' — this is stronger than my initial framing because...").

4. **Evidence from security playbook lessons.** When arguing for or against a UX adaptation, explicitly reference what worked or failed in the IQC token security process (phantom findings, severity inflation, Trust Model prerequisite, correlated model bias, etc.).

5. **No aesthetic or preference language in your own critique.** Model the discipline you are advocating: "This structure reduces persona projection risk" not "I prefer more granularity here."

6. **Falsifiability and counterevidence.** For every significant claim you make about why your approach or the opponent's is superior, include a one-sentence statement of what evidence or outcome would falsify your position.

7. **End with self-update.** After critiquing the other, explicitly state: (a) Which 1-3 elements of *your own original proposal* you would now revise or strengthen, and (b) Which 1-3 tensions remain unresolved even after this exchange.

8. **Severity inflation in methodology debate is itself a finding.** If you are tempted to rate the opponent's entire framework "Weak" because of one soft spot, apply your own proposed severity rubric to the *methodology proposal itself* before assigning labels.

---

## Scoring Rubric: Evaluating a UI/UX Methodology Proposal

Use this 6-dimension rubric to score the *opponent's full adaptation* (and re-score your own at the end). For each dimension give:

- **Score**: Strong | Adequate | Weak (with 1-sentence justification)
- **Specific risk introduced** if Weak or Adequate
- **Concrete fix** you would apply (or why opponent's version already fixes it)

### Dimension 1: Fidelity to Security Playbook Anti-Pattern Defenses
- Does it preserve the hard lessons (no correlation treated as independence, Trust/Pain Model as prerequisite, tooling/evidence non-negotiable above Medium, diminishing returns discipline, explicit stop conditions)?
- Does it introduce new "theater" vectors that the security version had closed?

### Dimension 2: Resistance to Subjectivity Creep (UI/UX Specific)
- How effectively does the proposal quarantine aesthetic preference, recency bias, designer defensiveness, and "vibes" from Medium+ findings?
- Are the quarantine mechanisms (language bans, evidence thresholds, persona locks) enforceable in a real prompt?

### Dimension 3: Actionability & Operational Clarity for a Real Product Team
- Can a product + design + research team execute this in 1-2 weeks on alpha.immutableqc.com without the process becoming the product?
- Are the phases, gates, artifacts, and handoffs specified at the level of "Day 2: do X with Y tool, produce Z artifact"?

### Dimension 4: Severity / Impact Calibration Rigor
- Does the rubric force causal-chain + segment exposure + quantified business/user harm before High/Critical?
- Does it have hard gates (not just guidance) that prevent inflation while still surfacing real, painful friction in critical journeys?

### Dimension 5: Debate & Synthesis Mechanics
- Is the proposed head-to-head format (or claim arbitration) likely to produce net-new signal rather than rephrasing or status-seeking?
- Does it include falsification pressure, arbiter criteria, or normalization steps that reduce both false positives and false negatives?

### Dimension 6: Grounding & Verification Loop Strength
- How completely does the proposal require (and enforce) behavioral evidence (analytics, replays, user quotes, accessibility task failures) before any claim can graduate from "hypothesis" to "verified finding"?
- Does it close the verification gap that plagued the security reviews ("we all agree this is bad" ≠ proof)?

**Overall Proposal Score** (not average — the weakest dimension is often the binding constraint): Strong / Adequate / Weak

---

## Output Format Required From Each Debater

Structure your response exactly like this (use markdown headings):

### 1. Overall Assessment
One paragraph: net assessment of the opponent's framework quality + the single highest-leverage strength and single highest-leverage weakness.

### 2. Dimension-by-Dimension Scoring
Use the 6 dimensions above. For each: Score + justification + risk + concrete improvement (either "your version already does this well" or "here is the patch").

### 3. Direct Engagement on Seeded Tensions
Numbered responses to each item in `Key_Tensions_Seed.md`. For each:
- Your position (with reference to your original response)
- Opponent's position (with reference to their text)
- Which is stronger and why (using rubric language)
- What a merged/better version would look like

### 4. New Anti-Pattern Risks Your Analysis Surfaces
Any failure modes the opponent's proposal (or the combined approach) would introduce that neither of you flagged in round 1.

### 5. Self-Update After Critique
- Elements of my original proposal I would now revise:
- Tensions that remain genuinely unresolved:

### 6. Final Recommendation
If a product team could only adopt *one* of the two frameworks tomorrow (or a specific hybrid), what exact version would you hand them, and what are the three mandatory guardrails?

---

## What Success Looks Like

- Both responses contain at least 4-5 "I was wrong / my version was incomplete on X because..." statements.
- Clear convergence on 60-70% of the mechanics (Pain Model necessity, evidence thresholds, model count, stop rules).
- Sharp, documented disagreement on the remaining 30-40% with concrete trade-off analysis (e.g., "Codex's arbiter rubric adds operational overhead but reduces severity inflation risk by Y; Kimi's direct confrontation is lighter but relies more on model discipline").
- The synthesis step can produce a v0.1 playbook that is tighter than either original proposal.

This is the same epistemic standard that made the Opus vs Kimi security head-to-head valuable. Apply it here.

---

*Protocol version controlled. Update only after both debate responses are in and synthesis begins.*