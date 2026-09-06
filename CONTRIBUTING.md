# 貢獻指南

感謝你願意參與麟曜數位工作室的開源專案。

我們歡迎 Bug 修正、功能改善、文件更新、測試、設計建議以及其他有助於專案發展的貢獻。

## 開始之前

在建立 Issue 或 Pull Request 前，請先：

* 搜尋是否已有相同或相關的 Issue。
* 確認你的變更符合專案目前的發展方向。
* 大型功能、重大 API 變更或架構調整，請先建立 Issue 討論。
* 安全漏洞請依照 `SECURITY.md` 私下回報，不要建立公開 Issue。

## 開發

不同專案可能使用不同的開發工具、套件管理器與測試流程。

請以該 repository 的 `README.md`、開發文件與設定檔為準。

提交變更前，請盡可能確認：

- 專案可以正常建置。
- 現有測試仍可通過。
- 新增行為有適當的測試或驗證方式。
- Lint、format 與型別檢查沒有新增錯誤。
- 公開 API、設定方式或使用方式有變更時，相關文件已同步更新。

## Pull Request

一個 Pull Request 應盡量只處理一個明確目的。

請：

- 使用清楚且能描述變更內容的標題。
- 說明變更的原因，而不只是列出修改內容。
- 關聯相關 Issue。
- 說明測試或驗證方式。
- UI 或視覺變更請盡可能提供截圖或錄影。
- Breaking change 必須明確標示並說明遷移方式。

維護者可能會要求調整實作方式、縮小變更範圍，或補充測試與文件。

Pull Request 是否合併，以及最終採用的實作方式，由專案維護者依專案方向決定。

## Commit

請依照以下規範建立 Commit。

Commit 標題採用 Linux kernel / Git 風格，並以前綴指出實際變更的區域、子系統、元件、目錄、套件或檔案：

```text
area: imperative patch summary
sub/sys: imperative patch summary
```

前綴應指出此次變更主要所屬的 repository 區域。請優先使用具體的目錄、套件、檔案、子系統或元件名稱。

除非 `fix`、`feat`、`chore`、`docs` 或 `refactor` 本身就是該 repository 中實際存在的區域名稱，否則請勿使用這類通用 Conventional Commits 前綴。

前綴應描述「變更屬於哪裡」，而不是「這是哪一種類型的變更」。

冒號後的摘要應使用祈使語氣的動詞，例如：

`fix`、`clarify`、`split`、`validate`、`rename`、`remove`、`add`、`update`、`document`

請勿使用 `fixed`、`added` 等過去式。

當一個變更橫跨多個區域時，如果存在明確的共同上層區域，請使用範圍最小的共同區域作為前綴。

如果沒有明確的共同區域，請以前述變更中最主要的行為作為前綴，而不要同時列出多個彼此無關的前綴。

冒號後的摘要應簡短描述這個 Commit 實際做了什麼，因為它會成為 Git 變更紀錄中顯示的第一行。

摘要應保持簡短、具體並使用祈使語氣。建議控制在 72 個字元以內。

除非第一個詞是專有名詞，否則冒號後的第一個單字應使用小寫，且標題結尾不要加句號。

例如：

```text
storybook: clarify build ownership
web/routes: split route-level chunks
ui/field: fix select menu positioning
server/auth: validate session cookie
githooks.txt: improve the intro section
```

如果無法單純從 diff 理解變更原因，請加入 Commit 內文。

內文應著重說明「為什麼需要這項變更」，而不是只是重複描述「修改了什麼」。

Pull Request 應：

* 說明主要變更的區域。
* 摘要說明對使用者或開發者可觀察到的影響。
* 列出實際執行過的驗證指令。
* 關聯相關 Issue。
* 對可見的 Web UI 變更提供截圖。

如果沒有執行任何驗證，請明確註明，並說明原因。

請勿聲稱執行過實際上沒有執行的指令。

對於不容易透過截圖呈現的 UI 變更，請描述視覺上的差異，以及實際進行過的人工檢查。

## 授權

每個 repository 可能採用不同的授權方式。

提交貢獻前，請閱讀該專案的 `LICENSE`、`COMMERCIAL-LICENSE.md` 或其他授權文件。

你提交的內容必須是你有權提供的作品，且不得在未取得適當授權的情況下包含第三方程式碼、素材或其他受著作權保護的內容。

部分專案可能另外要求 Contributor License Agreement（CLA，貢獻者授權協議）或其他貢獻授權程序；若有要求，會在該專案中另外說明。

## 行為準則

參與 Issue、Pull Request、Discussion 或其他專案社群互動時，請遵守我們的 `CODE_OF_CONDUCT.md`。

我們重視直接、專業且尊重彼此的技術討論。

感謝你的參與。
