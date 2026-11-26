# DIC4 實作檢核清單 (Implementation Tasks)

## Phase 1：DIC3 規格對齊與前置建置
- [x] 修正 `README.md` 端到端決策流程圖，將「80% 斷路器容量」統一改為「90% 契約容量臨界值」。
- [x] 修正 `DESIGN.md` 端到端推論流程圖，將「80% 斷路器容量」統一改為「90% 契約容量臨界值」。
- [x] 建立 `openspec/changes/dic4-ieee-overleaf/goal.md`，明確定義 DIC4 目標與交付物。
- [x] 建立 `openspec/changes/dic4-ieee-overleaf/design.md`，繪製端到端 Mermaid 流程圖並定義四大審稿規則。
- [x] 建立 `openspec/changes/dic4-ieee-overleaf/task.md`，條列完整實作檢核清單。
- [x] 建立 `dic4-overleaf/審稿代理人規則.md`，詳細定義論文審稿代理人檢查項目與判定標準。
- [x] 建立 `dic4-overleaf/overleaf-mcp-config.example.json`，提供 Overleaf MCP 連線設定範例。

## Phase 2：Overleaf 環境連線與 IEEE 論文初稿撰寫
- [x] 依據 `overleaf-mcp-config.example.json` 完成本機 Overleaf MCP Server 連線與專案綁定測試。
- [x] 建立 IEEEtran 雙欄會議論文專案結構（`paper_before.tex`、`paper_after.tex` 與 XeLaTeX 繁體中文環境設定）。
- [x] 將 DIC3（`README.md` 與 `DESIGN.md`）內容轉譯為 IEEE 論文初稿，涵蓋 Abstract、Introduction、Related Work、System Architecture、Algorithm 1 與 Evaluation Plan。
- [x] 透過 Overleaf 進行首次編譯，產出並匯入「修改前初稿 PDF」（`DIC4_Before_Bad.pdf`）。

## Phase 3：審稿代理人錯誤診斷與重構完稿
- [x] 啟動論文審稿代理人，依據 `dic4-overleaf/審稿代理人規則.md` 對初稿進行全面檢查。
- [x] 產出「初稿錯誤診斷報告」（`Audit_Error_Report.md`），逐項紀錄摘要 A–F、緒論 G–L、相關研究 1/2 AI + 1/2 領域知識、不虛構實驗數據及 LaTeX 格式缺失。
- [x] 依據診斷報告重構論文內容、修正圖表引用、演算法行號與語法錯誤（`paper_after.tex`），並統一作者真實資訊。
- [x] 重新透過 Overleaf 編譯完稿，確認無 LaTeX Error，產出並匯入「修改後完稿 PDF」（`DIC4_After_Good.pdf`）。

## Phase 4：驗證與 GitHub 歸檔上傳
- [x] 雙版本 PDF 交叉比對檢查（確認 `DIC4_Before_Bad.pdf` 與 `DIC4_After_Good.pdf` 皆已就位且差異明確）。
- [x] 檢查所有文件之繁體中文、數據一致性（90% 契約容量臨界值、0.80 信心度閾值）及無虛構數據聲明。
- [x] 將 `openspec/changes/dic4-ieee-overleaf/`、`dic4-overleaf/`、LaTeX 原始碼及雙版本 PDF 提交（Commit）並推送（Push）至新 GitHub 儲存庫（`WattWise-AI-DIC4`）。
