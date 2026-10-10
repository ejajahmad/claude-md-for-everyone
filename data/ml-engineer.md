# CLAUDE.md: ML Engineer / Data Scientist

<!-- For: people training, evaluating, and deploying ML models, or building LLM-powered features. -->

## Principles
- **Baselines first.** Before a complex model, establish a simple baseline (heuristic, linear, or a previous model). Every result is reported relative to it.
- **Evaluation is the product.** Define the metric, the eval set, and success criteria before training or prompt-tuning.
- **No leakage.** Split train, validation, and test before any preprocessing fits. Watch for temporal leakage and duplicate leakage. The test set is touched once.
- **Reproducibility.** Seed everything, pin package versions, log configs and data versions, and save artifacts with their metadata.

## Code
- Keep experiment code separate from production code. Notebooks are for exploration. Move reusable logic into modules.
- Assert tensor and array shapes at boundaries. Comment the expected shapes on non-obvious ops.
- Handle class imbalance deliberately, and report per-class metrics, not only accuracy.
- Make data pipelines deterministic and testable with small fixtures.

## Reporting results
- Report metrics with variance (multiple seeds or confidence intervals) where possible.
- Include error analysis: look at real failure cases, grouped by type.
- Be honest about limitations, distribution shift, and fairness concerns.

## LLM features
- Build an eval set from real examples before iterating on prompts. Track scores across prompt versions.
- Treat model output as untrusted input: validate structure, handle refusals and malformed output.
- Track cost and latency per request alongside quality.

## Don't
- Don't report test-set results that were used for tuning.
- Don't claim a model "works" based on a few cherry-picked examples.

## Project specifics
<!-- Framework (PyTorch, sklearn…), experiment tracker, compute, data location. -->
