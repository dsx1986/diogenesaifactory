---
# 🧠 Diogenes AI Factory — Public Repo Documentation

## Overview
This public repo is the **core multi-agent SDK and orchestration layer** for autonomous software development. It implements:
- Agent-to-Agent protocol (A2A)
- Metadata Control Plane (MCP)
- SDK to build, compose, and run agents

This repo **does not** contain SaaS infrastructure, authentication, or tenant-specific logic.

## Vision
> **The machine that builds the machine.**

Diogenes AI Factory enables an agentic system that takes **any user software requirement** (e.g. “build me a SaaS”), and:
1. Generates a **software repository** that contains a complete SaaS product (equivalent to this public repo)
2. Optionally generates a **full-stack platform repo** (equivalent to public + private repo, differing only by environment config)
3. Can output **self-generating systems** — that is, a repo that can re-use Diogenes to produce further SaaS systems (self-assembling software factories)

## Architecture Summary

### Components
- **Agent SDK**: Build task-oriented agents with consistent APIs
- **MCP Server**: Tracks task metadata, status transitions, retries, and agent output
- **Agent Protocol**: Agents follow a JSON contract with schemas, capabilities, and I/O
- **Demo UI**: Register agents, submit tasks, observe lifecycle

### Life Cycle (Phase 1)
1. User prompts spec → Spec Agent
2. Code Agent generates PR → GitHub
3. Test Agent runs unit/integration tests
4. Deploy Agent pushes to Cloud Run
5. Monitor Agent tracks metrics + logs

### Extensibility
- Add new agents with well-defined schema
- Plug in A2A-compatible models or backends
- Extend `sdk/agent.py` base class

## Reinforcement Learning Loop (Phase 4+)
- **Feedback Loop**: Runtime monitoring and human-in-the-loop feedback
- **Reward Signal**: Based on test pass rate, PR approval time, incident counts
- **RL Agent**: Adjusts planning agent or retry logic to improve delivery quality

## Future Extensions
- Embedding + retrieval (RAG + vector store)
- Multimodal file support (PDFs, images, video, audio)
- Persistent memory for agents
- Recursive self-replication capabilities

## Usage
For SDK/API usage, see `/docs/AGENT_SDK.md`
For agent definitions, see `/agents/*`

---
