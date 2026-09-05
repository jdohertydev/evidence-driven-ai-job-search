# Job-fit screening

The discovery problem is not simply finding vacancies containing a particular keyword. Job titles are inconsistent, and a role outside an obvious career path can still be highly relevant.

The screening workflow therefore uses **career-fit signals** rather than a single title match.

## Where the criteria came from

The criteria were defined before the Morgan & Morgan application. They came from a broader review of the kind of work I repeatedly find engaging: improving broken or inefficient processes, applying technology to practical problems, troubleshooting, implementing systems, learning unfamiliar tools and taking useful work through to a functioning result.

For the public repository, those preferences are deliberately reduced to professional job-fit signals rather than publishing the underlying private career-reflection material.

## Positive signals

Examples include:

- applied AI systems;
- workflow or process improvement;
- automation;
- digital products;
- educational technology;
- AI enablement or adoption;
- operational improvement;
- practical problem-solving with technology;
- troubleshooting;
- implementation;
- building or improving systems;
- turning ideas into useful working processes;
- meaningful autonomy and real responsibility.

## Negative signals

Examples include roles dominated by:

- routine administration;
- generic repetitive customer service;
- aggressive sales;
- pure classroom teaching;
- heavy supervision;
- little connection to systems improvement or technology.

These are **ranking signals, not hard filters**. The workflow is intentionally biased toward surfacing an unusual but potentially good opportunity rather than pretending it can make a definitive career decision.

## Current implementation

The current discovery layer is implemented as a scheduled ChatGPT task connected to my mailbox.

On each run it:

1. checks for new Indeed job-alert messages since the previous run;
2. reviews the vacancy information available in those alerts;
3. assesses each role against the defined fit criteria;
4. suppresses clearly weak matches;
5. surfaces strong or credible possible matches with reasons and uncertainties;
6. avoids intentionally repeating roles already reported;
7. leaves the decision to inspect the full vacancy or apply with me.

This distinction matters: **the orchestration is a configured AI task, not a custom application that I coded.** The value I am demonstrating here is the workflow design, criteria, controls and way the output feeds a higher-stakes evidence process.

## Triage, not final assessment

Job-alert emails can be incomplete. A short alert may omit important requirements, contract terms or context.

For that reason the screening result is treated as a triage decision:

```text
Alert says "possible fit"
        ↓
Human opens / verifies the full vacancy
        ↓
Only then does deeper application analysis begin
```

A confident application decision should never be based solely on an email snippet.

## Deduplication

The task is instructed not to repeat roles already reported. This is a practical conversational control rather than a dedicated external vacancy database with immutable IDs.

That means deduplication is useful but not presented as mathematically guaranteed. A more formal implementation would persist stable job IDs, source URLs and first-seen timestamps in a structured store.

## Why Morgan & Morgan was significant

The Morgan & Morgan AI / Automation Engineer vacancy strongly matched several signals at once: automation, AI, process improvement, troubleshooting, implementation, testing, documentation, communication and learning unfamiliar technology.

More importantly, those signals existed **before** the vacancy was analysed. The worked example therefore shows the discovery system finding a role that already matched the model rather than redefining the model to fit a target employer.

See the simplified public [job-fit criteria example](../examples/job-fit-criteria.example.md).
