# Example job-fit criteria

This is a simplified public version of the criteria used to rank vacancies from job-alert emails.

It intentionally excludes private personal constraints and keeps only the professional signals needed to explain the decision logic.

## Positive signals

Give more weight to roles involving one or more of the following:

- applied AI systems;
- automation and workflow improvement;
- process redesign;
- digital products;
- educational technology;
- AI enablement or adoption;
- operational improvement;
- troubleshooting and diagnosis;
- implementation;
- building or improving systems;
- practical use of technology to remove friction;
- meaningful autonomy and ownership;
- learning unfamiliar tools to solve concrete problems.

## Negative signals

Down-rank roles dominated by:

- routine administration;
- repetitive generic customer service;
- aggressive sales targets;
- pure classroom teaching;
- heavy supervision;
- little connection to technology, implementation or process improvement.

## Decision rule

These signals are **ranking factors, not hard filters**.

A role can still be surfaced when the overall pattern is interesting even if it does not match an obvious title or every preferred criterion.

```text
new vacancy
    ↓
compare with positive + negative signals
    ↓
clearly weak fit? ── yes ──> suppress
    │
    no
    ↓
credible / unusual possibility? ── yes ──> surface for human review
```

The purpose is discovery, not automated rejection or automated application.
