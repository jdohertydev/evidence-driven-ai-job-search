# Evidence and claim controls

The application stage is evidence-constrained. Persuasive wording is useful only when the underlying claim is accurate, relevant and defensible.

The purpose of this control layer is not to make every requirement look like a match. It is to make unsupported claims difficult to introduce accidentally.

## Source hierarchy

Different sources answer different questions. They are not interchangeable.

| Source | Authority | Typical use |
|---|---|---|
| Job advert | Employer-stated requirements | What the role asks for |
| Employer/public research | Business and role context | Understanding the environment; not inventing insider knowledge |
| Career-history records | Employment evidence | Responsibilities, systems used and historical examples |
| Qualification certificate | Qualification evidence | Exact award title, result and date |
| GitHub repositories | Project evidence | Scope, technologies, testing, limitations and implementation decisions |
| First-person input | Motivation and judgement | Why the work interests me; how I made decisions |

When sources conflict, the more authoritative source wins for that type of claim. For example, the certificate is authoritative for the exact qualification wording even if an older CV describes it differently.

## Claim states

Before important wording is used, I treat it as one of five states:

| State | Meaning | Action |
|---|---|---|
| **Supported** | Directly backed by an appropriate source | Use if relevant |
| **Supported with qualification** | Broadly true but easy to overstate | Narrow the wording |
| **Inference** | Reasonable interpretation rather than established fact | Label internally; publish only when appropriate |
| **Gap** | Requirement exists but supporting evidence does not | Keep as a development area |
| **Unsupported** | No reliable basis for the statement | Remove |

This is more useful than a simple match/no-match model because it preserves uncertainty instead of forcing every item into a positive answer.

## Claim rules

The workflow explicitly rejects common forms of inflation:

- **Exposure ≠ expertise**
- **Project work ≠ commercial experience**
- **Learning ≠ certification**
- **Prototype ≠ production system**
- **Familiarity ≠ mastery**
- **AI-assisted development ≠ wholly unaided authorship**
- **Reasonable inference ≠ verified employer fact**

If evidence is missing, the claim is removed, narrowed or recorded as a gap.

## Worked examples

| Candidate statement | Evidence state | Treatment |
|---|---|---|
| Built a VBA tool to improve a staff workflow | Supported by career history | Use |
| Designed, configured, tested and documented an n8n/OpenAI portfolio workflow | Supported by public repository | Use |
| Experienced Power Automate developer | No direct hands-on evidence identified | Do not claim |
| Microsoft experience | Too broad to be useful without context | Replace with the specific tools and tasks actually evidenced |
| Morgan & Morgan is expanding its AI delivery capability | Interpretation of public material | Treat as inference, not insider fact |

## Claim provenance

The ideal form of this process is not just a document containing good sentences. It is a set of claims that can be traced back to evidence.

A simplified record might look like:

```json
{
  "claim_id": "CLM-014",
  "claim": "Built an n8n workflow using controlled OpenAI output and human review",
  "evidence_ids": ["EVID-GH-001"],
  "status": "supported",
  "use": "cv-project-section"
}
```

The current application process uses this idea conceptually rather than through a full software implementation. The structured example shows the direction I would take if the workflow were formalised further.

## Public-data boundary

The public repository is deliberately sanitised. It does not publish raw private conversations, private email content, personal salary/living-cost information, credentials, account identifiers or source documents containing unnecessary personal data.

The worked example uses enough detail to explain the method without publishing the entire private application workspace.

## Final audit

Before an important sentence survives into an application, I use five questions:

1. **Is it true?**
2. **Can I evidence it?**
3. **Is it relevant to this role?**
4. **Is it stronger than the truthful alternatives?**
5. **Could I defend it if challenged in an interview?**

A sentence that fails any of those tests should not survive merely because it sounds good.
