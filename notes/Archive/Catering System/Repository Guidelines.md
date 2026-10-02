# Repository Guidelines

## Project Structure & Document Organization

This repository is a document-based catering research workspace, not a software application. All current materials are in the root directory:

- `roco-catering-options.pdf` and `roco-catering-options final v.pdf`: catering comparison deliverables.
- Persian-named PDFs: supplier introduction, organizational pricing, and a monthly menu.
- `roco-catering-options5`: an extensionless artifact; confirm its format before opening, renaming, or replacing it.

There are no source-code, test, or asset directories. Keep supplier references distinct from authored comparisons. If the collection grows, use `references/` for supplier originals and `reports/` for comparison deliverables.

## Development & Review Commands

No build system, dependency manager, or automated test runner is configured. Use PowerShell to inspect the workspace:

- `Get-ChildItem -File`: list documents and file sizes.
- `Test-Path -LiteralPath 'document.pdf'`: confirm a specific file exists.
- `Get-FileHash -LiteralPath 'document.pdf'`: compare checksums when checking for duplicate or changed files.

## Naming & Document Style

Preserve original supplier filenames, including Persian text. For new reports, use descriptive, dated names such as `catering-comparison-2026-09-16.pdf`. Avoid ambiguous suffixes such as `final-v2`.

Use clear headings, consistent tables, and explicit price units, dates, and service assumptions. For Markdown, use ATX headings (`## Heading`) and consistent bullet lists.

## Validation Guidelines

Review every new or revised PDF visually. Check page order, readable Persian text, table alignment, and clipping. Verify prices and menu details against the supplier references; distinguish quoted facts from estimates. No automated testing framework or coverage requirement currently exists.

## Commit & Pull Request Guidelines

No Git metadata is present, so existing commit conventions cannot be established. If version control is introduced, use concise, action-oriented messages such as `docs: update catering comparison`.

For reviews or pull requests, summarize changed documents, identify supporting sources, and explain revisions to prices or recommendations. Include screenshots when layout changes need review. Avoid publishing confidential supplier terms or internal organizational details without approval.
