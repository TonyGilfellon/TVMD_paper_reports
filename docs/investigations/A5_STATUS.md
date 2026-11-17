# A5 — independent full-cavity transverse-kick benchmark

**As of:** 2026-11-17 11:17:10 UTC (reporting reconciliation; no new scientific calculation).  
**Investigation owner / assigned file:** A5 / `docs/investigations/A5_STATUS.md`.  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_A5`.  
**Branch / HEAD:** `validation/m1-stage-a5` / `c7f0a6f9fb37a94127c440d0345e2528fc1d7f80`.  
**Decision ID:** `A5_R6I_R6J_SCIENTIFIC_REVIEW`; disposition `ACCEPTED_WITHIN_REPORTED_SCOPES_NEXT_STAGE_HOLD`.  
**Current status:** **PHYSICAL BENCHMARK HOLD**; computational validation **PASS within targeted scopes**; comparison infrastructure **CONDITIONAL** on a reviewed, compatible FRM handover.

## Source status and reconciliation

The 17 November coordinator baseline has been reconciled against retained A5 reports, decision records, result tables and test XML. Its 432-voltage replay, 30-test result and unresolved longitudinal sensitivity are supported. The baseline's proposed published LCLS-II comparison is corrected to the later accepted Route A scope: **full-cavity transverse voltage/kick is the provisional primary independent observable**. It is not a coupler-only coefficient. Any later coupler-only or published comparison requires a separately justified physical definition and compatible source; none is currently authorised. The baseline's unspecified “six-node agreement” is not used as evidence of physical convergence.

HEAD is the shared earlier Stage 2A analytic-validation commit, not a commit sealing the current investigation. The latest three scientific commits are `c7f0a6f9fb37a94127c440d0345e2528fc1d7f80` (Stage 2A pillbox/finite-boundary references), `8ae610404e422c05864d19742be7b0b7f7e54568` (Stage 1 voltage/coefficient observables), and `935eba1845994394fe78ad5f45f91f8cc0722b95` (decision numbering). The current status document and `validation/stage_a5/` evidence, including R6I/R6J, are **untracked working-tree evidence**, not committed/published scientific results. Their local paths and hashes below provide the current provenance. No new scientific commit or test execution was performed for this update.

## Accepted scope and scientific limits

| Scope | Decision and evidence |
|---|---|
| Independent Lorentz replay | **PASS, computational:** R6I reproduced 16 retained R6F cases / 432 complex voltages bit-for-bit, without TVMD fitting. Shared simulated fields mean this is formulation/reproducibility independence, not an independently certified electromagnetic reference. |
| Analytic and diagnostic implementation | **PASS, targeted:** retained R6J XML reports 30 tests, zero failures/errors/skips. Tests cover analytic pillbox/oblique waves, magnetic signs, H/B conversion, signed impulse, finite endpoints, phase-origin covariance and diagnostic interfaces. This is not a full-suite or physical-field PASS. Earlier stages retain the inherited 27-source CRLF-only raw-hash failure; no baseline was refreshed. |
| Physical reference convergence | **HOLD:** complex direct maps and TVMD maps/matrices did not stabilize on the retained longitudinal grids. No convergence order, absolute-error bound or mesh limit is established. |
| Radius/agreement interpretation | **Descriptive sensitivity accepted; validation HOLD:** no optimal radius selected. Minimizing benchmark disagreement on the same data would be calibration, not independent validation. |
| Next comparison | **CONDITIONAL:** infrastructure is ready to accept FRM-qualified, physically compatible data after all handover checks. No new agreement metric is authorised before review. |
| M0 / published interpretation | **HOLD:** M0 small transverse components remain unqualified for phase-sensitive physical use. No absolute kick accuracy, coupler-only or published LCLS-II agreement is established. |

Historical R1–R6H PASS, CONDITIONAL and HOLD decisions remain valid only in their original scopes. R6G established reconstruction/operator sensitivity without demonstrating a mesh cause. R6H session/startup HOLDs are not evidence of field failure. The later scientific review accepts R6I/R6J scopes and sets the next-stage HOLD; it does not promote physical validation or supersede earlier numerical limitations. Twenty historical top-level stage decision records are preserved in the R6J snapshot.

## Quantitative findings retained

Reference dataset: earlier Mode 9, **1.2999834328542283 GHz**, **2,170,925 tetrahedra**. R6F contains nine transverse trajectories on x,y in {-2.5,0,2.5} mm, 1601 longitudinal planes, repeated E/H acquisition and exact 801-plane overlaps. Raw integrity/repeatability is not physical accuracy.

Same-state direct-map nested relative L2 changes, denominator **the fine-grid direct transverse-map norm**:

| Planes | Trapezoid | Simpson |
|---|---:|---:|
| 201 → 401 | 24.58% | 31.68% |
| 401 → 801 | 13.63% | 20.38% |
| 801 → 1601 | 8.84% | 13.19% |

These combine unresolved sampling/recovery and quadrature sensitivity; they do not isolate pure quadrature error or compare solved meshes. At 1601 planes the fixed-nine-node direct/TVMD vector RMS discrepancy is **1389.46 V** (trapezoid) / **1394.00 V** (Simpson), where vector RMS is sqrt(mean(|delta Vx|²+|delta Vy|²)). These are discrepancies, not accuracy bounds.

For the earlier fine circular 201-plane trapezoid cardinal-five comparison, discrepancy changes **1367.00 → 328.43 → 175.94 V** for radii **2.5/3.75/5 mm**, with the direct reference fixed. No radius is validated by this decrease. At 1601 trapezoid planes, complex normalized RMS discrepancy is **4.78017e-4**, while its accelerating-crest projection is **4.45049e-5**, both normalized by the same independent axis voltage. These are dimensionless axis-voltage ratios, not relative errors against the transverse kick. Single-phase agreement can hide RF-quadrature disagreement.

## Physical contract

Peak phasors `Re[F exp(+i omega t)]`; E in V/m, H in A/m and vacuum B=mu0 H; coordinates converted mm→m once. Retained reference: straight +z, beta=1, z_ref=0, finite interval **[-0.23060958, 1.2660479] m**. Direct transverse voltage integrates `(Ex-v*By, Ey+v*Bx) exp(i omega(z-z_ref)/v) dz` from fields only. It never takes TVMD Hessians as inputs. Endpoint terms remain explicit in the TVMD comparison. Distinguish voltage [V], voltage Jacobian [V/m], longitudinal-voltage Hessian [V/m²] and physical angle.

Raw native complex scale/phase is preserved. A comparison scalar is determined once per solved mode from independently integrated on-axis VA, never fitted per radius/component. Signed momentum change is `q/v Re[exp(i phi) V_perp]`; angle also needs p0. Charge sign, operating amplitude, beam momentum and arrival phase remain required for an operational kick. Near-zero reference norms produce unavailable relative errors, not tuned denominators.

## Evidence and reproducibility

All paths below are relative to the scientific worktree, not this reporting clone:

- `docs/A5_INDEPENDENT_KICK_BENCHMARK_STATUS.md`: reconciled investigation report.
- `validation/stage_a5/r6a/direct_lorentz.py`, `r6a/CONVENTION_AND_SIGN_AUDIT.md`: independent force implementation and endpoint derivation.
- `validation/stage_a5/r6f/DECISION.json`, `R6F_SCIENTIFIC_REPORT.md`, `NESTED_CONVERGENCE_RESULTS.csv`, `MATHEMATICAL_CONVENTIONS.json`: acquisition/convergence scope and source provenance.
- `validation/stage_a5/r6i/REPLAY_VALIDATION.json`: SHA256 `eba2ef6459814b112e5eeecc8bc931985757427e08f99afa0a4c954d48b212ef`.
- `validation/stage_a5/r6j/DECISION.json`: SHA256 `b796ae2370b41ce4357d05b89d37e4f935459b2399b7db232f40c3331214047e`.
- `validation/stage_a5/r6j/SCIENTIFIC_REVIEW.json`: SHA256 `144ee962965c4910f0a83b93f5da6e600bc0a947c8f8539cf406748be9a116e2`; `NEXT_STAGE_HOLD.md` records the accepted Route A boundary.
- `validation/stage_a5/r6j/pytest_results.xml`: SHA256 `518226ff5d3842989bc5338593b4fbde9a2852616dda689f8b844b1bf04cce74` (30 tests). `RESULTS_PROVENANCE.json` records result-table hashes, which matched during this reporting reconciliation.
- `validation/stage_a5/r6j/COMPARISON_CONTRACT.md`, `FRM_INTERFACE_REQUEST.md`, `HISTORICAL_DECISION_SNAPSHOT.json`, `artifact_sha256.json`: interchange, dependency and retained evidence identities. Reproduction commands are in R6I/R6J `README.md`; they are documentation only here, not executed during reporting.

## Dependency, next action and reporting maintenance

FRM owns completion of **FRM-3B5 and FRM-4B** and a qualified numerical handover, including field/run/mesh hashes, integrated versus local derivative identity, exact coordinates/support/radius/order, frequency/phasor, endpoint/integration settings, common normalization and numerical uncertainty. A5 does not duplicate its CST acquisition, conditioning, mesh or longitudinal-qualification investigations. Operator-reported FRM-4A M0 ingestion PASS does not qualify its small transverse fields; M0 metadata is not independently hash-bound native provenance, and no M0 physical analysis was performed by A5.

**Next action: await a reviewed FRM handover.** Before new agreement metrics, verify source identity, coordinate compatibility, complex conventions, normalization, support eligibility and uncertainty/qualification scope. Retain incompatibilities as HOLD. No CST acquisition, radius optimisation, mesh analysis, new simulation or new physical benchmark claim is authorised. No programme-wide or other stream's status is changed by this report.

For future A5 scientific milestones, include reconciliation of this assigned status file in completion work under `docs/programme/REPORTING_PROTOCOL.md`: check repository status, safely synchronize a clean clone, prepare only this file and present its diff. Obtain explicit approval before committing or pushing; no automatic monitoring, synchronization or publication is implied.
