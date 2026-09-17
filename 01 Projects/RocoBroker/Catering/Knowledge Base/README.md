# Food Research Knowledge Base

This collection is part of the consolidated vault at `C:/Users/Sajad/Documents/Obsidian Vault`. Open [[01 Projects/RocoBroker/Catering/Knowledge Base/Home]] for food research, or [[Home]] for the whole second brain. No plugins are required.

## Repository architecture

| Path | Responsibility |
| --- | --- |
| `03 Resources/Comparisons/reports/` | Original comparison artifacts |
| `03 Resources/Suppliers/` | Supplier dossiers, source notes, and originals |
| `01 Maps/` | Navigation and relationships |
| `02 Projects/` | Active outcomes and next actions |
| `03 Resources/` | Source register, comparisons, and supplier dossiers |
| `04 Knowledge/Frameworks/` | Reusable evaluation and evidence methods |
| `05 Decisions/` | Decision records and rationale |
| `06 Inbox/` | Unprocessed questions and observations |
| `07 Templates/` | Repeatable note schemas |
| `scripts/` | Knowledge-base validation |

[[01 Projects/RocoBroker/Catering/Knowledge Base/Repository Guidelines|Repository Guidelines]] remains unchanged. Supplier originals are grouped under each dossier’s `references/` folder; authored comparisons are in `reports/`. Original names and contents are preserved.

## Treat knowledge like code

Original PDFs are inputs; source notes are the evidence interface; knowledge notes are reusable modules; project notes compose them; decision records are outputs. A link must express a real relationship, not merely make the graph larger.

Keep one main idea per knowledge note. Use explicit source/page references for claims. Label interpretation separately. Never silently replace supplier originals or assume a filename containing “final” proves approval.

## Validation

The original food workspace retains its validator. Run there with Node.js:

```powershell
node scripts/validate-vault.mjs
```

This checks file targets in wikilinks and local Markdown links, required properties in knowledge-base notes, and balanced code fences. It does not verify PDF facts, full YAML syntax, or visual rendering. There is no build step or external dependency.

## Note lifecycle

Capture → source review → synthesis → decision → revalidation.

Copy a note from [[01 Projects/RocoBroker/Catering/Knowledge Base/07 Templates/Source Template]], [[01 Projects/RocoBroker/Catering/Knowledge Base/07 Templates/Knowledge Template]], or [[01 Projects/RocoBroker/Catering/Knowledge Base/07 Templates/Decision Template]]. Replace prompts manually; no template plugin is assumed. Preserve Persian filenames and specify calendar, currency, quote validity, and review date when known.
