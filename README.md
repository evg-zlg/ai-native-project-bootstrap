# AI-Native Project Bootstrap Kit

A lightweight bootstrap kit for starting software projects with coding agents.

This is **not** meant to be a 20K-token mega-prompt pasted into every run. The useful pattern is:

1. give the agent a short entrypoint;
2. provide project context;
3. ask for a Bootstrap Proposal;
4. keep risky actions behind explicit approval gates;
5. let the agent open deeper reference docs only when needed.

## Use this first

Start here:

- [`AGENTS.md`](./AGENTS.md) — short agent protocol for this kit.
- [`QUICKSTART.md`](./QUICKSTART.md) — short agent entrypoint.
- [`CONTEXT_TEMPLATE.md`](./CONTEXT_TEMPLATE.md) — what to tell the agent about the project.
- [`BOOTSTRAP_PROPOSAL_CONTRACT.md`](./BOOTSTRAP_PROPOSAL_CONTRACT.md) — what the agent should return before implementation.
- [`SAFETY_BOUNDARIES.md`](./SAFETY_BOUNDARIES.md) — actions that require explicit approval.

Reference only:

- [`BOOTSTRAP_PROTOCOL.md`](./BOOTSTRAP_PROTOCOL.md) — detailed protocol/playbook. Do not paste this whole file into every agent run.
- [`PROMPT.md`](./PROMPT.md) — compatibility entrypoint for older links.
- [`examples/agent-message.md`](./examples/agent-message.md) — copy-paste starter message.

## Why this exists

When starting a new project with an agent, the same process has to be explained again and again: what context to gather, how to avoid dangerous actions, what project memory should exist, what the first proposal should contain, and when implementation is allowed.

This kit standardizes that startup flow without over-controlling the model.

## Core idea

Tell the agent the **why, context, constraints, and expected output**.
Do not micromanage every step.

The agent should produce a proposal first. Implementation starts only after explicit approval.

## Typical workflow

1. Send the agent the [`AGENTS.md`](./AGENTS.md) and [`QUICKSTART.md`](./QUICKSTART.md) links, or just the repository link.
2. Fill in the project context from [`CONTEXT_TEMPLATE.md`](./CONTEXT_TEMPLATE.md).
3. Ask for Phase 1 only: Bootstrap Proposal.
4. Review the proposal.
5. Approve implementation only when scope, gates, and first PR are clear.

## Related work

This kit is inspired by the AGENTS.md convention and the Agent1st protocol by applerom:

- https://github.com/applerom/agent1st/blob/main/AGENTS.md

The useful pattern is to give agents intent, constraints, acceptance criteria, evidence expectations, and durable continuity rules instead of step-by-step micromanagement.

## License

MIT. See [`LICENSE`](./LICENSE).
