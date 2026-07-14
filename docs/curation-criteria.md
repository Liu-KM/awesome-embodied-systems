# Curation Criteria

This repository curates systems for embodied foundation models, not robotics infrastructure or embodied-AI papers in general. The primary unit is a named system; papers and artifacts are evidence for it.

## Admission Gates

A public entry must pass all three gates in order. A later gate cannot compensate for failing an earlier one.

### 1. Embodied-Foundation-Model Scope

The system's primary workload must be a vision-language-action model (VLA), world-action model (WAM), embodied VLM/LLM, or infrastructure designed specifically to train, serve, deploy, simulate, evaluate, or safeguard such models.

Include:

- Foundation-model inference runtimes, serving systems, schedulers, compilers, performance tools, and real-robot deployment stacks.
- Distributed training, post-training, online-learning, fleet-feedback, and data systems built around embodied foundation models.
- Neural or world-model simulators and reusable evaluation environments for embodied-foundation-model policies.
- Reliability, observability, and safety mechanisms whose design is specific to these workloads.

Exclude:

- Autonomous-driving-only systems, legacy robotics systems, and generic middleware, ROS infrastructure, drivers, navigation stacks, schedulers, or control frameworks.
- Classical simulators, teleoperation rigs, data-collection platforms, and general robot-learning libraries whose organizing workload is not an embodied foundation model.
- Pipelines that use an LLM, VLM, or CLIP model only for one-off task generation, annotation, scoring, or interface glue.

### 2. Systems Contribution

The main causal contribution must be a reusable system abstraction or mechanism: an execution path, runtime, serving layer, scheduler, resource manager, data plane, training or post-training substrate, deployment design, neural-simulation environment, evaluation harness, observability mechanism, safety layer, or operational insight.

Model-system co-design can qualify. It must identify a system bottleneck, expose an explicit runtime or infrastructure mechanism, implement it beyond a demo wrapper, and report systems evidence such as latency, throughput, memory, utilization, reliability, scale, data movement, or closed-loop timing. Caching or speculative execution may therefore qualify; a model architecture, loss, token-pruning rule, or training recipe by itself does not.

Benchmark, dataset, task-suite, and leaderboard releases qualify only when their reusable system mechanism—not the new tasks, data, or metric—is the main contribution.

### 3. Evidence and Maturity

Every system needs public technical evidence that explains enough design for readers to learn from it. A peer-reviewed paper, preprint, or substantial technical report is sufficient evidence; a demo, marketing page, news post, fundraising announcement, or video is not.

Open-source code or a usable artifact is preferred but is not mandatory when the technical evidence clearly describes a real system. If implementation is not public, the README must say so explicitly.

Apply a rolling 12-month maturity rule from the review date:

- **First public date** is the earliest verifiable public release of the relevant paper, project, or usable artifact. A silently created empty repository is not a release.
- **At most 12 months old**: an entry may be listed provisionally after passing the first two gates and the technical-evidence requirement.
- **More than 12 months old**: the entry must also have at least one of these recognition signals:
  1. 20 or more citations;
  2. a formal peer-reviewed archival conference or journal publication; or
  3. 100 or more stars on the official GitHub repository.

For reproducibility:

- Use Semantic Scholar as the primary citation source and OpenAlex as a fallback. Record the source, count, and check date; do not add counts across sources.
- Count a main-track conference or journal paper once its official acceptance or proceedings record is verifiable. Workshops, demos, arXiv papers, and technical reports do not satisfy this signal by themselves.
- Count only the official repository's GitHub stars, recorded on the check date. Do not combine forks, mirrors, or repositories from unrelated implementations.
- Recheck a provisional entry once it becomes more than 12 months old. Archive it if it still has no recognition signal.

## Systemicity Levels

Use these internal levels to make the systems gate consistent. Do not expose them as reader-facing rankings.

| Level | Meaning | README |
|---|---|---|
| S0 | Non-system work: model, policy, representation, training recipe, dataset, benchmark, or task result. | Exclude |
| S1 | System-adjacent work: efficiency, tooling, or evaluation appears, but the reusable system contribution is not central. | Exclude |
| S2 | Systems-supporting work with a reusable runtime, framework, data substrate, simulator, or evaluation mechanism. | Include |
| S3 | Strong systems work with a clear abstraction, real implementation, systems metrics, stress or deployment evidence, and transferable insight. | Include |

## Screening Checklist

A candidate should answer yes to the first two questions and provide strong evidence for several others:

- Is an embodied foundation model the primary workload rather than an incidental component?
- Is the main contribution a reusable system mechanism rather than only a model or training change?
- Does it target a concrete bottleneck such as latency, throughput, memory, utilization, cost, scale, reliability, closed-loop timing, data movement, simulation fidelity, or deployment complexity?
- Is there a real implementation or deployed substrate beyond a narrow inference wrapper or demo?
- Does it report systems metrics in addition to task success, reward, accuracy, or generalization?
- Does it span multiple models, robots, tasks, environments, datasets, hardware targets, or operational settings, or provide an abstraction designed to do so?
- Does the design insight remain useful beyond the exact checkpoint used in the paper?

The last question is a diagnostic, not an absolute model-replacement test. Tight model-system co-design is acceptable when the system problem, interface, mechanism, and evidence remain explicit.

## Public Sections

Use these sections as navigation aids:

- Inference, Runtime, and Deployment
- Training, Post-training, and Data Systems
- Neural Simulation and Evaluation

Revisit the sections when the accepted systems reveal a more useful taxonomy.

## Review Record

For each candidate, privately record the system name, scope evidence, system mechanism, official artifact, representative paper, first public date, and maturity signal with source and check date. Merge follow-up papers that extend the same deployment substrate rather than inflating the catalog with duplicate system names.

The public repository should expose accepted systems and stable curation rules. Unresolved candidates, rejection reasons, citation/star checks, and borderline judgments belong in `docs/private/`, which is ignored by git.
