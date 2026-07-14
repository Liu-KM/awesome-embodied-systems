# Awesome Embodied Systems [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A systems-first catalog for embodied foundation models.

This repository tracks named systems whose primary purpose is to train, serve, deploy, simulate, evaluate, or safeguard embodied foundation models such as vision-language-action models (VLAs) and world-action models (WAMs). It is not a general robotics infrastructure list or a list of VLA/WAM papers.

Language: English | [中文](./README.zh-CN.md)

## What Belongs Here

An entry must pass all three gates:

- **Embodied-foundation-model scope**: the primary workload is a VLA, WAM, embodied VLM/LLM, or infrastructure designed specifically for these models. Using an LLM or VLM once inside an otherwise conventional robotics pipeline is not enough.
- **Systems contribution**: the work introduces a named, reusable runtime, serving layer, training or data system, deployment mechanism, neural simulator, evaluation environment, or reliability mechanism. Model-system co-design qualifies only when it exposes an explicit system mechanism and evaluates system bottlenecks.
- **Evidence and maturity**: the system has technical evidence that explains its design. If it was first made public more than 12 months ago, it must also have at least one community-recognition signal: 20+ citations, a formal peer-reviewed archival publication, or an official GitHub repository with 100+ stars. Recent systems without a recognition signal may be listed provisionally and are rechecked once they become more than 12 months old.

The gates are cumulative: recognition cannot rescue a generic robotics system or a model-only contribution. See the [curation criteria](./docs/curation-criteria.md) for the operational rules.

## Catalog

Accepted systems are organized by the part of the embodied-foundation-model lifecycle that they make practical:

- **Inference, Runtime, and Deployment**: execution engines, serving and scheduling mechanisms, performance tools, and real-robot deployment stacks.
- **Training, Post-training, and Data Systems**: distributed training, online learning, fleet feedback loops, world-model post-training environments, and foundation-model-scale robot data infrastructure.
- **Neural Simulation and Evaluation**: reusable world-model simulators and evaluation environments for embodied-foundation-model policies.

The categories are navigation aids, not a final taxonomy.

### Inference, Runtime, and Deployment

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| vla.cpp | Unified VLA inference runtime | [GitHub](https://github.com/VinRobotics/vla.cpp) ![stars](https://img.shields.io/github/stars/VinRobotics/vla.cpp?style=social) | [Paper](https://arxiv.org/abs/2606.08094) | arXiv | 2026 |
| Embodied.cpp | Portable VLA/WAM inference and control runtime | [GitHub](https://github.com/SEU-PAISys/Embodied.cpp) ![stars](https://img.shields.io/github/stars/SEU-PAISys/Embodied.cpp?style=social) | [Paper](https://arxiv.org/abs/2607.02501) | arXiv | 2026 |
| VLA-Perf | VLA inference performance modeling tool | [GitHub](https://github.com/NVlabs/vla-perf) ![stars](https://img.shields.io/github/stars/NVlabs/vla-perf?style=social) | [Paper](https://arxiv.org/abs/2602.18397) | arXiv | 2026 |
| VLA-Cache | Adaptive VLA token caching framework | [GitHub](https://github.com/siyuhsu/vla-cache) ![stars](https://img.shields.io/github/stars/siyuhsu/vla-cache?style=social) | [Paper](https://papers.nips.cc/paper_files/paper/2025/hash/f062da1973ac9ac61fc6d44dd7fa309f-Abstract-Conference.html) | NeurIPS | 2025 |
| Spec-VLA | Speculative VLA decoding framework | [GitHub](https://github.com/PineTreeWss/SpecVLA) ![stars](https://img.shields.io/github/stars/PineTreeWss/SpecVLA?style=social) | [Paper](https://aclanthology.org/2025.emnlp-main.1367/) | EMNLP | 2025 |
| Realtime-VLA FLASH | Speculative dVLA inference framework | [GitHub](https://github.com/dexmal/realtime-vla-flash) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-flash?style=social) | [Paper](https://arxiv.org/abs/2605.13778) | arXiv | 2026 |
| VLASH | Future-state-aware asynchronous VLA inference framework | [GitHub](https://github.com/mit-han-lab/vlash) ![stars](https://img.shields.io/github/stars/mit-han-lab/vlash?style=social) | [Paper](https://arxiv.org/abs/2512.01031) | arXiv | 2025 |
| Realtime-VLA V2 | Real-world VLA deployment stack | [GitHub](https://github.com/dexmal/realtime-vla-v2) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-v2?style=social) | [Paper](https://arxiv.org/abs/2603.26360) | arXiv | 2026 |
| Corki | Embodied-LLM inference, communication, and control co-design | [GitHub](https://github.com/hyy02/Corki) ![stars](https://img.shields.io/github/stars/hyy02/Corki?style=social) | [Paper](https://arxiv.org/abs/2407.04292) | ISCA | 2025 |
| TimelyLLM | Physical-execution-aware embodied LLM serving system | No public implementation located | [Paper](https://www.sigmobile.org/mobisys/2026/program/) | MobiSys | 2026 |

### Training, Post-training, and Data Systems

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| RLinf / RLinf-VLA | Scalable VLA RL and real-world post-training system | [GitHub](https://github.com/RLinf/RLinf) ![stars](https://img.shields.io/github/stars/RLinf/RLinf?style=social) | [System](https://www.usenix.org/conference/osdi26/presentation/yu-chao)<br>[VLA](https://arxiv.org/abs/2510.06710) | OSDI | 2026 |
| SOP / Learning While Deploying | Fleet-scale online VLA post-training system | Code unavailable for both: [SOP project](https://www.agibot.com/research/sop)<br>[LWD project](https://finch.agibot.com/research/lwd) | [SOP](https://arxiv.org/abs/2601.03044)<br>[LWD](https://arxiv.org/abs/2605.00416) | arXiv | 2026 |
| VLA Foundry | Unified LLM-to-VLM-to-VLA training framework | [GitHub](https://github.com/TRI-ML/vla_foundry) ![stars](https://img.shields.io/github/stars/TRI-ML/vla_foundry?style=social) | [Paper](https://arxiv.org/abs/2604.19728) | arXiv | 2026 |
| RehearseVLA | World-model virtual environment for VLA post-training | [GitHub](https://github.com/iSEE-Laboratory/RehearseVLA) ![stars](https://img.shields.io/github/stars/iSEE-Laboratory/RehearseVLA?style=social) | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Xiao_RehearseVLA_Simulated_Post-Training_for_VLAs_with_Physically-Consistent_World_Model_CVPR_2026_paper.html) | CVPR | 2026 |
| WoVR | Reliable world-model simulator for VLA RL post-training | [GitHub](https://github.com/RLinf/RLinf) ![stars](https://img.shields.io/github/stars/RLinf/RLinf?style=social)<br>[Models](https://huggingface.co/collections/RLinf/wovr) | [Paper](https://arxiv.org/abs/2602.13977) | arXiv | 2026 |
| World-Gymnast | World-model RL framework for VLA fine-tuning | [GitHub](https://github.com/world-gymnast/world-gymnast) ![stars](https://img.shields.io/github/stars/world-gymnast/world-gymnast?style=social) | [Paper](https://arxiv.org/abs/2602.02454) | ICLR Workshop | 2026 |
| Robo-DM | Large robot-dataset management for transformer policies | [GitHub](https://github.com/BerkeleyAutomation/robodm) ![stars](https://img.shields.io/github/stars/BerkeleyAutomation/robodm?style=social) | [Paper](https://arxiv.org/abs/2505.15558) | ICRA | 2025 |

### Neural Simulation and Evaluation

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| WorldGym | World-model-based VLA policy evaluation environment | [GitHub](https://github.com/world-model-eval/world-model-eval) ![stars](https://img.shields.io/github/stars/world-model-eval/world-model-eval?style=social) | [Paper](https://openreview.net/forum?id=hidBHy1CAw) | ICLR | 2026 |
| SimplerEnv | Sim-to-real VLA policy evaluation framework | [GitHub](https://github.com/simpler-env/SimplerEnv) ![stars](https://img.shields.io/github/stars/simpler-env/SimplerEnv?style=social) | [Paper](https://proceedings.mlr.press/v270/li25c.html) | CoRL | 2024 |
| Interactive World Simulator | Interactive neural simulator for VLA-policy training and evaluation | [GitHub](https://github.com/WangYixuan12/interactive_world_sim) ![stars](https://img.shields.io/github/stars/WangYixuan12/interactive_world_sim?style=social) | [Paper](https://arxiv.org/abs/2603.08546) | RSS | 2026 |
| GE-Sim 2.0 | Closed-loop video world simulator for VLA evaluation and learning | [GitHub](https://github.com/AgibotTech/GE-Sim-V2) ![stars](https://img.shields.io/github/stars/AgibotTech/GE-Sim-V2?style=social) | [Paper](https://arxiv.org/abs/2605.27491) | arXiv | 2026 |

## Entry Format

Accepted entries use this schema:

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

- `Type` is a short provisional label.
- `Code / Artifact` contains at most one or two primary official entry points. If no public artifact exists, state that explicitly.
- GitHub entries include a live stars badge:

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- `Paper` uses short link labels rather than full titles; a system family may have at most two representative papers.
- `Venue` records the representative paper's venue. A formal archival venue can supply one maturity signal; workshop and preprint labels cannot, and no venue substitutes for the first two admission gates.
- `Year` is the representative conference edition or journal publication year; for preprints, it is the first relevant public year. The exact first-public date used for maturity review is tracked separately.

## Not in Scope

Excluded by default:

- Autonomous-driving-only systems, legacy robotics systems, and general robot middleware, drivers, schedulers, navigation stacks, or control frameworks.
- Classical simulators, teleoperation platforms, data-collection rigs, and robot-learning frameworks not designed specifically for embodied foundation models.
- Standalone models, policies, losses, representations, token-pruning methods, action-tokenization tricks, prompting or planning methods, and training recipes without a reusable system abstraction.
- Work that uses an LLM, VLM, or CLIP model only as a one-off component for task generation, annotation, or scoring.
- Model-specific demo wrappers, benchmark- or leaderboard-only releases, marketing pages, news posts, videos, surveys, courses, reading lists, and other meta resources.
- Work more than 12 months past its first public date with none of the three recognition signals.

## Maintenance

See [Curation Criteria](./docs/curation-criteria.md) for the screening rubric and maturity-check procedure.

When updating this README, update [README.zh-CN.md](./README.zh-CN.md) in the same change. The two READMEs should stay structurally and semantically synchronized, but the Chinese version does not need to be a sentence-by-sentence translation.
