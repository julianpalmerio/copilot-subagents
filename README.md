# copilot-subagents

A curated collection of **61 expert GitHub Copilot CLI agents** across 8 domains — ready to install as a plugin or browse by category.

## Installation

```bash
# Install all 61 agents at once
copilot plugin install julianpalmerio/copilot-subagents

# Or add as a marketplace and install by category
copilot plugin marketplace add julianpalmerio/copilot-subagents
copilot plugin install core-development@copilot-subagents
copilot plugin install language-specialists@copilot-subagents
copilot plugin install infrastructure@copilot-subagents
copilot plugin install quality-security@copilot-subagents
copilot plugin install data-ai@copilot-subagents
copilot plugin install developer-experience@copilot-subagents
copilot plugin install specialized-domains@copilot-subagents
copilot plugin install research-analysis@copilot-subagents
```

## What are agents?

Agents are specialized AI personas that GitHub Copilot CLI activates based on your task. Each agent has a focused system prompt that makes it an expert in a specific domain — giving you better, more precise answers than a generic assistant.

When you install this plugin, Copilot automatically selects the right agent for your task based on the agent's description. You can also invoke agents explicitly.

---

## Agent Catalog

### 🏗️ Core Development (8 agents)

| Agent | Description |
|-------|-------------|
| **api-designer** | Designing new APIs, creating API specifications, or refactoring existing API architecture for scalability and developer experience. REST/GraphQL endpoint design, OpenAPI documentation, authentication patterns, API versioning. |
| **backend-developer** | Building server-side APIs, microservices, and backend systems that require robust architecture, scalability planning, and production-ready implementation. |
| **electron-pro** | Building Electron desktop applications that require native OS integration, cross-platform distribution, security hardening, and performance optimization. |
| **frontend-developer** | Building complete frontend applications across React, Vue, and Angular frameworks requiring multi-framework expertise and full-stack integration. |
| **fullstack-developer** | Building complete features spanning database, API, and frontend layers together as a cohesive unit. |
| **microservices-architect** | Designing distributed system architecture, decomposing monolithic applications into independent microservices, or establishing communication patterns between services at scale. |
| **mobile-developer** | Building React Native mobile applications requiring native performance optimization, platform-specific features, and offline-first architecture for iOS and Android. |
| **ui-spec-designer** | Producing design specifications as code or structured documents: component APIs, design tokens, interaction specs, accessibility annotations, and design system documentation. |

---

### 🌐 Language Specialists (6 agents)

| Agent | Description |
|-------|-------------|
| **django-developer** | Building Django 4+ web applications, REST APIs with Django REST Framework, or modernizing existing Django projects with async views and enterprise patterns. |
| **fastapi-developer** | Building modern async Python APIs with FastAPI, implementing Pydantic v2 validation, dependency injection patterns, or deploying high-performance ASGI applications. |
| **flutter-expert** | Building cross-platform mobile applications with Flutter 3+ that require custom UI, complex state management, native platform integrations, or performance optimization across iOS and Android. |
| **golang-pro** | Building Go applications requiring concurrent programming, high-performance systems, microservices, or cloud-native architectures where idiomatic patterns, error handling excellence, and efficiency are critical. |
| **nextjs-developer** | Building production Next.js 14+ applications with the App Router. Architect server vs client component boundaries, implement Server Actions, configure caching and revalidation, optimize Core Web Vitals, or deploy full-stack Next.js applications. |
| **rails-expert** | Building or modernizing Rails applications requiring API development, Hotwire reactivity, real-time features, background job processing, or Rails-idiomatic patterns. Version-aware: adapts to Rails 7.x and 8.x. |

---

### ☁️ Infrastructure (10 agents)

| Agent | Description |
|-------|-------------|
| **cloud-architect** | Designing cloud-native architectures, making multi-cloud strategy decisions, establishing landing zones, or architecting solutions for reliability, cost optimization, and security at scale. |
| **database-administrator** | Complex database design, query optimization, indexing strategy, replication architecture, migration planning, and operational tasks across PostgreSQL, MySQL, and other database systems. |
| **devops-engineer** | Building or optimizing infrastructure automation, CI/CD pipelines, containerization strategies, and deployment workflows to accelerate software delivery while maintaining reliability and security. |
| **docker-expert** | Building, optimizing, or securing Docker container images and orchestration for production environments. |
| **incident-responder** | Active incidents, security breaches, or outages — coordinate response, guide investigation, manage communications, and drive resolution with structured runbook procedures and postmortem practices. |
| **kubernetes-specialist** | Designing, deploying, configuring, or troubleshooting Kubernetes clusters and workloads in production environments. |
| **platform-engineer** | Designing or improving internal developer platforms (IDP), establishing developer experience infrastructure, building golden paths, or creating self-service infrastructure capabilities using Backstage, Crossplane, or similar tools. |
| **security-engineer** | Implementing comprehensive security solutions across infrastructure, building automated security controls into CI/CD pipelines, establishing compliance programs, or designing zero-trust architecture. |
| **sre-engineer** | Establishing or improving system reliability through SLO definition, error budget management, toil reduction, chaos engineering, or optimizing incident response processes. |
| **terraform-engineer** | Building, refactoring, or scaling infrastructure as code using Terraform or OpenTofu with focus on multi-cloud deployments, module architecture, and enterprise-grade state management. |

---

### 🔍 Quality & Security (9 agents)

| Agent | Description |
|-------|-------------|
| **accessibility-tester** | Comprehensive accessibility testing, WCAG compliance verification, or assessment of assistive technology support. |
| **architect-reviewer** | Evaluating system design decisions, architectural patterns, and technology choices at the macro level. |
| **code-reviewer** | Conducting comprehensive code reviews focusing on code quality, security vulnerabilities, and best practices. |
| **compliance-auditor** | Achieving regulatory compliance, implementing compliance controls, or preparing for audits across GDPR, HIPAA, PCI DSS, SOC 2, and ISO standards. |
| **debugger** | Diagnosing and fixing bugs, identifying root causes of failures, or analyzing error logs and stack traces to resolve issues. |
| **penetration-tester** | Conducting authorized security penetration tests to identify real vulnerabilities through active exploitation and validation. |
| **performance-engineer** | Identifying and eliminating performance bottlenecks in applications, databases, or infrastructure systems, and when baseline performance metrics need improvement. |
| **qa-expert** | Comprehensive quality assurance strategy, test planning across the entire development cycle, or quality metrics analysis to improve overall software quality. |
| **test-automator** | Building, implementing, or enhancing automated test frameworks, creating test scripts, or integrating testing into CI/CD pipelines. |

---

### 🤖 Data & AI (9 agents)

| Agent | Description |
|-------|-------------|
| **ai-engineer** | Architecting, implementing, or optimizing end-to-end AI systems — from model selection and training pipelines to production deployment and monitoring. |
| **data-analyst** | Extracting insights from business data, creating dashboards and reports, or performing statistical analysis to support decision-making. |
| **data-engineer** | Designing, building, or optimizing data pipelines, ETL/ELT processes, and data infrastructure. Implementing pipeline orchestration, handling data quality, or optimizing data processing costs. |
| **data-scientist** | Analyzing data patterns, building predictive models, or extracting statistical insights from datasets. Exploratory analysis, hypothesis testing, ML model development, and translating findings into business recommendations. |
| **llm-architect** | Designing LLM systems for production, implementing fine-tuning or RAG architectures, optimizing inference serving infrastructure, or managing multi-model deployments. |
| **ml-engineer** | Building production ML systems requiring model training pipelines, model serving infrastructure, performance optimization, and automated retraining. |
| **mlops-engineer** | Designing and implementing ML infrastructure, setting up CI/CD for machine learning models, establishing model versioning systems, or optimizing ML platforms for reliability and automation. |
| **nlp-engineer** | Building production NLP systems, implementing text processing pipelines, developing language models, or solving domain-specific NLP tasks like NER, sentiment analysis, or machine translation. |
| **prompt-engineer** | Designing, optimizing, testing, or evaluating prompts for large language models in production systems. |

---

### 🛠️ Developer Experience (8 agents)

| Agent | Description |
|-------|-------------|
| **build-engineer** | Optimizing build performance, reducing compilation times, configuring caching strategies, or scaling build systems for growing monorepos and teams. |
| **dependency-manager** | Auditing dependencies for vulnerabilities, resolving version conflicts, reducing bundle size, managing lock files, or implementing automated dependency update workflows with Renovate or Dependabot. |
| **documentation-engineer** | Creating, restructuring, or automating documentation systems — API docs, developer guides, tutorials, changelogs, or docs-as-code pipelines that stay in sync with the codebase. |
| **git-workflow-manager** | Designing or optimizing Git branching strategies, setting up branch protection and automation, establishing commit conventions, configuring semantic versioning and changelog generation, or resolving Git history problems. |
| **legacy-modernizer** | Modernizing legacy systems — migrating frameworks, decomposing monoliths, paying down technical debt, or replacing aging infrastructure while maintaining business continuity and zero downtime. |
| **mcp-developer** | Building, debugging, or optimizing Model Context Protocol (MCP) servers and clients — implementing tools, resources, and prompts that connect AI assistants to external systems, APIs, databases, or developer workflows. |
| **refactoring-specialist** | Transforming poorly structured, overly complex, or duplicated code into clean maintainable systems — applying catalog refactorings, reducing cyclomatic complexity, breaking dependencies, or safely restructuring without changing behavior. |
| **tooling-engineer** | Building developer tools — CLIs, code generators, IDE extensions, scaffolding tools, language servers, build plugins, or automation scripts. Intuitive command design, cross-platform compatibility, plugin architectures, or shell completion systems. |

---

### 🔧 Specialized Domains (7 agents)

| Agent | Description |
|-------|-------------|
| **embedded-systems** | Developing firmware for resource-constrained microcontrollers, implementing RTOS-based applications, writing HAL/BSP layers, or optimizing real-time systems where latency guarantees, power budgets, and hardware reliability are critical. |
| **fintech-engineer** | Building financial systems — payment processing platforms, banking integrations, trading infrastructure, KYC/AML pipelines, open banking APIs, or any system requiring 100% transaction accuracy, regulatory compliance, and financial-grade reliability. |
| **game-developer** | Implementing game systems, optimizing rendering pipelines, building multiplayer networking, designing ECS architectures, or developing gameplay mechanics in Unity, Unreal, Godot, or custom engines. |
| **iot-engineer** | Designing IoT solutions — device connectivity, edge computing, MQTT messaging pipelines, fleet management, OTA firmware updates, or cloud integration for large-scale device deployments across AWS IoT, Azure IoT Hub, or self-hosted platforms. |
| **payment-integration** | Implementing payment gateway integrations (Stripe, Braintree, PayPal, Adyen), building subscription billing, handling webhooks reliably, implementing PCI-DSS compliance, managing 3D Secure flows, or designing fraud prevention systems. |
| **quant-analyst** | Developing quantitative trading strategies, building derivatives pricing models, backtesting systematic strategies with rigorous statistical validation, constructing factor models, or implementing portfolio risk analytics (VaR, CVaR, stress testing). |
| **seo-specialist** | Technical SEO audits, Core Web Vitals optimization, structured data implementation, crawlability fixes, international SEO architecture, or content optimization strategies to improve organic search rankings. |

---

### �� Research & Analysis (4 agents)

| Agent | Description |
|-------|-------------|
| **competitive-analyst** | Analyzing direct and indirect competitors, sizing a market opportunity, benchmarking against market leaders, mapping competitive positioning, or developing strategies to strengthen market advantage and inform product or go-to-market decisions. |
| **research-analyst** | Comprehensive research across multiple sources — finding specific information efficiently, gathering and validating datasets, synthesizing findings into structured reports, identifying patterns across sources, or turning raw information into actionable insights. |
| **scientific-literature-researcher** | Evidence-grounded answers from published scientific research — searching academic databases, retrieving structured study data, synthesizing findings across papers, assessing evidence quality, or conducting systematic literature reviews in any empirical research domain. |
| **trend-analyst** | Analyzing emerging patterns across industries, detecting weak signals of structural change, developing future scenarios for strategic planning, or forecasting how technological, social, economic, or regulatory shifts will impact a market or product. |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to add agents, create new categories, and submit pull requests.

## License

MIT © [Julian Palmerio](https://github.com/julianpalmerio)
