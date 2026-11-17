# FRM R3 — seven-radius support and numerical interpretation
**ID:** FRM-NEXT-20261117-R3
**Worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_FRM`
**Assigned status:** `docs/investigations/FRM_STATUS.md`
**Authority:** Read-only; no new fitting/integration/CST.

## Common protocol
Read the reporting repository `docs/programme/REPORTING_PROTOCOL.md` and latest FRM/A5/S2 reports. Inspect primary scientific artifacts, preserve sealed decisions, hashes, HOLDs and provenance qualifications. Use a new PROPOSED / NOT SEALED output namespace. Do not edit other streams or programme files. Propose only your assigned investigation-status update; show diff and wait for explicit author approval before any commit/push. Record branch/HEAD, inputs, units, metrics, commands and limitations. No CST operations or new field exports are authorised.

## Tasks
1. Inspect FRM-4B1's 378 configurations, rank/support tables, existing complex coefficients and A5 handover for 2.5, 3.75, 5, 6, 7.5, 9 and 10 mm.
2. Provide A5 an exact read-only interface guide: source paths/hashes, units, complex coefficients, endpoint terms, normalization, coordinate support, polynomial orders and rank failures.
3. Explain existing absolute versus relative Hessian/Jacobian sensitivity, including near-zero denominators and model-support changes; distinguish field Hessians, integrated Hessians and transverse-voltage Jacobians.
4. Clarify that the historical 2.5–5 mm A5 discrepancy trend was not a seven-radius FRM Lorentz benchmark. Identify only the smallest discriminating future check, if evidence supports one.

## Deliverables
`FRM_R3_RADIUS_SUPPORT_AND_INTERFACE.md`, `FRM_R3_OBSERVABLE_LIMITATIONS.md`, and proposed diff to **only** `FRM_STATUS.md`. No new calculations, commit or push.
