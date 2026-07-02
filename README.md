# Awesome Embodied Systems [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A systems-first catalog of embodied intelligence and physical intelligence infrastructure.

This repository tracks named systems, not paper lists. Papers are included as technical evidence or entry points.

Language: English | [中文](./README.zh-CN.md)

## What Belongs Here

Core entries must satisfy three conditions:

- **Named system**: a platform, runtime, simulator, data engine, deployment stack, evaluation harness, fleet system, or other coherent system artifact.
- **Technical evidence**: a paper, preprint, technical report, or system paper that explains enough design for readers to learn from it.
- **Systems contribution**: the main contribution is a system mechanism or infrastructure, not only better model capability, training, representation, planning, or task performance.

Venue is metadata, not a gate. Systems may come from robotics, ML, CV, embodied AI, simulation, or systems venues if they satisfy the criteria.

## Catalog

Accepted systems are screened against the [curation criteria](./docs/curation-criteria.md) and organized under these provisional categories:

- **Runtime, Serving, and Deployment**: inference runtimes, serving systems, real-time control stacks, edge/cloud deployment systems, and execution infrastructure.
- **Simulation Infrastructure**: simulators and interactive environments for embodied workloads; evaluation harnesses only when they introduce reusable system mechanisms.
- **Data, Logging, and Experiment Infrastructure**: data collection systems, replay/logging tools, dataset infrastructure, experiment orchestration, and reproducibility tooling.
- **Robot Platforms and Fleet Systems**: robot learning platforms, fleet-scale systems, multi-robot infrastructure, and embodied-agent operation stacks.
- **Safety, Observability, and Reliability**: runtime safety systems, monitors, debugging tools, recovery mechanisms, reliability infrastructure, and operational lessons.

The categories are navigation aids, not a final taxonomy.

### Runtime, Serving, and Deployment

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| vla.cpp | Unified VLA inference runtime | [GitHub](https://github.com/VinRobotics/vla.cpp) ![stars](https://img.shields.io/github/stars/VinRobotics/vla.cpp?style=social) | [vla.cpp: A Unified Inference Runtime for Vision-Language-Action Models](https://arxiv.org/abs/2606.08094) | arXiv | 2026 |
| VLA-Perf | VLA inference performance modeling tool | [GitHub](https://github.com/NVlabs/vla-perf) ![stars](https://img.shields.io/github/stars/NVlabs/vla-perf?style=social) | [How Fast Can I Run My VLA? Demystifying VLA Inference Performance with VLA-Perf](https://arxiv.org/abs/2602.18397) | arXiv | 2026 |
| EfficientVLA | Training-free VLA inference acceleration framework | [GitHub (code coming soon)](https://github.com/YantaiYang-05/EfficientVLA) ![stars](https://img.shields.io/github/stars/YantaiYang-05/EfficientVLA?style=social) | [EfficientVLA: Training-Free Acceleration and Compression for Vision-Language-Action Models](https://arxiv.org/abs/2506.10100) | NeurIPS | 2025 |
| VLA-Cache | Adaptive VLA token caching framework | [GitHub](https://github.com/siyuhsu/vla-cache) ![stars](https://img.shields.io/github/stars/siyuhsu/vla-cache?style=social) | [VLA-Cache: Efficient Vision-Language-Action Manipulation via Adaptive Token Caching](https://papers.nips.cc/paper_files/paper/2025/hash/f062da1973ac9ac61fc6d44dd7fa309f-Abstract-Conference.html) | NeurIPS | 2025 |
| Spec-VLA | Speculative VLA decoding framework | [GitHub](https://github.com/PineTreeWss/SpecVLA) ![stars](https://img.shields.io/github/stars/PineTreeWss/SpecVLA?style=social) | [Spec-VLA: Speculative Decoding for Vision-Language-Action Models with Relaxed Acceptance](https://aclanthology.org/2025.emnlp-main.1367/) | EMNLP | 2025 |
| SpecPrune-VLA | Action-aware VLA token pruning framework | [GitHub](https://github.com/alexwhz-sjtu/SpecPrune-VLA) ![stars](https://img.shields.io/github/stars/alexwhz-sjtu/SpecPrune-VLA?style=social) | [SpecPrune-VLA: Accelerating Vision-Language-Action Models via Action-Aware Self-Speculative Pruning](https://arxiv.org/abs/2509.05614) | ICML | 2026 |
| Realtime-VLA FLASH | Speculative dVLA inference framework | [GitHub](https://github.com/dexmal/realtime-vla-flash) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-flash?style=social) | [Realtime-VLA FLASH: Speculative Inference Framework for Diffusion-based VLAs](https://arxiv.org/abs/2605.13778) | arXiv | 2026 |
| StreamingVLA | Streaming VLA execution framework | [GitHub](https://github.com/gen-robot/StreamingVLA) ![stars](https://img.shields.io/github/stars/gen-robot/StreamingVLA?style=social) | [StreamingVLA: Streaming Vision-Language-Action Model with Action Flow Matching and Adaptive Early Observation](https://arxiv.org/abs/2603.28565) | arXiv | 2026 |
| Realtime-VLA V2 | Real-world VLA deployment stack | [GitHub](https://github.com/dexmal/realtime-vla-v2) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-v2?style=social) | [Realtime-VLA V2: Learning to Run VLAs Fast, Smooth, and Accurate](https://arxiv.org/abs/2603.26360) | arXiv | 2026 |
| DORA | Dataflow robotics runtime | [GitHub](https://github.com/dora-rs/dora) ![stars](https://img.shields.io/github/stars/dora-rs/dora?style=social) | [DORA: Dataflow Oriented Robotic Architecture](https://arxiv.org/abs/2602.13252) | arXiv | 2026 |
| FogROS2 | Cloud/fog robotics deployment platform | [GitHub](https://github.com/BerkeleyAutomation/FogROS2) ![stars](https://img.shields.io/github/stars/BerkeleyAutomation/FogROS2?style=social) | [FogROS2: An Adaptive Platform for Cloud and Fog Robotics Using ROS 2](https://arxiv.org/abs/2205.09778) | arXiv | 2022 |
| micro-ROS | Embedded ROS 2 runtime | [micro_ros_setup](https://github.com/micro-ROS/micro_ros_setup) ![stars](https://img.shields.io/github/stars/micro-ROS/micro_ros_setup?style=social)<br>[micro_ros_arduino](https://github.com/micro-ROS/micro_ros_arduino) ![stars](https://img.shields.io/github/stars/micro-ROS/micro_ros_arduino?style=social) | [Micro-ROS](https://doi.org/10.1007/978-3-031-09062-2_2) | Springer | 2023 |
| PiCAS | ROS 2 executor scheduler | [GitHub](https://github.com/rtenlab/ros2-picas) ![stars](https://img.shields.io/github/stars/rtenlab/ros2-picas?style=social) | [PiCAS: New Design of Priority-Driven Chain-Aware Scheduling for ROS2](https://ieeexplore.ieee.org/document/9470466) | RTAS | 2021 |
| ROS-Phys-MC | Mixed-criticality ROS 2 scheduler | [GitHub](https://github.com/RTIS-Lab/ROS-Phys-MC) ![stars](https://img.shields.io/github/stars/RTIS-Lab/ROS-Phys-MC?style=social) | [Physics-Informed Mixed-Criticality Scheduling for F1Tenth Cars with Preemptable ROS 2 Executors](https://jwbaugh.github.io/papers/wilson-rtas-2025.pdf) | RTAS | 2025 |
| RTeX | Timing-predictable ROS 2 executor | [GitHub](https://github.com/ESLab2012/RTeX) ![stars](https://img.shields.io/github/stars/ESLab2012/RTeX?style=social) | [An Efficient and Timing-Predictable Multithreaded Executor for ROS 2](https://doi.org/10.1109/TCAD.2024.3380551) | IEEE TCAD | 2024 |

### Simulation Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| Habitat | Embodied AI simulation platform | [Habitat-Lab](https://github.com/facebookresearch/habitat-lab) ![stars](https://img.shields.io/github/stars/facebookresearch/habitat-lab?style=social)<br>[Habitat-Sim](https://github.com/facebookresearch/habitat-sim) ![stars](https://img.shields.io/github/stars/facebookresearch/habitat-sim?style=social) | [Habitat: A Platform for Embodied AI Research](https://arxiv.org/abs/1904.01201) | ICCV | 2019 |
| SAPIEN | Embodied manipulation simulation platform | [GitHub](https://github.com/haosulab/SAPIEN) ![stars](https://img.shields.io/github/stars/haosulab/SAPIEN?style=social) | [SAPIEN: A SimulAted Part-Based Interactive ENvironment](https://arxiv.org/abs/2003.08515) | CVPR | 2020 |

### Data, Logging, and Experiment Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| ALOHA | Bimanual teleoperation platform | [GitHub](https://github.com/tonyzhaozh/aloha) ![stars](https://img.shields.io/github/stars/tonyzhaozh/aloha?style=social) | [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://arxiv.org/abs/2304.13705) | RSS | 2023 |
| GELLO | Low-cost teleoperation hardware/software | [Software](https://github.com/wuphilipp/gello_software) ![stars](https://img.shields.io/github/stars/wuphilipp/gello_software?style=social)<br>[Hardware](https://github.com/wuphilipp/gello_mechanical) ![stars](https://img.shields.io/github/stars/wuphilipp/gello_mechanical?style=social) | [GELLO: A General, Low-Cost, and Intuitive Teleoperation Framework for Robot Manipulators](https://arxiv.org/abs/2309.13037) | IROS | 2024 |
| UMI | In-the-wild demonstration collection system | [GitHub](https://github.com/real-stanford/universal_manipulation_interface) ![stars](https://img.shields.io/github/stars/real-stanford/universal_manipulation_interface?style=social) | [Universal Manipulation Interface: In-The-Wild Robot Teaching Without In-The-Wild Robots](https://arxiv.org/abs/2402.10329) | RSS | 2024 |
| MimicGen | Demonstration data generation system | [GitHub](https://github.com/NVlabs/mimicgen) ![stars](https://img.shields.io/github/stars/NVlabs/mimicgen?style=social) | [MimicGen: A Data Generation System for Scalable Robot Learning using Human Demonstrations](https://arxiv.org/abs/2310.17596) | CoRL | 2023 |
| RoboGen | Generative simulation pipeline | [GitHub](https://github.com/Genesis-Embodied-AI/RoboGen) ![stars](https://img.shields.io/github/stars/Genesis-Embodied-AI/RoboGen?style=social) | [RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://proceedings.mlr.press/v235/wang24cc.html) | ICML | 2024 |

### Safety, Observability, and Reliability

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| ros2_tracing | ROS 2 tracing tool | [GitHub](https://github.com/ros2/ros2_tracing) ![stars](https://img.shields.io/github/stars/ros2/ros2_tracing?style=social) | [ros2_tracing: Multipurpose Low-Overhead Framework for Real-Time Tracing of ROS 2](https://arxiv.org/abs/2201.00393) | IEEE RA-L | 2022 |
| CARET | ROS 2 latency analysis tool | [GitHub](https://github.com/tier4/CARET) ![stars](https://img.shields.io/github/stars/tier4/CARET?style=social) | [CARET: Chain-Aware ROS 2 Evaluation Tool](https://ieeexplore.ieee.org/document/10086380) | EUC | 2022 |
| TILDE | ROS 2 dynamic message tracking tool | [GitHub](https://github.com/tier4/TILDE) ![stars](https://img.shields.io/github/stars/tier4/TILDE?style=social) | [TILDE: Topic-Tracking Infrastructure for Dynamic Message Latency and Deadline Evaluator for ROS 2 Application](https://doi.org/10.1109/DS-RT58998.2023.00010) | DS-RT | 2023 |

## Entry Format

Accepted entries use this schema:

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

- `Type` is a short provisional label.
- `Code / Artifact` contains at most one or two primary official entry points.
- If code is not released yet for an accepted system paper, mark the official repository status explicitly.
- GitHub entries include a live stars badge:

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- Multiple relevant papers are listed from earliest to latest; venues follow the same order.
- `Year` is the first representative public year, usually the first relevant paper year.

## Not in Scope

Excluded by default unless there is substantial system-level design:

- Standalone models, policies, losses, representations, action-tokenization tricks, prompting methods, planning methods, or training recipes.
- Model-specific inference repositories or narrow demo wrappers.
- Demo-only systems, marketing pages, news posts, videos, and fundraising announcements.
- General robotics middleware, drivers, navigation stacks, or control frameworks not tied to embodied intelligence workloads.
- General graphics or physics engines without an embodied-AI-specific system layer.
- Surveys, course pages, reading lists, awesome lists, leaderboards, and other meta resources.

## Maintenance

See [Curation Criteria](./docs/curation-criteria.md) for the screening rubric.

When updating this README, update [README.zh-CN.md](./README.zh-CN.md) in the same change. The two READMEs should stay structurally and semantically synchronized, but the Chinese version does not need to be a sentence-by-sentence translation.
