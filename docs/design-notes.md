# Design Notes

This repository intentionally separates the short agent entrypoint from the detailed protocol.

The short entrypoint gives the agent context, purpose, constraints, and the expected output. The long protocol remains available as reference, but it should not be pasted into every agent run.

This avoids the mega-prompt anti-pattern while preserving repeatable project startup standards.


## Related work: Agent1st

This kit references the Agent1st protocol by applerom as related work and inspiration:

- https://github.com/applerom/agent1st/blob/main/AGENTS.md

The main design lesson is to keep the agent entrypoint lightweight: intent, constraints, acceptance criteria, evidence, and continuity. The long bootstrap protocol should remain reference material, not something pasted into every run.
