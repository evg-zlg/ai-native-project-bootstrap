# Safety Boundaries

These are the main boundaries the bootstrap process should preserve.

The agent may propose plans, templates, docs, placeholders, and safe local scaffolding.

The agent must not do these without explicit owner approval:

- deploy to staging or production;
- create, modify, or expose real secrets;
- commit real `.env` values;
- send or commit real customer/client data;
- connect live external providers;
- change CI workflows;
- change package manager, runtime, provider, adapter, hosting, or infrastructure config;
- create or run database migrations;
- run destructive database commands;
- merge PRs;
- perform irreversible GitHub actions;
- mark its own output as approval.

## Approval language

Implementation may start only after clear approval such as:

- approved
- approve
- go
- do it
- proceed
- делай
- подтверждаю
- запускай
- можно делать

## Why these boundaries exist

The goal is to make project startup repeatable without accidentally crossing production, data, infrastructure, or ownership boundaries.
