# Awesome Embodied Systems

A curated survey of embodied intelligence and physical intelligence systems. A system is the primary entry; papers are evidence or entry points.

Language: English | [中文](./README.zh-CN.md)

## Contents

- [Scope](#scope)
- [Category Overview](#category-overview)
- [Catalog Notes](#catalog-notes)
- [Catalog](#catalog)
- [Not in Scope](#not-in-scope)
- [Maintenance](#maintenance)

## Scope

Core entries should satisfy three conditions:

- The entry is a named system, not just a paper, model, algorithm, or dataset.
- The system has technical evidence such as a paper, preprint, or technical report.
- The main contribution is a system mechanism or infrastructure, not only improved model capability or task performance.

Systems may come from robotics, ML, CV, embodied AI, simulation, or systems venues. Venue is metadata, not an admission gate.

For the detailed screening rubric, see [Curation Criteria](./docs/curation-criteria.md).

## Category Overview

The categories below are provisional navigation aids, not a final taxonomy.

| Category | What Belongs Here |
|---|---|
| Simulation and Evaluation Infrastructure | Embodied simulators, interactive environments, evaluation harnesses, task suites, and benchmark infrastructure. |
| Data, Logging, and Experiment Infrastructure | Data collection systems, replay/logging tools, dataset infrastructure, experiment orchestration, and reproducibility tooling. |
| Runtime, Serving, and Deployment | Inference runtimes, serving systems, real-time control stacks, edge/cloud deployment systems, and execution infrastructure. |
| Robot Platforms and Fleet Systems | Robot learning platforms, fleet-scale systems, multi-robot infrastructure, and embodied-agent operation stacks. |
| Safety, Observability, and Reliability | Runtime safety systems, monitors, debugging tools, recovery mechanisms, reliability infrastructure, and operational lessons. |

## Catalog Notes

Each catalog section uses this table schema:

| System | Type | Code / Artifact | Paper | Venue | Year |
|---|---|---|---|---|---|

Rules for table fields:

- `Type` is a short provisional label, not a fixed taxonomy.
- `Code / Artifact` should contain at most one or two primary official entry points.
- GitHub entries should include a live stars badge:

```md
[GitHub](https://github.com/owner/repo) ![stars](https://img.shields.io/github/stars/owner/repo?style=social)
```

- If a system has multiple relevant technical papers, list them from earliest to latest.
- If multiple papers are listed, list venues in the same order.
- `Year` is the first representative public year, usually the year of the first relevant paper.

## Catalog

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

## Not in Scope

The following are excluded by default unless they contain substantial system-level design:

- Standalone models, policies, losses, representations, action-tokenization tricks, prompting methods, planning methods, or training recipes.
- Model-specific inference repositories or narrow demo wrappers.
- Demo-only systems, marketing pages, news posts, videos, and fundraising announcements.
- General robotics middleware, drivers, navigation stacks, or control frameworks not tied to embodied intelligence workloads.
- General graphics or physics engines without an embodied-AI-specific system layer.
- Surveys, course pages, reading lists, awesome lists, leaderboards, and other meta resources.

## Maintenance

When updating this README, update [README.zh-CN.md](./README.zh-CN.md) in the same change. The two READMEs should stay structurally and semantically synchronized, but the Chinese version does not need to be a sentence-by-sentence translation.
