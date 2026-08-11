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

## node_31  (1 file)

- **Original**: `Intelligent_Truck_Matching_Ping2Hex_2605.07733.pdf` (5149 KB)
  - Recommended asset name: `node_31__Intelligent_Truck_Matching_Ping2Hex_2605.07733.pdf`
  - Path in sandbox: `node_31/Intelligent_Truck_Matching_Ping2Hex_2605.07733.pdf`

## node_32  (3 files)

- **Original**: `NetInjectBench_2607.10490.pdf` (1476 KB)
  - Recommended asset name: `node_32__NetInjectBench_2607.10490.pdf`
  - Path in sandbox: `node_32/NetInjectBench_2607.10490.pdf`

- **Original**: `eBPF_XDP_AI_Mitigation_2606.10508.pdf` (1031 KB)
  - Recommended asset name: `node_32__eBPF_XDP_AI_Mitigation_2606.10508.pdf`
  - Path in sandbox: `node_32/eBPF_XDP_AI_Mitigation_2606.10508.pdf`

- **Original**: `eBPF_XDP_Explainable_AI_IoT_Edge_2606.10508.pdf` (1031 KB)
  - Recommended asset name: `node_32__eBPF_XDP_Explainable_AI_IoT_Edge_2606.10508.pdf`
  - Path in sandbox: `node_32/eBPF_XDP_Explainable_AI_IoT_Edge_2606.10508.pdf`

## node_34  (6 files)

- **Original**: `AirGapAgent_Privacy_Conversational_2405.05175.pdf`
  - Recommended asset name: `node_34__AirGapAgent_Privacy_Conversational_2405.05175.pdf`
- **Original**: `Broadcast_ZeroTrust_AirGapped_AI_2603.24898.pdf`
  - Recommended asset name: `node_34__Broadcast_ZeroTrust_AirGapped_AI_2603.24898.pdf`
- **Original**: `Mind_The_Gap_Airgap_2409.04190.pdf`
  - Recommended asset name: `node_34__Mind_The_Gap_Airgap_2409.04190.pdf`
- **Original**: `Talking_to_Airgap_2512.15387.pdf`
  - Recommended asset name: `node_34__Talking_to_Airgap_2512.15387.pdf`
- **Original**: `Talking_to_the_Airgap_2512.15387.pdf`
  - Recommended asset name: `node_34__Talking_to_the_Airgap_2512.15387.pdf`
- **Original**: `Timing_Isolation_Hardware_Enclaves_MIT_2024.pdf`
  - Recommended asset name: `node_34__Timing_Isolation_Hardware_Enclaves_MIT_2024.pdf`

## node_35–node_66 and remaining

Full inventory of all 84 PDFs (including the large node_37 set, STAMP/STPA papers, HAIST papers, micro-expression, SOTA graphics, brat protocol, etc.) is maintained in the complete version of this file on the repository. Every entry follows the same pattern:

- Original filename + size
- Recommended Release asset name (node-prefixed)
- Sandbox path

**Total PDFs inventoried**: 84

When Release assets are uploaded, update the corresponding `nodes/node_XX/PDF_MANIFEST.md` files to include the Release download URLs.

---
*This file is the single source of truth for asset naming. Do not invent new names without updating this inventory.*
