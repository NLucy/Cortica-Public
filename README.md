# Cortica

**Intelligent memory evolves.**

Cortica is a research project on long-term memory for LLM systems.

The central claim is simple:

> Retrieval is not memory. A memory system should reshape itself over time.

Most LLM memory systems retrieve stored context. Cortica explores a different layer: a memory substrate that consolidates evidence, preserves provenance, derives reusable conclusions, and reconnects them during later recall.

The working hypothesis is that memory should do useful work before the model answers. It should reduce redundancy, expose structure, and hand the model compact evidence-linked state instead of raw top-k fragments.

This public repository is a research shell. It contains the thesis, benchmark protocol, and paper outline. Implementation details are private while the system is still under active development.

## What Cortica Studies

Cortica separates memory into three operations:

- **Memory**: durable records of user, document, or system evidence.
- **Dream**: maintenance that consolidates overlapping records and archives stale detail.
- **Rumination**: reasoning over bounded evidence frames to produce realizations, patterns, and principles.

The research question is whether later answers improve when recall can pull not only raw evidence, but also provenance-linked prior reasoning derived from that evidence.

## Structural Evidence Layer

Cortica is not just a prompt pattern around vector search.

The private implementation currently studies a structure-aware evidence assembly stack:

- corpus-calibrated evidence frames
- local similarity and activation fields
- graph-Laplacian spectral structure
- contrastive frame escalation
- Pareto frontier frame selection
- fixed-budget evidence assembly
- provenance-connected recall
- perturbation-stability testing

The point is not to add ornamentation. Each layer has to earn its place in an ablation. If it does not improve support recovery, stability, or context efficiency, it stays research-only or gets removed.

## Working Claim

Static retrieval repeatedly spends tokens rediscovering the same structure.

Evolving memory should compress prior reasoning into durable, cited thought objects, then reconnect those objects to future questions through the evidence that produced them.

In short:

> A corpus that never changes is not remembering. It is only being searched.

## Current Benchmark Direction

Cortica is evaluated against fixed longitudinal memory benchmarks:

- enterprise operating memory
- personal operating memory
- compliance and policy memory
- noisy evidence-frame selection
- competing evidence-frame selection
- fragmented evidence breadth
- Pareto frontier breadth

Each benchmark compares:

- **Hybrid recall**: raw lexical/semantic retrieval
- **Framed recall**: evidence-frame selection from the same candidate pool
- **Spectral recall**: graph-structured candidate selection
- **Contrastive recall**: competing-frame escalation when margins are weak
- **Pareto recall**: multi-objective frontier selection
- **Budgeted recall**: fixed-budget evidence assembly
- **Connected recall**: hybrid retrieval plus provenance-connected prior reasoning
- **Full recall**: connected recall plus ephemeral playbook signals

The early result pattern is twofold:

- provenance-connected prior reasoning improves support recovery when the answer depends on previously synthesized structure
- structure-aware evidence frames improve support recovery when raw top-k retrieval is noisy, fragmented, or pulled toward a competing neighborhood

See [Benchmark Protocol](./docs/Benchmark_Protocol.md).

## Public Boundary

This repository does not include:

- source code
- prompts
- private benchmark corpora
- UI prototypes
- database schemas
- deployment details
- proprietary implementation strategies

The public artifact is the thesis, evaluation shape, structural vocabulary, and paper trail.

## Paper

The current paper outline is here:

- [Cortica Position Paper](./docs/Cortica_Position_Paper.md)

## Status

Early research artifact. Not a released product.

Copyright 2026 Nathan A. Lucy. All rights reserved.
