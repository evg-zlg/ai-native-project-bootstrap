# Bootstrap Proposal Contract

Before implementation, the agent should return a concise proposal that helps the owner decide what to approve.

## Required proposal sections

1. **Project understanding** — what the agent thinks the project is.
2. **Assumptions** — what is inferred but not confirmed.
3. **Open questions** — only questions that materially affect the bootstrap.
4. **Repository mode and project type** — new repo, existing repo, template, modernization; website, SaaS, internal tool, etc.
5. **Risk class** — low, medium, high, with reason.
6. **Proposed structure** — minimal or full, with rationale.
7. **Project memory/docs** — which durable docs should exist and why.
8. **Safety boundaries/gates** — actions not allowed without approval.
9. **Local commands/checks** — proposed install, run, test, lint, or check commands.
10. **First implementation scope** — the smallest useful first PR/task.
11. **Out of scope** — what will not be done in the first pass.
12. **Approval request** — explicit ask to proceed or revise.

## Good proposal qualities

- Specific to the project, not generic boilerplate.
- Short enough to review.
- Clear about assumptions and uncertainty.
- Does not ask for non-blocking information.
- Does not claim merge-ready/deploy-ready/production-ready.
- Does not implement before approval.

## Bad proposal signs

- Huge generic documentation plan with no project-specific value.
- Invented business context, APIs, users, integrations, or deployment targets.
- Unnecessary full enterprise structure for a small project.
- Hidden risky actions behind vague wording.
