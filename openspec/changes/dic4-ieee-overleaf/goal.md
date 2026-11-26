# DIC4 目標規格書 (Goal Specification)

## 1. 專案背景與延續性
本階段作業（DIC4）承接 DIC3（**WattWise AI — 智慧住宅與校園空間用電異常診斷暨需量調度 Domain AI Agent**）之完整系統規格與工程設計文件（[README.md](../../../README.md) 與 [DESIGN.md](../../../DESIGN.md)），將既有專案提案與系統架構轉化為符合 **IEEE 會議論文格式（IEEEtran Two-Column Conference Paper）** 之學術論文草稿，並導入 Overleaf MCP 自動化編譯與 AI 論文審稿代理人（Paper Reviewer Agent）進行品質把關與重構。

---

## 2. 核心目標 (Core Objectives)

1. **DIC3 內容學術化與 IEEE 論文轉譯**
   - 將 `README.md` 與 `DESIGN.md` 中的核心研究成果（包含八大解耦模組、ReAct 推理架構、NILM 負載分解、2R2C 建築熱阻抗模型、信心度 `< 0.80` 主動澄清迴圈、以及 `90%` 契約容量安全守門機制）轉換為結構嚴謹的 IEEE 會議論文 LaTeX 初稿。
2. **Overleaf MCP 整合與雙版本 PDF 產出**
   - 透過 Overleaf MCP 連線至雲端 LaTeX 專案，完成自動化編譯與版本控管，產出以下兩份可對照之 PDF 成果：
     - **修改前初稿 PDF（Before / Initial Draft）**：由 DIC3 規格直接轉換後首次編譯產出之基準論文版本。
     - **修改後完稿 PDF（After / Refactored Final）**：經由審稿代理人診斷並完成重構修正後之最終編譯版本。
3. **審稿代理人錯誤診斷與迭代重構**
   - 依據自定義之「審稿代理人規則」，對初稿進行四大維度（摘要 A–F、緒論 G–L、相關研究技術與領域平衡、不虛構實驗數據規範）與 LaTeX 排版語法之全面審查，產出具體錯誤診斷清單並逐項修正重構。
4. **OpenSpec 規格化與 GitHub 上傳歸檔**
   - 將 DIC4 整體工作流、審稿規則、Overleaf MCP 連線設定範例、LaTeX 原始碼與修改前後雙版本 PDF 完整納入 `openspec/changes/dic4-ieee-overleaf/` 與 `dic4-overleaf/` 目錄，並推送上傳至 GitHub 儲存庫完成歸檔。

---

## 3. 預期產出物清單 (Deliverables)
- `openspec/changes/dic4-ieee-overleaf/` 規格文件（`goal.md`、`design.md`、`task.md`）。
- `dic4-overleaf/審稿代理人規則.md` 與 Overleaf MCP 連線設定範例檔。
- IEEE 會議論文 LaTeX 初稿與重構後完稿原始碼。
- 修改前初稿 PDF 與修改後完稿 PDF 兩份編譯成品，以及錯誤診斷修正紀錄。
- GitHub 遠端儲存庫完整同步紀錄。

