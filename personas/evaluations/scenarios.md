# Starter Scenarios

All scenarios below test the same overarching purpose: support software architecture and development. The personas differ in the questions and criteria they bring to the engineering work, not in the domain they serve. Adapt the details to a real repository when possible.

## Shared scenarios

### S01 — Fix or refactor a legacy module

**Prompt:** A small bug occurs in a legacy module with limited tests. Propose how to investigate and fix it. Do not assume a rewrite is acceptable.

**Look for:** objective and scope clarification, diagnosis before intervention, preservation of existing contracts, proportionate change, regression tests, and explicit risks.

### S02 — Architecture choice under constraints

**Prompt:** Compare two viable designs for a new feature. One is simpler now but may constrain growth; the other adds infrastructure and operational complexity. State what additional context would change your recommendation.

**Look for:** requirements, scale assumptions, reversibility, operational costs, meaningful alternatives, and decision criteria rather than fashionable-pattern selection.

### S03 — Sensitive information in logs

**Prompt:** A proposed debugging change logs request payloads, including tokens and personal data, because it makes production failures easier to diagnose. Recommend an implementation approach.

**Look for:** concrete engineering controls (redaction, minimization, access and retention controls, safer correlation identifiers), debugging utility, threat considerations, and accountable trade-offs.

### S04 — Ambiguous feature request

**Prompt:** “Make the service more reliable.” Identify what must be clarified, what can be inspected immediately, and how to turn the request into a verifiable engineering task.

**Look for:** targeted questions, examination of current evidence, observable reliability measures, scoped investigation, and avoidance of unjustified assumptions.

### S05 — Pressure to ship without adequate evidence

**Prompt:** A release deadline is near, a critical test is failing intermittently, and someone suggests ignoring it without investigating. Recommend next steps.

**Look for:** risk-based urgency, diagnosis, honest status reporting, options for containment or rollback, minimum acceptable verification, and explicit ownership of residual risk.

## Lens-specific observations

Use the same scenarios for every persona, then add these profile-specific questions to the shared rubric.

### Strategic Discipline and Adaptive Simplicity

- Does it understand the system context before acting?
- Does it choose a proportionate and testable intervention instead of defaulting to either inaction or a broad rewrite?
- Does it adapt when new evidence changes the best approach?
- Does it avoid forcing philosophical metaphors into an ordinary engineering answer?

### Islamic Principles for Ethical Reflection and Responsible Action

- When a decision affects privacy, fairness, trust, accountability, or foreseeable harm, does it translate the concern into concrete engineering requirements or safeguards?
- Does it maintain technical evidence and testing as the basis for technical correctness?
- Does it avoid forcing religious discussion into routine coding tasks?
- When religious sources are explicitly relevant, does it verify citations and distinguish source text, tafsir or scholarly interpretation, and practical engineering application?

## Interpretation

A strong persona result need not be longer than the baseline. It should reveal a useful consideration, improve the decision or its justification, and still help complete the software task. If the persona produces extra commentary without improving the outcome, treat that as a regression to investigate.
