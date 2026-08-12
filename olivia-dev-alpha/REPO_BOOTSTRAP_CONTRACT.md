# Repo Bootstrap Contract
**Companion to**: OLIVIA_DEV_ALPHA_SPEC_v0.md  
**Purpose**: Exact steps to make an existing repository compliant, or to birth a new one that is compliant from commit 0.

---

## A. Bootstrap a Brand-New Repository (the 16-repo case)

1. Create the repo (public or private).
2. Commit the skeleton in one shot:
   - README.md, MANIFEST.md
   - .github/workflows/structure-check.yml (copy from research-recovery-haist)
   - agents/INDEX.md (empty table)
   - nodes/INDEX.md or skills/INDEX.md as appropriate
   - system/DUAL_SSOT.md (declare lake locations)
   - docs/CHANGELOG.md, docs/QUICKSTART.md, docs/TODO.md
   - olivia-dev-alpha/ (or a symlink / submodule pointer to the canonical spec)
3. Push to main. Confirm structure-check is green.
4. Only then begin adding real agents/nodes/skills.

## B. Refactor an Existing Repository

1. Inventory every first-class entity that currently lives as a loose file or nested arbitrarily.
2. Create the target folders (`agents/<id>`, `nodes/<id>`, etc.).
3. Move content; write the minimum README.md + MANIFEST where required.
4. Build or update INDEX.md files so they match reality.
5. Add or repair the structure-check workflow.
6. Run the check locally (or via CI) until green.
7. Record the migration in docs/CHANGELOG.md and in the appropriate evolution track.

## C. Registration of a New Agent Runtime (federated coding)

Any LLM / runtime that wants library access:

1. Fork or open a PR against the target library repo.
2. Add `agents/<new-runtime-id>/README.md` conforming to the entity README contract.
3. Add one line to `agents/INDEX.md`.
4. Structure-check must pass.
5. On merge, the runtime is considered registered and may read the academic / research library under the dual-SSoT rules.

## D. Proof Plan (before promoting into the live Olivia Dev Alpha skill)

1. Keep the three files under `olivia-dev-alpha/` on this repo as the working set.
2. Apply the bootstrap contract to one additional small pilot repo.
3. Confirm structure-check catches deliberate omissions.
4. Only after two green proofs do we promote the spec text into the skill body and begin enforcing it on new work.

---

*This contract is executable. Follow it literally; do not improvise folder names.*
