# Rapid directed evolution guided by protein language models and epistatic interactions

**Authors:** Tran et al.
**Journal:** Science (2026)
**DOI:** [10.1126/science.aea1820](https://doi.org/10.1126/science.aea1820)

## Summary

The paper introduces **MULTI-evolve** (model-guided, universal, targeted installation of multimutants), an end-to-end machine learning framework for protein engineering. It tackles a core bottleneck: searching a 20^N sequence space for combinations of mutations that work synergistically rather than one at a time.

Three components are integrated into a single workflow:

1. **Protein language model ensemble** — identifies candidate function-enhancing mutations
2. **Neural network epistatic modeling** — trained on double mutants, extrapolates to higher-order multimutants
3. **MULTI-assembly** — a mutagenesis method that constructs multimutants (up to nine mutations) at up to 70% efficiency across multikilobase sequences

## Why It's Interesting

The key move is using **double mutants to learn epistasis and then extrapolate**, which collapses what traditionally takes multiple rounds of directed evolution into one. It also sidesteps the length limits and cost of gene synthesis, which is usually the practical ceiling on this kind of work.

## Key Results

- **APEX** (soybean ascorbate peroxidase) — >100-fold improvement in catalytic activity
- **CRISPR-Cas13d** — 10-fold improvement in trans-splicing activity
- **Anti-CD122 antibody** — multiobjective optimization: 6× expression and 3× binding affinity simultaneously
- Benchmarked across 73 protein datasets (mutation discovery) and 12 datasets (multimutant extrapolation)

## Notes

The multiobjective result on the antibody is worth noting — optimizing expression and affinity together, rather than trading one against the other, is the harder problem and the one that matters most for therapeutic development.

Open question: how well the epistatic model generalizes when the double-mutant training data is sparse or the protein has unusual fitness landscape structure.

## Tags

`protein-engineering` `protein-language-models` `directed-evolution` `epistasis` `deep-learning` `CRISPR`
