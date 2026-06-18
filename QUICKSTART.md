# Quickstart

This is the short prompt to give a coding agent.

```md
Use this repository as a lightweight project bootstrap kit:
https://github.com/evg-zlg/ai-native-project-bootstrap

Read AGENTS.md and QUICKSTART first.
Use the other files only when relevant:
- AGENTS.md for the lightweight operating protocol;
- CONTEXT_TEMPLATE.md for missing project context;
- BOOTSTRAP_PROPOSAL_CONTRACT.md for the expected proposal shape;
- SAFETY_BOUNDARIES.md for approval gates;
- BOOTSTRAP_PROTOCOL.md as detailed reference only if needed.

Goal:
Help me start or improve a software project so future humans and agents can continue it safely.

First phase only:
Produce a Bootstrap Proposal. Do not implement or modify files until I explicitly approve.

Project context:
- Project name:
- What we are building:
- Target users:
- Repository mode: new repo / existing repo / template / modernization
- Project type: website / SaaS / internal tool / bot-service / library-SDK / mobile / data-ML / other
- Preferred stack:
- Important constraints:
- Things to avoid:

Critical boundaries:
- no implementation before approval;
- no deploy;
- no real secrets;
- no real customer data;
- no CI/runtime/provider/infrastructure changes;
- no database schema/migration/destructive commands;
- agent output is proposal/evidence, not approval.

Ask questions only when missing information blocks a useful proposal. Otherwise make assumptions explicit.
```

## Principle

Modern agents usually do not need step-by-step micromanagement. They need clear context, purpose, constraints, tools, and a concrete output contract.
