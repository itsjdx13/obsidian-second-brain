---
type: "decision"
status: "implemented"
tags: ["food", "architecture"]
---
# ADR-001 Evidence-First Knowledge Base

## Context
This workspace contains six original research artifacts and [[01 Projects/RocoBroker/Catering/Knowledge Base/Repository Guidelines|contributor guidelines]], but previously had no linked-note structure.

## Decision
Use this folder as the Obsidian vault root. Preserve originals in place. Separate navigation, projects, source notes, reusable knowledge, decisions, inbox, and templates.

## Rationale
Vault-relative links keep source material nearby. Separate evidence and interpretation prevents unreviewed document names from becoming unsupported conclusions. A local validator provides a repeatable integrity check.

## Consequences
- No plugins, sync, publishing, or application configuration are required.
- PDF review remains necessary before factual synthesis.
- Existing artifacts and contributor guidelines stay unchanged.
- Navigation starts at [[01 Projects/RocoBroker/Catering/Knowledge Base/Home]]; maintenance instructions live in [[01 Projects/RocoBroker/Catering/Knowledge Base/README]].

## Reconsider when
Document volume requires a new attachment convention, multiple projects share the vault, or access-control requirements change.

This is a record of the implemented structure, not approval of a supplier or purchasing decision.
