# FRM — fitting radius, mesh and longitudinal integration

**Baseline:** 17 November 2026, historical handover (not independently re-audited).  
**Worktree:** `C:\Users\zup98752\PycharmProjects\TVMD_paper_FRM`; branch `investigation/frm-radius-mesh`.  
**Status:** **OPEN — numerical derivative accuracy not established**.

## Evidence reported
- FRM-3B5: **CONDITIONAL / LIMITED IDENTIFIABILITY**. Quadratic and cubic fits full-rank on 13- and 17-node supports; quartic full-rank on 17 nodes. Rank does not establish physical derivative accuracy.
- Reported E_z Hessian quadratic–quartic differences: **3.52–898.54%** across assessed comparisons; unresolved polynomial-order sensitivity.
- FRM-4A: **PASS for ingestion only** of paired complex E/H maps on **41 × 41 × 801** M0 Mode 9 grid; **not** a convergence PASS.
- Operator-supplied, GUI-confirmed M0 R10-h2.0 Mode 9: **1.2999834467254 GHz**, **2,571,481** tetrahedra, lossy-E Q **4.00149930514472e7**, beta=1 R/Q **1035.2132090001 Ω**, total energy **0.99920266915905** (unit presumed J, not independently verified).
- Visible settings: tetrahedral mesh, General (Lossy), nine modes above 1.15 GHz, ports enabled, adaptive tetrahedral refinement. The additive provenance supplement does not alter the sealed FRM-4A decision or establish native-state/hash binding.

## HOLD / next action
No demonstrated convergence of physically relevant TVMD Hessians across fitting radius, polynomial order, mesh and longitudinal resolution. **FRM-4B1:** read-only M0 Hessian sensitivity analysis over radius, order, longitudinal resolution and transverse support. No CST operations authorised by this baseline scope.

## Update requirements
FRM Codex owns only this file. Record latest decision ID, timestamp, scientific commit, exact evidence paths, numerical acceptance criteria, reproducibility commands, limitations and next action. Preserve failed or ambiguous results.
