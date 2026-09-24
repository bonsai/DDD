# KPI

**Key Performance Indicator** — a measurable indicator used to track whether a project or product is achieving its intended outcome.

## Purpose

KPI answers:

> Are we achieving the target?

## Structure

```yaml
id: KPI-001
name: example
objective: measurable outcome
metric: metric name
target: target value
unit: unit
period: measurement period
source: data source
owner: responsible owner
```

## Rules

- Measure an outcome or critical performance condition.
- Define a target and measurement period.
- Make the data source explicit.
- Keep the metric reproducible.
- Do not confuse KPI with a task or implementation detail.

## Relationship

```text
VISION → PRD → MVP → BUILD
                   ↓
                  KPI
             outcome check
```
