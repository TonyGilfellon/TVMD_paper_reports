# A5 — independent full-cavity transverse-kick benchmark

**As of:** 2026-11-17 12:52:41 UTC (FRM-4B1 compatibility assessment; no new physical kick calculation).  
**Investigation owner / assigned file:** A5 / `docs/investigations/A5_STATUS.md`.  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_A5`.  
**Branch / HEAD:** `validation/m1-stage-a5` / `c7f0a6f9fb37a94127c440d0345e2528fc1d7f80`.  
**Decision ID:** `A5-R6K-FRM4B1-COMPATIBILITY-PROPOSED`, instruction `A5-NEXT-20261117-R2`; **PROPOSED / NOT SEALED**. Earlier accepted R6I/R6J review remains unchanged.  
**Current status:** **PHYSICAL BENCHMARK HOLD**; computational validation **PASS within targeted scopes**; comparison infrastructure **CONDITIONAL** on a reviewed, compatible FRM handover.

## Source status and reconciliation

The 17 November coordinator baseline has been reconciled against retained A5 reports, decision records, result tables and test XML. Its 432-voltage replay, 30-test result and unresolved longitudinal sensitivity are supported. The baseline's proposed published LCLS-II comparison is corrected to the later accepted Route A scope: **full-cavity transverse voltage/kick is the provisional primary independent observable**. It is not a coupler-only coefficient. Any later coupler-only or published comparison requires a separately justified physical definition and compatible source; none is currently authorised. The baseline's unspecified “six-node agreement” is not used as evidence of physical convergence.

HEAD is the shared earlier Stage 2A analytic-validation commit, not a commit sealing the current investigation. The latest three scientific commits are `c7f0a6f9fb37a94127c440d0345e2528fc1d7f80` (Stage 2A pillbox/finite-boundary references), `8ae610404e422c05864d19742be7b0b7f7e54568` (Stage 1 voltage/coefficient observables), and `935eba1845994394fe78ad5f45f91f8cc0722b95` (decision numbering). The current status document and `validation/stage_a5/` evidence, including R6I/R6J, are **untracked working-tree evidence**, not committed/published scientific results. Their local paths and hashes below provide the current provenance. The R6K compatibility assessment is also untracked and PROPOSED / NOT SEALED. No new scientific commit, kick calculation or test execution was performed for this update.

## Accepted scope and scientific limits

| Scope | Decision and evidence |
|---|---|
| Independent Lorentz replay | **PASS, computational:** R6I reproduced 16 retained R6F cases / 432 complex voltages bit-for-bit, without TVMD fitting. Shared simulated fields mean this is formulation/reproducibility independence, not an independently certified electromagnetic reference. |
| Analytic and diagnostic implementation | **PASS, targeted:** retained R6J XML reports 30 tests, zero failures/errors/skips. Tests cover analytic pillbox/oblique waves, magnetic signs, H/B conversion, signed impulse, finite endpoints, phase-origin covariance and diagnostic interfaces. This is not a full-suite or physical-field PASS. Earlier stages retain the inherited 27-source CRLF-only raw-hash failure; no baseline was refreshed. |
| Physical reference convergence | **HOLD:** complex direct maps and TVMD maps/matrices did not stabilize on the retained longitudinal grids. No convergence order, absolute-error bound or mesh limit is established. |
| Radius/agreement interpretation | **Descriptive sensitivity accepted; validation HOLD:** no optimal radius selected. Minimizing benchmark disagreement on the same data would be calibration, not independent validation. |
| Existing FRM-4B1 handover | **HOLD for a qualified next physical comparison.** Accept only for source-qualified numerical interface inspection and next-check preparation. Integrated coefficients and conventions are supplied, but physical source binding, transverse accuracy/uncertainty and joint stability remain unqualified. No new agreement metric was calculated. |
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

## FRM-4B1 compatibility gate - PROPOSED / NOT SEALED

The existing handover has now been inspected directly in FRM, read-only, rather than treated as still absent. A5 R6K verifies **138 source records**, including FRM-4B1's index, preceding seals, four referenced raw E/H files and A5 contract sources; expected hashes match and sources remained unchanged during those checks. FRM-4B1's 14 recorded tests and A5's 432-voltage replay/30 tests remain software/computational evidence, not physical-validation PASSes. No source code from FRM was imported or executed.

The [local assessment source](C:/Users/zup98752/PycharmProjects/TVMD_paper_A5/validation/stage_a5/r6k/HANDOVER_ASSESSMENT.md) and 29-field MATCH/MISMATCH/MISSING/UNQUALIFIED matrix distinguish compatibility from qualification. Important results:

- **Resolved interface gaps:** explicit integrated g/H, electric endpoint B_end/J_end, endpoint-corrected T/K, rank/support membership, source hashes, units and independent per-grid/rule VA normalization. No rank-deficient case publishes unique coefficients: 348/378 M0 cases full rank; 30 deficient. The manifest's 387/357 totals additionally include nine historical cases.
- **Coordinates:** all nine A5 x/y positions and finite endpoints match M0 exactly; **201/201** longitudinal values match the historical R6F decimation. At 401/801 planes only **251/401** and **351/801** match binary64, with maximum coordinate differences **5.000000014e-8 m** / **7.499999999e-8 m**. No fields were interpolated and no tolerance was invented. R=2.5 mm circle contains cardinal five, not all nine positions; R>=3.75 mm contains nine, without implying any radius is numerically/physically optimal.
- **Different state:** M0 has operator-reported 2,571,481 tetrahedra and f=1.2999834467254 GHz, not the historical A5 reference's state/frequency. Native-state binding, physical orientation/handedness/FPC mapping and source-bound peak/time-phasor interpretation remain unqualified. Headers/byte hashes alone do not resolve them.
- **Numerical limit remains:** FRM's decision is CONDITIONAL - LIMITED STABILITY; no integrated H/quadrupole/K family is jointly stable. Recorded longitudinal Hxx/Hxy/Hyy sensitivity ranges are 8.48-68.55% / 32.91-310.03% / 15.19-82.95% against respective baseline complex magnitudes, with near-zero guards. These deterministic envelopes are not physical/statistical uncertainty bounds. No M0 1601 evidence exists; FRM-4B1 does not clear A5's historical 8.84%/13.19% direct-map changes or turn them into M0 error bars.

**Proposed gate: HOLD** for any qualified independent physical full-cavity voltage/kick comparison. The handover is accepted for the specifically limited use of numerical-interface inspection/protocol preparation only. It does not authorise new metrics. Prior physical HOLDs and scoped computational PASS/CONDITIONAL findings remain unchanged; no sealed decision is superseded.

New source paths relative to A5: `validation/stage_a5/r6k/{HANDOVER_ASSESSMENT.md,PROPOSED_HANDOVER_DECISION.json,COMPATIBILITY_MATRIX.md,COMPATIBILITY_MATRIX.csv,MINIMUM_NEXT_EVIDENCE_REQUEST.md,SOURCE_VERIFICATION.json,COORDINATE_COMPATIBILITY.json,HANDOVER_STRUCTURE.json,PROVENANCE.json}`. Reproduce metadata/hash/coordinate checks only with `python -B validation/stage_a5/r6k/assess_sources.py` and `build_matrix.py`; these neither integrate fields nor fit coefficients. FRM handover JSON hash is `ebb7e6ca1ba8f7ef7cfca06bc695cd514d45b868fa2496a09f7d86bc76b9540d`; FRM-4B1 artifact-index hash is `c1db6685bcad0dd7e60cf76435c4b4f0cdec51fc2b965c5b0d29a71ff443f1ec`. The raw E/H hashes and exact cited sources are retained in the A5 verification record.

## Dependency, next action and reporting maintenance

FRM-3B5 and FRM-4B1 numerical evidence is now available, with its LIMITED IDENTIFIABILITY / LIMITED STABILITY qualifications retained. A5 requests FRM/operator review of source/state/physical conventions and existing observable-specific qualification for independent on-axis L versus endpoint-aware T, not a duplicate mesh/conditioning study. The minimal later check would independently integrate the raw **same M0 state** on axis, first verify electric/magnetic implementation closure, then compare the complete complex native/VA-normalized voltage against the predeclared existing eligible coefficient family. It is only a proposed check: no computation is authorised by this report. H/K instability is not itself an on-axis dipole-error estimate.

Before any later physical comparison, require compatible source/coordinates/conventions, qualified uncertainty for both observables and a justified, predeclared observable-specific tolerance; do not choose radius, phase or amplitude to improve agreement. If no tolerance/qualification exists, any separately authorised discrepancy must remain descriptive, not accuracy PASS. No new native operation is automatically requested to fill missing evidence. Published LCLS-II/coupler-only comparison remains undefined without a justified baseline/excitation, geometry/orientation/reference-plane and compatible source; it remains outside the approved stage. No new kick metric, field manipulation, CST action, fit, mesh analysis, FRM/S2 change, scientific seal refresh or commit occurred.

The reporting clone initially contained unrelated untracked publishing helpers, so no pull was attempted into a dirty tree. A concurrent FRM_STATUS.md edit appeared during assessment and was left untouched. Only this assigned A5 status file is proposed for editing; the scientific decision is not sealed and publication awaits explicit approval.

For future A5 scientific milestones, include reconciliation of this assigned status file in completion work under `docs/programme/REPORTING_PROTOCOL.md`: check repository status, safely synchronize a clean clone, prepare only this file and present its diff. Obtain explicit approval before committing or pushing; no automatic monitoring, synchronization or publication is implied.
