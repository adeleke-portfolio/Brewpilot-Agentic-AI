# BrewPilot — Agentic AI Operations Orchestrator

> **Production-grade multi-agent AI system automating supply chain monitoring, customer support triage, and refund resolution for a specialty coffee roastery.**

Built with **LangGraph, LangChain, RAG, MCP, and LLM evaluation**.

---

## 🎯 The Problem

A mid-sized specialty coffee roastery operates with critical manual bottlenecks:

- **Manual customer support** — 40+ emails/day, each taking 10–15 minutes to investigate and reply.
- **No real-time supply chain visibility** — stockouts and supplier delays discovered only when customers complain.
- **Inconsistent policy enforcement** — refunds approved or denied arbitrarily across staff members.
- **No demand forecasting** — either over-stocks perishable beans or runs out of bestsellers.

The roastery is losing revenue through inefficiency but lacks the technical capability to build autonomous AI systems that solve these problems reliably.

## 💡 The Solution

BrewPilot is a **multi-agent orchestrator** that automates the roastery's operational workflows end-to-end:

- **Intake Agent** — reads customer emails and classifies them (Order Status, Refund, Inventory Question, Complaint).
- **Resolution Agent** — checks order history, verifies return policy via RAG, and either processes refunds or escalates.
- **Supplier Watch Agent** — monitors supplier lead times and reliability scores, flagging risks before they become stockouts.
- **Orchestrator (LangGraph)** — routes each request, manages state, enforces human-in-the-loop for high-value decisions, and logs every action.

The system proves its own value through **evaluation metrics** (touchless rate, cost per resolution, accuracy) and **live operational dashboards** (Grafana for monitoring, Power BI for business KPIs).

## ✨ Features

- [ ] **Email classification** with structured JSON output (category, sentiment, urgency)
- [ ] **Multi-agent orchestration** via LangGraph state machine
- [ ] **RAG-based policy lookup** — grounded answers from supplier contracts and return policy PDFs
- [ ] **Tool use** — SQL query, refund API, supplier database, inventory check
- [ ] **Human-in-the-loop** escalation for refunds > $500 and negative sentiment
- [ ] **Prompt injection defense** — sanitized inputs, allow-listed tools
- [ ] **Evaluation harness** — 50-email golden test set with accuracy, precision, recall
- [ ] **Live dashboards** — Grafana (ops) + Power BI (business)
- [ ] **Docker deployment** — FastAPI endpoint + containerized agents
- [ ] **Interactive Streamlit demo** — public URL for recruiters to test the system live

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Language** | Python 3.12 |
| **Data Processing** | Pandas, NumPy, Polars, DuckDB |
| **LLMs** | Claude (Anthropic), GPT-4.1 (OpenAI), Gemini 2.5 (Google) — benchmarked |
| **Agent Frameworks** | LangChain, LangGraph, CrewAI, MCP |
| **Vector Store** | ChromaDB |
| **Databases** | SQLite (dev), PostgreSQL (prod) |
| **Dashboards** | Grafana (live ops), Power BI (business story) |
| **Deployment** | Streamlit (demo), FastAPI (API), Docker (container) |
| **Evaluation** | Custom golden test set, LLM-as-judge, confusion matrix |

## 📁 Project Structure
