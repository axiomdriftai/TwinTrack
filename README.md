# TwinTrack

TwinTrack is a structural comparison instrument for long-form human-LLM interaction. It places a human conversational archive alongside a synthetic profile generated under controlled input conditions, rendering both as temporal signatures derived from non-semantic structural properties alone.

This is not about what is said. It is about how interaction unfolds over time — and whether different input regimes produce structurally distinguishable results.

## The Research Question

Each synthetic profile was designed to produce plausible-looking interaction. What varies between them is the input regime: the structural properties of how a user drives a conversation — entropy, density, affect, and topical coherence.

TwinTrack asks whether input regime alone can reproduce the temporal signature of a real long-form human thread.

The consistent finding is that it cannot. Controlled input produces characteristic collapse patterns, burst-recovery cycles, or mid-thread exhaustion that do not appear in genuine human interaction. These differences are visible in structure without any analysis of content.

## What TwinTrack Shows

**Top panel — Chalk:** A fixed human archive (293 model turns, normalized to a shared temporal grid). Chalk exhibits sustained variance across the full thread, with periodic high-activity regions and no structural collapse.

**Bottom panel — Synthetic profile:** One of three controlled input regimes, selectable from the controls panel. All profiles were run to 200 turns; model response lengths are estimated from word count and normalized to the same grid as Chalk for direct comparison.

Both panels share a rolling mean line and optional variance band. A shared y-axis option allows direct magnitude comparison across the two tracks.

## Synthetic Profiles

Profiles are identified by their input regime, not by characterization. Each represents a distinct pattern of user-side structural behavior.

**Sparse** — Near-zero input entropy. User turns are monosyllabic or single-word throughout. Model responses begin with moderate length and variance before collapsing as the model exhausts strategies for engaging with minimal input. Mean response volume is substantially lower than Chalk.

**Effusive** — High-density, sustained high-affect input. User turns are verbose and enthusiastic throughout. Model responses peak unusually high in the early thread (exceeding 1,000 estimated tokens at points) before a structural collapse around the midpoint, followed by partial recovery. This burst-collapse-recovery pattern does not appear in Chalk.

**Structured** — Systematic, pedagogically-driven input. User turns build sequentially on previous responses in an ordered, educational pattern. Model responses maintain moderate consistency through the first half of the thread before a near-complete collapse from which there is no recovery. The most human-appearing profile in isolation; the most structurally revealing in comparison.

## What TwinTrack Is and Is Not

TwinTrack is a demonstration instrument. It is designed to:

1. Show that input regime produces measurable structural consequences in model response behavior
2. Illustrate the divergence between controlled synthetic interaction and real long-form human interaction
3. Present this divergence without recourse to semantic content, sentiment, or meaning

It does not claim to measure: understanding, alignment, quality, intelligence, or the validity of any input style. No profile is presented as better or worse — only as structurally distinct.

## Implementation

TwinTrack is implemented as a static single-file HTML application. All data is pre-processed and embedded. No files are uploaded, no data is transmitted, and no computation occurs server-side.

Human data (Chalk) is derived from the BigFlame archive used in Variance Register, restricted to model response turns and normalized to a 300-point temporal grid. Synthetic profiles were generated through controlled API runs with fixed system instructions defining user simulator behavior, then processed identically.

## Notes

This project was developed by Axiom Drift AI. AI-assisted coding tools were used during implementation, consistent with modern software development practice. All conceptual framing, measurement logic, and evaluation criteria are human-directed.

The six synthetic profiles from the original generation run are referenced as Profiles I, IV, V, VII, IX, and X. Three (Sparse, Effusive, Structured) are presented here on the basis of maximum structural contrast.

## Related Work

*Beyond Content: Temporal Dynamics of Long-Form Human-LLM Interaction*
https://doi.org/10.5281/zenodo.18273459

[Axiom Drift AI](https://axiomdrift.ai)
