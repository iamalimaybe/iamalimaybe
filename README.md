## Featured Projects

### Requirements Intelligence Assistant

A local LLM workflow for software requirement analysis where model output is treated as untrusted until it passes validation, semantic checks, regression tests, and structured run-report validation.

This project shows practical AI-integrated engineering from a backend perspective. The focus is not model training or ML research. The focus is building reliable software workflows around LLMs.

#### What it demonstrates

* trusted context validation before prompt generation
* local LLM execution through Ollama and Qwen3
* structured JSON output handling
* malformed JSON repair fallback
* output normalization and enrichment from trusted context
* JSON Schema validation
* context-driven semantic validation
* positive, negative, and multi-context regression tests
* structured run reports with PASS/FAIL validation

#### Why it matters

Many AI features work in demos but fail in real workflows because the output is not validated, tested, or tied back to trusted business context.

This project demonstrates how LLM output can be used inside a controlled backend-style workflow where incorrect, incomplete, or unsupported results are detected before being accepted.

#### Tested contexts

* payment webhook integration
* production report backend workflow
* review moderation admin workflow

#### Proof

Release tag:

`v0.1-validation-first-local-llm-workflow`

Main demo command:

`python .\scripts\run_demo_multi_context_workflow.py --model qwen3:4b`

Repository:

[View repository](https://github.com/iamalimaybe/requirements-intelligence-assistant)
