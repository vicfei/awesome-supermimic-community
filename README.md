<div align="center">

# Awesome SuperMimic Community

[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: CC0](https://img.shields.io/badge/License-CC0_1.0-blue.svg)](LICENSE)

**Community hub for [SuperMimic](https://arxiv.org/abs/2610.28480): deep dives, reproduction tracking, and the surrounding stack — humanoid whole-body control trained through a differentiable world model on a single GPU.**

English · [简体中文](README_zh-CN.md)

</div>

---

> **Unofficial supplement.** For implementations, extensions and demos, the primary list is
> [DiaoOrg/awesome-supermimic](https://github.com/DiaoOrg/awesome-supermimic) — go there first.
> This list covers what a primary list doesn't: paper deep-dives (with a Chinese-reading
> section), a status-tracked reproduction board, the research lineage, and the toolchain
> underneath.

**Why it matters in one line:** SuperMimic trains a humanoid motion tracker in **3 hours on
one H100**, surpassing a 7-day / 128-GPU baseline (SONIC) — a >1000× reduction in GPU-hours,
zero failed motions out of 129,514, deployed on a real Unitree G1.

## Paper & Official

- [Paper (arXiv 2610.28480)](https://arxiv.org/abs/2610.28480)
- [Project page](https://supermimic.github.io/) — highlights, compute charts, real-G1 footage
- [Browser demo](https://supermimic.github.io/demo/) — run the policy in your browser
- [DiaoOrg/awesome-supermimic](https://github.com/DiaoOrg/awesome-supermimic) — the primary list

## Deep dives & readings

Interpretations, walk-throughs, and lecture-style breakdowns. Multi-language welcome.

- *(section opening — PRs welcome; Chinese-language readings especially wanted)*

## Reproduction tracker

Third-party reproductions and extensions, with status. One row per effort.

| Effort | Hardware | Status | Notes |
|---|---|---|---|
| *(none tracked yet — PRs welcome, see format below)* | | | |

Row format: `| [repo/page](link) \| GPU \| ✅ reproduced / 🔄 in progress / ⚠️ partial / ❌ blocked \| one-line takeaway |`

## Lineage & toolchain

Where SuperMimic comes from, and the stack it runs on.

**World-model lineage**

- [dreamerv3 (danijar)](https://github.com/danijar/dreamerv3) — the world-model training line that made "learn the dynamics, plan inside it" mainstream for control.
- Genie (DeepMind) — generative interactive world models; foundation of the "learned simulator" premise. (Papers, no official open code.)

**Simulator & training stack**

- [google-deepmind/mujoco_warp](https://github.com/google-deepmind/mujoco_warp) — GPU-accelerated MuJoCo; the contact-physics collector side of the loop.
- [mujocolab/mjlab](https://github.com/mujocolab/mjlab) — Isaac Lab API on MuJoCo Warp; composable env building blocks.
- [leggedrobotics/rsl_rl](https://github.com/leggedrobotics/rsl_rl) — the PPO implementation lineage used across modern locomotion stacks.
- [Rhoban/bam](https://github.com/Rhoban/bam) — extended friction models for low-cost servo actuators; the sim2real bridge for hardware in this weight class.

**The baseline it beat**

- SONIC — state-of-the-art motion tracker referenced in the paper (7 days × 128 GPUs). See paper §comparisons.

## Parallel low-compute works

The broader "compute collapse" wave SuperMimic rides — one GPU or none.

- [aalmuzairee/squint](https://github.com/aalmuzairee/squint) — visual SAC solving SO-101 arm tasks in minutes of training (UCSD).
- [jonathanhawkins/microduck-lab](https://github.com/jonathanhawkins/microduck-lab) — RL biped policies trained on a plain Mac, no CUDA, live browser viewer.
- [pollen-robotics/microduck_rl](https://github.com/pollen-robotics/microduck_rl) — full open sim2real recipe (mjlab + PPO) for a 800 g biped.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Short version: one link per bullet, one line why;
reproduction rows must carry status evidence; no attribution watermarks.

## License

[CC0-1.0](LICENSE)
