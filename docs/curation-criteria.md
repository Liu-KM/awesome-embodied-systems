# Curation Criteria

This repository curates embodied systems, not embodied AI papers in general. Papers and repositories are evidence for a system; they are not the primary unit of curation.

## Core Rule

A work belongs in the core list when its main contribution makes embodied agents, robots, simulators, data pipelines, deployment stacks, runtime infrastructure, or evaluation workflows more feasible, efficient, reliable, scalable, observable, safe, or reproducible under real system constraints.

The boundary is the contribution mechanism:

- Include works whose primary contribution is a system abstraction, runtime, scheduler, compiler, protocol, middleware, storage layer, serving layer, control plane, monitoring tool, debugging tool, safety layer, data pipeline, simulator infrastructure, deployment framework, evaluation harness, or operational lesson.
- Exclude works whose primary contribution is a model, policy, representation, loss, action tokenization trick, pretraining recipe, fine-tuning recipe, prompting method, planning method, or task performance result.
- Exclude benchmark or task-suite releases whose main contribution is new tasks, datasets, metrics, or leaderboards rather than a reusable system mechanism.
- Exclude general robotics middleware, drivers, navigation stacks, and control frameworks unless they directly contribute to embodied AI training, inference, simulation, evaluation, deployment, data, safety, or observability.
- Exclude general graphics or physics engines unless the listed system is an embodied-AI-specific platform or wrapper built for embodied workloads.

## Required Evidence

Every listed system should have technical evidence that teaches system design. A peer-reviewed paper, preprint, technical report, or system paper is sufficient. A demo, marketing page, news post, fundraising announcement, or video is not sufficient by itself.

Open-source code or a usable artifact is preferred, especially for infrastructure lists. It is not a hard requirement when an accepted or published system paper clearly describes a reusable runtime, deployment mechanism, data pipeline, simulator, profiling tool, or acceleration framework. If implementation is not yet public, the README entry must mark that status explicitly.

## Systemicity Levels

Use these levels when judging candidates:

| Level | Meaning | README |
|---|---|---|
| S0 | Non-system work. The main contribution is a model, policy, representation, training recipe, dataset release, or task result. | Exclude |
| S1 | System-relevant work. It touches deployment, tools, efficiency, or evaluation, but systems contribution is not central. | Exclude |
| S2 | Systems-supporting work. It provides embodied infrastructure, tooling, runtime, data pipeline, evaluation harness with reusable system mechanics, simulator infrastructure, deployment framework, or similar reusable system value. | Include |
| S3 | Strong systems work. It has a core system abstraction or mechanism, real implementation, systems metrics, stress tests or deployment evidence, and transferable system insight. | Include |

## Checklist

A candidate becomes more system-like when the answer is yes:

- Does it target a system bottleneck such as latency, throughput, cost, energy, reliability, safety, scale, observability, reproducibility, scheduling, data movement, simulation scale, or deployment complexity?
- Does it introduce a system mechanism rather than only a model or training change?
- Does it have a real implementation beyond a model-specific inference wrapper?
- Does it report systems metrics, not only task success, reward, accuracy, or generalization?
- Does it work across multiple models, robots, tasks, environments, datasets, hardware targets, or evaluation settings?
- Does it produce design insight that transfers to future embodied systems?

If the model architecture were replaced and the contribution would mostly disappear, the work is probably model-centric. If the abstraction, runtime, pipeline, infrastructure, evaluation harness, or deployment lesson would still matter, the work is probably systems-relevant.

## Provisional README Sections

Use these sections as temporary navigation aids:

- Runtime, Serving, and Deployment
- Simulation Infrastructure
- Data, Logging, and Experiment Infrastructure
- Robot Platforms and Fleet Systems
- Safety, Observability, and Reliability

These sections are not a final taxonomy. Revisit them after enough candidate systems have been reviewed to expose better categories.

## Public vs Private Notes

The public repository should expose accepted systems and curation rules. Unresolved candidates, rejection reasons, borderline judgments, and candidate-pool templates should live in private working notes until a system is ready to be promoted.

Use `docs/private/candidates.md` for local candidate tracking. The `docs/private/` directory is ignored by git.
