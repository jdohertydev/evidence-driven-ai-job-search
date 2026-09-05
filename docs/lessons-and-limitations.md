# Lessons and limitations

This project is useful partly because it shows where AI helps and where it should not be trusted without review.

## What AI helped with most

The strongest uses were not simply generating prose. They were:

- comparing a vacancy against a large amount of career evidence;
- identifying relevant experience hidden under unrelated job titles;
- extracting requirements into a structured form;
- challenging weak or unsupported claims;
- comparing alternative CV structures;
- testing whether a cover-letter paragraph was actually serving its purpose;
- separating verified facts from inference;
- repeatedly reviewing a draft against explicit criteria.

## Where human judgement mattered most

AI could produce fluent wording that was still wrong for the application. Human review was necessary to decide:

- whether a role genuinely felt worth pursuing;
- whether a project was the strongest evidence rather than merely the most impressive-sounding one;
- whether a claim fairly represented my level of experience;
- whether an inference was too speculative to publish;
- whether the writing sounded natural and specific rather than generic;
- when further iteration was making the application better versus merely different.

## Current limitations

### The application stage is not fully automated

This repository documents an AI-assisted workflow, not an autonomous application agent. Research, evidence selection, positioning, drafting and final approval still involve substantial manual judgement.

### Job-alert information can be incomplete

An email alert may not contain enough information for a confident decision. A surfaced role may still require inspection of the full advert before applying.

### Fit criteria are subjective

The ranking model represents my current career priorities. It is not a general-purpose measure of whether a vacancy is objectively good.

### Language models can overstate certainty

A model can produce plausible connections that are not sufficiently supported by the evidence. That is why source authority and claim checking are explicit parts of the workflow.

### More automation would not automatically be better

It would be technically possible to automate more of the pipeline, but application decisions involve identity, judgement and reputational risk. I currently prefer to automate repetitive retrieval and filtering while keeping higher-stakes decisions under human control.

## Possible future development

A more formal implementation could introduce structured requirement and evidence records, for example:

```json
{
  "requirement_id": "REQ-07",
  "requirement": "scripting ability",
  "evidence_ids": ["EVID-PS-01", "EVID-VBA-02"],
  "confidence": "high"
}
```

Application claims could then carry evidence references and be automatically flagged when no source supports them.

That would turn the current documented method into a more explicit **claim-provenance system** while preserving human approval at the end.
