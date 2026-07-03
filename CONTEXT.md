# Awesome Embodied Systems

This context defines the language for a curated survey of embodied intelligence and physical intelligence systems. The repository treats systems as first-class objects, with papers and artifacts serving as evidence or entry points.

## Language

**System**:
A named embodied intelligence or physical intelligence platform, benchmark, dataset engine, simulator, deployment stack, robot learning stack, or model-integrated technical artifact with a reusable system abstraction or distinctive system-level design. A model does not count as a system merely because it has an inference repository or a narrow demo wrapper.
_Avoid_: Paper, method, standalone model, model-specific demo repo

**Embodied System**:
A system concerned with perception, decision-making, action, simulation, evaluation, data collection, or deployment in physical or interactive environments. Pure LLM agents, web agents, computer-use agents, CV methods, or NLP methods are out of scope unless they explicitly operate in a physical or simulated embodied environment.
_Avoid_: Agent when it only means a software-only workflow

**System Abstraction**:
A reusable boundary, interface, architecture, pipeline, platform, or integration pattern that can support more than one experiment, model, task, robot, environment, dataset, or evaluation setting. A work can also qualify if it is model-specific but contains distinctive system-level design beyond ordinary model inference.
_Avoid_: Thin wrapper, demo script, inference-only repository

**Systems Contribution**:
A contribution whose main causal mechanism is a system abstraction, infrastructure component, execution path, resource-management strategy, deployment design, observability mechanism, safety mechanism, evaluation harness, or operational insight. The boundary is not whether the work improves agent intelligence, but whether the improvement mainly comes from system design rather than model capability, representation, or training.
_Avoid_: Intelligence improvement as the system boundary, capability gain alone

**System Bottleneck**:
A real constraint that limits embodied workloads, such as latency, jitter, throughput, memory, energy, cost, scalability, scheduling, reliability, fault tolerance, observability, reproducibility, deployment complexity, safety enforcement, real-time control, data movement, storage, simulation scale, or multi-robot coordination.
_Avoid_: Task success as the only bottleneck

**Systemicity Level**:
An internal screening grade for curation strength: S0 means non-system, S1 means system-relevant but not a systems contribution, S2 means infrastructure or tooling with embodied systems value, and S3 means a strong systems contribution with implementation, systems metrics, and transferable insight. The core README should list S2 and S3 systems, but should not expose this level as a reader-facing ranking field.
_Avoid_: Reader-facing score, public ranking, binary system/non-system label when the evidence is borderline

**Model-Centric Work**:
A work whose main contribution is a model, policy, representation, or training recipe rather than a reusable embodied system abstraction. Model-centric works are out of scope unless they include distinctive system-level design, infrastructure, evaluation, deployment, or integration content.
_Avoid_: Listing a model only because code is available

**General Robotics Infrastructure**:
Robot middleware, drivers, navigation stacks, control frameworks, or hardware support systems that are broadly useful for robotics but not specifically tied to embodied intelligence or physical intelligence workloads. General robotics infrastructure is out of scope unless it directly contributes to embodied AI training, inference, simulation, evaluation, deployment, data, safety, or observability.
_Avoid_: Awesome robotics middleware scope

**Embodied Simulator**:
A simulation or interactive-environment infrastructure designed for embodied AI, robot learning, embodied evaluation, synthetic data generation, or physical intelligence workloads. General graphics engines and physics engines are out of scope unless the listed system is an embodied-AI-specific platform or wrapper built on top of them.
_Avoid_: General game engine, general physics engine

**Paper**:
A publication that documents, motivates, evaluates, or introduces a system. Papers are evidence or entry points for a system, not the primary object being curated; README paper cells should use short link labels such as `Paper` instead of full paper titles.
_Avoid_: Entry, item, primary record, full-title table cell

**Technical Evidence**:
A peer-reviewed paper, preprint, technical report, or system paper that explains enough of a system's design, architecture, data, evaluation, infrastructure, or deployment approach for readers to learn from it. Demos, marketing pages, news posts, fundraising announcements, and videos are not sufficient evidence by themselves.
_Avoid_: Demo-only listing, news-only listing

**Publication Venue**:
The conference, journal, workshop, or preprint venue attached to the representative paper listed for a system. Venue is an evidence signal for visibility, review standard, and community positioning, but it is not an admission gate for the curated list.
_Avoid_: Conference when the source may be a journal, workshop, or preprint; venue as a hard filter

**Year**:
The representative first-public year for a system, usually the year of the representative paper. If no formal publication exists, use the preprint, technical report, or public artifact release year.
_Avoid_: Latest update year, repository activity year

**Public Entry Point**:
A publicly accessible link that lets readers inspect or follow a system, such as a code repository, project page, documentation site, dataset, benchmark, model artifact, paper, or technical report. Public entry points help readers access the system, but they do not replace the need for technical evidence.
_Avoid_: Name-only listing, private reference

**Code / Artifact**:
The main usable public artifact for a system, preferably a code repository and otherwise documentation, project page, dataset, benchmark, model artifact, or demo. This field should list at most one or two primary official entry points, prioritizing source repositories, official docs, official project pages, and then dataset, benchmark, or model artifacts.
_Avoid_: Open Source as a separate field, Public Entry as a table column

**Annotation**:
A short explanatory note about why a system matters or what design insight it offers. Annotations are optional and should not be a required README table column in the first version because they increase maintenance and translation cost.
_Avoid_: Required why-it-matters column

**Type**:
A short descriptive label for what kind of system is being listed. Type labels are provisional until enough systems have been collected to justify a stable taxonomy.
_Avoid_: Premature fixed taxonomy

**Section**:
A provisional README grouping used to help readers navigate the list before a stable taxonomy exists. Sections may be reorganized as more systems are collected and should not be treated as final categories.
_Avoid_: Final category, stable taxonomy

**Candidate Pool**:
A private working collection of possible systems, rejected systems, and borderline cases that need more evidence before being promoted to the public README. The candidate pool is for curation work, not for readers.
_Avoid_: Public backlog, public rejected list

**Public Documentation**:
Committed repository documentation intended for readers and contributors, such as the README, curation criteria, templates, and accepted scope decisions. Public documentation should not expose unresolved candidate judgments unless they are ready to be shared.
_Avoid_: Draft notes, private screening notes

**Private Working Notes**:
Local curation notes used to track uncertain candidates, rejection reasons, and unfinished research. Private working notes should not be treated as the public source of truth.
_Avoid_: Public README, committed documentation

**Meta Resource**:
A survey, course page, awesome list, reading list, leaderboard-only page, or other resource that points to systems without itself being an embodied system. Meta resources are out of scope for the curated system list.
_Avoid_: Survey section, related resources section
