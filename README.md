# 校園設備報修系統

## 文件結構
```
repair-demo/
├── skills/
│   └── repair-attachment-upload/
│       └── skill.md
├── Agents.md
├── Software-spec.md
├── README.md
```

## 核心文件
* `Software-spec.md`：寫了系統目標、核心功能、限制與規則、驗收條件，是所有修改的依據。
* `Agents.md`：AI Agent 的工作規則。規定 Agent 修改前要先做什麼、開發時要注意什麼、改完要怎麼回報。
* `skills/repair-attachment-upload/skill.md`：附件上傳的 skill。寫了什麼時候用、需要什麼輸入、怎麼做、做完要檢查什麼。

## 如何使用這個Skills
1. 先看 `Software-spec.md`，了解這個系統要做什麼、有哪些限制。
2. 再看 `Agents.md`，了解 AI Agent 要遵守的規則。
3. 要做附件上傳功能時，讓 Agent 讀 `skills/repair-attachment-upload/skill.md`，照裡面的流程做。
4. Agent 改完後，對照 `Software-spec.md` 的驗收條件，逐項檢查結果。
5. 看 Agent 回報的修改檔案、測試結果和不確定的地方，確認沒問題再收下修改。

## 如何測試
1. 開啟報修表單，選一張照片，送出
2. 選一份 PDF，送出
3. 選一個不支援的檔案，確認會顯示錯誤訊息
4. 以管理員身分查看案件，確認看得到附件