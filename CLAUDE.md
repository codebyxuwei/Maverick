# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is a **document repository**, not a software project. It stores periodic
work-report presentations (工作汇报 = "work report") in Microsoft PowerPoint
(`.pptx`) format. There is no application source code, build system, test
suite, linter, or dependency manifest.

Because of this, the usual "build / lint / test" commands do not apply. Do not
invent or run such commands. Treat tasks here as document management
(organizing, adding, renaming, or extracting content from `.pptx` files)
rather than code changes.

## Layout

- `工作汇报PPT/` — the canonical folder of report decks, one `.pptx` per report.
- `工作汇报PPT.zip` — a zip archive containing the same decks as the folder.
  When changing reports, update **both** the folder and (if the archive is
  meant to stay in sync) regenerate the zip, or confirm with the user which is
  the source of truth.
- `README.md` — currently just the project title (`Maverick`).

## Conventions

- **File naming**: reports follow `工作汇报YYYYMMDD.pptx`, where the date is the
  report date with no separators (e.g. `工作汇报20250630.pptx`). Keep this
  pattern for new reports — do not introduce a different naming scheme.
- The decks span 2025 on a roughly biweekly cadence (one file dated `20151029`
  appears to be a year typo for 2025; confirm with the user before "fixing" a
  filename, since renaming changes the apparent report date).
- `.pptx` files are **binary** (zipped OOXML). Do not attempt to edit them as
  text. To inspect or modify slide content programmatically, use a library
  such as `python-pptx`; to read raw XML, unzip the `.pptx` first. Prefer
  reporting what you find and asking the user before altering binary documents.

## Git

- Active development branch: `claude/claude-md-docs-5pRtM`.
- Commits so far are bulk uploads ("Add files via upload"). Large binary
  `.pptx`/`.zip` files are committed directly to the repo (no Git LFS), so be
  mindful of repository size when adding decks.
