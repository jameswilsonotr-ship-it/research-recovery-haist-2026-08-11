# Research Recovery + HAIST Continuity

**Public archive of the 2026-08-11 research recovery session**

This repository documents the dual-Source-of-Truth (dual-SSoT) research scaffold built after a Valerie context-drift event. It captures:

- 66 formalized research nodes
- Agent-to-node attunements for the bi-cameral swarm
- Academic PDF corpus organization (binaries primarily on Google Drive; this repo holds structure + Markdown)
- Evolution history, work targets, and cross-system links

## Quick navigation

| Path | Purpose |
|------|---------|
| [`docs/QUICKSTART.md`](docs/QUICKSTART.md) | How to orient yourself in under 5 minutes |
| [`docs/CHANGELOG.md`](docs/CHANGELOG.md) | Version history of the recovery |
| [`docs/TODO.md`](docs/TODO.md) | Open research and structural work |
| [`nodes/`](nodes/) | One folder per research node (01–66) |
| [`agents/`](agents/) | One folder per major agent / role |
| [`system/`](system/) | Cross-links, dual-SSoT maps, citation index |
| [`history/`](history/) | Session history, targets, work-queue snapshots |

## Full PDF corpus

The complete set of academic PDFs (~84 files) is **not** stored as Git blobs here because of Contents API limits. Primary binary backup:

- Google Drive folder: [v1.1.0 full-with-pdfs](https://drive.google.com/drive/folders/1G3bFznzNKxGNShb29mzrXwZXP6B6-CJ-)
- Archive: [research_recovery_full_with_pdfs_v1.1.0_2026-08-11.tar.gz](https://drive.google.com/file/d/1xUI7JwPGZ-HDmpZr7kwbFzhiMd798foN/view)

Each `nodes/node_XX/` folder contains a `PDF_MANIFEST.md` listing the expected files and their Drive / original arXiv-PMC identifiers so the structure remains usable even without the binaries present.

## Dual SSoT rule

Every research node carries both:
1. Academic anchors (preprints, OpenStax, arXiv, PMC)
2. Practical / field anchors

PDF originals remain archival source of truth; Markdown extracts and this repository are the agent-facing surface.
