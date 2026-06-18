# AI-Native Project Bootstrap Kit

A lightweight starter kit for launching software projects with coding agents.

It helps you give an agent the right project context, boundaries, and expected output before implementation starts.

Use it when you want an agent to:

1. understand the project goal and constraints;
2. ask only the questions that matter;
3. produce a clear Bootstrap Proposal;
4. define project memory, docs, gates, and first PR scope;
5. avoid risky actions until explicitly approved.

## Use this first

Start with these files:

- [`AGENTS.md`](./AGENTS.md) — general agent protocol;
- [`QUICKSTART.md`](./QUICKSTART.md) — short entrypoint for a new agent run;
- [`CONTEXT_TEMPLATE.md`](./CONTEXT_TEMPLATE.md) — project context to fill in;
- [`BOOTSTRAP_PROPOSAL_CONTRACT.md`](./BOOTSTRAP_PROPOSAL_CONTRACT.md) — expected proposal format;
- [`SAFETY_BOUNDARIES.md`](./SAFETY_BOUNDARIES.md) — actions that require explicit approval.

Reference material:

- [`BOOTSTRAP_PROTOCOL.md`](./BOOTSTRAP_PROTOCOL.md) — deeper bootstrap reference;
- [`PROMPT.md`](./PROMPT.md) — compatibility entrypoint for older links;
- [`examples/agent-message.md`](./examples/agent-message.md) — copy-paste starter message.

## Why this exists

Starting a project with an agent often requires repeating the same setup context: what is being built, what decisions should be captured, what risks are off-limits, and what the first safe work packet should look like.

This kit turns that repeated explanation into a reusable project startup flow.

## Core idea

Give the agent:

- intent;
- project context;
- constraints;
- safety boundaries;
- expected output.

The agent should produce a Bootstrap Proposal first. Implementation starts only after explicit approval.

## Typical workflow

1. Send the agent the repository link.
2. Ask it to read `AGENTS.md` and `QUICKSTART.md` first.
3. Fill in the project context using `CONTEXT_TEMPLATE.md`.
4. Ask for Phase 1 only: Bootstrap Proposal.
5. Review the proposal.
6. Approve implementation only when scope, gates, and first PR are clear.

## Related work

This kit is inspired by the AGENTS.md convention and the Agent1st protocol by applerom:

- https://github.com/applerom/agent1st/blob/main/AGENTS.md

The useful pattern is to give agents intent, constraints, acceptance criteria, evidence expectations, and durable continuity rules instead of step-by-step micromanagement.

## License

MIT. See [`LICENSE`](./LICENSE).
