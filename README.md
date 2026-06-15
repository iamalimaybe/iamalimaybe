## Featured Projects

### LLM Evaluation Registry

A Java/Spring Boot backend quality layer for evaluating and comparing LLM workflow behavior across prompt versions, model providers, reusable evaluation cases, individual runs, and queued batch runs.

The registry tracks workflows, prompt versions, test cases, model runs, raw outputs, parsed structured outputs, scoring results, batch progress, regression comparisons, and review notes so LLM behavior can be measured instead of guessed.

It supports local Ollama execution, optional OpenAI provider execution, deterministic JSON parsing, scoring rules, single-run regression comparison, queued batch evaluation, batch cancellation, and batch-level regression comparison.

This project shows how AI behavior can be tested, compared, persisted, and reviewed through backend engineering instead of relying on informal prompt testing.

#### What it demonstrates

* Java 17 and Spring Boot backend API design
* PostgreSQL persistence with Liquibase migrations
* provider-based model execution abstraction
* local LLM execution through Ollama
* optional OpenAI provider integration
* controlled prompt execution for structured JSON output
* raw model output capture
* parsed JSON output storage
* deterministic evaluation against expected fields, required facts, and forbidden claims
* critical scoring rules for high-risk checks
* single-run regression comparison
* queued batch evaluation across enabled evaluation cases
* batch progress tracking with pass/fail/error counts and average score
* batch cancellation for queued and running batches
* batch-level regression comparison with per-case differences
* review notes and audit-friendly result storage
* Swagger/OpenAPI documentation
* Docker Compose setup for app and PostgreSQL
* unit tests for evaluator, regression comparison, batch comparison, provider routing, Ollama client, and OpenAI client

#### Why it matters

Prompt and model changes can silently make an AI workflow worse.

This project treats LLM behavior as something that should be measured, compared, and reviewed. The focus is not chatbot interaction. The focus is building a backend evaluation layer where AI output is captured, validated, scored, compared, and made auditable.

#### Proof

Latest release tag:

`v0.6-openai-provider`

Key completed releases:

* `v0.1-registry-core`
* `v0.2-model-execution-evaluation`
* `v0.3-evaluator-scoring-rules`
* `v0.4-queued-batch-evaluation`
* `v0.5-batch-comparison`
* `v0.6-openai-provider`

Repository:

[View repository](https://github.com/iamalimaybe/llm-evaluation-registry)

---

### AI Ticket Triage Service

A Java/Spring Boot backend for structured support ticket triage with validated AI output, PostgreSQL persistence, auditability, and human review workflows.

The service accepts support tickets, analyzes them using either deterministic logic or a local Ollama model, validates the structured analysis result, stores both raw and parsed output, and exposes APIs plus a lightweight React review console.

This project shows how LLM output can be handled inside a backend system where correctness, persistence, and reviewability matter.

#### What it demonstrates

* Java 17 and Spring Boot backend API design
* local LLM integration through Ollama and Qwen3
* deterministic analyzer fallback for stable development and tests
* structured AI output parsing and validation
* raw model output storage for audit/debugging
* PostgreSQL persistence with Liquibase migrations
* confidence-based review decisioning
* review status workflow with `NEEDS_REVIEW`, `REVIEWED`, and `NOT_REQUIRED`
* consistent API error responses
* Swagger/OpenAPI documentation
* Docker Compose setup for app and PostgreSQL
* lightweight React + TypeScript frontend review console
* GitHub Actions CI for backend tests and frontend build

#### Why it matters

AI features are risky when model output is accepted directly.

This project treats AI output as untrusted until it is parsed, validated, persisted, and routed through review rules when needed. The focus is not chatbot behavior. The focus is building production-aware backend workflows around AI output.

#### Proof

Release tag:

`v0.3-frontend-review-console`

Repository:

[View repository](https://github.com/iamalimaybe/ai-ticket-triage-service)

---

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
