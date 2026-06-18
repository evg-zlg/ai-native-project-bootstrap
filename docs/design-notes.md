# Design Notes

This repository intentionally separates the short agent entrypoint from the detailed protocol.

The short entrypoint gives the agent context, purpose, constraints, and the expected output. The long protocol remains available as reference, but it should not be pasted into every agent run.

This avoids the mega-prompt anti-pattern while preserving repeatable project startup standards.
