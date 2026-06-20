## Featured Projects

### EVReady Pakistan

A deployed Pakistan-focused EV platform with a public frontend, public backend API, and internal AI recommender service.

The architecture routes AI recommendations through the backend gateway instead of exposing the recommender or local model runtime directly.

**Shows:** Spring Boot API gateway, React/Vite frontend, PostgreSQL, Liquibase, Docker deployment, internal service integration, async AI recommendation flow, rate limiting, persisted recommendation runs, and local Ollama/Qwen model usage.

**Repos:**
[Frontend](https://github.com/iamalimaybe/ev_ready_front) · [Backend](https://github.com/iamalimaybe/ev_ready_back) · [AI Recommender](https://github.com/iamalimaybe/evready-ai-recommender-service)

---

### RAG Document Assistant

A Java/Spring Boot RAG backend with a thin React UI for grounded document question answering, citations, missing-info handling, QA run history, and audit visibility.

**Shows:** document upload, text extraction, chunking, local embeddings with Ollama, PostgreSQL + pgvector retrieval, prompt context budgeting, structured LLM output parsing, citation validation, retrieved evidence snapshots, and persisted QA runs.

**Why it matters:** RAG answers are not accepted blindly. Retrieved chunks, cited chunks, prompts, model output, and QA runs are stored so answers can be inspected and improved.

**Release:** `v0.3-thin-react-ui`
**Repo:** [rag-document-assistant](https://github.com/iamalimaybe/rag-document-assistant)

---

### LLM Evaluation Registry

A Java/Spring Boot backend quality layer for evaluating and comparing LLM workflow behavior across prompt versions, model providers, reusable evaluation cases, individual runs, and queued batch runs.

**Shows:** prompt versioning, evaluation cases, provider abstraction, Ollama and OpenAI execution paths, raw and parsed model output storage, deterministic scoring, regression comparison, batch execution, cancellation, and review notes.

**Why it matters:** Prompt and model changes can silently make AI workflows worse. This project makes LLM behavior measurable, comparable, and auditable.

**Release:** `v0.6-openai-provider`
**Repo:** [llm-evaluation-registry](https://github.com/iamalimaybe/llm-evaluation-registry)

---

### AI Ticket Triage Service

A Java/Spring Boot backend for structured support ticket triage with validated AI output, PostgreSQL persistence, auditability, and a lightweight React review console.

**Shows:** local LLM integration through Ollama/Qwen, deterministic analyzer fallback, structured output validation, raw model output storage, confidence-based review routing, review statuses, consistent API errors, Swagger docs, Docker Compose, and CI.

**Why it matters:** AI output is treated as untrusted until it is parsed, validated, persisted, and routed through review rules.

**Release:** `v0.3-frontend-review-console`
**Repo:** [ai-ticket-triage-service](https://github.com/iamalimaybe/ai-ticket-triage-service)

---

### Requirements Intelligence Assistant

A local LLM workflow for software requirement analysis where model output must pass schema validation, semantic checks, regression tests, and structured run-report validation.

**Shows:** trusted context validation, local Ollama/Qwen execution, malformed JSON repair, output normalization, enrichment from trusted context, JSON Schema validation, semantic validation, negative tests, multi-context regression tests, and PASS/FAIL run reports.

**Why it matters:** The workflow detects unsupported, incomplete, or hallucinated model output before it is accepted.

**Release:** `v0.1-validation-first-local-llm-workflow`
**Repo:** [requirements-intelligence-assistant](https://github.com/iamalimaybe/requirements-intelligence-assistant)
