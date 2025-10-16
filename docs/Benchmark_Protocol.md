# Benchmark Protocol

Cortica is evaluated as an evolving memory substrate, not as a general question-answering model.

The benchmark asks two questions:

> Does provenance-connected prior reasoning improve later recall compared with raw hybrid retrieval?

> Can structure-aware evidence framing improve context assembly before any LLM synthesis occurs?

## Benchmark Shape

Each fixture contains:

- memory records
- prior reasoning records
- provenance links between reasoning and source memories
- test questions
- expected supporting records

The fixtures are longitudinal. They include change over time, repeated signals, contradictions, and higher-order patterns.

Evidence-frame fixtures also include noisy candidate pools, competing semantic neighborhoods, fragmented support evidence, and multi-objective frame tradeoffs.

## Current Benchmark Families

### Enterprise Operating Memory

Tests whether memory can recover operational structure across departments, policies, financial signals, customer feedback, and evolving priorities.

### Personal Operating Memory

Tests whether memory can recover stable preferences, personal constraints, recurring goals, and prior self-understanding across ordinary interactions.

### Compliance and Policy Memory

Tests whether memory can preserve current policy state, identify superseded rules, and use prior reasoning without treating it as raw policy evidence.

### Evidence-Frame Selection

Tests whether corpus-calibrated frame selection can recover coherent support records from noisy retrieval candidates.

### Competing Evidence Frames

Tests whether graph structure and contrastive escalation can carry a second plausible frame forward when a selected frame has weak margins.

### Fragmented Evidence Breadth

Tests whether evidence selection can preserve support distributed across weakly connected records instead of collapsing to a narrow cluster.

### Pareto Frontier Breadth

Tests whether multi-objective frontier ranking can recover support that a scalar frame score leaves split.

## Recall Modes

### Hybrid

Raw lexical and semantic retrieval.

This is the baseline.

### Framed

Candidate evidence frames selected by local relevance, density, boundary contrast, concept diversity, and provenance coverage.

### Spectral

Graph-Laplacian community selection over the candidate pool.

### Framed Spectral

Evidence-frame selection assisted by local spectral structure.

### Contrastive

Framed spectral selection plus competing-frame escalation when the selected frame has a weak margin against a materially different neighbor.

### Pareto

Framed spectral contrastive selection with Pareto frontier ranking across multiple evidence-frame objectives.

### Budgeted

Submodular-style evidence selection under the same estimated context budget as raw top-k.

### Connected

Hybrid retrieval plus graph-connected prior reasoning. If retrieved memories previously produced a realization, pattern, or principle, that prior thought can be included with clear provenance.

### Full

Connected recall plus stored playbook signals. This mode tests whether internal strategy notes help or distract.

## Metrics

Primary metric:

- support recovery: whether expected supporting records are recovered

Secondary metrics:

- prior reasoning use
- playbook signal use
- context-budget discipline
- perturbation stability
- judged groundedness
- judged relevance
- judged concision
- overall answer quality

## Current Result Pattern

Across the current fixed longitudinal fixtures, connected recall improves support recovery over hybrid retrieval when questions depend on prior synthesized structure.

Across the evidence-frame fixtures, structural selectors improve support recovery before the LLM is asked to synthesize. The strongest current selector uses framed spectral contrastive selection with Pareto frontier ranking.

This is the core result.

The claims are intentionally narrow:

> Connected prior reasoning can improve memory recall on longitudinal tasks where static retrieval misses the interpretation already produced by earlier reasoning.

> Corpus-calibrated evidence selection can improve support recovery when raw top-k retrieval contains noise, competing neighborhoods, or fragmented evidence.

## What This Does Not Prove

It does not prove universal superiority over agentic search, large context windows, or all retrieval pipelines.

It shows a measurable direction: memory systems may gain value by evolving, selecting evidence from corpus structure, and reconnecting prior reasoning to future recall.
