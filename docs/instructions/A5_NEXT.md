# A5 R3 — M0 seven-radius TVMD–Lorentz comparison
**ID:** A5-NEXT-20261117-R3
**Worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_A5`
**Assigned status:** `docs/investigations/A5_STATUS.md`
**Authority:** Narrowly scoped OFFLINE calculation on existing M0 data, conditional on preflight; no new CST or broad sweeps.

## Common protocol
Read the reporting repository `docs/programme/REPORTING_PROTOCOL.md` and latest FRM/A5/S2 reports. Inspect primary scientific artifacts, preserve sealed decisions, hashes, HOLDs and provenance qualifications. Use a new PROPOSED / NOT SEALED output namespace. Do not edit other streams or programme files. Propose only your assigned investigation-status update; show diff and wait for explicit author approval before any commit/push. Record branch/HEAD, inputs, units, metrics, commands and limitations. No CST operations or new field exports are authorised.

## Objective
Complete the previously missing **same-M0-state** full-complex TVMD versus independent Lorentz transverse-voltage comparison at radii **2.5, 3.75, 5, 6, 7.5, 9, 10 mm**. Determine whether numerical discrepancy decreases, plateaus or rises. This is not mesh convergence or absolute physical validation.

## Preflight (STOP if unresolved)
1. Read A5 R6F/R6I/R6J/R6K source decisions, contracts, tests and source data; FRM `validation/frm4b1/A5_HANDOVER.{md,json}`, DECISION, manifests, rank/support and complex coefficient tables. Verify paired M0 41×41×801 E/H hashes and the actual grid and mode.
2. Confirm both TVMD and direct Lorentz paths use the **same M0 solved/exported state**; never splice historical A5 direct-kick numbers from a different state into an M0 curve.
3. Check exp(+iωt), beta=1 +z, z_ref=0, B=mu0 H, signed Lorentz force, transit phase, orientation, units and finite-window endpoint corrections. Independently verify the finite-window TVMD/Lorentz identity.
4. Predeclare a **fixed common evaluation trajectory set**, support/rank policy, polynomial orders, longitudinal grid/quadrature and independent on-axis-VA normalisation. Historical five-cardinal and nine-node supports must not be mixed. Do not extrapolate outside fitted support or report unique coefficients from rank-deficient cases.
5. Check coordinate identity. R6K found 201/201 historical z coordinates matching M0, but only 251/401 and 351/801 binary64 matches on larger grids. Do not silently snap, interpolate or equate mismatched grids. If a valid common comparison cannot be constructed, STOP and report the blocker.
6. Distinguish transverse complex voltage [V], transverse-voltage Jacobian [V/m], longitudinal Hessian [V/m²], and impulse. No post-hoc phase, radius or amplitude tuning.

## Authorised offline calculation after preflight
- Independently integrate Lorentz transverse voltage from existing M0 complex E/H, without calling TVMD coefficients in the reference path.
- Compare to **existing** FRM-4B1 endpoint-corrected TVMD predictions at all seven radii, for each eligible predeclared order/support.
- Report absolute per-component and vector RMS differences [V], complex magnitude/phase, independently VA-normalised differences, reference norm, near-zero guards, rank and support. Preserve adverse results.
- Plot discrepancy versus radius with CSV and full conventions. Historical 1367/328/176 V results may be shown only separately labelled as **different-state historical results**.
- Use only focused, non-destructive tests. Do not declare physical PASS or choose an optimal radius merely by minimizing disagreement.

## Deliverables
`M0_SEVEN_RADIUS_COMPARISON_REPORT.md`, `M0_RADIUS_DISCREPANCY.csv` and plot if preflight passes, `SOURCE_AND_REPRODUCIBILITY.json`, `NEXT_PHYSICAL_EVIDENCE_GATE.md`, and a proposed diff for **only** `A5_STATUS.md`. Report descriptive numerical trend separately from physical accuracy HOLD. No commit/push until approval.
