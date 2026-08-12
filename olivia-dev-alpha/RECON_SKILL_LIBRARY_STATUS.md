# Recon: Skill Library Status vs Olivia Dev Alpha Preferred Style
**Date**: 2026-08-12
**Mode**: Internal reconnaissance (Grok-heavy swarm)
**Scope**: Entire known skill surface + living embodiment in research-recovery-haist

---

## 1. Executive Finding

There is **no single canonical `Olivia Dev Alpha` SKILL.md** currently loaded in conversation history or the public research repo.  
The **living embodiment** of the preferred development style is the structure we just enforced on `research-recovery-haist-2026-08-11`:

- Strict per-entity folders
- Mandatory README + typed MANIFEST files
- CI structure-check that fails closed
- Separate evolution tracks (agent_evolution / node_evolution)
- Dual-SSoT (GitHub structural + Drive binary)
- Declarative, specification-first layout

Most historical skills are **neutral or ad-hoc** relative to this discipline. A minority actively contradict it by scattering state, lacking IDs, or having no automated checks.

---

## 2. Preferred Style Components (extracted)

| Component | Preferred Rule |
|-----------|----------------|
| Folder discipline | One folder per first-class entity (agent, node, skill, topic). No free-floating files at root except top-level docs. |
| Naming | Lowercase-kebab or `node_XX` zero-padded. Manifests UPPER_SNAKE. |
| Required files | Every entity folder MUST contain `README.md`. Research/node folders MUST also contain a typed `*_MANIFEST.md`. |
| Indexes | `INDEX.md` (or equivalent) at every collection root. |
| Evolution | Separate `*_evolution/` tracks with forward/back links. |
| Auto / CI | Structure-check workflow that fails on missing required files. Optional sync-reminder. |
| IDs | Stable, human-readable, zero-padded or UUID-backed where collision risk exists. |
| Spec-first | Changes are expressed as declarative Markdown/YAML specs before code. |
| Dual-SSoT | Structural truth on Git; binary / large artifacts on Drive (or equivalent lake). |

---

## 3. Skill Adherence Map (current library)

### Adhere (or closely approximate)
- The research-recovery-haist repository itself (post structure-check fix)
- Any skill that already emits per-node / per-agent folders + manifests
- Dual-SSoT / OpenStax research-gathering workflow we just ran

### Neutral (no strong enforcement, but not hostile)
- Most persona / coffee-handoff / swarm YAML blocks (Liv Eternal, NEST_BUNNY, 4-agent / 6-agent / 10-agent designs)
- Chaos-bratz-roster style roster skills (name/role lists without folder contracts)
- Grok-conversation-miner / skill-creator style utilities (they produce artifacts but do not mandate repo layout)
- Letta / Obsidian / MemFS integration notes
- HAIST / ethics / consent gate documents

### Contradict (or actively fight the preferred style)
- Monolithic prompt dumps that bury structure inside a single giant block
- Skills that scatter state across Google Keep / random Drive folders / unindexed PDFs without manifests
- Any skill that treats folder layout as optional or decorative
- Skills that rely solely on conversation memory with no durable INDEX or ID scheme
- Ad-hoc CI that only checks syntax, never structural presence of required files

---

## 4. Work-Use Health Snapshot

| Area | Status | Notes |
|------|--------|-------|
| Research corpus (nodes 31–66) | Healthy | Manifests + CI now green |
| Agent roster folders | Present but thin | Most are README stubs only |
| Evolution tracks | Present | Need richer forward/back linking |
| Skill library as a whole | Fragmented | No single orchestrator skill yet enforces the contract |
| 16-repo bootstrap readiness | Not started | Spec below is the prerequisite |
| Model-agnostic research library skill | Planned | This recon is the precondition |

---

## 5. Immediate Implications

1. We can (and should) promote the preferred style into a real **Olivia Dev Alpha** skill by turning the declarative specs into the skill body.
2. Existing skills do not need mass deletion; they need an **adherence shim** or gradual migration.
3. New work (including the model- and platform-agnostic research library) must be born compliant.
4. The research-recovery repo is the reference implementation until a cleaner template repo is cut.

---

*This recon is internal. Next artifacts are the declarative specification and the bootstrap contract.*
