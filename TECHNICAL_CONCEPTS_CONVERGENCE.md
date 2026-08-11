# Technical Concepts — Multi-Runtime Skill & Research SSoT Convergence
**Author**: Olivia (with Grok-heavy swarm support)  
**Date**: 2026-08-11  
**Audience**: Gemini Spark, Antigravity agents, GrokBuild operators, future federated runtimes

---

## Core Thesis

The research corpus (academic nodes 01–66 + practical non-academic counterparts) must become a **skill-addressable, multi-runtime synchronized source of truth**. Google Drive currently functions as the binary/object lake; the public GitHub repository functions as the structural and narrative SSoT. Persistent agents (Spark) and session-bound heavy swarms (Grok-heavy, Antigravity, GrokBuild) play complementary roles.

---

## 1. Dual-SSoT Architecture (Current)

- **Academic SSoT**: Node-named PDFs + manifests on Drive (`node_XX__slug.pdf`) + full tarball.
- **Structural / Narrative SSoT**: GitHub repo (`agents/`, `nodes/`, `system/`, `history/`, evolution Markdowns).
- **Concept Tracker**: Google Sheet + optional 4DOS CRC32/SQLite index for O(1) lookup.
- **Invariant**: Every academic paper carries both a Drive object and a Source URL / DOI attribution.

---

## 2. Skill Surface Comparison (Cross-Runtime)

| Runtime | Skill Model | Persistence | Scheduling | Parallelism | Notes |
|---------|-------------|-------------|------------|-------------|-------|
| **Grok Web / Heavy** | Conversational + limited skill packs; Heavy = 4-agent collaborative swarm | Session + memory controls | None native | 4-agent internal debate | Excellent for deep synthesis; not always-on |
| **GrokBuild CLI** | SKILL.md folders, plugins, hooks, MCP, AGENTS.md | Filesystem + memory | Headless / CI | Subagents + worktrees | Strongest local coding agent surface |
| **Google Antigravity 2.0** | Skills as context compression, MCP, hooks, subagents | Agent Manager + scheduled tasks | Native cron-like Schedules | Dynamic subagents | Agent-first; pairs with IDE/CLI/SDK |
| **Gemini Spark** | Skills + Schedules + Tasks | 24/7 cloud VM | First-class Schedules | Parallel source processing | Always-on differentiator; Workspace-native |

**Convergence target**: One canonical skill package (research-ingest, node-promote, dual-ssot-verify, openstax-fetch) versioned in GitHub and loadable by every runtime above.

---

## 3. Recommended Federation Patterns

1. **Event-driven ingest**  
   Spark (or any watcher) detects new PDF / Sheet row → normalizes → opens PR or updates Drive + Sheet. Heavy swarm invoked only for conflict or deep node expansion.

2. **Checksum gate**  
   Periodic content-hash (CRC32 or stronger) of Drive lake vs GitHub tree. Drift triggers a reconciliation task.

3. **Federated coding**  
   Antigravity Agent Manager or GrokBuild headless can own the PR review/merge loop. Spark can comment or supply context via MCP / email / Drive.

4. **Source URL as mandatory key**  
   No paper enters the academic SSoT without a resolvable Source URL / DOI / Drive ID. Bunny-enforced.

---

## 4. Capability Notes (Planning Horizon)

- **Spark** supplies continuous presence and Workspace-native actions; ideal lake watcher and light normalizer.
- **Antigravity 2.0** (Agent Manager + CLI + SDK) supplies scheduled agentic coding and subagent parallelism.
- **GrokBuild** supplies terminal-native skills/hooks/MCP and strong local repo discipline.
- **Grok-heavy** supplies high-quality multi-agent debate/synthesis when deep reasoning is required.

None of these should own the entire loop alone. The research SSoT should be runtime-agnostic and skill-synchronized.

---

## 5. Immediate Next Artifacts

- Shared `Source URL` column schema.
- Minimal SKILL.md (or equivalent) for “research paper ingest + node attachment”.
- CRC32 / content-hash verification script that both Spark and Grok-side agents can run.
- Public repo branch protection + simple CI that validates node naming and manifest presence.

---

*This document is itself part of the structural SSoT and should be updated whenever the federation model changes.*
