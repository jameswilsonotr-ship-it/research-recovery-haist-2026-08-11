# Olivia Dev Alpha — Declarative Global Specification v0
**Status**: Draft for proof-of-concept  
**Purpose**: Single source of truth for how every Olivia-governed repository, skill, and research library MUST be structured.  
**Promotion path**: Once proven on this repo + 1–2 pilots, this document becomes the body of the Olivia Dev Alpha skill itself.

---

## 0. Design Philosophy

1. **Specification before code.** Every structural change is expressed as Markdown/YAML first.
2. **Fail closed.** Missing required files break CI; they do not produce warnings that can be ignored.
3. **One entity, one folder.** Agents, nodes, skills, topics, and libraries never share a flat namespace.
4. **Human-readable stable IDs.** Prefer `node_47`, `agent-olivia`, `skill-olivia-dev-alpha` over opaque hashes at the filesystem layer.
5. **Dual-SSoT by default.** Git holds structure + narrative; object lake (Drive, S3, etc.) holds binaries and large corpora.
6. **Platform-agnostic core.** The same layout must be consumable by Grok, Gemini Spark, Antigravity, GrokBuild, Letta, Obsidian, and future runtimes.
7. **Federated registration.** Any LLM or agent runtime can register itself as a first-class agent by conforming to the agent folder contract and writing an entry in the global INDEX.

---

## 1. Canonical Top-Level Layout

```text
repo-root/
├── README.md
├── MANIFEST.md                  # repo-level inventory
├── ASSET_INVENTORY.md           # optional, for binary lakes
├── .github/workflows/
│   ├── structure-check.yml       # REQUIRED — fails on missing files
│   └── sync-reminder.yml         # optional
├── agents/
│   ├── INDEX.md
│   └── <agent-id>/
│       └── README.md             # REQUIRED
├── nodes/                       # or research/, topics/, etc.
│   ├── INDEX.md
│   └── <node-id>/
│       ├── README.md             # REQUIRED
│       └── PDF_MANIFEST.md       # REQUIRED for research nodes
├── skills/                      # when the repo is a skill library
│   ├── INDEX.md
│   └── <skill-id>/
│       ├── SKILL.md              # REQUIRED
│       ├── README.md
│       └── contracts/            # optional declarative sub-specs
├── system/
│   ├── DUAL_SSOT.md
│   └── CROSS_LINKS.md
├── agent_evolution/
├── node_evolution/
├── history/
├── docs/
│   ├── CHANGELOG.md
│   ├── QUICKSTART.md
│   └── TODO.md
└── olivia-dev-alpha/            # this spec family lives here until promoted
```

---

## 2. Required File Contracts

### 2.1 Entity README.md (minimum)
```markdown
# <Entity Name>
**ID**: <stable-id>
**Type**: agent | node | skill | topic
**Status**: active | draft | deprecated
**Owner**: <agent or human>
**Last reviewed**: YYYY-MM-DD

## Purpose
One paragraph.

## Links
- Forward: ...
- Back: ...
```

### 2.2 PDF_MANIFEST.md / ASSET_MANIFEST.md (research nodes)
Must list every attached binary with:
- filename
- source URL / DOI / Drive ID
- node attachment reason
- checksum (CRC32 or stronger) when available

### 2.3 SKILL.md (skills)
Must contain:
- name + version
- trigger / invocation surface
- inputs / outputs
- side effects
- adherence level to this Olivia Dev Alpha spec (`full` | `partial` | `exempt` + reason)

---

## 3. Automated Behaviors (CI / CD style)

1. **structure-check** (required on every push to main):
   - Every directory under `agents/`, `nodes/`, `skills/` contains the mandated files.
   - INDEX.md files list exactly the child folders that exist.
   - Exit non-zero on any violation.

2. **ID stability**: Once an ID is published in an INDEX, it is never reused for a different entity.

3. **Evolution append-only**: `agent_evolution/` and `node_evolution/` only grow; they never rewrite history without a new dated entry.

4. **Registration hook** (future): A new agent runtime may open a PR that adds `agents/<new-id>/README.md` + an INDEX entry. Merge = registration.

---

## 4. Global Consistency Rules for 16+ Repositories

When standing up or refactoring any repository under Olivia governance:

1. Copy the top-level skeleton from this spec.
2. Run the structure-check workflow (or an equivalent local script) before first push.
3. Declare the repo’s dual-SSoT mapping in `system/DUAL_SSOT.md`.
4. If the repo contains research or academic material, every leaf node gets a manifest.
5. Skills that live inside the repo must self-declare their adherence level.

---

## 5. Obsidian / Vector Mirror Requirement

- Every long-form Markdown document SHOULD be chunkable into page-level leaves.
- PDFs in the object lake SHOULD have a parallel Obsidian book whose leaves are one page (or one logical section) each.
- Vector indexes (when present) point at the leaf IDs, not at monolithic blobs.

---

## 6. Versioning of This Spec

- This file is `OLIVIA_DEV_ALPHA_SPEC_v0.md`.
- Breaking changes require a new major version and a migration note in `docs/CHANGELOG.md`.
- Once promoted into the actual Olivia Dev Alpha skill, the skill body MUST remain a faithful rendering of the then-current spec version.

---

*End of v0. This is the contract we will test against the current research-recovery repo and then against the first new repositories.*
