# Task B test results

Test method: executed the inline JavaScript from `practice/02-campus-picker/output/index.html` in Node.js v24 using a lightweight mock DOM. This checks filtering and rendered text/element state, but does not verify real-browser layout, touch behavior, or screenshot appearance.

1. **Indoor / 15 / low** — Only A01–A04 are eligible; observed A04 with deterministic random input.
2. **Outdoor / 15 / medium** — Observed “No matching activities.”; no history entry was added and filters were not relaxed.
3. **Outdoor / 30 / medium** — Repeated three picks; each was A09.
4. **All / 60 / all, six successful picks** — History held exactly five entries, newest first, matching the last five picks.
5. **Reset filters** — Values returned to all / 30 / all; existing history count stayed unchanged.
6. **Clear history and English mode** — History became empty; English control labels and activity names appeared.

**Revision check:** With the no-match result visible, switching English → Chinese → English updated the message each time. This behavior and all six checks passed after revision.

No interactive browser test screenshots were captured because the in-app browser blocked local `file://` access. The local test runner was temporary and removed after execution; no test dependency or file was added to the app.
