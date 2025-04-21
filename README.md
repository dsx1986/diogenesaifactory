# 🧠 Diogenes AI Factory

> **“The real industrial revolution is when machines start building software — for us, and with us.”**

**Diogenes AI Factory** is an open multi-agent framework that enables the automation of the **entire software development lifecycle** — from idea to production — driven by intelligent agents.

This repository is the core **open SDK and agent runtime layer** of the Diogenes system. It empowers anyone to build, extend, and experiment with agents that plan, code, test, deploy, and monitor software — together.

---

## 🚀 What Is This?

Diogenes AI Factory turns product development into a collaborative workflow between **humans** and **autonomous agents**.

Imagine:
- You describe a feature → Agents generate a spec
- Agents generate code → Submit PRs → Test → Deploy
- Agents monitor behavior → Suggest fixes
- And everything is coordinated in a shared memory + orchestration layer

This repo is the **public agent SDK and core protocol implementation**. It excludes SaaS-specific infra like multi-tenancy, auth, billing, and BYOC — those live in our private repo.

---

## 🧩 What’s Inside

| Component            | Description |
|---------------------|-------------|
| `agents/`           | Modular AI agents (e.g. spec, code, test, deploy, monitor) |
| `a2a/`              | [Google A2A Protocol](https://github.com/google/A2A) integration for agent-to-agent collaboration |
| `mcp/`              | Metadata Control Plane to track task lifecycle and agent state |
| `sdk/`              | Type-safe, extensible agent SDK |
| `samples/`          | Example projects and workflows |
| `demo/`             | Local UI + CLI for interacting with agents |
| `docs/`             | Developer guide, architecture, agent contracts |

---

## 🧠 Philosophy

Diogenes AI Factory is built with a belief:

> 🏗️ **Code is not the product. The conversation that produces it is.**

Our mission is to create a world where:
- Developers focus on ideas, not scaffolding
- Teams delegate repetitive work to reliable agents
- Software builds itself — through intent, feedback, and iteration

---

## 🛠️ Getting Started

```bash
git clone https://github.com/diogenes-ai/diogenesaifactory.git
cd diogenesaifactory
uv venv
source .venv/bin/activate
uv sync
```

Then, start a local agent:

uv run agents/langgraph

Launch the UI:

cd demo/ui
uv run

Register your agents at http://localhost:12000

---

## 🧬 Build Your Own Agent

You can create custom agents with a simple spec:

```python
from sdk.agent import Agent

class MyAgent(Agent):
    def describe(self):
        return {
            "id": "my-agent",
            "name": "My Custom Agent",
            "description": "Does something cool.",
        }

    def run(self, input):
        return {"output": "Hello from MyAgent!"}

````

---

## 🤝 Contributing

We welcome:
	•	New agents (testers, doc writers, linters, UX critics!)
	•	Orchestration improvements
	•	Retrieval-augmented workflows
	•	SDK improvements and utilities

Start with CONTRIBUTING.md

---

## 📚 Documentation
	•	📖 Agent Protocol Spec
	•	🧠 Architecture
	•	🧪 Examples
	•	🚦 A2A Overview

---

## 🏗️ What’s NOT in This Repo

This public repo contains only the open framework. It does not include:
	•	SaaS multi-tenancy or auth
	•	BYOC (Bring Your Own GitHub, Jira, etc.)
	•	Cloud billing, user accounts
	•	Private infrastructure or deployments

For commercial use or integration, contact us at info@diogenes.ai

---

## ⚡ Vision

We are not just automating tasks — we are redefining what it means to build software.

Diogenes AI Factory is the first step toward a world where software engineers, product managers, and AI agents collaborate as peers.

Join us in the next revolution.

---

## 📎 License

Apache 2.0 — Open and extensible.

---

## 🌍 Connect
	•	🧭 Website: https://diogenes.ai
	•	🧪 Twitter: @DiogenesAI
	•	🧑‍💻 Community: Discord

 
