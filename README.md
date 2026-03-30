# copilot-subagents

A collection of custom GitHub Copilot subagents.

## Structure

```
.github/
└── agents/      # Custom Copilot subagent definitions (.md files)
```

## Usage

Each subagent is defined as a Markdown file inside `.github/agents/`. GitHub Copilot automatically discovers agents placed in that directory.

To add a new agent, create a `.md` file in `.github/agents/` following the [custom agent specification](https://docs.github.com/en/copilot/customizing-copilot/building-custom-agents-for-copilot).

## License

See [LICENSE](LICENSE).
