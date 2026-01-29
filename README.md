# COMET-SG1  
## A Stability-Oriented Behavior-Space Autoregressive Regressor for Edge AI

**Author:** Shakhyar Gogoi  
arXiv: [https://arxiv.org/abs/2601.20772](https://arxiv.org/abs/2601.20772)

DOI: [![arXiv](https://img.shields.io/badge/arXiv-2601.20772-b31b1b.svg)](https://arxiv.org/abs/2601.20772)



**Keywords:** Edge AI, Time-Series Prediction, Autoregressive Models, TinyML, Embedded Systems

---

## Overview

This repository accompanies the research paper:

**COMET-SG1: A Stability-Oriented Behavior-Space Autoregressive Regressor for Edge AI**  
by **Shakhyar Gogoi**

The work introduces a lightweight autoregressive regression framework designed for
**microcontroller-class edge devices**, with an explicit focus on **long-horizon stability**
under autoregressive rollout.

Unlike recurrent or attention-based sequence models, COMET-SG1 advances predictions
through **memory-anchored transitions in a learned behavior space**, enabling bounded,
predictable inference suitable for deterministic embedded deployment.

---

## Abstract (Short)

Edge AI systems impose strict constraints on memory, computation, and long-horizon
stability. Many neural sequence models achieve competitive short-horizon accuracy
but exhibit unstable behavior when deployed autoregressively on constrained hardware.
COMET-SG1 addresses this limitation by encoding multi-scale temporal context into a
compact behavior space and advancing predictions via memory-anchored state transitions.
The resulting model avoids recurrence and attention, relies only on linear operations,
and exhibits bounded long-horizon behavior by construction, making it suitable for
ultra-low-power embedded systems.

---

## Key Characteristics

- Stability-oriented autoregressive inference
- Multi-scale temporal encoding (short / medium / long context)
- Behavior-space memory of observed transitions
- Weighted L1 distance matching
- Learned linear correction for reversal handling
- No recurrence, no attention, no deep stacks
- Fixed-point compatible operations
- Designed for Arduino- and Cortex-M–class hardware

---

## Motivation

In autoregressive deployment, small prediction errors compound over time, leading to
drift, oscillation, or collapse. This issue is especially problematic in edge settings,
where frequent re-anchoring to ground truth is infeasible.

COMET-SG1, proposed by **Shakhyar Gogoi**, addresses this by anchoring each update to
empirically observed behavior transitions rather than repeatedly applying a single-step
predictor.

---

## Embedded Feasibility

Inference consists exclusively of:
- Linear projections
- Absolute differences (L1 distance)
- Scalar weighting
- Vector accumulation

All operations are deterministic and compatible with fixed-point arithmetic, making
the model suitable for ultra-low-power embedded systems.

---

## Paper

The full paper is included in this repository:

**COMET-SG1: A Stability-Oriented Behavior-Space Autoregressive Regressor for Edge AI**  
Shakhyar Gogoi  
(PDF)

---

## Citation

If you use or reference this work, please cite the arXiv preprint:

S. Gogoi, “COMET-SG1: Lightweight Autoregressive Regressor for Edge and Embedded Systems,”  
arXiv:2601.20772, 2026. https://doi.org/10.48550/arXiv.2601.20772

<details>
<summary>BibTeX</summary>

```bibtex
@article{gogoi2026cometsg1,
  title   = {COMET-SG1: Lightweight Autoregressive Regressor for Edge and Embedded Systems},
  author  = {Gogoi, Shakhyar},
  journal = {arXiv preprint arXiv:2601.20772},
  year    = {2026},
  doi     = {10.48550/arXiv.2601.20772}
}
```

---

## Author

**Shakhyar Gogoi**  
Independent Researcher  
Focus: Edge AI, Time-Series Modeling, Autoregressive Systems
