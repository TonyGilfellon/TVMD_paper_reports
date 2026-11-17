# FRM — next instruction: numerical qualification decision

**Instruction ID:** FRM-NEXT-20261117-R2  
**Authority:** Read-only scientific assessment and proposed reporting update only.  
**Reporting repository:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_reports`  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_FRM`  
**Assigned reporting file:** `docs/investigations/FRM_STATUS.md`

## Objective
Assess the completed FRM-4B1 evidence and recommend the minimum defensible next decision for Route A TVMD. Do not treat a full-rank fit, low residual, or agreement with a non-independent reference as proof of physical derivative accuracy.

## Mandatory source review
Read `docs/programme/REPORTING_PROTOCOL.md` and the latest published FRM, A5, S2 status reports. In the scientific FRM worktree, inspect `docs/FRM_4B1_M0_NUMERICAL_STABILITY_REPORT.md`, `validation/frm4b1/DECISION.json`, `validation/frm4b1/A5_HANDOVER.md`, `validation/frm4b1/A5_HANDOVER.json`, the source/provenance manifests and relevant prior sealed decisions. Verify source existence and note missing or untracked artifacts. Do not infer provenance from the reporting summary alone.

## Questions to resolve
1. For each candidate observable (integrated on-axis voltage V0, integrated longitudinal-voltage Hessian Hxx/Hxy/Hyy, endpoint-corrected transverse-voltage Jacobian K_T, and any proposed quadrupole quantity), distinguish numerical repeatability, identifiability, sensitivity, and independently established physical accuracy.
2. Build a matrix of radius, polynomial order, transverse support/density, longitudinal sampling, quadrature, source-state/mesh and endpoint dependencies. Record numerical envelopes with definitions, units, denominators and near-zero guards; preserve all adverse cases and rank deficiencies.
3. Determine whether any *narrowly stated* observable can be qualified from existing evidence. If not, explicitly retain HOLD/CONDITIONAL. Do not invent a tolerance or choose an optimal radius by minimizing disagreement against the same reference.
4. Identify the smallest discriminating next evidence step(s), each with a precise question, prerequisites, measurable acceptance criterion, expected scientific value and whether CST/operator approval is required. Distinguish documentary/analysis-only checks from new acquisition or mesh studies.
5. State exactly what can and cannot be handed to A5, including native-state hashes, coordinate/support definitions, field phasor, normalization, finite endpoints and uncertainty limitations. Do not imply that M0 ingestion PASS establishes transverse-field accuracy.

## Deliverables
- A concise, source-linked scientific decision memo in the FRM scientific worktree, clearly marked **PROPOSED / NOT SEALED**; avoid modifying sealed records.
- An observable-by-observable qualification table with PASS/CONDITIONAL/HOLD scoped to each claim.
- A minimum-evidence decision tree, separating steps possible without CST from steps requiring separate user approval.
- A proposed update to **only** `docs/investigations/FRM_STATUS.md`, including UTC time, scientific HEAD, evidence paths and unresolved dependencies; show the diff for approval.

## Boundaries
No new CST solve, GUI operation, re-export, interpolation of incompatible grids, optimization, modification of sealed artifacts, rerun of expensive analyses, Git commit or push without separate explicit approval. Do not edit A5/S2 or programme files. If existing evidence is sufficient for a conclusion, stop without creating redundant calculations.
