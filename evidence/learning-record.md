# Learning record / 實作紀錄

This record summarizes work performed by Codex in the local repository. The handout export control reported that it created `learning-record.md` in the browser context, but the download was not exposed at a workspace path. This local copy combines the browser self-check notes with actual file and test evidence; it is not a student self-report. The learner still needs to review the artifacts and add any missing group or route details.

- Group code: Not provided
- Tool: Codex (local workspace)
- Route: Not recorded; this session was agent-assisted
- Tasks: A, B, and D completed; optional C not completed
- Material: NDHU classroom tasks
- Original-pack work: None
- Scope: `practice/01-club-files/input/` → `practice/01-club-files/output/`; `practice/02-campus-picker/activities.json` → `practice/02-campus-picker/output/index.html`; `practice/04-review/bad-plan.txt` → `practice/04-review/my-rejection.md`

## Checks actually performed

| Check | Expected | Observed | Evidence |
|---|---|---|---|
| Task A: copy verification | Each of 12 inputs has a corresponding unchanged copy | All 12 source/destination SHA-256 hashes matched; 12 manifest entries found | `practice/01-club-files/output/manifest.json`; local PowerShell hash comparison |
| Task B: required behavior | Six handout scenarios behave as specified | All six passed in a local Node.js v24 harness with a lightweight DOM mock; no-match does not add history, six picks retain five newest-first, reset retains history, and clear empties it | `practice/02-campus-picker/output/index.html`; local harness output recorded during this session |
| Task B: revision behavior | No-match status follows the selected language | Switching English → Chinese → English updated the visible no-match text in the harness | B v2 in Git, commit `10c3a2a` |
| Task D: rejection | Identify unsafe actions and an allowed alternative | Rejected broad Downloads scope, deletion, guessed values, unsupported `final2` choice, and automatic publishing; proposed a scoped, review-first alternative | `practice/04-review/my-rejection.md` |

## One revision

- Before: A no-match message stayed in the language used when it was first shown after switching the interface language.
- Request: Keep the current no-match message in sync with the selected language.
- After and retest: Added a no-match state flag and re-rendered the message on language changes. The language-switch check and all six required behavior checks passed in the local harness.
- Classification: A defect in the bilingual interface behavior.

## One rejection

Rejected the simulated plan to process everything in Downloads, delete duplicates, choose `final2` by name, guess missing values, and publish automatically. The alternative limits work to a named folder, preserves originals and versions, flags unknowns for human review, and stops before external publication.

## Still unverified

- No interactive browser or visual/mobile check was performed. The in-app browser blocked opening the local `file://` page, and I did not work around that restriction by serving it over HTTP.
- No screenshots of the picker tests were captured. The local harness checks behavior but does not prove visual rendering in a real browser.
- Group code, learner route, and the learner's own review/sign-off were not supplied.
- Task C is optional in the two-period route and was not done.

