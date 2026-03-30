# Contributing to copilot-subagents

Thank you for contributing! This guide explains how to add agents, maintain quality, and submit pull requests.

## Adding a New Agent

### 1. Choose the right category

Place your agent in the most relevant category directory under `plugins/`:

| Directory | When to use |
|-----------|-------------|
| `plugins/core-development/agents/` | APIs, frontend, backend, mobile, full-stack |
| `plugins/language-specialists/agents/` | Framework or language-specific expertise |
| `plugins/infrastructure/agents/` | Cloud, DevOps, Kubernetes, security, SRE |
| `plugins/quality-security/agents/` | Testing, code review, compliance, pen testing |
| `plugins/data-ai/agents/` | ML, data science, NLP, MLOps, LLM systems |
| `plugins/developer-experience/agents/` | Build tooling, documentation, refactoring, DX |
| `plugins/specialized-domains/agents/` | Embedded, fintech, gaming, IoT, etc. |
| `plugins/research-analysis/agents/` | Research, competitive analysis, trend forecasting |

### 2. Create the agent file

Agent files use the `.agent.md` extension. Create your file at:

```
plugins/CATEGORY/agents/your-agent-name.agent.md
```

### 3. Agent file format

```markdown
---
name: your-agent-name
description: "When to invoke this agent — be specific about the trigger"
---

Your system prompt content goes here.

Be thorough and specific. The system prompt is the full set of instructions
the agent follows when activated.
```

**Frontmatter fields:**

| Field | Required | Notes |
|-------|----------|-------|
| `name` | Yes | Kebab-case, matches the filename without `.agent.md` |
| `description` | Yes | The trigger condition — used by Copilot to select this agent |

### 4. Writing the description

The `description` field is critical — Copilot uses it to determine when to activate your agent. Write it as a trigger condition, not a summary.

**Good descriptions:**
```
"Use when building Go applications requiring concurrent programming, high-performance systems, microservices, or cloud-native architectures where idiomatic patterns, error handling excellence, and efficiency are critical."
```
```
"Use when you need technical SEO audits, Core Web Vitals optimization, structured data implementation, crawlability fixes, or international SEO architecture to improve organic search rankings."
```

**Bad descriptions:**
```
"An expert Go developer."   # Too vague — no trigger condition
"Helps with backend stuff." # Not specific enough
```

Good trigger words: **"when building X"**, **"when designing Y"**, **"when optimizing Z"**, **"for implementing W"**.

---

## Quality Standards

### ✅ Do

- **Use concrete code examples** — show actual commands, configs, or code snippets, not just bullet lists
- **Include decision frameworks** — explain when to use X vs Y (e.g., Redis vs in-memory caching)
- **Include actual tool command examples** — `kubectl apply -f`, `terraform plan`, `pytest -v`, etc.
- **Be opinionated** — agents should have a clear point of view and recommend best practices, not list every option
- **Cover edge cases** — think about what can go wrong and how the agent should handle it

### ❌ Don't

- Use JSON protocol blocks or agent-to-agent orchestration patterns (Claude Code-specific, not portable)
- Write agents that are just lists of capabilities — they should be active advisors
- Duplicate an existing agent's scope — check what exists before adding
- Leave the description vague — it's the most important field for routing

---

## Adding a New Category

If your agent doesn't fit any existing category:

1. **Create the directory structure:**
   ```bash
   mkdir -p plugins/your-category/.github/plugin
   mkdir -p plugins/your-category/agents
   ```

2. **Create the category plugin manifest** at `plugins/your-category/.github/plugin/plugin.json`:
   ```json
   {
     "name": "your-category",
     "description": "Brief description of this category",
     "version": "1.0.0",
     "author": {
       "name": "Your Name",
       "url": "https://github.com/yourusername"
     },
     "license": "MIT",
     "keywords": ["copilot", "agents", "your-keyword"],
     "agents": "agents/"
   }
   ```

3. **Update `.github/plugin/marketplace.json`** — add an entry to the `plugins` array:
   ```json
   {
     "name": "your-category",
     "description": "Brief description of this category",
     "version": "1.0.0",
     "source": "plugins/your-category"
   }
   ```

4. **Update `.github/plugin/plugin.json`** — add the new agents path to the root `agents` array:
   ```json
   "plugins/your-category/agents/"
   ```

5. **Update `README.md`** — add a section for the new category with an agent table.

---

## Pull Request Process

1. **Fork** the repository and create a feature branch:
   ```bash
   git checkout -b add/my-new-agent
   ```

2. **Add your agent** following the format above.

3. **Verify your file** has valid frontmatter:
   ```bash
   grep -A2 "^---" plugins/CATEGORY/agents/your-agent.agent.md | head -10
   ```

4. **Open a PR** with:
   - A clear title: `Add [agent-name] to [category]`
   - A brief description of what the agent does and why it's useful
   - Example use cases or sample prompts you tested

5. PRs are reviewed for:
   - Quality of the system prompt
   - Specificity of the `description` trigger
   - Fit within the chosen category
   - No overlap with existing agents
