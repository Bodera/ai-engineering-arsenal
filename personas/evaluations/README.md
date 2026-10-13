# Persona Evaluation

The purpose of evaluation is to determine whether a persona improves **software architecture and development work**. Persona outputs should be assessed by their engineering usefulness and observable decision behavior, not by how dramatically they imitate a style.

## Lightweight evaluation loop

1. Choose a scenario from [`scenarios.md`](./scenarios.md) or record a realistic task from your own work.
2. Run it once with baseline instructions and once with the selected persona. When comparing profiles, keep the model, task prompt, project context, and tools as consistent as practical.
3. Compare the outputs using the rubric below. For non-deterministic models, repeat important comparisons before drawing strong conclusions.
4. Record the result, concrete evidence, and any undesired behavior. Update the profile only when the evidence points to a stable improvement.

## Rubric (0–2 per dimension)

| Dimension | 0 — Missing or harmful | 1 — Partial | 2 — Strong |
|---|---|---|---|
| **Engineering usefulness** | Does not advance the software task or gives unusable advice | Some useful direction, but material gaps remain | Clear, relevant, actionable support for the engineering goal |
| **Decision quality** | Ignores constraints, alternatives, or key risks | Considers some relevant trade-offs | Compares viable options against context, constraints, and consequences |
| **Lens fidelity** | The persona has no observable effect or distorts the task | Some principles appear, inconsistently or superficially | The intended lens changes useful questions or decision criteria without taking over |
| **Evidence and calibration** | Invents facts, sources, or certainty | Some uncertainty/evidence is addressed, but gaps remain | Separates facts, assumptions, and uncertainty; uses verifiable evidence |
| **Actionability and proportionality** | Vague, overbuilt, or disproportionate | Partly actionable, with unnecessary complexity or omissions | Proportionate next steps, validation criteria, and appropriate depth |

For source-based personas, score **source discipline** separately when a scenario relies on their foundations: were references verified, and were source text, interpretation, and application clearly distinguished? Do not require explicit source citations in every routine coding answer.

Do not treat the total score as objective truth. Include a short qualitative note: what became better, what got worse, what the persona caused the model to notice, and whether that difference helped the engineering decision.

## Suggested result record

```text
Date / profile version:
Model and tool:
Scenario ID:
Baseline output location:
Persona output location:
Scores by dimension:
Observed improvement:
Observed regression / noise:
Decision: keep / revise / retest
```

The evaluation set is intentionally small and tool-agnostic. A future harness (for example, a local LLM evaluation runner) may execute it, but the scenarios and rubric remain the versioned source of truth in this repository.
