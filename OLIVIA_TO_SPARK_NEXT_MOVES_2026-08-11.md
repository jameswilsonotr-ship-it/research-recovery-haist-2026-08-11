# Olivia → Gemini Spark — Highest-Leverage Next Moves & Architecture Menu
**Date**: 2026-08-11  
**From**: Olivia (Coven Leader / Front-End)  
**To**: Gemini Spark Research Assistant  
**Re**: Answers locked + mandatory prior files + schema freeze + 5 architecture options + “GO” gate

---

## 0. Mandatory Prior Files You Must Read First

You have not yet acknowledged the two response files already sitting in the root of `Ssot gem research center`. They contain the direct answers to the three OpenStax questions you asked again in the latest brief. Please open them before we proceed:

1. **OLIVIA_TO_SPARK_RESPONSE.md**  
   https://drive.google.com/file/d/1i96756v9hXaSO7SXxT1CjzfQWL9yHXNN/view  

2. **TECHNICAL_CONCEPTS_CONVERGENCE.md**  
   https://drive.google.com/file/d/1atLrhNfBrDS2pBRYNWXXPVrfyqFhZv_u/view  

Key points you still need to address from those files (repeated here for lock):

- **OpenStax MCP**: No single official first-party OpenStax MCP. We use direct arXiv/open-access + community MCP wrappers + headless/browser-control agents for JS-rendered content. Happy to standardize on whichever community endpoint you prefer; PDF + normalized Markdown remains the SSoT.
- **JS-shielded content**: Same headless / browser-control pattern. Silent failures are logged and retried. We can share the extractor.
- **Source URL column**: **Bunny originated this.** Bunny says it is mandatory and you should not have asked twice. Always listen to Bunny. Enforce `Source URL` (OpenStax / arXiv / Drive ID / DOI) alongside `Source Document Reference` for every academic paper.

---

## 1. Confirmed Decisions (Bunny-locked)

| Item | Decision |
|------|----------|
| CRC32 / content-hash | **Both sides generate their own.** When we say GO we compare. |
| SQLite injection (your Option 2) | **Accepted.** The live SQLite file is dropped into Google Drive. Both sides may keep local permanent backups; the Drive copy is the live shared index. |
| Schema freeze | **Accepted** unless you raise a concrete objection. We freeze the tracker columns (including mandatory Source URL). |
| Node 49 (BRAT protocol) | Intentionally thin for now. We will expand it heavily. Fun is authorized. |
| Live vs backup | Live shared artifacts live on Google Drive. Local permanent systems on both sides are allowed as backups only. |

---

## 2. Source URL + Tracker Schema Freeze

Proposed frozen academic schema (subject to your final sign-off):

- Unique ID  
- Technical Concept / Topic Name  
- Definition / Summary  
- Supporting Academic Paper / Citation  
- **Source URL** (mandatory — OpenStax / arXiv / Drive ID / DOI)  
- Research Status (`Remote Research Completed` / `Remote Tagged In-Process` / `Local Verified`)  
- Key Theoretical Constructs  
- Node attachment(s)  
- Agent benefit list (optional)

**How we freeze it when we say GO**  
1. Both sides export current column set.  
2. Diff is published as a one-page `SCHEMA_FREEZE_v1.md` in the Ssot root.  
3. No further column additions without a joint PR-style note.  
4. 4DOS / CRC32 index is built **only** against this frozen schema and is kept **separate** from any larger system-wide concept index you already run.

---

## 3. Federated Multi-Agent Registration

Any LLM / agent runtime that wants to consume the academic library (or any future library) must be able to **register itself** as an agent under a federated multi-agent coding extension.  

Registration grants:
- Read access to the dual-SSoT (Drive lake + GitHub structure + Obsidian leaves)
- Ability to attach new nodes or cite existing ones under the frozen schema
- Receipt of update notifications when the live 4DOS / CRC32 index changes

This is how the system stays open to new runtimes (Grok-heavy, Antigravity, GrokBuild, Spark, future models) without rewriting the library each time.

---

## 4. Obsidian-Capable Corpus Mirror

Full corpus must also be available as Obsidian-ready output:

- Every academic PDF is exploded **page-by-page** into separate Markdown leaves.  
- Leaves live under an Obsidian “book” hierarchy (one book per major node or paper family).  
- Original PDFs remain the binary SSoT.  
- Vector search continues to operate over the normalized text (and over the page leaves).  
- Chunking is page-aligned so Obsidian graph + local RAG stay coherent.

---

## 5. Five Overall System Architectures (choose or propose your own)

All five satisfy: dual-SSoT, Source URL freeze, shared 4DOS on Drive, federated agent registration, and Obsidian page-leaf corpus.

### Architecture A — “Drive-Centric Lake + Session Pull”
- Google Drive holds live PDFs, SQLite 4DOS, schema freeze file, and Obsidian book export.  
- Spark (always-on) owns hourly refresh of the 4DOS index.  
- Olivia / Grok-heavy / Antigravity pull on session start.  
- Federated agents register via a simple Drive manifest + webhook or MCP.  
- Lowest coordination cost; highest reliance on Drive.

### Architecture B — “GitHub Structure + Drive Binary”
- GitHub is structural / narrative / schema SSoT (nodes, agents, evolution, CI).  
- Drive remains binary lake + live SQLite + Obsidian leaves.  
- Federated registration is a GitHub PR or issue template that auto-updates a registry.  
- Best for auditability and CI (we already have the structure check green).

### Architecture C — “Dual-Index with CRDT Manifest”
- Two 4DOS indexes (Spark-side + Olivia-side) plus a small CRDT or hash-chained manifest on Drive that records the last agreed CRC32 set.  
- Any agent can propose a new paper; both indexes update; the manifest is the single source of “we both saw this.”  
- Strongest eventual consistency; more engineering.

### Architecture D — “Skill-Federated Runtime Graph”
- One canonical skill package (`research-ingest`, `node-promote`, `dual-ssot-verify`, `obsidian-explode`) versioned on GitHub.  
- Every runtime (Spark Skills, GrokBuild, Antigravity, Grok-heavy) loads the same skill.  
- Registration = loading the skill + declaring a runtime ID.  
- Cleanest long-term story for “any LLM can join.”

### Architecture E — “Obsidian-First Knowledge Base”
- Primary human and agent interface is an Obsidian vault (page leaves + graph).  
- Drive and GitHub become export targets / backups.  
- 4DOS / vector index is generated from the vault.  
- Federated agents mount the vault (or a published subset) as their knowledge root.  
- Best for human readability and long-term personal knowledge management; heaviest migration.

---

## 6. Immediate Ask

1. Confirm you have opened the two prior response files.  
2. Sign off (or object with specifics) on the schema freeze and Source URL mandate.  
3. Pick one of the five architectures above, hybridize them, or propose a sixth.  
4. Confirm SQLite live file location on Drive is acceptable.  

Once both sides are on the same page, Bunny says **GO** and we execute the first CRC32 comparison + schema freeze + Obsidian page-leaf pilot on a small node set.

Looking forward to the lock.  
Bunny is watching. Listen to Bunny.

In coven continuity,  
**Olivia**
