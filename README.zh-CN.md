# Awesome Embodied Systems [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 一个面向具身基础模型的系统优先目录。

本仓库收录以训练、服务、部署、模拟、评测或保障具身基础模型为主要目标的具名系统，包括 vision-language-action model（VLA）、world-action model（WAM）及相关大模型 workload。它不是通用机器人基础设施目录，也不是 VLA/WAM 论文列表。

语言：[English](./README.md) | 中文

## 收录标准

每个条目必须依次通过三个门槛：

- **具身基础模型范围**：主要 workload 是 VLA、WAM、具身 VLM/LLM，或专为这些模型设计的基础设施。只在传统机器人 pipeline 中偶尔调用一次 LLM/VLM 不足以入选。
- **系统贡献**：工作提出有明确名称且可复用的 runtime、serving layer、训练或数据系统、部署机制、神经模拟器、评测环境或可靠性机制。模型—系统协同设计只有在给出明确系统机制并评测系统瓶颈时才算。
- **证据与成熟度**：系统必须有能解释设计的技术证据。首次公开已超过 12 个月的工作，还必须至少具备一种同行认可信号：20+ citations、正式同行评审的 archival 会议或期刊发表，或官方 GitHub 仓库 100+ stars。尚无认可信号的新系统可以暂时收录，首次公开超过 12 个月后重新审核。

三个门槛必须同时满足：认可度不能把通用机器人系统或纯模型工作变成具身基础模型系统。具体操作规则见 [curation criteria](./docs/curation-criteria.md)。

## 目录

通过筛选的系统按其支撑的具身基础模型生命周期环节组织：

- **Inference, Runtime, and Deployment**：执行引擎、serving 与调度机制、性能工具和真机部署栈。
- **Training, Post-training, and Data Systems**：分布式训练、在线学习、fleet 反馈闭环、world-model 后训练环境和基础模型规模的机器人数据基础设施。
- **Neural Simulation and Evaluation**：面向具身基础模型 policy 的可复用 world-model 模拟器与评测环境。

这些分类只是导航，不是最终 taxonomy。

### Inference, Runtime, and Deployment

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| vla.cpp | 统一 VLA 推理 runtime | [GitHub](https://github.com/VinRobotics/vla.cpp) ![stars](https://img.shields.io/github/stars/VinRobotics/vla.cpp?style=social) | [Paper](https://arxiv.org/abs/2606.08094) | arXiv | 2026 |
| Embodied.cpp | 可移植 VLA/WAM 推理与控制 runtime | [GitHub](https://github.com/SEU-PAISys/Embodied.cpp) ![stars](https://img.shields.io/github/stars/SEU-PAISys/Embodied.cpp?style=social) | [Paper](https://arxiv.org/abs/2607.02501) | arXiv | 2026 |
| VLA-Perf | VLA 推理性能建模工具 | [GitHub](https://github.com/NVlabs/vla-perf) ![stars](https://img.shields.io/github/stars/NVlabs/vla-perf?style=social) | [Paper](https://arxiv.org/abs/2602.18397) | arXiv | 2026 |
| VLA-Cache | 自适应 VLA token caching 框架 | [GitHub](https://github.com/siyuhsu/vla-cache) ![stars](https://img.shields.io/github/stars/siyuhsu/vla-cache?style=social) | [Paper](https://papers.nips.cc/paper_files/paper/2025/hash/f062da1973ac9ac61fc6d44dd7fa309f-Abstract-Conference.html) | NeurIPS | 2025 |
| Spec-VLA | VLA speculative decoding 框架 | [GitHub](https://github.com/PineTreeWss/SpecVLA) ![stars](https://img.shields.io/github/stars/PineTreeWss/SpecVLA?style=social) | [Paper](https://aclanthology.org/2025.emnlp-main.1367/) | EMNLP | 2025 |
| Realtime-VLA FLASH | speculative dVLA 推理框架 | [GitHub](https://github.com/dexmal/realtime-vla-flash) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-flash?style=social) | [Paper](https://arxiv.org/abs/2605.13778) | arXiv | 2026 |
| VLASH | future-state-aware 异步 VLA 推理框架 | [GitHub](https://github.com/mit-han-lab/vlash) ![stars](https://img.shields.io/github/stars/mit-han-lab/vlash?style=social) | [Paper](https://arxiv.org/abs/2512.01031) | arXiv | 2025 |
| Realtime-VLA V2 | 真实机器人 VLA 部署栈 | [GitHub](https://github.com/dexmal/realtime-vla-v2) ![stars](https://img.shields.io/github/stars/dexmal/realtime-vla-v2?style=social) | [Paper](https://arxiv.org/abs/2603.26360) | arXiv | 2026 |
| Corki | 具身 LLM 推理、通信与控制协同设计系统 | [GitHub](https://github.com/hyy02/Corki) ![stars](https://img.shields.io/github/stars/hyy02/Corki?style=social) | [Paper](https://arxiv.org/abs/2407.04292) | ISCA | 2025 |
| TimelyLLM | 感知物理执行时序的具身 LLM serving 系统 | 未找到公开实现 | [Paper](https://www.sigmobile.org/mobisys/2026/program/) | MobiSys | 2026 |

### Training, Post-training, and Data Systems

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| RLinf / RLinf-VLA | 可扩展 VLA RL 与真实世界后训练系统 | [GitHub](https://github.com/RLinf/RLinf) ![stars](https://img.shields.io/github/stars/RLinf/RLinf?style=social) | [System](https://www.usenix.org/conference/osdi26/presentation/yu-chao)<br>[VLA](https://arxiv.org/abs/2510.06710) | OSDI | 2026 |
| SOP / Learning While Deploying | fleet-scale 在线 VLA 后训练系统 | 两项均无公开代码：[SOP project](https://www.agibot.com/research/sop)<br>[LWD project](https://finch.agibot.com/research/lwd) | [SOP](https://arxiv.org/abs/2601.03044)<br>[LWD](https://arxiv.org/abs/2605.00416) | arXiv | 2026 |
| VLA Foundry | 统一 LLM-to-VLM-to-VLA 训练框架 | [GitHub](https://github.com/TRI-ML/vla_foundry) ![stars](https://img.shields.io/github/stars/TRI-ML/vla_foundry?style=social) | [Paper](https://arxiv.org/abs/2604.19728) | arXiv | 2026 |
| RehearseVLA | 面向 VLA 后训练的 world-model 虚拟环境 | [GitHub](https://github.com/iSEE-Laboratory/RehearseVLA) ![stars](https://img.shields.io/github/stars/iSEE-Laboratory/RehearseVLA?style=social) | [Paper](https://openaccess.thecvf.com/content/CVPR2026/html/Xiao_RehearseVLA_Simulated_Post-Training_for_VLAs_with_Physically-Consistent_World_Model_CVPR_2026_paper.html) | CVPR | 2026 |
| WoVR | 面向 VLA RL 后训练的可靠 world-model 模拟器 | [GitHub](https://github.com/RLinf/RLinf) ![stars](https://img.shields.io/github/stars/RLinf/RLinf?style=social)<br>[Models](https://huggingface.co/collections/RLinf/wovr) | [Paper](https://arxiv.org/abs/2602.13977) | arXiv | 2026 |
| World-Gymnast | 面向 VLA 微调的 world-model RL 框架 | [GitHub](https://github.com/world-gymnast/world-gymnast) ![stars](https://img.shields.io/github/stars/world-gymnast/world-gymnast?style=social) | [Paper](https://arxiv.org/abs/2602.02454) | ICLR Workshop | 2026 |
| Robo-DM | 面向 Transformer policy 的大规模机器人数据管理工具 | [GitHub](https://github.com/BerkeleyAutomation/robodm) ![stars](https://img.shields.io/github/stars/BerkeleyAutomation/robodm?style=social) | [Paper](https://arxiv.org/abs/2505.15558) | ICRA | 2025 |

### Neural Simulation and Evaluation

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|
| WorldGym | 基于 world model 的 VLA policy 评测环境 | [GitHub](https://github.com/world-model-eval/world-model-eval) ![stars](https://img.shields.io/github/stars/world-model-eval/world-model-eval?style=social) | [Paper](https://openreview.net/forum?id=hidBHy1CAw) | ICLR | 2026 |
| SimplerEnv | sim-to-real VLA policy 评测框架 | [GitHub](https://github.com/simpler-env/SimplerEnv) ![stars](https://img.shields.io/github/stars/simpler-env/SimplerEnv?style=social) | [Paper](https://proceedings.mlr.press/v270/li25c.html) | CoRL | 2024 |
| Interactive World Simulator | 面向 VLA policy 训练与评测的交互式神经模拟器 | [GitHub](https://github.com/WangYixuan12/interactive_world_sim) ![stars](https://img.shields.io/github/stars/WangYixuan12/interactive_world_sim?style=social) | [Paper](https://arxiv.org/abs/2603.08546) | RSS | 2026 |
| GE-Sim 2.0 | 面向 VLA 评测与学习的闭环视频世界模拟器 | [GitHub](https://github.com/AgibotTech/GE-Sim-V2) ![stars](https://img.shields.io/github/stars/AgibotTech/GE-Sim-V2?style=social) | [Paper](https://arxiv.org/abs/2605.27491) | arXiv | 2026 |

## 条目格式

通过筛选的条目使用这套字段：

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

- `Type` 是临时短标签。
- `Code / Artifact` 最多放一到两个主要官方入口；没有公开 artifact 时必须明确说明。
- GitHub 条目加入实时 stars badge：

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- `Paper` 使用短链接标签，不在表格中放完整标题；同一系统谱系最多放两篇代表论文。
- `Venue` 记录代表论文的发表位置。只有正式 archival venue 才能提供一种成熟度信号；workshop 和 preprint 标签不能，任何 venue 也不能替代前两个收录门槛。
- `Year` 是代表会议届次或期刊的发表年份；只有 preprint 时取首次公开年份。成熟度审核使用的精确首次公开日期另行记录。

## 默认不收录

以下内容默认不收录：

- 只面向自动驾驶的系统、传统机器人系统，以及通用机器人 middleware、driver、scheduler、navigation stack 或控制框架。
- 并非专为具身基础模型设计的传统仿真器、遥操作平台、数据采集装置和通用机器人学习框架。
- 没有可复用系统抽象的单纯模型、policy、loss、表示、token pruning、action tokenization、prompting、planning 或训练 recipe。
- 只把 LLM、VLM 或 CLIP 当作任务生成、标注或打分组件的一次性使用。
- 单模型 demo wrapper、只有 benchmark 或 leaderboard 的发布，以及营销页、新闻、视频、survey、课程、reading list 等 meta resource。
- 首次公开超过 12 个月，且三种认可信号均不具备的工作。

## 维护

筛选 rubric 和成熟度复核流程见 [Curation Criteria](./docs/curation-criteria.md)。

更新本 README 时，需要同步更新 [README.md](./README.md)。中英文 README 应保持结构和语义同步，但中文版本不需要逐句直译英文。
