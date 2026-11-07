# bulletproofsoftware-ai

**Open-source infrastructure for building reliable, governed, self-hostable AI-agent systems.**

A suite of composable, self-hosted building blocks for AI agents — persistent memory,
multi-agent orchestration, governance, compliance and runtime security, and the developer
tooling that ties them together. The services are self-hosted; the plugins run inside
Claude Code.

🌐 [bulletproofsoftware.ai](https://bulletproofsoftware.ai)

---

## 🧠 Memory

| Repo | What it does |
|------|--------------|
| [**bulletproof-memory**](https://github.com/bulletproofsoftware-ai/bulletproof-memory) | Persistent, tiered memory for AI agents — an MCP server with semantic recall, a web dashboard, and the scheduled maintenance workflows that keep it healthy. |
| [bulletproof-process-knowledge-mcp](https://github.com/bulletproofsoftware-ai/bulletproof-process-knowledge-mcp) | MCP server exposing a `process_knowledge` Qdrant collection through three tools: semantic query, exact lookup, record validation. |

## 🎼 Orchestration

| Repo | What it does |
|------|--------------|
| [bulletproof-conductor-kernel](https://github.com/bulletproofsoftware-ai/bulletproof-conductor-kernel) | Domain-agnostic orchestration kernel for multi-agent workflows in Claude Code: tier classification, gate enforcement, audit-logged state. |
| [bulletproof-conductor-dev](https://github.com/bulletproofsoftware-ai/bulletproof-conductor-dev) | The dev-domain workflow orchestrator built on the kernel — multi-agent pipelines with programmatic phase-gate enforcement and requirement tracking. |
| [bulletproof-orchestrator](https://github.com/bulletproofsoftware-ai/bulletproof-orchestrator) | A lightweight orchestrator posture for Claude Code: scout, verifier and worker subagents with an enforced citation return contract. |
| [bulletproof-event-router](https://github.com/bulletproofsoftware-ai/bulletproof-event-router) | A central event dispatcher: receive events, match routing rules, fan out to n8n, state, and actions. |
| [bulletproof-metrics-engine](https://github.com/bulletproofsoftware-ai/bulletproof-metrics-engine) | Outcome metrics and predictive scaling from your event stream. |

## 🛡️ Governance, Security & Compliance

| Repo | What it does |
|------|--------------|
| [bulletproof-governance-plugin](https://github.com/bulletproofsoftware-ai/bulletproof-governance-plugin) | An agent-governance framework for Claude Code: identity, trust, audit, policy, and memory governance. |
| [bulletproof-compliance](https://github.com/bulletproofsoftware-ai/bulletproof-compliance) | A central compliance system: projects send evidence to one server, which keeps it in a tamper-evident ledger and generates NIST SSDF, SOC 2 change-management, AI provenance, SBOM/VEX and OSCAL documents. |
| [bulletproof-runtime-security](https://github.com/bulletproofsoftware-ai/bulletproof-runtime-security) | Runtime security and SOC2-style evidence for AI agents: identity, behavior, threats, and memory integrity. |
| [bulletproof-codehardener](https://github.com/bulletproofsoftware-ai/bulletproof-codehardener) | Security assurance platform for AI-first developers: open-source security tools behind one interface that coding agents call through MCP. |
| [bulletproof-validation-gate](https://github.com/bulletproofsoftware-ai/bulletproof-validation-gate) | A Claude Code Stop hook that refuses unverified "done" claims — an adversarial verifier for completion. |

## 🔌 Agent Infrastructure

| Repo | What it does |
|------|--------------|
| [bulletproof-a2a-gateway](https://github.com/bulletproofsoftware-ai/bulletproof-a2a-gateway) | An agent-to-agent gateway: authenticated, rate-limited, audited invocation between agents, with an MCP bridge. |
| [bulletproof-agent-economics](https://github.com/bulletproofsoftware-ai/bulletproof-agent-economics) | Cost metering, budget monitoring, model routing, and chargeback for multi-agent systems. |
| [bulletproof-markdown-for-agents](https://github.com/bulletproofsoftware-ai/bulletproof-markdown-for-agents) | A self-hosted proxy that turns web pages and documents into clean, agent-ready Markdown, with prompt-injection detection in front of the agent. |

## 🧰 Tooling

| Repo | What it does |
|------|--------------|
| [bulletproof-context-guard](https://github.com/bulletproofsoftware-ai/bulletproof-context-guard) | Claude Code plugin that measures where your context window actually goes — and warns before you run out. |
| [bulletproof-docs-portal](https://github.com/bulletproofsoftware-ai/bulletproof-docs-portal) | Minimal local web app to browse and PDF-export project documentation across the projects under one root directory. |

---

## Install via the bulletproof marketplace

The Claude Code plugins are published through one catalog,
[bulletproofsoftware-ai/bulletproof-marketplace](https://github.com/bulletproofsoftware-ai/bulletproof-marketplace).
Each entry is pinned to a release tag, so compatible versions install together and updates
arrive in one place. In a Claude Code session:

```text
/plugin marketplace add bulletproofsoftware-ai/bulletproof-marketplace
/plugin install context-guard@bulletproof
```

The marketplace README lists every plugin it carries and how to turn on auto-update.

## Getting started

Most services are self-hostable via Docker and ship with an `.env.example` and a
README. The **[memory system](https://github.com/bulletproofsoftware-ai/bulletproof-memory)**
is a good place to start — one clone + `./install.sh` brings up the full stack.

Contributions are welcome: see [CONTRIBUTING.md](https://github.com/bulletproofsoftware-ai/.github/blob/main/CONTRIBUTING.md)
and the [Code of Conduct](https://github.com/bulletproofsoftware-ai/.github/blob/main/CODE_OF_CONDUCT.md).

All project repositories are licensed **Apache-2.0**.
