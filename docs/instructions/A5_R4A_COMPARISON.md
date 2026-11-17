# A5 R4A — descriptive same-M0-export linearised TVMD–Lorentz comparison

**Instruction ID:** A5-R4A-M0-LINEARISED-20261117  
**Owner:** A5  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_A5`  
**Reporting repository:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_reports`  
**Authority:** Author-approved **narrowly scoped offline calculation** using existing M0 E/H exports and already-computed FRM-4B1 coefficients, subject to the numerical preflight below. No CST, new export, refitting, coefficient reconstruction, phase/amplitude calibration or new physical accuracy claim.

## Purpose and changed R3 gate
R3 stopped because native solved-state/physical-axis/phasor provenance was not independently certified and complete order-dependent finite-offset predictions were not supplied. R4A **explicitly permits a descriptive same-export numerical consistency comparison under stated conventions** despite the former limitation. It **does not** release the physical benchmark HOLD. The latter limitation is addressed by changing the declared observable to the **linearised** endpoint-corrected prediction, not silently treating it as the full order-3/4 field.

## Dependency and mandatory sources
Before running, read the FRM R4A coefficient-interface note and confirm its `READY FOR LIMITED NUMERICAL USE` decision. Inspect the latest reporting protocol and FRM/A5 R3 status reports; the A5 R6A force implementation, R6F/R6I/R6J/R6K/R6L contracts and source records; FRM-4B1 handover and underlying coefficient/rank/normalisation records. Use exact raw M0 E/H files and verify hashes against recorded values. Retain all sealed historical decisions. If the FRM interface is BLOCKED, stop and report precisely why.

## Predeclare numerical contract before seeing agreement
- **Source:** only paired M0 `M0_R10_h2mm_E_41x41x801.txt` and `M0_R10_h2mm_H_41x41x801.txt`, matching verified hashes. Never use historical R5/R6F direct voltages as the M0 reference.
- **Fitting radii [mm]:** 2.5, 3.75, 5, 6, 7.5, 9, 10. **Orders:** 2/3/4, only existing full-rank FRM-4B1 0.5-mm-density, 801-plane trapezoidal families with exact compatible definitions. Preserve each family separately; do not cherry-pick.
- **Fixed evaluation trajectories [mm]:** `(0,0)`, `(2.5,0)`, `(-2.5,0)`, `(0,2.5)`, `(0,-2.5)` at every radius. Keep the evaluation set constant, distinct from the fit support. Report axis and four off-axis statistics separately, because the on-axis term may dominate.
- **Longitudinal integration:** native M0 801 actual-coordinate z samples and trapezoidal rule as the primary comparison. Do not borrow historical 401/801 coordinates or silently interpolate. If the raw M0 grid permits nested exact 201-plane subgrids, they may be evaluated **only as a separately labelled diagnostic** using pre-existing matching FRM coefficients, without regridding; do not assume Simpson or 1601 data are available.
- **Conventions to verify:** complex peak phasors `Re[F exp(+iωt)]`, +z β=1 trajectory, z_ref=0, `B=μ0H`, E [V/m], H [A/m], x/y [m], z endpoints and frequency from M0; signed Lorentz transverse voltage `∫(Ex-v By, Ey+v Bx) exp(iω(z-z_ref)/v) dz`. Check actual sign, handedness and endpoint definitions against source contracts; no assertion of independently certified physical orientation.
- **TVMD observable:** `T_lin(r;R,p)=T0(R,p)+K_T(R,p) r`, where `T0` [V] and `K_T` [V/m] are existing complex **finite-endpoint-corrected** FRM values. Use only after verifying their definitions in the interface note. This is the first-order Taylor prediction at finite offset, even when `p=3/4` supplied the fitted on-axis coefficients. It is **not** a complete order-p finite-offset transverse-voltage reconstruction.
- **Independent reference:** calculate direct Lorentz transverse voltage on the same M0 grid at each fixed evaluation point, from E/H only, without accessing TVMD fit coefficients in the reference path. Compute it once per trajectory and reuse unchanged across all fitting radii/orders.
- **Normalisation:** retain native complex voltages and independently integrated M0 on-axis longitudinal accelerating voltage `V_A` (not fitted `V0`) as a fixed, radius/order-independent normaliser. Never optimise registration, phase, amplitude or tolerance against direct kicks. Guard near-zero denominators; report raw and normalised metrics separately.

## Numerical preflight — stop only for calculation-defining blockers
Verify raw hashes, coordinates, field components, finite endpoints, frequency, reference formula and signs, existence/definitions of all required T0/K_T families, rank, unit conversions, fixed evaluation points and finite values. Record any genuine missing input and STOP that affected case; do not silently substitute coefficients or methods. **Uncertified physical provenance/axis orientation alone is not a STOP for this explicitly descriptive same-export calculation**, but must be prominently documented and continues to block a physical benchmark claim. Do not invent a physical error budget or retrospective numerical acceptance threshold.

## Calculation and reporting
1. Independently integrate M0 Lorentz transverse voltage for the fixed five points using the verified A5 path. Include a focused analytic identity/sign/endpoint check, including nonzero endpoint terms. Do not modify the source fields.
2. Evaluate `T_lin` from existing T0/K_T for each eligible radius/order; calculate the complex vector discrepancy `ΔT=T_lin−T_Lorentz`.
3. For each radius/order, report: all five pointwise complex x/y values (or a machine-readable companion table); RMS vector absolute discrepancy [V] over all five and separately four off-axis points; maximum vector discrepancy [V]; x/y RMS; discrepancy normalised by `|V_A|`; reference Lorentz RMS norm; and phase-sensitive complex comparisons. Clearly distinguish `|Δ|/|V_A|` from relative error against the small transverse voltage. Include near-zero guards and a separate on-axis discrepancy.
4. Plot **absolute complex vector RMS discrepancy versus fitting radius**, with separate lines by polynomial order and clearly identified evaluation sets. Also plot or tabulate `T0`, `K_T` and off-axis discrepancies versus radius to expose coefficient instability. Do not suppress unfavorable cases or claim convergence from a decreasing curve.
5. Where data permit, add a separately labelled exact-nested-grid longitudinal sensitivity check. Do not mix quadrature or sampling changes into the primary radius curve.
6. Interpret the result in terms of **same-export numerical consistency and linearisation sensitivity only**. Discuss the truncation effect of first-order Taylor approximation at ±2.5 mm, especially for p=3/4; do not attribute discrepancies uniquely to mesh, TVMD physics or quadrature.
7. Retain physical kick/mesh-convergence/published-LCLS-II comparisons as HOLD. No radius optimisation or validation PASS is authorised.

## Deliverables and decision
Create a fresh **PROPOSED / NOT SEALED** directory `validation/stage_a5/r4a_m0_linearised/` with:
- `R4A_REPORT.md` — preflight, full conventions, complete tables/plots, numerical conclusion and limitations;
- `R4A_POINTWISE_COMPLEX.csv`, `R4A_RADIUS_METRICS.csv`, and at least one labelled discrepancy-versus-radius figure **if preflight passes**;
- `SOURCE_AND_REPRODUCIBILITY.json` — exact raw hashes, coefficient manifest/FRM interface hashes, code paths, scientific HEAD, commands, environment, tests and output hashes;
- `DECISION.json` — scoped `DESCRIPTIVE NUMERICAL RESULT / PARTIAL / STOP`, with physical HOLD preserved;
- `NEXT_EVIDENCE_GATE.md` — whether a full finite-offset calculation or an independent mesh/physical reference would materially add information.

Run focused non-destructive tests only; preserve original results and snapshots. Propose a change to **only** `docs/investigations/A5_STATUS.md`, show the diff, and await separate explicit author approval before commit/push. Do not modify FRM/S2/programme files. Do not commit scientific outputs or overwrite sealed artifacts without separate approval.
