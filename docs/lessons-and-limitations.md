# Lessons and limitations

This project is useful partly because it shows where AI helps and where it should not be trusted without review.

## What AI helped with most

The strongest uses were not simply generating prose. They were:

- comparing a vacancy against a large amount of career and project evidence;
- identifying relevant experience hidden under unrelated job titles;
- extracting requirements into a structured form;
- challenging weak or unsupported claims;
- comparing alternative CV information hierarchies;
- testing whether a cover-letter paragraph was actually serving its purpose;
- separating verified facts from inference;
- repeatedly reviewing a draft against explicit criteria.

The biggest gain came from **structured challenge**, not one-click generation.

## Where human judgement mattered most

AI could produce fluent wording that was still wrong for the application. Human review was necessary to decide:

- whether a role genuinely felt worth pursuing;
- whether a project was the strongest evidence rather than merely the most impressive-sounding one;
- whether a claim fairly represented my level of experience;
- whether an inference was too speculative to publish;
- whether the writing sounded natural and specific rather than generic;
- when further iteration was making the application better versus merely different.

## Failure modes I actively watch for

| Failure mode | Why it matters | Control |
|---|---|---|
| Incomplete job-alert data | A role can be mis-ranked from a short snippet | Treat alert screening as triage only |
| Plausible but unsupported connection | AI can make two facts sound more related than they are | Require an evidence source for important claims |
| Experience inflation | Familiarity can become expertise through wording drift | Explicit claim rules and gap recording |
| Employer-research overreach | Public signals can become confident claims about internal strategy | Separate fact from inference |
| Generic drafting | Fluent text can hide weak motivation or poor evidence | Evaluate against application-specific criteria |
| Iteration drift | Repeated rewriting can move away from the evidence | Re-check against source hierarchy after major revisions |
| Privacy leakage | Raw source material can contain personal or account information | Publish only sanitised examples and summaries |

## Current limitations

### The application stage is not fully automated

This repository documents an AI-assisted workflow, not an autonomous application agent. Research, evidence selection, positioning, drafting and final approval still involve substantial manual judgement.

That is intentional rather than an unfinished claim of autonomy.

### The discovery layer is configured rather than custom-coded

The live job-alert review runs as a scheduled ChatGPT task connected to my mailbox. I designed and refined the instructions, criteria, notification rules and output behaviour, but I did not build the scheduling or mailbox connector infrastructure.

### Job-alert information can be incomplete

An alert may omit important requirements, contract terms or context. A surfaced role still requires inspection of the full vacancy before a serious application decision.

### Deduplication is pragmatic rather than transactional

The task is instructed not to repeat roles already reported, but it does not currently maintain a dedicated database keyed by stable vacancy IDs. A formal implementation should persist source IDs and timestamps.

### Fit criteria are subjective

The ranking model represents my current career priorities. It is not a general-purpose measure of whether a vacancy is objectively good.

### Language models can overstate certainty

A model can produce plausible connections that are not sufficiently supported by the evidence. Source authority and claim checking are therefore explicit parts of the workflow.

### More automation would not automatically be better

It would be technically possible to automate more of the pipeline, but application decisions involve identity, judgement and reputational risk. I prefer to automate repetitive retrieval and filtering while keeping higher-stakes decisions under human control.

## What I would formalise next

A production-style version could introduce structured requirement, evidence and claim records, for example:

```json
{
  "requirement_id": "REQ-07",
  "requirement": "scripting ability",
  "evidence_ids": ["EVID-PS-01", "EVID-VBA-02"],
  "confidence": "high",
  "status": "supported"
}
```

Useful extensions would include:

- persistent vacancy IDs and first-seen timestamps;
- fetching and storing the full vacancy before final fit assessment;
- source URLs and retrieval dates for employer research;
- a claim ledger linking each important application statement to evidence IDs;
- automatic warnings for claims with no supporting evidence;
- explicit confidence states rather than forced yes/no matching;
- an audit trail showing when a human accepted, qualified or rejected an AI suggestion.

That would turn the current documented method into a more formal **claim-provenance and decision-support system** while preserving human approval at the end.
