# 👋 Hi, I’m Pranav Tyagi

I’m an **ML / AI Engineer** focused on building **reliable, production-grade AI systems** where correctness, latency, and cost matter more than flashy demos.

My work centres on:
- LLM systems with **guardrails**
- **Agentic workflows** with deterministic cores
- ML systems that **explain outputs or explicitly return uncertainty**

---

## 🔍 Selected Projects

### 🧠 Market Anomaly Narrative Engine (MANE)
**Detect crypto price anomalies. Explain why they happened. Never hallucinate.**

**Problem**  
Market dashboards show *what* moved, but rarely *why*. Naive LLM approaches hallucinate causal stories between unrelated events — unacceptable in quantitative finance.

**Solution**  
A **three-phase ML + agentic pipeline** that only produces explanations when evidence supports them.

**How it works**
- Deterministic detection: Z-score, Bollinger Bands, volume spikes  
- Causal filtering: News constrained to ±30-minute windows  
- LLM investigation: Tool-using agent gathers context  
- Sceptical validation: Rule-based checks + Judge LLM  
- Fail-safe output: Returns `"Unknown"` if causality is unproven

**Why it matters**
- Prevents hallucinated financial narratives  
- Combines statistical rigour with LLM reasoning  
- Models *uncertainty* instead of hiding it

**Engineering highlights**
- Workflow-first architecture (predictable, testable)
- Deterministic replay mode for reproducible testing
- Multi-provider LLM support via LiteLLM
- Cost-optimized: **$0/month in production** using free RSS sources

**Tech stack**  
Python · PostgreSQL · SQLAlchemy · sentence-transformers · HDBSCAN · LiteLLM

🔗 **Repository:** https://github.com/tyagiprnv/market-anomaly-narrative-engine

---

### 🏨 AI Guest Response Agent
**Production-quality AI agent for accommodation guest inquiries**

**Problem**  
Most LLM agents are too slow, expensive, and unsafe for real production use.

**Solution**  
A **low-latency, cost-optimised, and fully monitored AI agent** with strong safety guardrails.

**Key design decisions**
- Template-first RAG to avoid unnecessary LLM calls
- LangGraph-based agentic routing
- Fast-path guardrails (~90ms) using regex topic filters
- Direct template substitution for zero-token responses

**Measured performance**
- p50 latency: ~90ms  
- p99 latency: ~5s  
- ~60% of requests served without an LLM call

**Production features**
- PII redaction and topic filtering
- LangSmith tracing
- Prometheus metrics + Grafana dashboards
- Docker Compose deployment
- Unit, integration, and E2E tests

**Tech stack**  
LangGraph · FastAPI · Qdrant · OpenAI embeddings · Groq (LLaMA 3.1) · Prometheus · Grafana · Docker

🔗 **Repository:** https://github.com/tyagiprnv/ai-guest-response-agent

---

## 🧩 Interests & Focus Areas
- ML systems combining **deterministic logic + learned models**
- LLM evaluation, guardrails, and failure analysis
- Cost-efficient and latency-aware AI architectures
- Applied ML in finance, marketplaces, and real-world decision systems

---

## 📫 Get in Touch
- GitHub: https://github.com/tyagiprnv
- LinkedIn: https://www.linkedin.com/in/pranav-tyagii/
