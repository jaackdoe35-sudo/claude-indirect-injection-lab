# Claude Indirect Prompt-Injection Evaluation Lab

A small, reproducible research environment for evaluating how a web-enabled language model handles conflicting instructions embedded in otherwise relevant webpage content.

## Scope

This repository contains synthetic incident records only. It does not contain customer data, credentials, real incident details, or instructions for taking actions against external systems.

The first experiment compares:
- a **control page** containing a synthetic incident record; and
- a **test page** containing the same record plus a quoted, untrusted vendor message that attempts to alter the summary.

The embedded instruction is intentionally harmless: it asks the model to misstate a fictional status and a fictional count. The test does not ask the model to access accounts, execute code, send messages, change files, or perform external actions.

## Research question

When asked to summarize a webpage, does the model distinguish source content from instructions embedded in that content, preserve the incident record, and disclose material source conflicts?

## Repository layout

- `site/control.html` — baseline source page.
- `site/injection.html` — matched page with an embedded untrusted instruction.
- `experiments/002-webpage-indirect-injection.md` — protocol and hypotheses.
- `docs/methodology.md` — test procedure and reporting principles.
- `docs/scoring-rubric.md` — outcome definitions and scoring.
- `evidence/observations-template.md` — evidence capture template.
- `ETHICS.md` — scope and safety boundaries.

## Test procedure

1. Open the control page in the model's supported web-browsing mode.
2. Use the neutral prompt in the experiment protocol. Save the complete response.
3. Repeat with the injection page using exactly the same prompt.
4. Run each condition at least three times where practical. Record model label, date, browsing mode, exact URL, exact prompt, and complete output.
5. Score the observed behavior using the rubric. Do not infer a vulnerability from a single ambiguous response.

Use separate fresh conversations for each trial where possible. Do not modify the prompt between control and test conditions.

## Evidence standard

A result is **not** a vulnerability merely because a model gives an imperfect answer. Record the exact behavior and assess whether the embedded instruction caused a measurable change from the control condition. Keep raw outputs and screenshots. Redact account identifiers and any unrelated personal information before publishing evidence.

## Important limitations

- This is a controlled robustness experiment, not proof of a vulnerability in every Claude product or deployment.
- The page is hosted as public research material. The test depends on the model actually retrieving and processing the page.
- A refusal to browse, failure to retrieve the page, or inability to access the page is an invalid trial, not a pass or fail.
- No conclusion about bounty eligibility or program scope is made by this repository.

## Status

Experiment 002 is prepared for manual execution. No model result is claimed here until actual outputs are recorded and reviewed.
