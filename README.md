# IQC UI/UX Multi-Model Review

This repository is dedicated to applying the multi-model LLM auditing methodology (developed during the IQC token security audit) to the user interface and user experience of the Immutable Quality Control product.

## Background

Through an extensive security audit of the IQC smart contracts, we developed a structured approach to using multiple frontier AI models for deep technical review. This included:

- Iterative reviews with increasing context
- Head-to-head debates between strong models
- Explicit rubrics and "Pain/Threat Models"
- Heavy focus on avoiding common LLM failure modes ("consensus theater", phantom findings, severity inflation, etc.)

We are now adapting this same rigorous process to audit and improve the current UI/UX.

## Repository Structure (Planned)

```
.
├── README.md
├── methodology/               # Adapted playbook and principles for UI/UX
├── prompts/                   # Review prompts for different models
├── raw-outputs/               # Raw model responses
├── synthesis/                 # Consolidated findings and recommendations
└── decisions/                 # Key decisions and design rationale
```

## Current Status

This repo is in the early setup phase. The first major activity is adapting the security auditing methodology specifically for UI/UX work.

## Related Research

The original multi-model security auditing methodology and playbook live here:  
https://github.com/fabreu08/IQC-token-research

---

*Part of the Immutable Quality Control (IQC) research efforts.*
