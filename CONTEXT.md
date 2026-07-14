# Awesome Embodied Systems

This context defines the language for a curated catalog of systems for embodied foundation models. The repository treats named systems as first-class objects, with papers and artifacts serving as evidence or entry points.

## Language

**System**:
A named technical artifact with a reusable abstraction, mechanism, or operational design. A paper, model, checkpoint, dataset, or inference script does not become a system merely by having a repository.
_Avoid_: Paper, method, standalone model, thin wrapper

**Embodied Foundation Model**:
A large learned model whose perception, reasoning, prediction, or action outputs participate in a physical or simulated sensor–decision–action loop, including VLAs, WAMs, and embodied VLM/LLM planners. Scale alone is insufficient without embodied interaction.
_Avoid_: Any robot policy, software-only agent
_Catalog scope_: Autonomous-driving-only models may fit this broad definition but are excluded by the repository's chosen domain boundary.

**Embodied Foundation Model System**:
A system whose primary purpose is to train, serve, deploy, simulate, evaluate, or safeguard embodied foundation models. This is the canonical meaning of an accepted “embodied system” in this repository.
_Avoid_: Any system that happens to run on a robot

**Foundation-Model-Native Infrastructure**:
Infrastructure whose interfaces or mechanisms are shaped by foundation-model workloads, such as autoregressive or diffusion inference, multimodal state, large-model training, world-model rollouts, or model latency inside a control loop. Incidental model support does not make generic infrastructure foundation-model-native.
_Avoid_: General robotics infrastructure with one VLA example

**System Abstraction**:
A reusable interface, execution model, architecture, pipeline, environment, or integration boundary that can support more than a single demo. Reuse may be demonstrated across models, robots, tasks, environments, datasets, hardware, or deployments.
_Avoid_: Demo script, checkpoint-specific wrapper

**Systems Contribution**:
A contribution whose main causal mechanism is a system abstraction, execution path, resource-management strategy, data substrate, deployment design, simulator environment, evaluation harness, reliability mechanism, or operational insight. Capability gain alone is not a systems contribution.
_Avoid_: Model accuracy or task success as the system boundary

**Model–System Co-Design**:
A design in which model structure and system execution are changed together to address a concrete bottleneck. It qualifies when the system problem, interface, mechanism, implementation, and systems evidence are explicit, even if the mechanism is not model-agnostic.
_Avoid_: Relabeling an architecture or training trick as a system

**System Bottleneck**:
A real constraint on embodied-foundation-model operation, such as latency, jitter, throughput, memory, utilization, energy, cost, scale, scheduling, reliability, observability, data movement, simulation fidelity, deployment complexity, or closed-loop timing.
_Avoid_: Task success as the only bottleneck

**Systemicity Level**:
An internal screening grade: S0 is non-system, S1 is system-adjacent, S2 has a reusable supporting system mechanism, and S3 is strong systems work with implementation, systems evidence, and transferable insight. Only S2 and S3 belong in the public catalog; the level is not a reader-facing ranking.
_Avoid_: Public score, prestige ranking

**Model-Centric Work**:
Work whose main contribution is a model, policy, representation, loss, or training recipe and whose systems content is incidental. It remains out of scope even when it reports efficiency or releases code, unless a distinct system mechanism is central.
_Avoid_: Listing a model because it has an inference repository

**General Robotics Infrastructure**:
Middleware, ROS components, drivers, schedulers, navigation stacks, control frameworks, robot platforms, or general robot-learning libraries not organized around embodied foundation models. Such infrastructure is out of scope regardless of its engineering quality.
_Avoid_: Awesome robotics middleware scope

**Neural Simulator**:
A learned or world-model-based environment that exposes reusable closed-loop interaction for training or evaluating embodied-foundation-model policies. A world-model architecture by itself is not a simulator system.
_Avoid_: Classical simulator, action-conditioned video model without an environment layer

**Technical Evidence**:
A peer-reviewed paper, preprint, or substantial technical report that explains enough system design and evaluation for readers to learn from it. Demos, marketing pages, news posts, fundraising announcements, and videos are not sufficient by themselves.
_Avoid_: Demo-only listing, news-only listing

**First Public Date**:
The earliest verifiable public release of the relevant paper, project, or usable artifact. An empty or private repository's creation date is not treated as a public release.
_Avoid_: Latest update date, silent repository creation

**Recognition Signal**:
Evidence that a system older than 12 months has received community validation: 20+ citations, a formal peer-reviewed archival publication, or 100+ stars on its official GitHub repository. The source and check date must be recorded privately.
_Avoid_: Author claims, combined fork stars, workshop appearance alone

**Maturity Gate**:
The conditional check inside the Evidence and Maturity gate, applied after the first two gates and technical evidence: systems more than 12 months past their first public date need at least one recognition signal. Maturity never compensates for being out of scope or model-centric.
_Avoid_: Prestige as the first screening criterion

**Provisional Entry**:
An accepted system that is at most 12 months old and has not yet needed to demonstrate a recognition signal. It is rechecked once it becomes more than 12 months old and archived if it has not matured.
_Avoid_: Permanent exception for recent arXiv work

**Formal Archival Publication**:
A verifiable peer-reviewed main-track conference or journal publication. Workshops, demos, technical reports, and preprints do not count as this recognition signal by themselves.
_Avoid_: Treating every venue label as equivalent

**Publication Venue**:
The venue attached to the paper link listed for a system. A formal archival venue may satisfy one maturity signal, but workshop or preprint labels cannot, and no venue replaces the scope and systems-contribution gates.
_Avoid_: Venue as the sole admission rule

**Paper**:
A publication that documents, motivates, evaluates, or introduces a system. Papers are evidence or entry points, not the primary objects being curated.
_Avoid_: Entry, item, full-title table cell

**Year**:
The representative conference edition or journal publication year; for a preprint, the first relevant public year. The separate First Public Date, rather than this display field, controls maturity review.
_Avoid_: Latest update year, using the table year as the maturity date

**Code / Artifact**:
The main usable official entry point for a system, preferably source code and otherwise documentation, models, data, or a project page. If no artifact is public, the catalog states that explicitly.
_Avoid_: Unofficial reimplementation as the primary link

**System Family**:
A named substrate and its direct follow-up papers or extensions that share the same implementation and operational architecture. A family is normally represented by one row to avoid double-counting papers as systems.
_Avoid_: One README entry per paper revision

**Type**:
A short descriptive label for what kind of system is listed. Type labels and catalog sections remain provisional until enough systems justify a stable taxonomy.
_Avoid_: Premature fixed taxonomy

**Candidate Pool**:
A private working collection of possible systems, rejections, maturity checks, and borderline cases awaiting evidence. It is a curation workspace, not a public rejected list.
_Avoid_: Public backlog

**Public Documentation**:
Committed documentation intended for readers and contributors, including the READMEs, criteria, glossary, and accepted scope decisions. It should expose stable rules and accepted systems, not unresolved screening notes.
_Avoid_: Draft judgments in the public README

**Private Working Notes**:
Local notes that record candidate evidence, rejection reasons, citation and star checks, and unfinished research. They are not the public source of truth.
_Avoid_: Committed candidate dump

**Meta Resource**:
A survey, course, awesome list, reading list, or leaderboard-only page that points to systems without itself being one. Meta resources are outside the catalog.
_Avoid_: Related-resources section posing as systems
