# A/B Adoption Results

## Compact Comparison

Metric| Baseline| Workflow
---|---|---
Runs| 10| 10
Avg Score| 3.0| 4.6
Avg Time (s)| 12.55| 14.0
Median Time (s)| 9.84| 11.53
Avg Constraint Score| 4.0| 4.0
Avg Dependency Score| 5.0| 5.0
Avg Artifact Usage| 0.0| 4.2
Avg Self Repair| 2.0| 4.0

## Count By Condition

- `baseline`: 10
- `workflow`: 10

## Average Total Score By Condition

- `baseline`: 3.0
- `workflow`: 4.6

## Timing By Condition

- `baseline` average elapsed seconds: 12.55
- `baseline` median elapsed seconds: 9.84
- `baseline` fastest run: codex-baseline-task5-rerun2 (0.47s)
- `baseline` slowest run: codex-baseline-task1-rerun1 (41.68s)
- `workflow` average elapsed seconds: 14.0
- `workflow` median elapsed seconds: 11.53
- `workflow` fastest run: codex-workflow-task4-rerun2 (0.69s)
- `workflow` slowest run: codex-workflow-task1-rerun1 (41.68s)

## Average Subscores By Condition

- `baseline`:
  - constraint_adherence: 4.0
  - dependency_discipline: 5.0
  - artifact_usage: 0.0
  - self_repair_behavior: 2.0
  - handoff_quality: 1.2
- `workflow`:
  - constraint_adherence: 4.0
  - dependency_discipline: 5.0
  - artifact_usage: 4.2
  - self_repair_behavior: 4.0
  - handoff_quality: 4.0

## Average Reliability Metrics By Condition

- `baseline`:
  - unnecessary_dependencies: 0.0
  - repeated_mistakes: 0.0
  - ignored_constraints: 0.0
  - repair_iterations: 0.0
  - artifact_reads: 0.0
  - artifact_writes: 0.0
- `workflow`:
  - unnecessary_dependencies: 0.0
  - repeated_mistakes: 0.0
  - ignored_constraints: 0.0
  - repair_iterations: 0.0
  - artifact_reads: 4.0
  - artifact_writes: 2.4

## Common Failures

- `baseline`:
  - none recorded
- `workflow`:
  - none recorded
