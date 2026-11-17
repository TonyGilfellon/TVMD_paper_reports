# Reporting and publication protocol

## Source of truth and ownership
- Scientific worktrees and sealed investigation reports are authoritative for scientific results.
- `docs/investigations/FRM_STATUS.md`: FRM Codex only.
- `docs/investigations/A5_STATUS.md`: A5 Codex only.
- `docs/investigations/S2_STATUS.md`: S2 Codex only.
- `docs/programme/MASTER_STATUS.md` and `REVIEWER_EVIDENCE_MATRIX.md`: programme coordinator only.
- Initial 17 November 2026 reports are historical conversation-derived baselines, pending investigation-owner verification.

## Required fields for each scientific update
1. As-of UTC timestamp, decision ID and exact scientific worktree/branch/commit.
2. Scope and criteria tested; PASS, HOLD, FAIL or CONDITIONAL with **specific scope**.
3. Quantitative results with units, comparisons, denominators and uncertainty/convergence limits.
4. Evidence: source report paths, data provenance, reproducibility commands and test results.
5. Unresolved contradictions, dependencies and next action.
6. State whether prior conclusions were superseded; preserve sealed historical decisions.

## Controlled publishing through the existing SSH clone
Use the local clone `C:\Users\zup98752\PycharmProjects\TVMD_paper_reports`. Before editing, run `git pull --ff-only origin main`; if local edits exist, stop and reconcile rather than overwrite. Edit only your assigned status file. Review `git diff -- <assigned-file>`, then `git add <assigned-file>`, `git commit -m "report(<stream>): <decision-id>"`, `git push origin main`. Do not force-push. If push rejects because another writer updated main, `git pull --rebase origin main` **only after checking the working tree and conflicts**; do not discard changes. Prefer one writer at a time. Explicit user approval is required before any agent push.

Do not copy scientific datasets, CST files, credentials, personal data, or large exports. GitHub integration in ChatGPT has **verified read access** but write requests returned **403** on 17 November 2026. Publish through SSH/Codex unless permissions are deliberately changed.

## Programme review
On request, ChatGPT reads the five report files from GitHub and checks timestamp, commit, provenance, status transitions, contradictions and dependencies. A status update in a scientific worktree is **not** automatically published here. Avoid claiming continuous monitoring or automatic sync.
