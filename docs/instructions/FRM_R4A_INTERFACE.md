# FRM R4A — read-only coefficient-interface clarification

**Instruction ID:** FRM-R4A-INTERFACE-20261117  
**Owner:** FRM  
**Scientific worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_FRM`  
**Reporting repository:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_reports`  
**Authority:** Read-only examination and an interface note only. No refitting, integration, new numerical sweep, CST operation, changes to sealed artifacts, or publication.

## Objective
Supply A5 with a verified, unambiguous interface for the existing FRM-4B1 M0 coefficient families required to evaluate the **linearised finite-window transverse voltage** `T0 + K_T @ [x,y]` at seven fitting radii. FRM does not own the Lorentz calculation or benchmark decision.

## Required review
Read the latest reporting protocol, FRM/A5 R3 statuses, FRM-4B1 source report, `validation/frm4b1/A5_HANDOVER.md`, `A5_HANDOVER.json`, coefficient/rank/support/normalisation manifests, and endpoint definitions. Inspect the underlying source files, not only summaries. Preserve original hashes and provenance qualifications.

## Interface questions to resolve
1. Identify **exact existing source paths, field names, schema, indices and units** for each radius 2.5, 3.75, 5, 6, 7.5, 9, 10 mm, orders 2/3/4, transverse spacing 0.5 mm and 801-plane trapezoid cases. Confirm actual availability and full rank; do not infer missing data.
2. Give the explicit mathematical definition of `T0` [V] and `K_T` [V/m], including endpoint electric contributions, phasor `exp(+iωt)`, transit phase, coordinate axes, frequency, β, z reference, H-to-B conversion, and any sign/normalisation conventions. Specify whether these quantities represent the full finite-window transverse voltage at the origin and its derivative or something else.
3. State precisely whether `T0` and `K_T` are **native-scale complex coefficients** and identify any independent on-axis `V_A` [V] normalisation. A5 must not use fitted `V0` as the normaliser or adjust phase/amplitude to improve agreement.
4. Confirm the intended linearisation `T(r)=T0+K_T r` is algebraically supported by the handover and distinguish it from a full order-3/4 finite-offset prediction. Explain any coefficient-order limitations, truncation terms, rank/support and numerical-instability qualifications.
5. Identify the five fixed evaluation positions `(0,0), (+/-2.5,0), (0,+/-2.5)` mm, their inclusion in all radius supports, and the actual M0 z grid. Report any incompatibility or ambiguity that would block the **limited** calculation.
6. Clarify that the 21 full-rank cases alone do not demonstrate stable derivatives or physical accuracy; preserve all adverse FRM-4B1 sensitivity evidence.

## Deliverable and handover
Create one new, **PROPOSED / NOT SEALED** file in the FRM scientific worktree, e.g. `validation/frm_r4a_interface/FRM_R4A_COEFFICIENT_INTERFACE.md`, with an exact machine-readable mapping table (CSV/JSON only if needed), source hashes, reproducibility pointers and explicit `READY FOR LIMITED NUMERICAL USE / BLOCKED` disposition. Supply its exact local path to A5. If any essential definition is unresolved, mark BLOCKED with the smallest missing evidence request. Do not invent or calculate coefficients.

No modification of `FRM_STATUS.md` is required for this small handover unless the author separately requests publication. No commits/pushes without separate explicit approval. Do not edit A5 or S2 files.
