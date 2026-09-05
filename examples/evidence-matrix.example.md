# Example requirement-to-evidence matrix

This simplified example shows how I separate evidence, confidence and gaps before writing application materials.

| Requirement | Evidence | Source type | Confidence | Treatment |
|---|---|---|---:|---|
| Workflow automation | [AI-Assisted Submission-Scope Guidance](https://github.com/jdohertydev/ai-assisted-submission-scope-guidance); [Outlook Class Calendar Automation](https://github.com/jdohertydev/outlook-class-calendar-automation) | Public GitHub projects | High | Lead evidence |
| AI-assisted workflows | Controlled OpenAI use inside an n8n workflow with structured output and human review | Public GitHub project | High | Lead evidence |
| Testing / reliability | n8n failure-path testing; dry runs and SHA-256 verification in [PowerShell Photo Archive Automation](https://github.com/jdohertydev/powershell-photo-archive-automation) | Public GitHub projects | High | Emphasise |
| Scripting | PowerShell, Python and VBA examples | Projects / career history | High for practical use | Avoid claiming expert depth |
| APIs / webhooks | Portfolio examples | Public project evidence | Medium | Use precisely; avoid broad commercial-experience wording |
| Documentation / handover | Repository documentation; historical training/support work | GitHub / career history | High | Emphasise |
| Power Automate | No direct hands-on evidence identified | Gap | Low | Do not claim experience |
| Entra / Intune / Copilot Studio | No substantial direct evidence identified | Gap | Low | Record as development areas |

## Decision logic

```text
Requirement
    ↓
Is there appropriate evidence?
    ├── No → record gap / do not claim
    └── Yes
         ↓
Is the wording proportionate to the evidence?
    ├── No → narrow or qualify
    └── Yes → candidate claim
                  ↓
             final QA review
```

## Principle

The matrix is not designed to make every cell green.

A useful application should make strengths visible while also making unsupported claims difficult to introduce accidentally. A visible gap is preferable to a persuasive statement that cannot survive an interview question.
