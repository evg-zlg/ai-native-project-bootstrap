# AI-Native Project Bootstrap

A compact entrypoint plus a detailed reference protocol for starting software projects with coding agents.

The goal is not to paste a huge prompt into every session. The goal is to give the agent a small starting instruction, then keep the deeper bootstrap rules in the repository as reference documentation.

## Use this first

Give your agent this link:

```txt
https://github.com/evg-zlg/ai-native-project-bootstrap
```

Or point directly to the short entrypoint:

```txt
https://github.com/evg-zlg/ai-native-project-bootstrap/blob/main/QUICKSTART.md
```

## What problem it solves

Many coding agents start too fast: they code before understanding the project, forget context across sessions, invent structure, miss safety boundaries, or change risky things without an explicit gate.

This bootstrap makes the agent first produce a proposal:

- what we are building;
- what project mode/type it is;
- what structure and docs are needed;
- what safety gates apply;
- what the first PR should contain;
- what is explicitly out of scope.

Implementation starts only after owner approval.

## What is already covered

- New repos and existing repos.
- Minimal vs full project structure.
- Durable project memory so future agents do not depend on chat history.
- Product and technical docs.
- Explicit gates for deploy, secrets, CI, production, database, infrastructure, providers, and customer data.
- Reusable UI/component policy for web projects.
- Optional prompts, workflows, skills/playbooks, and evidence/review lanes.
- Anti-slop rules so the agent does not create useless boilerplate docs.
- A two-phase process: proposal first, implementation only after approval.

## Files

- [`QUICKSTART.md`](./QUICKSTART.md) — short prompt to give the agent first.
- [`BOOTSTRAP_PROTOCOL.md`](./BOOTSTRAP_PROTOCOL.md) — full detailed protocol/reference.
- [`PROMPT.md`](./PROMPT.md) — compatibility entrypoint for older links.
- [`examples/agent-message.md`](./examples/agent-message.md) — copy-paste starter message.
- [`docs/profile-cleanup-notes.md`](./docs/profile-cleanup-notes.md) — optional GitHub profile cleanup notes.

## Recommended agent message

```md
Read this repository as an AI-native project bootstrap protocol:
https://github.com/evg-zlg/ai-native-project-bootstrap

Start with QUICKSTART first.
Use BOOTSTRAP_PROTOCOL.md only as a reference when details are needed.

Project context:
- Project name:
- What we are building:
- Target users:
- Repository mode: new repo / existing repo / template / modernization
- Preferred stack:

Start with Phase 1 only: Discovery and Bootstrap Proposal.
Do not implement until I explicitly approve the proposal.
```

## License

MIT. See [`LICENSE`](./LICENSE).
