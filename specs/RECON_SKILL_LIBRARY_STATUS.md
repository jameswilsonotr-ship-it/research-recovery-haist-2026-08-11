# Skill Library Reconnaissance Status
**Date**: 2026-08-12  
**Scope**: Internal only — Olivia / Grok-Heavy swarm  
**Purpose**: Map current skill library adherence to the preferred development style that Olivia Dev Alpha is intended to enforce.

## 1. Finding: No Canonical Olivia Dev Alpha Definition

Conversation history and the current public research-recovery repository do **not** contain a single, complete `Olivia Dev Alpha` or `system-roadmap` SKILL.md with explicit, machine-enforceable rules for:

- Folder discipline
- Automatic ID generation
- CI/CD structure contracts
- Declarative vs imperative coding style

The strongest *living embodiment* of the intended style is the repository itself:

`jameswilsonotr-ship-it/research-recovery-haist-2026-08-11`

Its structure, required manifests, dual-SSoT rule, and `.github/workflows/structure-check.yml` are the de-facto reference implementation.

## 2. Preferred Style Extracted from Living Embodiment

| Component | Observed Rule |
|-----------|---------------|
| Top-level docs | `README.md`, `docs/QUICKSTART.md`, `docs/CHANGELOG.md`, `docs/TODO.md` required |
| Domain folders | `agents/`, `nodes/`, `system/`, `history/`, `docs/` |
| Per-item folders | Every `nodes/node_XX/` must contain `README.md` + `PDF_MANIFEST.md` |
| Indexes | `nodes/INDEX.md`, `agents/INDEX.md` |
| Cross-system | `system/DUAL_SSOT.md` and related maps |
| Evolution | Separate `agent_evolution/`, `node_evolution/` |
| CI | Structure & Manifest Check fails the build if required files are missing |
| Naming | Stable, zero-padded or descriptive IDs; no silent renames |
| Dual storage | Markdown + structure in Git; heavy binaries on Drive with manifests |
| Philosophy | Declarative first, specification before code, dual-SSoT |

## 3. Skill Library Adherence Map (Current State)

Because most skills live as conversational or session-scoped artifacts rather than versioned folders, the map is qualitative.

### Adhere (or closely match)
- Research-recovery structure itself (the reference)
- Any skill that already emits required README + MANIFEST pairs
- Dual-SSoT conscious research nodes
- Skills that produce Obsidian-compatible Markdown with stable IDs

### Neutral (neither enforce nor violate)
- Most conversational skills (grok-conversation-miner style)
- Frame/video parsers and one-off tool skills (e.g. grok-imagine-mp4-frame-parser)
- Persona / roster skills (chaos-bratz-roster and similar)
- Ad-hoc skill-creator outputs that are single-file or prompt-only

### Contradict or Drift Risk
- Skills that scatter files without indexes or manifests
- Skills that rename or renumber entities without changelog / evolution log
- Skills that mix binary artifacts into Git without a manifest pointing to external storage
- Skills that treat structure as optional or conversation-ephemeral only
- Any skill that hard-codes a single LLM/platform instead of remaining model-agnostic

## 4. Implications for Olivia Dev Alpha

Olivia Dev Alpha should become the **meta-skill** that:

1. Defines the declarative contract (this document + companion specs).
2. Can audit any skill or repository against that contract.
3. Can bootstrap new repositories (target: 16) from the same contract.
4. Can refactor existing projects into compliance.
5. Remains the single source of truth for “how we write skills and libraries” so the future model- and platform-agnostic research library skill inherits the same discipline.

## 5. Immediate Recommendation

Treat the two companion files in this `/specs` folder as the v0 contract:

- `OLIVIA_DEV_ALPHA_SPEC_v0.md` — the normative specification
- `REPO_BOOTSTRAP_CONTRACT.md` — how to apply it to existing + new repos

Promote into the formal Olivia Dev Alpha skill only after a test pass against this research-recovery repository and one additional clean bootstrap.
