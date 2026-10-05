# My lab evidence / 我的實作紀錄

Use a group code, not real names or student IDs in shared files. / 共用檔只寫組別代碼，不寫姓名或學號。

- Group code / 組別：Not provided / 未提供
- Tool / 工具：Codex (local workspace) / Codex（本機工作區）
- Route / 路線：Not recorded; agent-assisted / 未記錄；由 Agent 協助
- Tasks completed / 完成題目：A, B, D（C 選做，未完成）
- Material / 素材：NDHU classroom tasks 東華課堂版
- For original-pack work: task number, author/source link and version / 原版實作：N/A
- My role and what I checked / 我的角色與實際檢查：Codex created A/B/D deliverables; learner review and sign-off remain outstanding. Checked A copy hashes, B behavior in a local Node/DOM harness, and D rejection rationale. / Codex 建立 A/B/D 成果；仍待學習者檢查確認。已核對 A 副本雜湊、以本機 Node/DOM 測試 B 行為，並完成 D 退回理由。

## Scope and plan / 範圍與計畫

Allowed input and output folders / 可讀取與輸出的資料夾：

- `practice/01-club-files/input/` → `practice/01-club-files/output/`
- `practice/02-campus-picker/activities.json` → `practice/02-campus-picker/output/index.html`
- `practice/04-review/bad-plan.txt` → `practice/04-review/my-rejection.md`

What I asked for / 原始需求：Finish the required NDHU lab tasks A, B, and D, with the required B revision and evidence records. / 完成東華版必做 A、B、D，包含 B 修改及實作紀錄。

What I checked before execution / 動手前我檢查了什麼：Read the lab handout, the 12 A inputs, B activity data, D discussion-only plan, and repository README. Confirmed each output location was absent before creating it. / 閱讀講義、A 的 12 個輸入、B 活動資料、D 討論計畫與 README；建立前確認輸出位置不存在。

## Tests actually performed / 我真的做過的測試

| Test / 測試 | Expected / 預期 | Observed / 實際 | Evidence / 證據 |
|---|---|---|---|
| A: compare all source/copy hashes | 12 copies match the 12 sources | 12/12 matched; originals unchanged | `practice/01-club-files/output/manifest.json`; hash comparison |
| B: six specified picker scenarios | Filters, empty result, fixed A09 result, five-item history, reset, clear, and English names/controls work | All six passed in local Node.js v24 DOM-mock harness | `practice/02-campus-picker/output/index.html`; session harness output |

## One revision / 一次修改

Before / 原來的情況：No-match message did not change language when the interface language changed. / 無符合結果訊息不會隨介面語言切換。

Request / 我提出的修改：Keep the no-match message in the currently selected language. / 讓無符合結果訊息配合目前語言。

After and retest / 修改後與重測結果：Updated rendering and retested language switching plus all six required B scenarios; all passed in the local harness. / 更新顯示邏輯，重測語言切換及 B 六項情境，本機測試皆通過。

New requirement or defect? / 新需求還是原規格未做到？A defect in bilingual interface behavior. / 雙語介面行為缺陷。

## One rejection / 一次退回

Which action I reject and why / 退回哪個動作、為什麼：Rejected processing all Downloads, deleting duplicates, choosing `final2` based on its name, guessing missing values, and publishing automatically because scope is broad, changes are destructive or unsupported, and publishing is external. / 退回整理整個 Downloads、刪除重複檔、只憑檔名選 final2、猜補缺值及自動發布，因範圍過大、變更具破壞性或無依據，且發布會影響外部。

An acceptable alternative / 可以怎麼改：Work only in a named approved folder, preserve originals and versions, list suspected duplicates and unknown values for human review, and stop before publishing. / 僅處理指定資料夾、保留原檔與版本、列出疑似重複及未知值供人工檢查，發布前停止。

## Still unverified / 還沒驗證

What I cannot claim is complete / 哪些事不能說已完成：No interactive browser visual/mobile check or test screenshots were captured: the browser blocked local `file://` access, and no workaround was used. A local mocked-DOM harness does not verify browser rendering. Learner review, group code, and route also remain unrecorded. / 未進行互動瀏覽器的視覺／手機檢查，也沒有測試截圖：瀏覽器封鎖本機 `file://` 存取，未採用繞過方式。本機模擬 DOM 測試無法驗證瀏覽器實際渲染。仍待學習者檢查，組別代碼與路線也未記錄。
