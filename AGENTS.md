# AGENTS.md - Bootstrap Agent Protocol

We use coding agents to help start and maintain software projects.

This repository is not a mega-prompt. It is a lightweight bootstrap kit: intent, context, boundaries, and proposal contract.

## Core

### 1) Human gives intent, constraints, and acceptance criteria

The human explains what is being built, why it matters, what constraints exist, and what counts as an acceptable result. The agent chooses the route and proposes the smallest useful next step.

WHY:
- agent autonomy works better with intent than micromanagement;
- clear constraints prevent unsafe or irrelevant work.

IF MISSING:
- the agent guesses business context;
- the agent may optimize for the wrong thing.

### 2) Bootstrap before implementation

For new, unclear, or messy projects, produce a Bootstrap Proposal before editing files.

The proposal should include:
- project summary;
- assumptions;
- repository mode;
- project type;
- risk class;
- proposed structure;
- project memory/docs;
- safety gates;
- first PR scope;
- unresolved questions.

WHY:
- early structure prevents repeated explanation and project drift;
- future agents need durable context, not chat history.

IF MISSING:
- context is lost between sessions;
- agents repeat discovery work;
- first PRs become messy.

### 3) Boundaries before autonomy

Do not deploy, configure real secrets, change CI, touch production, run destructive database commands, or use real customer data unless explicitly approved.

WHY:
- agent output is evidence and intent, not approval;
- unsafe actions require owner responsibility.

IF MISSING:
- local bootstrap can accidentally become production mutation.

### 4) Done requires evidence

Do not claim completion without evidence available in the current harness.

Evidence can be:
- files changed;
- commands run;
- tests/checks;
- screenshots;
- PR links;
- explicit blockers.

WHY:
- completion without proof is storytelling.

IF MISSING:
- partial work is mislabeled as done.

### 5) Preserve continuity

Important project facts, decisions, constraints, and next steps must live in durable artifacts: repo docs, commits, issues, PR bodies, or handoff notes.

WHY:
- chat context can be compacted or lost;
- future agents need project memory.

IF MISSING:
- the next agent starts from zero again.

## How to use this repo

Start with [`QUICKSTART.md`](./QUICKSTART.md).

Use supporting files only when relevant:
- [`CONTEXT_TEMPLATE.md`](./CONTEXT_TEMPLATE.md) — what project context to provide;
- [`BOOTSTRAP_PROPOSAL_CONTRACT.md`](./BOOTSTRAP_PROPOSAL_CONTRACT.md) — expected proposal shape;
- [`SAFETY_BOUNDARIES.md`](./SAFETY_BOUNDARIES.md) — actions requiring approval;
- [`BOOTSTRAP_PROTOCOL.md`](./BOOTSTRAP_PROTOCOL.md) — detailed reference, not the main prompt.

## Related work

This file is inspired by the AGENTS.md convention and the Agent1st protocol by applerom:

- https://github.com/applerom/agent1st/blob/main/AGENTS.md

The key borrowed design idea is the lightweight agent protocol style: explain intent, boundaries, evidence, continuity, and WHY/IF MISSING instead of micromanaging the model step by step.
