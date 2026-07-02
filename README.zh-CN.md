# Awesome Embodied Systems

一个关于具身智能和物理智能系统的精选 survey。系统是主要条目，论文只是系统的证据或入口。

语言：[English](./README.md) | 中文

## 目录

- [范围](#范围)
- [分类概览](#分类概览)
- [表格说明](#表格说明)
- [目录](#目录)
- [默认不收录](#默认不收录)
- [维护](#维护)

## 范围

核心条目应满足三个条件：

- 条目是一个有明确名称的系统，而不是单篇论文、单个模型、单个算法或单个数据集。
- 系统有 paper、preprint 或 technical report 等技术证据。
- 主要贡献是系统机制或基础设施，而不只是模型能力或任务表现提升。

系统可以来自 robotics、ML、CV、embodied AI、simulation 或 systems venue。Venue 是 metadata，不是入选门槛。

详细筛选标准见 [Curation Criteria](./docs/curation-criteria.md)。

## 分类概览

下面的分类只是临时导航，不是最终 taxonomy。

| 分类 | 收录内容 |
|---|---|
| Simulation and Evaluation Infrastructure | 具身仿真器、交互环境、评测 harness、任务套件和 benchmark infrastructure。 |
| Data, Logging, and Experiment Infrastructure | 数据采集系统、回放和日志工具、数据集基础设施、实验编排和可复现工具。 |
| Runtime, Serving, and Deployment | 推理 runtime、serving 系统、实时控制栈、边云部署系统和执行基础设施。 |
| Robot Platforms and Fleet Systems | 机器人学习平台、fleet-scale 系统、多机器人基础设施和具身 agent 运行栈。 |
| Safety, Observability, and Reliability | 运行时安全系统、监控、调试工具、恢复机制、可靠性基础设施和运维经验。 |

## 表格说明

每个 catalog section 使用同一套表格字段：

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

字段规则：

- `Type` 是临时短标签，不是固定 taxonomy。
- `Code / Artifact` 最多放一到两个主要官方入口。
- GitHub 条目应加入实时 stars badge：

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- 如果一个系统有多篇相关技术论文，按系统发展时间从早到晚列出。
- 如果列出多篇论文，`Venue` 按相同顺序列出。
- `Year` 是系统首次公开的代表年份，通常是第一篇相关论文年份。

## 目录

### Simulation and Evaluation Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

### Data, Logging, and Experiment Infrastructure

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

### Runtime, Serving, and Deployment

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

### Robot Platforms and Fleet Systems

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

### Safety, Observability, and Reliability

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

## 默认不收录

除非包含实质性的系统级设计，以下内容默认不收录：

- 单纯模型、policy、loss、表示、action-tokenization trick、prompting 方法、planning 方法或训练 recipe。
- 针对单个模型的 inference repo 或狭窄 demo wrapper。
- 只有 demo、营销页、新闻稿、视频或融资公告的系统。
- 没有绑定具身智能 workload 的通用机器人 middleware、driver、navigation stack 或控制框架。
- 没有 embodied-AI-specific system layer 的通用图形或物理引擎。
- survey、课程页、reading list、awesome list、leaderboard 和其他 meta resource。

## 维护

更新本 README 时，需要同步更新 [README.md](./README.md)。中英文 README 应保持结构和语义同步，但中文版本不需要逐句直译英文。
