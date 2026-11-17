# S2 R3 — pillbox analytical versus CST evidence assessment
**ID:** S2-NEXT-20261117-R3
**Worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_S2_20261115`
**Assigned status:** `docs/investigations/S2_STATUS.md`
**Authority:** Read-only; no new fitting/integration/CST.

## Common protocol
Read the reporting repository `docs/programme/REPORTING_PROTOCOL.md` and latest FRM/A5/S2 reports. Inspect primary scientific artifacts, preserve sealed decisions, hashes, HOLDs and provenance qualifications. Use a new PROPOSED / NOT SEALED output namespace. Do not edit other streams or programme files. Propose only your assigned investigation-status update; show diff and wait for explicit author approval before any commit/push. Record branch/HEAD, inputs, units, metrics, commands and limitations. No CST operations or new field exports are authorised.

## Tasks
1. Inspect Stage 2B five-mode pillbox evidence (TM010, TM110a/b, TM210a/b), 61x61x121 complex E/H maps, matched native/ideal E0/E1/E3, D1/E2, B1 gap and S2 R2 evidence package. Verify primary source paths.
2. Inventory available analytical-versus-CST comparisons for complex voltages and derivatives, normal/skew quadrupoles, orientations, TVMD versus Fourier/polar, radii/orders/sampling/noise and finite-window quadrature.
3. Separate analytical fitting correctness, source-calibrated CST/ideal agreement, FEM discretization, export interpolation, phase/normalization/orientation and integration uncertainties. Do not call source-calibrated ideal derivatives independent CST physical truth.
4. Determine whether existing evidence supports a bounded Route A validation section and recommend figures/tables. Account for cases where correctly specified polar models outperform TVMD.
5. Only if a genuine scientific gap remains, specify minimal additional CST acquisition (consider TM210 doublet), independent mesh levels, mode tracking, identical coordinates, complex E/H, source provenance, prospective metrics and acceptance criteria. Denser export is not mesh refinement.

## Deliverables
`PILLBOX_EVIDENCE_ASSESSMENT.md`, `PILLBOX_VALIDATION_GAP_MATRIX.csv`, `PILLBOX_NEXT_DECISION.md` (A existing evidence sufficient / B limited offline analysis / C new CST acquisition), and `PROPOSED_CST_ACQUISITION.md` only if C. Proposed diff to **only** `S2_STATUS.md`. No new calculations, commit or push.
