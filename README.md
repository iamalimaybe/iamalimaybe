## Featured Projects

### Requirements Intelligence Assistant

Validation-first local LLM workflow for grounded software requirement analysis.

This project demonstrates a production-aware LLM pipeline where model output is treated as untrusted until it passes deterministic validation. It uses Ollama, trusted context JSON, JSON Schema validation, context-driven semantic validation, negative regression tests, multi-context regression, structured run reporting, and local model comparison.

**Tech:** Python, Ollama, JSON Schema, local LLMs, validation pipelines, regression testing

**Key engineering focus:**

* Local LLM workflow using `qwen3:4b` and `qwen3:8b`
* Trusted context JSON as the semantic source of truth
* Prompt generation from structured requirement context
* Malformed JSON repair fallback
* Deterministic normalization and enrichment
* JSON Schema validation
* Context-driven semantic validation
* Positive and negative regression tests
* Multi-context validation across different requirement types
* Structured run reports and run-report schema validation
* Local model comparison runner

**Positioning:**
I built this to show how LLM output can be grounded, validated, tested, and accepted or rejected through deterministic engineering checks instead of trusting raw model responses.

[View repository](https://github.com/iamalimaybe/requirements-intelligence-assistant)
