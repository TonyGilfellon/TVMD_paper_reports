# FRM — fitting radius, mesh and longitudinal integration

**As of:** 2026-11-17T16:10:39Z (UTC; R3 completion verification, documentary only).
**Owner / decision ID:** FRM / FRM-NEXT-20261117-R3 (PROPOSED / NOT SEALED); existing seven-radius evidence and A5 read-only interface.
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_FRM`.
**Branch / HEAD:** `investigation/frm-radius-mesh` / `c7f0a6f9fb37a94127c440d0345e2528fc1d7f80`.
**Artifact state:** investigation reports/results are untracked local artifacts, not contained in this HEAD; source manifests and SHA-256 seals identify the evidence. Only new proposed documentary assessment files were created for this update; sealed scientific files/results were not changed.
**Current status:** **CONDITIONAL — LIMITED STABILITY** for FRM-4B1. Physical derivative accuracy and mesh convergence remain unestablished.

## R3 seven-radius support and interface — PROPOSED / NOT SEALED

Instruction `docs/instructions/FRM_NEXT.md` / **FRM-NEXT-20261117-R3** was assessed with the reporting protocol and current FRM/A5/S2 reports at reporting HEAD `c4278e26fc822c03340cd84d92c41a779e1b131a`. Scientific branch/HEAD above is unchanged. No new fit, integration, field-array analysis, interpolation, test run, Lorentz benchmark or CST operation occurred; all scientific decisions and provenance limitations are preserved.

Deliverables in the scientific FRM worktree, new namespace `validation/frm_next_20261117_r3/`:

- `FRM_R3_RADIUS_SUPPORT_AND_INTERFACE.md`: exact seven-radius support/rank transcription and A5 interface covering source paths/hashes, case IDs, SI complex coefficients, finite endpoints, normalization, map layout and rank failures. SHA-256 `96a2b886fb36d24ed88b0e6622fb3ca57977583f5e3f0ac8cb251ed09166b932`.
- `FRM_R3_OBSERVABLE_LIMITATIONS.md`: absolute/relative sensitivity interpretation, weak denominators, changed populations, observable distinctions and smallest future gate. SHA-256 `91e759bef97ae15f085a5653a1f1ed7c118845d51e00a55a9ca56fcb8d66d812`.
- `SOURCE_REVIEW.json`: documentary source/index identities; 110 indexed artifacts checked unchanged. No raw-field reparse/rehash or native-state qualification. New documents remain untracked, PROPOSED / NOT SEALED, not part of scientific HEAD.

**Support:** the 378 M0 configurations include all seven radii (2.5/3.75/5/6/7.5/9/10 mm), orders 2/3/4, density strides 1/2/4, 201/401/801 planes and both quadratures. 348 full-rank cases remain eligible for model-specific coefficients, not physical accuracy. All 30 failures remain: coarsest 2 mm lattice at R=2.5 mm (ranks 5/6, 5/10, 5/15) and R=3.75 mm cubic/quartic (8/10, 9/15), repeated across six z/rule choices. The rank table's additional nine historical fits are not M0 configurations.

**Interpretation:** absolute complex deltas retain their units; relative changes divide by the baseline magnitude and are unavailable below the recorded cancellation guard. At R=10 mm, finest-density 801 trapezoid quadratic versus quartic, existing Hxx absolute change is 1,177,816.4661 V/m² (relative 4.6791), Hxy 572,880.6415 V/m² (5.5583), and Kxx 43,229.5420 V/m (4.6791). These are sensitivities, not electromagnetic error bars. A local field Hessian [V/m³], integrated Vz Hessian [V/m²] and transverse-voltage Jacobian [V/m] cannot be interchanged. `Bx/By` coefficient labels denote endpoint B_end [V/m], not magnetic flux density. Direct VA remains distinct from fitted V0.

**Historical scope correction:** the R5-h2 fine-grid A5 cardinal-five 201-plane trapezoid discrepancy trend 1367.00 → 328.43 → 175.94 V at 2.5/3.75/5 mm was not a seven-radius M0 Lorentz benchmark. No historical 6/7.5/9/10 mm discrepancy is supplied or inferred. Seven-radius M0 coefficient sensitivity does not establish an optimal radius, physical convergence or isolated cylinder-radius effect.

**Disposition:** retain CONDITIONAL numerical evidence and physical benchmark HOLD. The smallest immediate next gate is documentary: define the intended observable, uncertainty/normalization and independently justified tolerance, and resolve existing source/convention gaps. Only a separately authorised same-M0 on-axis direct-integration versus endpoint-aware T check is a minimal later numerical candidate, as already proposed by A5; implementation closure/agreement would remain descriptive without physical qualification. H/K instability is not an on-axis dipole-error bound. No new seven-radius sweep, mesh study, CST acquisition or automatic FRM-4B2 is recommended. Existing evidence suffices for bounded descriptive-methodology discussion with caveats.

Reporting checkout contained an S2 edit and unrelated untracked publication helpers; no pull was made over them. Only FRM_STATUS.md is proposed here. R2 reporting publication at `e4f516df93552e30f03a5a77ec2dd8880f9d6d69` did not seal its scientific memo; this R3 delta awaits explicit approval before commit/push.

### R3 completion verification — 17 November 2026

All four R3 requirements are covered by the two deliverables: (1) all seven radii and 378 M0 configurations with the 348/30 eligibility split; (2) exact A5 read-only source/coefficient/support/endpoint/normalization interface; (3) absolute versus relative complex sensitivity, near-zero guards, population changes and distinct derivative units; (4) historical three-radius versus seven-radius scope and the smallest conditional future check. **R3 documentary assessment is complete; reporting approval remains pending.** This is not a new software, convergence or physical-validation PASS and does not seal the proposed scientific documents.

Fresh completion checks confirmed both R3 document hashes above, all 110 indexed artifacts unchanged, and all four external E/H inputs present at their recorded sizes. Raw field hashes/native state were not freshly requalified. Retained test XML was inspected: FRM-4B1 **14**, FRM-4A **20**, FRM-3B5 **8** tests, each with zero failures/errors/skips. These historical tests concern implementation/ingestion/identifiability; **no tests ran for R3**. No scientific output was changed or recomputed during this verification.

**R3 findings versus historical numbers:** R3 supplies documentary support/rank accounting, an exact interface and interpretation, not new Hessians or kick results. All numerical values in this section are transcribed from existing FRM-4B1/A5 evidence. Integrated derivative eligibility does not establish stability: the retained final decision remains **CONDITIONAL — LIMITED STABILITY**, with physical derivative/kick **HOLD**. Prior snapshot, load, candidate-preservation and ingestion decisions remain in their original scopes. Missing independently bound M0 native provenance, physical orientation/phasor certainty and calibrated error budgets remain unresolved.

**Read-only reproducibility:** from the scientific FRM worktree at the HEAD above, inspect the R3 instruction and both documents, then join `validation/frm4b1/RANK_SPECTRA.csv` and `COEFFICIENTS.csv` by `case_id`; use `SUPPORT_MEMBERSHIP.csv` for exact nodes and `SENSITIVITY_ALL_ORDERS_DENSITIES.csv` for existing complex deltas/guards. A metadata-only example is `Import-Csv validation/frm4b1/RANK_SPECTRA.csv | Where-Object { $_.dataset -eq 'M0' -and $_.planes -eq '801' -and $_.rule -eq 'trapezoid' } | Select-Object radius_mm,density_stride,degree,n,rank,columns`. Use `Get-FileHash -Algorithm SHA256` for the two R3 documents and compare prior artifact-index entries without refreshing them. Read existing JUnit `testsuite` attributes in `validation/frm4b1/pytest_results.xml`, `validation/frm4a/pytest_results.xml` and `validation/frm3b5/pytest_results.xml`; do not execute the historical fitting/integration/test commands merely to reproduce this documentary assessment. `SOURCE_REVIEW.json` remains the original R3 review-time snapshot, not a refreshed baseline.

The reporting tree now also contains A5/S2 owner edits and publication helpers; they are preserved. No pull is attempted over local changes, no other status/programme file is edited, and no commit/push is authorised by this completion verification.

## Proposed Route A decision assessment — FRM-NEXT-20261117-R2

**Recommendation:** retain FRM-4B1 **CONDITIONAL — LIMITED STABILITY** and physical integrated-derivative/kick **HOLD**. No new narrowly scoped physical PASS is justified without an independently supported observable-specific tolerance and qualified provenance. Existing bounded software/ingestion PASS decisions remain unchanged. No new scientific calculation, test run, fitting, integration, interpolation, CST operation or agreement metric was performed.

The direct on-axis integral **VA [V] is distinct from fitted V0 [V]**. VA has no transverse polynomial-identifiability issue, but lacks independently established physical accuracy. V0 is comparatively insensitive in the tested families (longitudinal 0.47–1.29 ppm, order 1.37–9.14 ppm, density 0.600–32.25 ppm); this does not validate H or K_T. Hxx/Hxy/Hyy, K_T and normal/skew quadrupole descriptors remain CONDITIONAL as model-specific numerical outputs and HOLD as stable physical quantities. Rank-deficient cases remain negative results; no scalar quadrupole or favorable-phase selection repairs them.

The source-linked memo and supporting review records are **PROPOSED / NOT SEALED** in the FRM scientific worktree:

- `docs/FRM_NEXT_20261117_R2_DECISION_MEMO.md`: observable qualification table, numerical-envelope definitions, A5 handover boundary and decision tree. SHA-256: `3eaa7a023e337d6c148592afa09915533625caee153795486fd837bc3771607d`.
- `validation/frm_next_20261117_r2/DEPENDENCY_MATRIX.csv`: 11 dependency rows covering radius, order, density, z/quadrature, source-state, endpoints, influence, normalization and weak-field diagnostics; existing numerical tables remain authoritative.
- `validation/frm_next_20261117_r2/NEXT_EVIDENCE_GATES.md`: precise questions, prerequisites, prospective measurable acceptance criteria and separate documentary/offline/native authorization boundaries.
- `validation/frm_next_20261117_r2/SOURCE_REVIEW.json` and `review_sources.py`: documentary audit of 110 indexed artifacts (44 FRM-4B1, 29 FRM-4A, 35 FRM-3B5, two provenance); zero missing files/hash mismatches. All four external raw E/H inputs exist at recorded sizes. Raw hashes were not freshly recomputed; no native-state certification is inferred. Ten reviewed scientific source documents remain untracked. The assessment is not contained in scientific HEAD.

**Smallest next gate:** author review of the intended physical claim, normalization and independently justified componentwise accuracy budget, followed by an existing-document lineage/convention check. Existing evidence suffices for a bounded descriptive-methodology discussion without duplicate calculations. If a physical claim is required, unresolved provenance or failure of the predeclared budget retains HOLD; do not tune radius/tolerance against the reference. A new discrete-operator analysis, evaluator acquisition or controlled mesh study would each need its own discriminating question and separate authorization. No automatic FRM-4B2 is proposed.

**A5 interface:** source paths/hashes, actual coordinates/supports, rank/spectra, integrated complex g/H, endpoint B_end/J_end, T/K, VA normalization and deterministic sensitivity envelopes can be handed over conditionally. M0 native-state/mesh/field-buffer hash binding, independently repeated acquisition, physical orientation/time-phasor certainty, verified-J energy scale and calibrated physical error bounds cannot be represented as established. R5 snapshot hashes do not supply missing M0 lineage. A5's physical benchmark HOLD and S2's separate editorial/physical gates remain unchanged.

**Reporting reconciliation:** published FRM/A5/S2 reports were read at reporting HEAD `672870ab37c5f3a08531e865d943de4a7a7053be`, matching remote main by a read-only check. Two unrelated untracked publishing helpers prevented a clean-tree pull; they were left untouched, and the assigned FRM file was checked unchanged before this edit. The R2 status delta was subsequently published at e4f516df93552e30f03a5a77ec2dd8880f9d6d69; the R2 scientific memo remains proposed/unsealed. The R3 status delta above remains uncommitted pending approval. Other streams' reports and programme files are outside this edit's scope.

## Latest scope and findings

FRM-4B1 is complete. It assessed the validated M0 R10-h2.0 integrated complex voltage maps at circular radii 2.5, 3.75, 5, 6, 7.5, 9 and 10 mm; polynomial orders 2/3/4; nested 201/401/801 longitudinal planes; actual-coordinate trapezoidal/Simpson quadrature; and axis-preserving transverse spacings 0.5/1/2 mm. Of 378 M0 combinations, 348 were full rank and 30 rank deficient. Rank-deficient cases have no published unique derivative coefficients.

- For the finest transverse density and 801-plane trapezoidal quadratic baselines, fitted V0 longitudinal sensitivity envelopes across 201/401 planes were 0.47–1.29 ppm across radii. Hxx/Hxy/Hyy relative envelopes were respectively 8.48–68.55%, 32.91–310.03% and 15.19–82.95%. Denominators are each baseline complex coefficient magnitude; absolute complex changes and near-zero guards are retained.
- On identical supports, quadratic-to-quartic changes were 211–1215% for Hxx, 63.5–1230% for Hxy and 293–1279% for Hyy. Quadratic/cubic Hessian agreement follows parity on symmetric supports and is not independent validation. Lower residuals do not establish physical accuracy.
- Transverse-density and radius-population changes remain substantial. No Hessian, quadrupole or endpoint-corrected TVMD Jacobian family demonstrated joint stability across the declared variations. No externally justified observable-specific tolerance was available; no universal percentage threshold or radius optimum was invented.
- Finite-window endpoints were retained over z = −0.23060958 to +1.2660479 m. H refers to integrated longitudinal-voltage derivatives [V/m²]; K_T refers to the endpoint-corrected transverse-voltage Jacobian [V/m]. These are distinct from local field Hessians [V/m³].
- A separate temporary weak-field perturbation altered up to approximately 32.83 V and 32.60 V in individual transverse-voltage-map components. It left Ez and endpoint fields unchanged, so TVMD Hessians/Jacobians were unchanged by construction. This is a diagnostic, not a field correction or calibrated uncertainty.
- The bounded R5-h2.0 comparison used 88,641 exact common xyz positions and common circles through 5 mm. Native and independently on-axis-VA-normalized coefficients are separate; no fitted phase/amplitude registration or interpolation occurred. Remaining configuration/recovery confounds prevent an isolated refinement-radius or accuracy claim.

## Preserved decisions and unresolved evidence

- **FRM-2:** radius, sampling and polynomial-order diagnostics remain valid as scoped numerical evidence; decreasing TVMD–direct discrepancy did not establish coefficient or physical convergence. Historical A5 acceptance decisions are unchanged.
- **FRM-3B2:** verified private reference snapshot preserved: 591 files, 22 companion directories, 13,292,988,684 bytes; source pre/post and private identity checks passed. This does not qualify subsequent CST loading.
- **FRM-3B3:** **HOLD — PRIVATE LOAD NOT QUALIFIED** remains: independent Design Environment startup timed out for PID 15780; private project opening and saved-result access were not established. No fresh process inspection was made for this report; current PID/session state is unknown. Native-operation suspension remains applicable unless separately released.
- **FRM-3B4 candidate evidence:** bounded acquisition-preservation qualification is not full filesystem identity: Model.lok was inaccessible and post-acquisition GUI confirmation was not supplied. No later numerical result upgrades this qualification.
- **FRM-3B5:** **CONDITIONAL — LIMITED IDENTIFIABILITY**. 18/45 geometry/order cases were full rank. Thirteen-point supports identify quadratic/cubic fits; 17-point supports identify quadratic/cubic/quartic fits. Ez quadratic-to-quartic Hessian relative Frobenius changes were 3.52–898.54% across the three planes. Exact repeats do not establish derivative stability. These are local field derivatives, not integrated kick coefficients.
- **FRM-4A:** sealed **PASS — M0 MAPS VALIDATED FOR FRM ANALYSIS**, ingestion only. The paired 41×41×801 maps are complete and coordinate-consistent; historical 201-plane z coordinates are exactly embedded. Weak transverse-field/recovery qualifications remain open; ingestion PASS is not physical validation.

## M0 provenance and conventions

Immutable source directory: `E:\HOMmix_full_cavity_coupler\data\2mm_on_axis_mesh_refinement_10mm_radiuis`.

| Input | SHA-256 |
|---|---|
| `M0_R10_h2mm_E_41x41x801.txt` | `26d09744780fc2ed1190cd112ddfce6090bafd4d71ed5eb7886b9da4267945f4` |
| `M0_R10_h2mm_H_41x41x801.txt` | `a1330f09fd35e169ae85243e43a6ee8c2225406b0486b0a95d130edd57ce1ba7` |

Operator-supplied/GUI-confirmed M0 Mode 9: frequency 1.2999834467254 GHz; 2,571,481 tetrahedra; lossy-E Q 4.00149930514472e7; beta=1 R/Q 1035.2132090001 Ω; total energy 0.99920266915905, unit presumed J. Settings: tetrahedral, General (Lossy), nine modes above 1.15 GHz, ports enabled, **adaptive tetrahedral refinement disabled**, accuracy 1e−6, minimum Q 1.0, thermal losses enabled, second-order solver. Scaling was reported satisfactory. These claims are not independently hash-bound native-state evidence; no energy normalization follows from them.

The numerical convention follows A5 R6J: exp(+iωt), positive transit phase, β=1, straight +z, z_ref=0, E [V/m], H [A/m], B=μ0H. Physical handedness/FPC orientation and time-phasor interpretation are not independently established by the export headers; physical interpretation remains provisional. Native scale is primary. Optional per-VA columns divide by directly integrated on-axis VA independently of fitting radius, not fitted V0. Diagnostic envelopes are not statistical confidence intervals or electromagnetic error bounds.

## Evidence and software validation

Paths below are relative to the scientific FRM worktree, not this reporting repository:

- `docs/FRM_4B1_M0_NUMERICAL_STABILITY_REPORT.md`; `validation/frm4b1/{SPECIFICATION.md,MANIFEST.json,DECISION.json,ARTIFACT_SHA256.json}`.
- Complex coefficient/support/spectrum/sensitivity/influence tables and figures: `validation/frm4b1/`. Compact A5 interface: `A5_HANDOVER.md` and `A5_HANDOVER.json` there.
- Earlier sources: `docs/FRM_3B5_LOCAL_DERIVATIVE_REPORT.md`, `docs/FRM_4A_M0_FIELD_VALIDATION_REPORT.md`, `docs/FRM_4A_OPERATOR_PROVENANCE_SUPPLEMENT.md`, `docs/FRM_NUMERICAL_EVIDENCE_MILESTONE_2.md`; associated sealed validation folders.
- FRM-4B1 report SHA-256: `1da3efefab1db4323ad5d2481c49e6eff11987ff3aef3484b9e0242b9bb4136c`.
- FRM-4B1 artifact-index SHA-256: `c1db6685bcad0dd7e60cf76435c4b4f0cdec51fc2b965c5b0d29a71ff443f1ec`.

Recorded FRM-4B1 validation: **14 tests passed**, one dependency deprecation warning; all-M0-trajectory trapezoid agreement with the tested core; 44 sealed artifacts checked without mismatches; four raw source E/H files and earlier seals verified unchanged. Earlier scoped tests: FRM-3B5 eight passed; FRM-4A twenty passed. These are software/ingestion validations, not physical-validation PASS decisions. No scientific calculation or test was rerun for this reporting task.

Reproducibility: use `..\TVMD_paper\.venv\Scripts\python.exe -B`, with FRM root and `src` on PYTHONPATH. Modules: `validation.frm4b1.analyse`, then `validation.frm4b1.summarize`; focused tests: `-m pytest -q -p no:cacheprovider validation/frm4b1/test_analysis.py`. Follow `validation/frm4b1/README.md` for a separate output location; do not overwrite sealed outputs.

## Dependencies, next actions and reporting control

1. Scientific review of FRM-4B1 is the current gate. No automatic FRM-4B2 progression, new mesh solve or acquisition is authorised by this report.
2. Any follow-up must specify an observable and justified stability tolerance, and address polynomial/population dependence and longitudinal field-recovery sensitivity. A larger radius or better agreement alone is insufficient.
3. Matched R5-h2.0 51-point reference acquisition remains absent and requires separate approval. Candidate R5-h1.75 has no exact common xyz positions with the M0 lattice; do not silently interpolate. Multiple local mesh controls differ between states.
4. A5 owns the independent physical coupler-kick benchmark, excitation/phase/impulse interpretation and force agreement. FRM supplies source-qualified numerical families and limitations only; no A5 benchmark or radius optimisation was performed.
5. Future FRM milestone completion includes reconciling this assigned status file under `docs/programme/REPORTING_PROTOCOL.md`, reviewing the diff, and obtaining explicit approval before commit/push. No continuous monitoring or automatic publication is claimed.

**Baseline reconciliation:** the coordinator's historical report is superseded only as a current status summary: FRM-4B1 is complete rather than pending, and the ambiguous adaptive-refinement baseline is corrected to operator-confirmed disabled. All sealed historical decisions, HOLDs, CONDITIONAL findings and provenance limitations remain preserved. That historical summary was subsequently committed in the reporting repository; R2 reporting was published at e4f516df93552e30f03a5a77ec2dd8880f9d6d69 without sealing the scientific memo; the FRM-NEXT-20261117-R3 delta above remains proposed and unpublished.
