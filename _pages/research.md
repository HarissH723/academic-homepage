---
layout: page
title: Research
permalink: /research/
description: Memristor and RRAM devices, in-memory and neuromorphic computing, device-aware continual learning, and efficient AI hardware.
nav: true
nav_order: 2
---

My research connects the physics of emerging memory devices with learning algorithms and hardware systems. I am most interested in what becomes possible when device behavior — variability, stochasticity, temporal dynamics, and programming constraints — is treated as part of the design, rather than as an imperfection to suppress.

The thread running through my work is a single question: how does a learning algorithm change when the physical cost of writing a weight is made explicit?

<div class="qs-divider" role="presentation"><span>◇</span></div>

## Adaptive resistive-memory programming for continual learning

**Zhongrui Wang Lab, Southern University of Science and Technology · July 2024 – present**

Resistive memory stores a weight as a physical conductance, so every weight update is a real programming event with energy cost, stochasticity, and accuracy consequences. In class-incremental learning this matters twice over: the network must keep learning new classes without overwriting what it already knows, while the hardware must not spend programming effort uniformly across all weights.

Our work studies **adaptive programming** for redox resistive memory: instead of updating the whole array, we examine how programming stochasticity and the relative importance of individual weights can be used to decide _which_ weights deserve a careful, repeated update and which do not. Selectively updating high-impact weights reduces programming overhead and mitigates forgetting.

**What I contributed**

- Python-based simulation of device variability in two-dimensional memristor arrays, including stochastic programming behavior.
- Device-variability-aware programming experiments, and robustness-testing workflows that I refined together with my mentor into the final evaluation protocol.
- Class-incremental learning experiments with MobileNet on CIFAR-100, including the training and data-loading pipelines.
- Analysis and visualization of intermediate representations and prediction behavior: PCA, t-SNE, feature maps, and confusion matrices.

The resulting study appeared in _Advanced Materials_ (2026) as a co-first-authored paper. [Publication and DOI]({{ '/publications/' | relative_url }}).

<div class="qs-divider" role="presentation"><span>◇</span></div>

## Semiconductor device fabrication and characterization

**SUSTech cleanroom · March – May 2026**

I fabricated and characterized Ta/Al₂O₃ capacitor structures, following a complete process flow rather than isolated steps:

- **Cleaning and patterning** — RCA cleaning, photolithography, and overlay alignment.
- **Deposition** — LPCVD, atomic layer deposition (ALD), and Ta sputtering.
- **Structuring and treatment** — ICP dry etching and rapid thermal processing (RTP).
- **Characterization** — C–V measurements and SEM-based failure analysis.

The interesting part was not the equipment list but the causal chain: how oxidation of tantalum, interface condition, and process variation propagate into measured capacitance and device integrity. Cleanroom work made the gap between an idealized device model and a real, repeatable device very concrete, and it is the main reason I want device physics to inform — rather than merely constrain — my algorithmic work.

<div class="qs-divider" role="presentation"><span>◇</span></div>

## Broader hardware and system experience

This is not my primary research direction, but it keeps my device-level work anchored to circuit- and system-level constraints.

- **Digital design** — a five-stage pipelined RV32I processor in Verilog, including control and hazard handling, a two-bit saturating-counter branch predictor, and a four-way set-associative cache; verified on a Xilinx Nexys A7 FPGA at 185 MHz.
- **Circuits and process** — 0.18 μm CMOS two-stage operational amplifiers in Virtuoso (five-transistor OTA versus folded-cascode), a 6×6 carry-save multiplier from schematic to post-layout verification, and CMOS process simulation in Silvaco ATHENA.
- **Embodied AI** — vision-language-action manipulation with SO-101 (LeRobot, Isaac Sim) and Unitree G1-D (data collection and conversion, SmolVLA inference and deployment), plus parameter-efficient GR00T fine-tuning and residual reinforcement learning for imitation-policy error compensation.

[See the projects]({{ '/projects/' | relative_url }}) for details of each.
