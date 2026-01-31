👋 Hi, I’m Pranav Tyagi

I’m an ML / AI Engineer focused on building reliable, production-grade AI systems — especially where correctness, latency, and cost matter more than flashy demos.

My work centers on:

LLM systems with guardrails

Agentic workflows with deterministic cores

ML systems that explain their outputs (or admit uncertainty)

Below are two recent projects that best represent how I think and build.

🔍 Selected Projects
🧠 Market Anomaly Narrative Engine (MANE)

Detect crypto price anomalies. Explain why they happened. Never hallucinate.

Problem
Market dashboards tell you what moved, but not why. Naive LLM approaches hallucinate causal stories between unrelated events — unacceptable in quantitative finance.

What I built
A three-phase ML + agentic system that only produces explanations when evidence supports them.

How it works

Deterministic detection: Z-score, Bollinger Bands, volume spikes

Causal filtering: News constrained to a ±30 min window

LLM investigation: Tool-using agent gathers context

Skeptical validation: Rule-based + Judge LLM verification

Fail-safe output: Returns "Unknown" if causality is unproven

Why it matters

Prevents hallucinated financial narratives

Combines statistical rigor with LLM reasoning

Explicitly models uncertainty instead of hiding it

Engineering highlights

Workflow-first architecture (predictable, testable)

Deterministic replay mode for 100% reproducible tests

Multi-provider LLM support via LiteLLM

Cost optimized: $0/month in production using free RSS sources

Tech stack
Python · SQLAlchemy · PostgreSQL · sentence-transformers · HDBSCAN · LiteLLM · CLI tooling

🔗 Repository: (link your MANE repo here)

🏨 AI Guest Response Agent

Production-quality AI agent for accommodation guest inquiries

Problem
Most LLM agents are slow, expensive, and unsafe for production customer-facing use.

What I built
A low-latency, cost-optimized, monitored AI agent with strong safety guarantees.

Key design decisions

Template-first RAG: Skip LLM calls whenever possible

Agentic routing: LangGraph workflow with conditional execution

Fast-path guardrails: Regex-based topic filtering (~90ms)

Direct template substitution: Zero-token responses for common queries

Measured performance

p50 latency: ~90ms

p99 latency: ~5s

60% of requests served without an LLM call

Production features

PII redaction & topic filtering

LangSmith tracing

Prometheus metrics + Grafana dashboards

Full Docker Compose deployment

Unit, integration, and E2E tests

Why it matters
This project demonstrates real-world ML engineering:

Latency vs quality tradeoffs

Cost-aware system design

Observability and failure modes

Shipping AI safely, not just making it work

Tech stack
LangGraph · FastAPI · Qdrant · OpenAI embeddings · Groq (LLaMA 3.1) · Prometheus · Grafana · Docker

🔗 Repository: (link your agent repo here)

🧩 What I’m Especially Interested In

ML systems that combine deterministic logic + learned models

LLM evaluation, guardrails, and failure analysis

Cost-efficient AI architectures

Applied ML in finance, marketplaces, and real-world decision systems

📫 Get in Touch

GitHub: https://github.com/your-username

LinkedIn: (optional)
