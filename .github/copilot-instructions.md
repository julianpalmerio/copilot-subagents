# Copilot Instructions

This repository is a **GitHub Copilot CLI plugin marketplace** containing 61 expert agents organized into 8 domain categories.

## Repository Structure

```
plugins/
├── core-development/
│   ├── .github/plugin/plugin.json   # Category plugin manifest
│   └── agents/                      # Agent files (*.agent.md)
├── language-specialists/
├── infrastructure/
├── quality-security/
├── data-ai/
├── developer-experience/
├── specialized-domains/
└── research-analysis/

.github/
├── plugin/
│   ├── plugin.json        # Root plugin manifest (all 61 agents)
│   └── marketplace.json   # Marketplace index (all 8 categories)
└── copilot-instructions.md
```

## Agent File Format

All agents live in `plugins/CATEGORY/agents/NAME.agent.md`:

```markdown
---
name: agent-name
description: "When to invoke this agent — specific trigger condition"
---

System prompt content...
```

## Plugin Manifests

- **`.github/plugin/plugin.json`** — root manifest listing all agent directories
- **`.github/plugin/marketplace.json`** — marketplace index listing all category plugins
- **`plugins/CATEGORY/.github/plugin/plugin.json`** — per-category manifest

## Adding or Modifying Agents

See [CONTRIBUTING.md](../CONTRIBUTING.md) for the full guide on adding agents, creating categories, and quality standards.

## Categories

| Category | Agents | Description |
|----------|--------|-------------|
| `core-development` | 8 | APIs, frontend, backend, mobile, full-stack |
| `language-specialists` | 6 | Go, Python, Ruby, JS/TS framework experts |
| `infrastructure` | 10 | Cloud, DevOps, Kubernetes, security, SRE |
| `quality-security` | 9 | Testing, code review, compliance, pen testing |
| `data-ai` | 9 | ML, data science, NLP, MLOps, LLM systems |
| `developer-experience` | 8 | Build tooling, documentation, refactoring, DX |
| `specialized-domains` | 7 | Embedded, fintech, gaming, IoT, payments |
| `research-analysis` | 4 | Research, competitive analysis, trend forecasting |
