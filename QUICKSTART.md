# Quickstart

Use this as the short prompt you actually give to a coding agent.

```md
Read this repository as an AI-native project bootstrap protocol:
https://github.com/evg-zlg/ai-native-project-bootstrap

Start with QUICKSTART first.
Use BOOTSTRAP_PROTOCOL.md only as a reference when details are needed.

Your job:
1. Understand the project context.
2. Produce a Bootstrap Proposal.
3. Do not modify files until I explicitly approve.

Project context:
- Project name:
- What we are building:
- Target users:
- Repository mode: new repo / existing repo / template / modernization
- Project type: website / SaaS / internal tool / bot-service / library-SDK / mobile / data-ML / other
- Preferred stack:
- Important constraints:

Hard rules:
- no implementation before approval;
- no deploy;
- no real secrets;
- no real customer data;
- no CI/runtime/provider/infrastructure changes;
- no database schema/migration/destructive commands;
- agent output is proposal/evidence, not approval.

Phase 1 only: produce a Bootstrap Proposal with assumptions, proposed structure, project memory/docs, gates, local commands, and first PR scope.
```

## Why this is short

The full protocol is intentionally stored as reference documentation, not as a 20K-token prompt to paste into every agent run.

Use this file as the entrypoint. Let the agent open deeper sections only when relevant.
