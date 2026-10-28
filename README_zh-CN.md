<div align="center">

# Awesome SuperMimic Community

[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: CC0](https://img.shields.io/badge/License-CC0_1.0-blue.svg)](LICENSE)

**[SuperMimic](https://arxiv.org/abs/2610.28480) 社区中枢：深度解读、复现追踪与上下游技术栈——单 GPU、可微世界模型训练人形全身控制。**

[English](README.md) · 简体中文

</div>

---

> **非官方补充清单。** 实现与扩展请先看主清单
> [DiaoOrg/awesome-supermimic](https://github.com/DiaoOrg/awesome-supermimic)。
> 本清单覆盖主清单不做的事：论文精读（含中文解读区）、状态化复现追踪、研究谱系与底层工具链。

**一句话为什么重要：** SuperMimic 用 **1 块 H100 训练 3 小时**，超越了 7 天 × 128 GPU 的
SOTA 基线（SONIC）——GPU 时缩减超 1000 倍，129,514 个动作零失败，真机 Unitree G1 部署。

## 论文与官方

- [论文 (arXiv 2610.28480)](https://arxiv.org/abs/2610.28480)
- [项目主页](https://supermimic.github.io/) — 亮点、算力对比图、真机 G1 视频
- [浏览器 Demo](https://supermimic.github.io/demo/) — 在网页里跑策略
- [DiaoOrg/awesome-supermimic](https://github.com/DiaoOrg/awesome-supermimic) — 官方主清单

## 深度解读与阅读

解读、精读、讲义式拆解，欢迎多语言。

- （章节开设中——欢迎 PR，中文解读尤其稀缺）

## 复现追踪

第三方复现与扩展，带状态。一项一行。

| 复现 | 硬件 | 状态 | 备注 |
|---|---|---|---|
| （暂无——欢迎 PR，格式见下） | | | |

行格式：`| [仓库/页面](链接) \| GPU 型号 \| ✅ 已复现 / 🔄 进行中 / ⚠️ 部分 / ❌ 卡住 \| 一句话结论 |`

## 研究谱系与工具链

SuperMimic 从哪来，跑在什么上面。

**世界模型谱系**

- [dreamerv3 (danijar)](https://github.com/danijar/dreamerv3) — 世界模型训练线，让"学动力学、在模型里规划"成为控制的主流范式。
- Genie（DeepMind）— 生成式可交互世界模型，"学习型仿真器"前提的奠基。（论文系列，无官方开源码。）

**仿真与训练栈**

- [google-deepmind/mujoco_warp](https://github.com/google-deepmind/mujoco_warp) — GPU 加速 MuJoCo；循环里"接触物理收集"一侧。
- [mujocolab/mjlab](https://github.com/mujocolab/mjlab) — MuJoCo Warp 上的 Isaac Lab API，可组合环境构件。
- [leggedrobotics/rsl_rl](https://github.com/leggedrobotics/rsl_rl) — 现代运动控制栈通用的 PPO 实现谱系。
- [Rhoban/bam](https://github.com/Rhoban/bam) — 低成本舵机的扩展摩擦模型；这个量级硬件的 sim2real 桥。

**被超越的基线**

- SONIC — 论文对照的 SOTA 动作跟踪器（7 天 × 128 GPU），见论文对比章节。

## 同期低算力工作

SuperMimic 所处的"算力塌方"大潮——单卡或无卡。

- [aalmuzairee/squint](https://github.com/aalmuzairee/squint) — 视觉 SAC 分钟级解决 SO-101 机械臂任务（UCSD）。
- [jonathanhawkins/microduck-lab](https://github.com/jonathanhawkins/microduck-lab) — 普通 Mac 无 CUDA 训练双足 RL，浏览器实时查看。
- [pollen-robotics/microduck_rl](https://github.com/pollen-robotics/microduck_rl) — 800g 双足的全开源 sim2real 配方（mjlab + PPO）。

## 贡献

见 [CONTRIBUTING.md](CONTRIBUTING.md)。短版：一条一链、一句为什么；复现行必须带状态证据；禁止署名水印。

## 许可

[CC0-1.0](LICENSE)
