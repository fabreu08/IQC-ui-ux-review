# Pain Model: Immutable QC Application (alpha.immutableqc.com)

**Version**: 0.1  
**Date**: 2026-05-31  
**Product**: The core web application (Express + EJS) at immutable.polsia.app / alpha.immutableqc.com  
**Purpose**: Ground all future UI/UX work, audits, and prioritization in real user jobs, constraints, and business outcomes. This is the prerequisite artifact per the UI/UX Multi-Model Auditing Playbook v0.2.

---

## 1. Primary Personas

### P1: Lab Technician / Instrument Operator (Primary)
- **Goals**: Quickly and accurately capture measurements from instruments (pH, temperature, HPLC, etc.), sign them, and submit to the immutable ledger with minimal friction.
- **Constraints**: Often rushed, working at the bench, may have gloves on, variable lighting, multiple instruments, time pressure during runs.
- **Emotional state**: Wants confidence that "this record won't come back to bite me later." Fear of manual entry errors or lost data.
- **Device/Context**: Desktop or laptop in lab (sometimes shared), occasional tablet. Low tolerance for multi-step wizards or slow wallet flows.
- **Jobs-to-be-done**: "Record this pH reading with proof it came from this instrument at this time, without re-typing everything."

### P2: QC Analyst / Reviewer
- **Goals**: Efficiently review batches of QC packets, apply domain expertise to attest or flag issues, maintain personal accountability via signature.
- **Constraints**: High volume during certain periods, needs to see context (raw readings, metadata, previous attestations) quickly. Regulatory or SOP pressure.
- **Emotional state**: Responsible for quality. Wants to move fast on clear cases and have clear escalation for ambiguous ones.
- **Device/Context**: Desktop in office or lab. Needs good comparison views and audit trail visibility.

### P3: Lab Manager / QA Director
- **Goals**: Oversee lab-wide data integrity, monitor review queues and bottlenecks, demonstrate compliance to auditors or clients.
- **Constraints**: Not doing the daily work but accountable for it. Needs dashboards and traceability, not just raw data entry.
- **Emotional state**: Needs to sleep at night knowing the chain of custody is solid.
- **Device/Context**: Mix of desktop + occasional mobile for status checks.

### P4: Compliance / External Auditor (Secondary / Future)
- **Goals**: Independently verify that data has not been altered since capture and that proper reviewer attestations exist.
- **Constraints**: External party, limited system access, needs exportable or publicly verifiable artifacts.

---

## 2. Critical User Journeys (CUJs)

These are the flows where failure is catastrophic for trust, compliance, or adoption.

### CUJ-1: Source-to-Ledger Capture & Commit (Highest Priority)
**Persona**: Lab Technician (P1)
**Steps**:
1. Select or register instrument.
2. Enter or upload measurement (manual or HPLC CSV).
3. Review auto-extracted metadata.
4. Connect wallet (if on-chain commit needed).
5. Sign (ECDSA or EIP-191).
6. Submit → local ledger entry + optional on-chain `commitQCPacket`.
**Success signals**: Reading appears in ledger within seconds with valid signature and chain hash. User sees clear confirmation + links.
**Failure signals**: "Step 1/3" spinner hangs, wallet signature fails silently, low balance blocks without clear guidance, CSV parse errors lose user work.
**Business impact**: Directly blocks daily usage and on-chain value prop. Highest drop-off risk.

### CUJ-2: QC Packet Creation + Routing for Review
**Persona**: Technician or Lab Manager
**Success**: Easy bundling of related readings into a packet, assignment to appropriate reviewer(s), clear status tracking.
**Failure**: Unclear what constitutes a "packet", no way to add context/comments, reviewers don't get notified or see the packet easily.

### CUJ-3: Reviewer Attestation Workflow
**Persona**: QC Analyst (P2)
**Success**: Reviewer can quickly see the full packet + raw evidence, apply judgment, sign their attestation, and see it reflected in the immutable record.
**Failure**: Slow loading of context, unclear what "attest" actually means legally/technically, no way to request more information from the operator.

### CUJ-4: Immutable Ledger & Provenance Verification
**Persona**: All (especially P3 and auditors)
**Success**: Anyone can navigate from a reading → full chain of signatures and attestations → on-chain proof, with clear explanations and export options.
**Failure**: Cryptic hashes, broken links between DB records and on-chain events, no human-readable "what this proves" explanation.

### CUJ-5: Stake Management for On-Chain Operations (Enabler)
**Persona**: Lab Manager / Power users who need to commit
**Success**: Clear view of staked balance, easy top-up/unstake (when supported), warnings when balance is too low for commits.
**Failure**: Users discover too late that they can't commit because of staking requirements.

---

## 3. Success Signals (Observable & Measurable)

- % of submitted readings that successfully reach the ledger with valid signature within 10 seconds.
- % of QC packets that receive at least one attestation within SLA (e.g., 24-48h).
- Wallet connection success rate on first attempt from the submit page.
- HPLC CSV upload → successful parsing + submission conversion rate.
- Repeat usage: users returning to submit more readings after first successful commit.
- Time-to-first-on-chain-proof for new users.

---

## 4. Failure Signals (Observable)

- Abandoned submissions at "Step 1/3" or wallet signature step (from analytics or session replays).
- High rate of faucet requests (indicates friction with token balance for commits).
- Support tickets or demo feedback mentioning "I don't know if my data is actually on-chain".
- Review queue growing with unclaimed packets.
- Users manually copying data out because they don't trust the system for long-term records.
- Low on-chain event volume relative to DB submissions.

---

## 5. Business Impact Mapping

| Failure in CUJ                  | User Harm                          | Business Impact                          | Severity for Product |
|--------------------------------|------------------------------------|------------------------------------------|----------------------|
| Failed or confusing submit     | Lost work, eroded trust in "immutable" claim | Churn before seeing value, bad word-of-mouth | Critical |
| Weak reviewer UX               | Reviewers slow or skip attestations | Compliance theater instead of real QC   | High |
| Opaque provenance / ledger     | Users and auditors can't verify    | Core value prop (trust) collapses       | Critical |
| Staking / token friction       | Users can't commit on-chain        | On-chain differentiation never realized | High |
| Poor mobile / bench experience | Technicians avoid the tool         | Low daily usage, data stays in paper/Excel | High |

---

## 6. Device / Context Matrix (Observed + Expected)

- Primary: Desktop/laptop in lab or office (Windows + macOS)
- Secondary: Shared lab computers, occasional tablets
- Future: Mobile for status checks or simple approvals
- Constraints: Variable network (some labs have poor connectivity), shared machines (no persistent wallet state), users may not be power users of crypto wallets.

---

## 7. Accessibility & Compliance Baseline (Initial)

- Current: Basic responsive design, some ARIA on wallet buttons.
- Required for target users: WCAG 2.1 AA minimum (lab environments often have accessibility policies; auditors may use screen readers).
- Known gaps: Complex forms (submit with tabs + dynamic HPLC preview), data tables (ledger, readings), wallet connection flows.

---

## 8. Data Provenance for This Pain Model (v0.1)

- Codebase exploration of `/views/submit.ejs`, `/public/js/wallet.js`, server routes for readings/qc-packets, and recent commits (May 2026).
- PROJECT_STATE.md and CLAUDE.md from the app repo.
- Historical context from prior development sessions (wallet integration, HPLC, V2 registry switch, staking requirements).
- No direct session replays or user interviews yet for this v0.1 (to be added in next iteration).

---

**Next per Playbook v0.2**:
- Gather minimal behavioral evidence (analytics events that already exist + any session recordings if available).
- Run structured review (using the claim card format) against the highest-risk CUJ (CUJ-1: Submit flow).
- Then prioritize concrete coding work.

This Pain Model will be versioned and frozen before any deep UI changes or audits.