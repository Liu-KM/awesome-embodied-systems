# Awesome Embodied Systems [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 一个系统优先的具身智能和物理智能基础设施目录。

本仓库收录有明确名称的系统，不做普通论文列表。论文只作为技术证据或入口。

语言：[English](./README.md) | 中文

## 收录标准

核心条目必须满足三个条件：

- **有明确名称的系统**：平台、runtime、仿真器、数据引擎、部署栈、评测 harness、fleet 系统或其他完整系统 artifact。
- **有技术证据**：paper、preprint、technical report 或 system paper，能让读者学到系统设计。
- **有系统贡献**：主要贡献是系统机制或基础设施，而不只是模型能力、训练、表示、planning 或任务表现提升。

Venue 是 metadata，不是入选门槛。只要满足标准，系统可以来自 robotics、ML、CV、embodied AI、simulation 或 systems venue。

## 目录

通过筛选的系统会按 [curation criteria](./docs/curation-criteria.md) 审核，并先放在以下临时分类下：

- **Runtime, Serving, and Deployment**：推理 runtime、serving 系统、实时控制栈、边云部署系统和执行基础设施。
- **Simulation Infrastructure**：面向具身 workload 的仿真器和交互环境；只有引入可复用系统机制的 evaluation harness 才收录。
- **Data, Logging, and Experiment Infrastructure**：数据采集系统、回放和日志工具、数据集基础设施、实验编排和可复现工具。
- **Robot Platforms and Fleet Systems**：机器人学习平台、fleet-scale 系统、多机器人基础设施和具身 agent 运行栈。
- **Safety, Observability, and Reliability**：运行时安全系统、监控、调试工具、恢复机制、可靠性基础设施和运维经验。

这些分类只是导航，不是最终 taxonomy。

### Runtime, Serving, and Deployment

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| vla.cpp | 统一 VLA 推理 runtime | [GitHub](https://github.com/VinRobotics/vla.cpp) ![stars](https://img.shields.io/github/stars/VinRobotics/vla.cpp?style=social) | [vla.cpp: A Unified Inference Runtime for Vision-Language-Action Models](https://arxiv.org/abs/2606.08094) | arXiv | 2026 |
| VLA-Perf | VLA 推理性能建模工具 | [GitHub](https://github.com/NVlabs/vla-perf) ![stars](https://img.shields.io/github/stars/NVlabs/vla-perf?style=social) | [How Fast Can I Run My VLA? Demystifying VLA Inference Performance with VLA-Perf](https://arxiv.org/abs/2602.18397) | arXiv | 2026 |
| EfficientVLA | training-free VLA 推理加速框架 | [GitHub (code coming soon)](https://github.com/YantaiYang-05/EfficientVLA) ![stars](https://img.shields.io/github/stars/YantaiYang-05/EfficientVLA?style=social) | [EfficientVLA: Training-Free Acceleration and Compression for Vision-Language-Action Models](https://arxiv.org/abs/2506.10100) | NeurIPS | 2025 |
| VLA-Cache | 自适应 VLA token caching 框架 | [GitHub](https://github.com/siyuhsu/vla-cache) ![stars](https://img.shields.io/github/stars/siyuhsu/vla-cache?style=social) | [VLA-Cache: Efficient Vision-Language-Action Manipulation via Adaptive Token Caching](https://papers.nips.cc/paper_files/paper/2025/hash/f062da1973ac9ac61fc6d44dd7fa309f-Abstract-Conference.html) | NeurIPS | 2025 |
| Spec-VLA | VLA speculative decoding 框架 | [GitHub](https://github.com/PineTreeWss/SpecVLA) ![stars](https://img.shields.io/github/stars/PineTreeWss/SpecVLA?style=social) | [Spec-VLA: Speculative Decoding for Vision-Language-Action Models with Relaxed Acceptance](https://aclanthology.org/2025.emnlp-main.1367/) | EMNLP | 2025 |
| SpecPrune-VLA | action-aware VLA token pruning 框架 | [GitHub](https://github.com/alexwhz-sjtu/SpecPrune-VLA) ![stars](https://img.shields.io/github/stars/alexwhz-sjtu/SpecPrune-VLA?style=social) | [SpecPrune-VLA: Accelerating Vision-Language-Action Models via Action-Aware Self-Speculative Pruning](https://arxiv.org/abs/2509.05614) | ICML | 2026 |
| Realtime-VLA FLASH | speculative dVLA 推理框架 | [GitHub](https://github.com/dexmal/realtime-vla-flash) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-flash?style=social) | [Realtime-VLA FLASH: Speculative Inference Framework for Diffusion-based VLAs](https://arxiv.org/abs/2605.13778) | arXiv | 2026 |
| StreamingVLA | 流式 VLA 执行框架 | [GitHub](https://github.com/gen-robot/StreamingVLA) ![stars](https://img.shields.io/github/stars/gen-robot/StreamingVLA?style=social) | [StreamingVLA: Streaming Vision-Language-Action Model with Action Flow Matching and Adaptive Early Observation](https://arxiv.org/abs/2603.28565) | arXiv | 2026 |
| Realtime-VLA V2 | 真实机器人 VLA 部署栈 | [GitHub](https://github.com/dexmal/realtime-vla-v2) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-v2?style=social) | [Realtime-VLA V2: Learning to Run VLAs Fast, Smooth, and Accurate](https://arxiv.org/abs/2603.26360) | arXiv | 2026 |
| DORA | 数据流机器人 runtime | [GitHub](https://github.com/dora-rs/dora) ![stars](https://img.shields.io/github/stars/dora-rs/dora?style=social) | [DORA: Dataflow Oriented Robotic Architecture](https://arxiv.org/abs/2602.13252) | arXiv | 2026 |
| FogROS2 | 云/雾机器人部署平台 | [GitHub](https://github.com/BerkeleyAutomation/FogROS2) ![stars](https://img.shields.io/github/stars/BerkeleyAutomation/FogROS2?style=social) | [FogROS2: An Adaptive Platform for Cloud and Fog Robotics Using ROS 2](https://arxiv.org/abs/2205.09778) | arXiv | 2022 |
| micro-ROS | 嵌入式 ROS 2 runtime | [micro_ros_setup](https://github.com/micro-ROS/micro_ros_setup) ![stars](https://img.shields.io/github/stars/micro-ROS/micro_ros_setup?style=social)<br>[micro_ros_arduino](https://github.com/micro-ROS/micro_ros_arduino) ![stars](https://img.shields.io/github/stars/micro-ROS/micro_ros_arduino?style=social) | [Micro-ROS](https://doi.org/10.1007/978-3-031-09062-2_2) | Springer | 2023 |
| PiCAS | ROS 2 executor 调度器 | [GitHub](https://github.com/rtenlab/ros2-picas) ![stars](https://img.shields.io/github/stars/rtenlab/ros2-picas?style=social) | [PiCAS: New Design of Priority-Driven Chain-Aware Scheduling for ROS2](https://ieeexplore.ieee.org/document/9470466) | RTAS | 2021 |
| ROS-Phys-MC | 混合关键性 ROS 2 调度器 | [GitHub](https://github.com/RTIS-Lab/ROS-Phys-MC) ![stars](https://img.shields.io/github/stars/RTIS-Lab/ROS-Phys-MC?style=social) | [Physics-Informed Mixed-Criticality Scheduling for F1Tenth Cars with Preemptable ROS 2 Executors](https://jwbaugh.github.io/papers/wilson-rtas-2025.pdf) | RTAS | 2025 |
| RTeX | timing-predictable ROS 2 executor | [GitHub](https://github.com/ESLab2012/RTeX) ![stars](https://img.shields.io/github/stars/ESLab2012/RTeX?style=social) | [An Efficient and Timing-Predictable Multithreaded Executor for ROS 2](https://doi.org/10.1109/TCAD.2024.3380551) | IEEE TCAD | 2024 |

### Simulation Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| Habitat | 具身 AI 仿真平台 | [Habitat-Lab](https://github.com/facebookresearch/habitat-lab) ![stars](https://img.shields.io/github/stars/facebookresearch/habitat-lab?style=social)<br>[Habitat-Sim](https://github.com/facebookresearch/habitat-sim) ![stars](https://img.shields.io/github/stars/facebookresearch/habitat-sim?style=social) | [Habitat: A Platform for Embodied AI Research](https://arxiv.org/abs/1904.01201) | ICCV | 2019 |
| SAPIEN | 具身操作仿真平台 | [GitHub](https://github.com/haosulab/SAPIEN) ![stars](https://img.shields.io/github/stars/haosulab/SAPIEN?style=social) | [SAPIEN: A SimulAted Part-Based Interactive ENvironment](https://arxiv.org/abs/2003.08515) | CVPR | 2020 |

### Data, Logging, and Experiment Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| ALOHA | 双臂遥操作平台 | [GitHub](https://github.com/tonyzhaozh/aloha) ![stars](https://img.shields.io/github/stars/tonyzhaozh/aloha?style=social) | [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://arxiv.org/abs/2304.13705) | RSS | 2023 |
| GELLO | 低成本遥操作软硬件 | [Software](https://github.com/wuphilipp/gello_software) ![stars](https://img.shields.io/github/stars/wuphilipp/gello_software?style=social)<br>[Hardware](https://github.com/wuphilipp/gello_mechanical) ![stars](https://img.shields.io/github/stars/wuphilipp/gello_mechanical?style=social) | [GELLO: A General, Low-Cost, and Intuitive Teleoperation Framework for Robot Manipulators](https://arxiv.org/abs/2309.13037) | IROS | 2024 |
| UMI | 野外示教采集系统 | [GitHub](https://github.com/real-stanford/universal_manipulation_interface) ![stars](https://img.shields.io/github/stars/real-stanford/universal_manipulation_interface?style=social) | [Universal Manipulation Interface: In-The-Wild Robot Teaching Without In-The-Wild Robots](https://arxiv.org/abs/2402.10329) | RSS | 2024 |
| MimicGen | 示教数据生成系统 | [GitHub](https://github.com/NVlabs/mimicgen) ![stars](https://img.shields.io/github/stars/NVlabs/mimicgen?style=social) | [MimicGen: A Data Generation System for Scalable Robot Learning using Human Demonstrations](https://arxiv.org/abs/2310.17596) | CoRL | 2023 |
| RoboGen | 生成式仿真 pipeline | [GitHub](https://github.com/Genesis-Embodied-AI/RoboGen) ![stars](https://img.shields.io/github/stars/Genesis-Embodied-AI/RoboGen?style=social) | [RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://proceedings.mlr.press/v235/wang24cc.html) | ICML | 2024 |

### Safety, Observability, and Reliability

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| ros2_tracing | ROS 2 tracing 工具 | [GitHub](https://github.com/ros2/ros2_tracing) ![stars](https://img.shields.io/github/stars/ros2/ros2_tracing?style=social) | [ros2_tracing: Multipurpose Low-Overhead Framework for Real-Time Tracing of ROS 2](https://arxiv.org/abs/2201.00393) | IEEE RA-L | 2022 |
| CARET | ROS 2 延迟分析工具 | [GitHub](https://github.com/tier4/CARET) ![stars](https://img.shields.io/github/stars/tier4/CARET?style=social) | [CARET: Chain-Aware ROS 2 Evaluation Tool](https://ieeexplore.ieee.org/document/10086380) | EUC | 2022 |
| TILDE | ROS 2 动态消息追踪工具 | [GitHub](https://github.com/tier4/TILDE) ![stars](https://img.shields.io/github/stars/tier4/TILDE?style=social) | [TILDE: Topic-Tracking Infrastructure for Dynamic Message Latency and Deadline Evaluator for ROS 2 Application](https://doi.org/10.1109/DS-RT58998.2023.00010) | DS-RT | 2023 |

## 条目格式

通过筛选的条目使用这套字段：

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

- `Type` 是临时短标签。
- `Code / Artifact` 最多放一到两个主要官方入口。
- 如果已接收的系统论文还没有发布代码，需要明确标注官方仓库状态。
- GitHub 条目加入实时 stars badge：

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- 多篇相关论文按系统发展时间从早到晚列出；`Venue` 使用相同顺序。
- `Year` 是系统首次公开的代表年份，通常是第一篇相关论文年份。

## 默认不收录

除非包含实质性的系统级设计，以下内容默认不收录：

- 单纯模型、policy、loss、表示、action-tokenization trick、prompting 方法、planning 方法或训练 recipe。
- 针对单个模型的 inference repo 或狭窄 demo wrapper。
- 只有 demo、营销页、新闻稿、视频或融资公告的系统。
- 没有绑定具身智能 workload 的通用机器人 middleware、driver、navigation stack 或控制框架。
- 没有 embodied-AI-specific system layer 的通用图形或物理引擎。
- survey、课程页、reading list、awesome list、leaderboard 和其他 meta resource。

## 维护

筛选规则见 [Curation Criteria](./docs/curation-criteria.md)。

更新本 README 时，需要同步更新 [README.md](./README.md)。中英文 README 应保持结构和语义同步，但中文版本不需要逐句直译英文。
