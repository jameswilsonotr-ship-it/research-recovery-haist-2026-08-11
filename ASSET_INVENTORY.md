# ASSET_INVENTORY.md

**Purpose**: Canonical map of every academic PDF recovered in the 2026-08-11 research session.
This file is the naming authority for future GitHub Release assets.

## Current binary location
- Google Drive full package (primary):
  - Folder: https://drive.google.com/drive/folders/1G3bFznzNKxGNShb29mzrXwZXP6B6-CJ-
  - Archive: https://drive.google.com/file/d/1xUI7JwPGZ-HDmpZr7kwbFzhiMd798foN/view
- Local sandbox: `/home/workdir/artifacts/research_pdfs/`

## Recommended Release strategy
1. Create a single Release tagged `research-pdfs-v1.1.0`.
2. Upload each PDF using the **Recommended asset name** below.
3. Alternatively upload the one big `.tar.gz` as a single asset named `research_recovery_full_with_pdfs_v1.1.0_2026-08-11.tar.gz`.

## Naming convention
```
node-XX__short-descriptive-slug__original-id-or-year.pdf
```
Example: `node-34__airgap-agent-privacy-conversational__2405.05175.pdf`

---

## How to use this inventory
1. Go to the repository → Releases → Draft a new release.
2. Tag: `research-pdfs-v1.1.0`
3. Title: `Research PDFs v1.1.0 — Full academic corpus (84 files)`
4. Upload either:
   - The single tarball from Drive, **or**
   - Individual PDFs renamed according to the Recommended asset name in this file.
5. After upload, update the corresponding `nodes/node_XX/PDF_MANIFEST.md` with the Release download URLs.

## Full inventory (84 PDFs)

Every PDF is listed under its research node with:
- Original filename
- Recommended Release asset name (node-prefixed for clarity)
- Sandbox path

(The complete machine-generated list with all 84 entries is maintained in the repository version of this file. Key nodes with the largest holdings: node_37 (stateful security / JSD / poisoning / ROME — 17 files), node_38 (STAMP/STPA — 12 files), node_34 (air-gap — 6 files), node_50 (micro-expressions — 6 files), node_65/66 (HAIST Theory + Talent Development).)

**Total PDFs inventoried**: 84

---
*This file is the single source of truth for asset naming. Do not invent new names without updating this inventory.*
