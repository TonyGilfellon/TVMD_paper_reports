# A5 — next instruction: FRM handover compatibility gate

**Instruction ID:** A5-NEXT-20261117-R2  
**Authority:** Read-only interface and scientific compatibility assessment only.  
**Reporting repository:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_reports`  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_A5`  
**Assigned reporting file:** `docs/investigations/A5_STATUS.md`

## Objective
Decide whether the *existing* FRM-4B1 handover is sufficiently qualified and compatible to support any next independent full-cavity transverse-voltage/kick comparison. The current physical benchmark remains HOLD unless evidence explicitly resolves its gates. The primary provisional observable is full-cavity transverse voltage/kick, **not** an isolated coupler-only coefficient.

## Mandatory source review
Read the latest published FRM and A5 reports and `docs/programme/REPORTING_PROTOCOL.md`. Inspect A5's `validation/stage_a5/r6j/FRM_INTERFACE_REQUEST.md`, `COMPARISON_CONTRACT.md`, `NEXT_STAGE_HOLD.md`, `SCIENTIFIC_REVIEW.json`, R6F convergence results and R6I/R6J evidence. Inspect FRM's `validation/frm4b1/A5_HANDOVER.md` and `.json` and the underlying FRM-4B1 decision/provenance documents directly in the FRM scientific worktree. Verify exact sources; do not rely only on summary descriptions.

## Questions to resolve
1. Produce a field-by-field compatibility matrix: solved mode/state and hashes; E/H acquisition and spatial coordinates; supported transverse radius and trajectory; longitudinal window, plane count and quadrature; frequency, time-phasor and transit phase; E/H-to-B and sign conventions; endpoint treatment; native and on-axis-voltage normalization; output units and physical impulse interpretation; and numerical qualification/uncertainty.
2. For each field mark **MATCH / MISMATCH / MISSING / UNQUALIFIED**, cite exact evidence, and specify whether it blocks any physical comparison. Keep untracked artifacts and operator-only metadata explicitly qualified.
3. Distinguish the existing computational PASS (432 complex voltages bit-for-bit; 30 targeted tests) from the unresolved physical reference convergence (801→1601 direct-map changes of 8.84% trapezoid and 13.19% Simpson). Determine whether FRM-4B1 resolves *any* of these issues without overclaiming.
4. Identify the minimum next *independent* physical check, the data it requires and the explicit acceptance conditions. Avoid selecting fitting radius or calibration to minimize agreement error. Preserve complex, phase-sensitive comparisons rather than relying on crest projection alone.
5. State whether a published LCLS-II or coupler-only comparison is currently well-defined. If not, record the definition/source/convention gap and leave it outside the approved next-stage scope.

## Deliverables
- A source-linked **PROPOSED / NOT SEALED** A5–FRM handover decision and compatibility matrix in the A5 scientific worktree.
- Explicit gate result: **ACCEPT FOR A SPECIFIC LIMITED USE**, **CONDITIONAL**, or **HOLD**, with observable and limitations; no generic PASS.
- A prioritized blocker list and minimal next evidence request addressed to FRM/operator, without duplicating FRM's mesh/conditioning analysis.
- A proposed update to **only** `docs/investigations/A5_STATUS.md`; show diff and await approval.

## Boundaries
No new physical kick calculation, CST operation, re-export, field manipulation, phase/amplitude fitting, radius optimization, external-paper agreement claim, modification of sealed evidence, commit or push without separate explicit approval. Do not edit FRM/S2 or programme files. Read the FRM worktree without writing to it.
