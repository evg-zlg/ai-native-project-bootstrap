# AI-Native Project Bootstrap Prompt

A practical bootstrap prompt for coding agents that need to initialize or improve a software repository in an AI-native way.

It helps an agent create durable project memory, technical docs, workflow rules, safety gates, local commands, and reusable component/skill policies without relying on chat history.

## When to use it

Use this prompt when you are starting a new software project, preparing an existing repository for agentic development, or turning a messy repo into something future agents can safely continue.

It is especially useful for:

- client websites and landing pages;
- SaaS/product MVPs;
- internal tools;
- bots and integration services;
- libraries, packages, and SDKs;
- existing repo modernization.

## How to use

Give your coding agent a link to [`PROMPT.md`](./PROMPT.md) and then describe the project.

Example message:

```md
Read and follow this bootstrap prompt:
https://github.com/<owner>/<repo>/blob/main/PROMPT.md

Project context:
- Project name: ...
- What we are building: ...
- Target users: ...
- Preferred stack, if any: ...
- Repository mode: new repo / existing repo / template / modernization

Start with Phase 1 only: Discovery and Bootstrap Proposal.
Do not implement until I explicitly approve the proposal.
```

The prompt is intentionally two-phase:

1. **Discovery and Bootstrap Proposal** — the agent collects only the missing context, lists assumptions, proposes structure, gates, and first PR scope.
2. **Implementation after explicit approval** — the agent creates or updates files only after the owner says `approved`, `go`, `proceed`, `делай`, or another explicit approval phrase.

## What it creates

Depending on project size and type, the prompt guides the agent toward either a minimal or full structure.

Minimal structure usually includes:

```txt
README.md
.env.example
.gitignore

docs/
  PRODUCT.md
  ARCHITECTURE.md
  DECISIONS.md
  OPEN_QUESTIONS.md

.agent/
  PROJECT_RULES.md
  AGENT_PROTOCOL.md
  GATES.md
  REVIEW_CHECKLIST.md

scripts/
  check.sh
```

Full structure can additionally include deeper technical docs, local skills/playbooks, route prompts, memory update policy, and external evidence/review workflow docs.

## Safety model

The prompt makes the agent treat its own output as evidence and intent, not approval.

By default, the agent must not:

- deploy to staging or production;
- configure real secrets;
- commit real `.env` values;
- run destructive database commands;
- change CI, package/runtime, provider, adapter, or infrastructure settings;
- connect live external providers;
- commit real customer data;
- merge PRs;
- mark its own work as approved.

Owner/project gates decide what is merge-ready, deploy-ready, and production-ready.

## Files

- [`PROMPT.md`](./PROMPT.md) — the full agent bootstrap prompt.
- [`examples/agent-message.md`](./examples/agent-message.md) — copy-paste starter message for an agent.
- [`docs/profile-cleanup-notes.md`](./docs/profile-cleanup-notes.md) — optional notes for presenting this publicly from a GitHub profile.

## License

MIT. See [`LICENSE`](./LICENSE).
