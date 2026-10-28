# ADR-0001: Record architecture decisions

- **Date:** 2026-10-13
- **Status:** `accepted`
- **Deciders:** Project owner
- **Tags:** process

## Context

This build will be planned over a long period before construction. We need a durable way to remember *what* we chose and *why*, including rejected options and product brands.

## Decision

Use Architecture Decision Records (ADRs) for cross-cutting choices, plus per-feature `decisions.md` / `products.md` for scoped choices. All planning lives in Markdown in this repo until the build phase, when work moves into Jira.

## Why

- Survives long gaps between planning sessions
- Matches a software-engineering workflow we already know
- Makes future epic/story creation mechanical instead of archaeological

## Alternatives considered

### Alternative A — Keep everything in one notebook / chat history

- Pros: Low friction
- Cons: Hard to search, no structure, decisions get lost
- Why not: Retires-and-builds-later timeline needs structure

### Alternative B — Jump straight to Jira

- Pros: Ready for sprints
- Cons: Heavy for early research; tickets go stale during long planning
- Why not: Planning phase first; Jira at build time

## Consequences

### Positive

- Clear audit trail of choices and product picks

### Negative / trade-offs

- Slight ceremony when making a decision (worth it)

### Follow-ups

- [ ] Use feature templates as we flesh out each epic
- [ ] Write real ADRs as major choices land
