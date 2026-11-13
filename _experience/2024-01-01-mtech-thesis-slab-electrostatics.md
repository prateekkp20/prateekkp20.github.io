---
title: "Fast and Accurate Electrostatics for Slab (2D-Periodic) Systems"
collection: experience
type: "Research"
venue: "M.Tech. Thesis, IIT Kanpur"
date: 2024-01-01
period: "Jan 2024 – Jul 2025"
excerpt: "Advised by Dr. Vishal Agarwal and Dr. Swarnendu Biswas. Developed THE2D, a top-hat-function formulation of Ewald summation for slab systems, 13.6× cheaper than 2D-PME at matched accuracy."
---

Advisors: Dr. Vishal Agarwal (Dept. of Chemical Engineering) and Dr. Swarnendu Biswas (Dept. of Computer Science & Engineering), IIT Kanpur.

- Developed *THE2D*, a top-hat-function formulation of Ewald summation for slab systems, recasting a closed-form direct sum.
- Incorporated FFT-accelerated Particle-Mesh Ewald evaluation of the formulation, reducing computational cost from O(N²) to O(N log N).
- Validated against an exact 2D Ewald reference (2D-PHL-Ewald): relative error < 10⁻⁶ in energies across a range of window parameters and neutral systems of 1k–15k ions; derived parameter guidelines for trading accuracy against cost.
- Implemented the formulation in C++ with OpenMP and FFTW-based particle-mesh Ewald: **120–180× faster** than direct summation for systems of up to 25k ions, and a 5.4× speedup on 6 physical cores.
- Applied profiling-guided optimization (Intel VTune) to identify real-space kernel bottlenecks; replaced exact error-function evaluation with a polynomial approximation, reducing runtime by ~30% while preserving < 10⁻⁷ numerical accuracy.
- Benchmarked against the established 2D-PME method (Kawata et al., 2001) at matched accuracy, achieving a **13.6× lower runtime cost** for a 10k-ion system and cutting the estimated wall-clock time of a 1 ns MD trajectory from 19.1 to 1.4 days.
