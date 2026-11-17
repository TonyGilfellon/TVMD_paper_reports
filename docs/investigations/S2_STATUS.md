# S2 — catalogue correctness and Route A evidence

**As of:** 2026-11-17T11:17:07Z (UTC; documentary reconciliation).

**Decision ID:** S2-REPORT-20261117-R1 — proposed owner reconciliation; awaiting approval, not committed/published.

**Scientific worktree (S):** `C:\Users\zup98752\PycharmProjects\TVMD_paper_S2_20261115`.

**Branch / current commit:** `s2/catalogue-preflight-20261115` / `12a52d750340a4c9c9e59da7c4aa4a4055e5e94c`.

**Inherited evidence root (O):** `C:\Users\zup98752\PycharmProjects\TVMD_paper`.

**Overall:** bounded software ACCEPT/PASS; retrospective descriptive import PASS; native-reference CONDITIONAL; independent physical validation and further execution HOLD. Existing evidence supports a bounded comparative-methodology argument without another B1 calculation. Distinct novelty, practical consequence and editorial adequacy remain unresolved.

## Reconciliation of the historical baseline

This prospectively supersedes the coordinator's conversation-derived baseline, not sealed scientific decisions. Its historical 749-test Stage 2 PASS remains valid for that suite; it was not catalogue validation or a physical-accuracy result.

Reduced radial-model preparation and easier cross-geometry automation are hypotheses, not measured benefits. Complete Cartesian and complete polar polynomial spaces are equivalent and may share automation. Fourier methods can recover normal/skew quadrupoles; restricted harmonic models are not all Fourier methods. Correctly informed radial models often perform better. RouteD remains HOLD and W24/W25 investigations are closed for this revision; no automatic extension is recommended if RouteA novelty remains insufficient.

## Milestones and precise acceptance scope

All numerical/test results below are attributed captured evidence, NOT rerun during this reporting task.

| Decision / milestone | Result | Boundary |
|---|---|---|
|Stage1/Stage2 prior-art studies|Stage 2 historical 749 tests passed; complex recovery, radius/support/noise, contamination and endpoint controls|Analytical/synthetic finite designs, not full published joint-method reproduction or physical native accuracy.|
|S2 closure,16 November|230 passed:84 S2 including34 closure cases plus146 selected algebra regressions; no skips/errors/failures. Schema 0.1.1 clarifies model-dependent origins while legacy 0.1.0 records survive.|Bounded contract/conversion/provenance/reliability software ACCEPT. Closure commit `3abfd996557f9f0b9aba59958769af2687fc16a4`; no calibrated physical accuracy.|
|S3.2B import,16 November|15 unique records: modes1/5/6/14/15 x H4/T4/P4,R20mm,trap121. Exact source-row/value/round-trip fidelity.265 passed:35 new+84 S2+146 regressions; no skips/errors/failures.|Descriptive unchanged-value retrospective import only; source/calibration/reference uncertainty remains explicit. No refit, integration or CST.|
|S3.2B Git preservation|58 explicit additions preserved at current commit;57 accepted file hashes matched delivery; committed blobs matched working bytes.|Later preservation supersedes import-time 'untracked/no commit' status only. Historical reports/values unchanged; subsequent documentary packages remain untracked/hash-bound, not contained in this commit.|
|D1 radial-prior investigation|240 analytical checks and pilot PASS; exact finite-training-design risk accepted. R10mm/N197/golden/IID0.1% joint RMS risks: T0.001413584; P0.0006437341 at correct prior,0.006106142 at 10% high prior.|Fixed dimensionless scales and stipulated covariance, not measured radial-scale uncertainty. D01 and 949 validation/895 projection last-change failures remain; three raw-sign reversals are equivalent-basis roundoff.|
|E0/E1/E3 native comparison|Five modes,R16/20/24mm with 97/145/213 native samples, three saved quadratures;240 experiment fits.55 focused/related tests and310 staged checks passed. P smaller conditional joint error in 59/60 T/P pairs; exception retained.|Source-calibrated ideal reference, not independent true CST derivatives. H4/P4=9complex DOF,T4=15; correct kappa is extra information.|
|E2 covariance|0/0.1/1% stipulated circular complex Gaussian voltage noise;405 risk rows;92 strict pair/observable/condition ordering reversals,7 joint.|Exact conditional moments, not measured FEM noise. Pair-order reversals need not change the global minimum-risk model.|
|B1 gap assessment,17 November|Existing ideal derivatives, analytical/native fits and signed window/frequency/quadrature controls already cover the bounded comparison. No new analytical/software experiment recommended.|True FEM/export/quadrature bounds and physical kicks unresolved. Optional TM010 mesh study requires separately qualified source/budget/permission; DecisionsA/B remain HOLD.|
|Evidence/figure audit,17 November|17 claim dispositions,six-section plan,25-group/30-atomic reviewer mapping.34 PNG/PDF assets match accepted hashes;7 PNGs viewed;27 bounded source/document files unchanged. Proposed 2 core evidence figures+3tables.|No new result/figure/manuscript. Native plot needs final-size legibility review. Scientific coherence is not proof of novelty, practical utility or editorial acceptance.|

## Native metrics, source ancestry and adverse evidence

The ideal reference is independent of competing local fits but uses global phase/scale/orientation projection from the same native source. Ideal own-frequency transit differs from measured-frequency native integration; saved native endpoints are `[-0.057652396,+0.057652396] m`. Legacy analytical radius `0.08826348295016158 m` and candidate parameter `88.263483 mm` have different literals; this alone is not proof of a different physical geometry. Endpoint/frequency differences are explicitly budgeted. Exact historical export-to-solution binding and absolute calibration remain conditional. Physical mode14 is TM210a despite raw TM210b labeling.

E1's dimensionless joint score weights `(V,Vx,Vy,Vxx,Vxy,Vyy)` by `(1,R0,R0,R0^2,R0^2,R0^2)/Vref`, with R0=20mm and each mode's frozen ideal RMS. It includes V and counts Vxy once. Separate gradient error is V/m; Hessian Frobenius error is V/m^2 with weight2 on squared cross-derivative error. Do not pool these with older leading-vector percentages. Full complex/nominal-zero components remain available.

Native-minus-ideal discrepancy combines possible FEM, export interpolation/serialization, calibration, geometry, frequency/window/quadrature effects; it is not isolated FEM error. Frequency agreement is not derivative convergence. Lower reconstruction residual may coexist with worse derivatives; 10/45 higher-order comparisons increased error. Retain all quadrature sensitivities, rank/support failures and contrary cases. No new physical error bar, threshold, workflow-saving or superiority claim is supplied.

## Authoritative evidence and reproducibility

Paths below are relative to S unless prefixed O. Local scientific records remain authoritative; this report does not replace them.

- `validation/tvmd_catalogue_s2_closure_20261116/TVMD_S2_CLOSURE_DECISION.md`, test matrix, `verification/attempt_03/EXECUTION.json` and JUnit:230-test closure and full command/environment/guard.
- `validation/tvmd_catalogue_s3_2b_import_20261116/TVMD_S3_2B_DECISION.md`, `SOURCE_TO_RECORD_MAPPING.csv`, `IMPORT_MANIFEST.json`, `RECORD_VALIDATION.json`, `ROUNDTRIP_VERIFICATION.json`, `verification/attempt_01/EXECUTION.json`, stdout and `junit.xml`:265-test run and 15-record fidelity.
- `validation/tvmd_catalogue_s3_2b_git_closure_20261116/PRESERVATION_DECISION.md`, `COMMIT_VERIFICATION.json`, `POSTCOMMIT_PRESERVATION.json`: later 58-file preservation commit. The import decision's old HEAD/untracked wording is a retained snapshot, not current Git status.
- O/`benchmarks/tvmd_prior_art/stage2/results/SCIENTIFIC_REVIEW.md`, `PRIORITY0_AUDIT.md`, regression transcript and saved CSVs:749-test suite, negative designs and analytical force limits. Complete published Riemann joint comparison is not reproduced; its separate convention gate remains.
- O/`validation/route_a_radial_prior_investigation_20261113/SCIENTIFIC_REVIEW.md`, `MATHEMATICAL_VERIFICATION.md`, `results/FIXED_SLICE_RISK.csv`: authoritative D1 interpretation and exact finite-design risk.
- O/`validation/route_a_pillbox_matched_comparison_20261113/REPORT.md`, `SOURCE_AND_REPRODUCTION_REPORT.md`, `FROZEN_INPUTS.json`, `results/RESULTS.csv`, `COMPONENTS.csv`, `QUADRATURE_COMPONENTS.csv`: matched native/ideal outputs and signed saved-rule sensitivity.
- O/`validation/route_a_pillbox_e2_covariance_20261113/REPORT.md`, `DECISION.md`, `results/RISK_RESULTS.csv`, `COMPONENT_RISKS.csv`: conditional covariance/risk.
- `validation/route_a_b1_scientific_gap_assessment_20261117/B1_SCIENTIFIC_GAP_MATRIX.md`, `FINAL_RECOMMENDATION.md`, `PRESERVATION.json`: exact source/convention gaps and no duplicate experiment recommendation.
- `validation/route_a_evidence_figure_audit_20261117/`: claim/section/figure/reviewer/readiness documents; `FIGURE_PROVENANCE_INVENTORY.json`, `PRESERVATION.json`, `OUTPUT_SHA256.json` bind inspected sources/graphics. These documentary files are currently untracked, not part of current HEAD.

Reproduction commands are preserved verbatim as `command` arrays with `cwd`, `env`, source hashes and output paths in the two EXECUTION.json files above. The S3.2B capture uses Python3.10.11 and `python.exe -B -m pytest -q -p no:cacheprovider` with the explicit full test/node list; preserve its isolated PYTHONPATH/source guard, PYTEST_DISABLE_PLUGIN_AUTOLOAD=1, PYTHONNOUSERSITE=1 and single-thread BLAS environment. No abbreviated test invocation is asserted to reproduce 265 tests. A repeat needs a fresh output namespace and separate authority; those records do not authorise rerunning or overwriting final packages. No tests ran for this update.

Current bounded documentary SHA-256 anchors, checked during reconciliation:

- S3.2B `OUTPUT_SHA256.json`: `4615f6710669f889057fe89f0235900a26474794a84a3b855ba41b0cf8823f43`.
- B1 `FINAL_RECOMMENDATION.md`: `923e180f960aba56420a3298155a8d8189e064f0c2e504a29574cbe4df92196e`.
- Figure audit `ROUTE_A_READINESS_ASSESSMENT.md`: `5a5a4786d8884dfcb6575bc40e81dfb9c374adb6f03e8ffa2622fa6286880f53`.

Prior-art boundaries: [Riemann, Neumann and Weis, LINAC2012 MOPB066](https://proceedings.jacow.org/LINAC2012/papers/mopb066.pdf) is the source of the published comparator, whose full joint method is not reproduced here; [Wroe, Sheehy and Apsimon, PRAB25,062001(2022)](https://doi.org/10.1103/PhysRevAccelBeams.25.062001) documents established multipolar/Bessel field representations. These citations do not resolve the separate published-method convention or novelty gates.

These checks do not freshly verify scientific arrays/physical archives. No datasets, projects, credentials or large exports are copied into reporting.

## Dependencies, next action and retained gates

1. Author/co-author review of bounded contribution, six-section scope, all negative results and conceptual coupler treatment. Novelty and consequential utility remain open; software correctness does not resolve them.
2. No additional B1 analytical calculation recommended. Do not duplicate D1/noise/fitting/quadrature studies. Stronger native/physical claims require separately justified source/reference/error-budget evidence; no automatic CST, A5/FPC, RouteD or W24/W25 restart.
3. E02-B is already confirmed: measured comparative advantage is no longer the author's mandatory pre-drafting prerequisite. Unmeasured advantage claims stay excluded. The last source-verified editorial assessment did not establish complete editable assets or editorial adequacy; this task did not recover them. Actual drafting/figure/response work remains unauthorised.
4. Retain Stage2B native-source qualification; D01 HOLD; 949/895 continuum limits; original pillbox pilot FAIL; R5-B/R5-C HOLD; B12 STOP; B17 suspension; reduced RouteD convention HOLD; W24-2 HOLD; W25 numerical/TVMD HOLD; P1 scientific threshold/execution gates. No physical gate is released by software/import acceptance.
5. Future S2 milestones: manually reconcile this assigned report against new sealed evidence at completion; synchronise only safely with a clean reporting tree; preserve historical decisions; show report/diff and obtain approval before committing or pushing. No continuous monitoring/automatic publication is claimed. Other investigations/programme files are outside S2 ownership.

**Reporting state:** clean reporting checkout was synchronised with `git pull --ff-only origin main` (already up to date). A5/FRM owner edits then appeared; the pre-edit check stopped, confirmed S2 unchanged, and reconciled ownership without pulling over or modifying either report. Only this assigned S2 file is proposed here. No scientific worktree edits/calculations/tests, no staging, commit or push. **STOP pending author approval.**
