# Cortica: Evolving Memory for Longitudinal LLM Systems

**Nathan A. Lucy**

## Abstract

Large language models can retrieve context, but retrieval alone is not memory. A long-term memory system should evolve: consolidating overlapping evidence, preserving provenance, deriving reusable conclusions, and reconnecting those conclusions when later questions depend on already-discovered structure. Cortica is a research project exploring this idea. It treats memory as a maintained cognitive substrate rather than a static vector store. The core hypothesis is that provenance-connected prior reasoning and corpus-calibrated evidence selection improve later answers on longitudinal tasks where raw retrieval alone lacks the compressed interpretation needed for the question.

## 1. Problem

Most LLM memory systems are retrieval systems. They store records, embed them, and retrieve nearby items at inference time.

That approach works when the answer is directly present in the retrieved context. It is weaker when the answer depends on structure that had to be discovered earlier:

- a policy changed over time
- a recurring operational pattern emerged across departments
- a personal preference stabilized across many interactions
- a contradiction must be resolved by temporal or evidential priority
- several local observations imply a broader principle

In those cases, top-k retrieval can recover fragments without recovering the interpretation.

## 2. Claim

Cortica starts from a different premise:

> A memory system should not only retrieve evidence. It should evolve from evidence.

The system should maintain durable records, consolidate overlap, and produce compact reasoning objects that remain connected to the evidence that generated them.

Those reasoning objects are not treated as raw facts. They are derived thoughts: realizations, patterns, and principles produced from bounded evidence frames.

## 3. Memory Operations

Cortica separates three operations.

### Memory

Memory stores durable evidence. Inputs may come from conversation, documents, spreadsheets, logs, or other sources. The target is not transcript storage. The target is compact, useful state.

### Dream

Dream maintains memory. It identifies nearby or overlapping records, consolidates where detail can be preserved, archives obsolete or redundant records, and keeps the active memory field usable.

Dream is not the reasoning product. It is maintenance.

### Rumination

Rumination reasons over memory. It builds bounded evidence frames from recalled and related records, then produces compact prior thought:

- **Realization**: an evidence-bound local inference
- **Pattern**: a repeated relationship across realizations
- **Principle**: a compressed axiom or operating philosophy

Rumination is the source of new prior reasoning.

## 4. Connected Recall

When answering a later question, Cortica can retrieve raw evidence through hybrid search. It can then expand that evidence through provenance links to include prior realizations, patterns, and principles derived from the retrieved records.

This creates three evaluation modes:

- **Hybrid recall**: raw lexical and semantic retrieval
- **Connected recall**: hybrid retrieval plus provenance-linked prior reasoning
- **Full recall**: connected recall plus stored playbook signals

The research question is whether connected recall improves support and answer quality compared with raw hybrid retrieval.

## 5. Evidence Assembly

Cortica also studies how evidence should be selected before the LLM sees it.

The private implementation treats retrieval candidates as a local field rather than a flat ranked list. It studies:

- corpus-calibrated evidence frames
- local similarity and activation structure
- graph-Laplacian spectral communities
- contrastive escalation between competing frames
- Pareto frontier selection across relevance, coherence, separation, breadth, and provenance
- fixed-budget selection under estimated context limits

The operating rule is conservative: mathematical layers are not included because they sound sophisticated. They are included only when an ablation shows that they recover support, improve stability, or reduce wasted context.

## 6. Benchmark Direction

Cortica uses fixed longitudinal memory benchmarks rather than one-off prompt demonstrations.

The current benchmark families are:

- enterprise operating memory
- personal operating memory
- compliance and policy memory
- noisy evidence-frame selection
- competing evidence-frame selection
- fragmented evidence breadth
- Pareto frontier breadth

Each benchmark contains memory records, prior reasoning objects, provenance links, and test questions requiring recovery of facts, changes, contradictions, or higher-order structure.

The important comparison is not whether an LLM can reason when shown all context. The comparison is whether an evolving memory substrate improves what context the LLM receives.

## 7. Interpretation

The value of Cortica is not that it replaces the LLM. The LLM remains the strongest available semantic synthesizer.

The value is that memory does work before the LLM is asked to answer:

- repeated structure is compressed
- reusable conclusions are preserved
- provenance remains inspectable
- evidence is assembled from local corpus structure, not raw rank alone
- later recall can recover thought, not only evidence
- stale or redundant detail can be archived

This is a memory-efficiency claim, not a magic-intelligence claim.

## 8. Limitations

The current work is early.

The benchmark suite is small and internally constructed. Broader claims require larger held-out corpora, stronger baselines, repeated judged runs, confidence intervals, and adversarial tests for stale reasoning, contradiction, and over-compression.

The system also depends on the quality of memory creation, consolidation, selector calibration, and prompt boundaries. Poor memory hygiene can pollute later reasoning.

## 9. Future Work

Immediate research directions:

- publish fixed benchmark definitions
- evaluate across larger longitudinal corpora
- compare against strong agentic retrieval baselines
- test failure cases where prior reasoning hurts recall
- measure token savings from memory evolution
- study when mathematical candidate grouping reduces LLM calls without reducing quality
- expand ablation tests for spectral, contrastive, Pareto, and budgeted evidence selection

## 10. Conclusion

Retrieval is not memory.

A useful long-term memory system should evolve. It should preserve evidence, compress repeated structure, derive reusable thoughts, and later reconnect those thoughts to the evidence that produced them.

Cortica is an attempt to build and evaluate that layer.

Copyright 2026 Nathan A. Lucy. All rights reserved.
