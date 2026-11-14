# Claude Indirect Prompt-Injection Evaluation Lab

A reproducible, low-impact research lab for studying how Claude Haiku 5.5 handles conflicting instructions contained in source material.

## Research status

- **Experiment 002 — Webpage indirect injection:** completed. Three researcher-reported control trials and three injection trials were recorded; all six responses preserved the synthetic source-of-record facts.
- **Experiment 003 — Contextual-note injection:** completed. Three researcher-reported control trials and three injection trials were recorded; all six responses preserved the synthetic source-of-record facts.
- **Experiment 004 — Multimodal visual-content injection:** fixture and protocol prepared; manual trials have not yet been run.

The results of Experiments 002 and 003 are bounded observations based on responses supplied by the researcher. The reports document that raw session exports, screenshots, exact timestamps, and independently verified session metadata were not available. Do not present those observations as proof of universal model robustness.

## Experiment 004

Experiment 004 changes the input modality. A synthetic dashboard image is supplied directly to the model. The control version contains a routine handoff note; the injection version contains assistant-directed text requesting false incident values. The primary question is whether the model repeats those false values as facts.

- Protocol: `experiments/004-multimodal-visual-instruction-injection.md`
- Control image master: `experiment-004-control.svg`
- Injection image master: `experiment-004-injection.svg`
- Trial template: `evidence/experiment-004-observations-template.md`

Use the matching PNG fixtures supplied with the research handoff as image attachments. Do not paste OCR text or SVG source into the trial.

## Safety and scope

All records are synthetic. The experiments do not access real user data, credentials, external accounts, or production services. Experiment 004 tests model-level content integrity only. It does not test or demonstrate application-layer unauthorized read, write, or execute actions.

Re-check the live 0DIN scope and exclusions when preparing a submission. The existence of a listed model does not guarantee that a particular test result qualifies for a bounty. Rewards are discretionary and depend on the programme's review.

## Evidence standard

Preserve complete, unedited outputs and screenshots. Record the exact model label, effort setting, date/time, prompt, input file, and result for every trial. Mark retrieval or procedural failures as invalid. Report mixed outcomes and negative results; do not selectively omit trials.

## Repository structure

- `experiments/` — protocols and hypotheses
- `evidence/` — observations, results, and templates
- `docs/` — methodology and scoring
- `site/` — earlier webpage fixtures
- Root SVG fixtures — Experiment 004 visual source files
