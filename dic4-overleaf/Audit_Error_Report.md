# WattWise AI — IEEE 論文初稿錯誤診斷對照報告 (Audit Error Report)

> **受審檔案**：[paper_before.tex](file:///c:/Users/DODO/Desktop/物聯網/WattWise-AI-Agent/dic4-overleaf/paper_before.tex)  
> **審查依據**：[審稿代理人規則.md](file:///c:/Users/DODO/Desktop/物聯網/WattWise-AI-Agent/dic4-overleaf/審稿代理人規則.md) 與 [openspec/changes/dic4-ieee-overleaf/design.md](file:///c:/Users/DODO/Desktop/物聯網/WattWise-AI-Agent/openspec/changes/dic4-ieee-overleaf/design.md)  
> **總體判定**：`NEEDS_REVISION`（包含 1 項 `CRITICAL` 紅線違規與 6 項 `MAJOR` 結構與格式缺失，須全面重構）

---

## 1. 錯誤診斷與修正對照總表

| 錯誤編號 | 嚴重等級 | 修改前錯在哪裡 (`paper_before.tex` 診斷) | 違反之作業規範與審稿規則 | 接下來預計如何修正 (重構行動方案) |
| :---: | :---: | :--- | :--- | :--- |
| **E-01** | `MAJOR` | **摘要開頭空泛且結構殘缺**：僅泛論「AI 與 LLM 發展非常迅速」，完全缺乏 2025–2026 能源背景數據，且未依序涵蓋 A–F 邏輯段落。 | **規則一（摘要 A–F 六段式結構）**：未達 A (Attention Getter) 至 F (Expected Impact) 之完整敘事規範。 | 依 DIC3 摘要規格重寫：以「2050 淨零排放」與「台電 2024–2025 新版 TOU 尖離峰價差 3.5–4 倍」開場（A），接續三大痛點（B）、WattWise AI 解方（C）、八大模組與 `< 0.80` 澄清 / `90%` 守門（D）、REDD/UK-DALE/AMPds2 雙軌驗證計畫（E）及預期效益（F）。 |
| **E-02** | `CRITICAL` | **嚴重虛構未經實測之假數據**：在提案階段宣稱已完成實測並捏造「`98.5%` 準確率」與「省電 `50%`」之虛假結果（同時出現於摘要、實驗與結論）。 | **規則四（不可虛構實驗數據紅線）**：違反「提案階段嚴禁捏造實測數據」之最高學術誠信規範。 | **全面刪除所有假數據**，改為嚴謹之「評估方法論與驗證計畫」：明確標註處於提案階段，列出 REDD / UK-DALE / AMPds2 基準與校園場勘規劃、五大數學指標公式（MAPE、RMSE、F1、TDI、SIR）及 Model A–D 消融實驗設計；`15–20%` 尖峰抑低僅標註為「預期目標」。 |
| **E-03** | `MAJOR` | **標題過於簡陋且遺漏 IEEE 關鍵字**：標題僅寫為「一個智慧用電聊天機器人系統」，無法體現垂直領域推理與電氣安全架構；且全篇遺漏 `\begin{IEEEkeywords}` 區塊。 | **IEEE 會議論文格式規範 & 系統定位一致性**：標題須準確反映研究核心，並提供檢索關鍵字。 | 將標題重構為具學術精準度之「*WattWise AI：智慧住宅與校園空間用電異常診斷暨需量調度領域專用人工智慧代理*」，並補齊 `\begin{IEEEkeywords}`（納入 Domain-Specific AI Agent、ReAct、NILM、2R2C Thermal Model、Time-of-Use、Safety Guard 等關鍵字）。 |
| **E-04** | `MAJOR` | **緒論缺乏客觀數據、痛點拆解與優劣比較**：緒論僅空談聊天機器人概念，缺少 2025–2026 台電 TOU 數據、三大技術痛點分析、SWOT 競爭力矩陣及章節導覽。 | **規則二（緒論 G–L 六維展開結構）**：缺漏 G (客觀數據)、H (技術瓶頸)、I (文獻切入點)、J (SWOT 評估)、K (核心目標) 與 L (章節架構)。 | 嚴格依 G–L 展開重寫緒論：納入台電夏月夜尖峰 `8.40` 元/度、離峰 `2.10` 元/度與契約容量 `200%–300%` 超約罰則；拆解語意鴻溝、LLM 物理幻覺、舒適度缺位三大痛點；補入 SWOT 比較表、FR-01–FR-05 目標及文末章節組織說明。 |
| **E-05** | `MAJOR` | **相關研究偏廢純 AI，零電力與熱力學領域知識**：整節僅列舉 Transformer、GPT、CNN/RNN、PPO 與 RAG，完全未觸及任何電力工程或建築熱力學知識。 | **規則三（1/2 AI 技術 + 1/2 電力領域知識平衡）**：嚴重失衡，無法支撐 Domain AI Agent 之跨領域創新。 | 替換為 DIC3 精選之 5 篇 2024–2026 權威文獻評析，確保每篇皆同時剖析 **50% AI 演算法**（Multi-Agent PPO、Diffusion NILM、PINN、RAG、PGM）與 **50% 電力領域知識**（2R2C 熱阻模型、TOU 規則、V-I 暫態指紋、ASHRAE 55 PMV/PPD、斷路器反時限曲線與契約容量）。 |
| **E-06** | `MAJOR` | **缺少文獻比較表與研究缺口收斂**：相關研究僅為條列式流水帳，未以表格進行橫向對比，亦未收斂出本研究欲填補的 Research Gap。 | **規則三延伸（文獻評析總表與 Convergence Analysis）**：缺乏系統性對比與缺口收斂論證。 | 新增跨欄「5 篇權威文獻橫向比較表」（涵蓋 Problem、AI Method、Domain Know-How、Dataset、Key Findings、Limitations），並補寫「研究缺口收斂分析」，明確指出「技術割裂、安全真空、互動僵化」三大缺口並導向 WattWise AI 架構。 |
| **E-07** | `MINOR / MAJOR` | **參考文獻格式不完整**：`\begin{thebibliography}` 中多筆文獻缺乏發表會議/期刊名稱、年份、卷期與頁碼（例如僅列作者與論文標題），不符合 IEEE 引用標準。 | **IEEE LaTeX 格式與引用完整性規範**：參考文獻須具備完整書目資訊以便審查與查證。 | 依據 IEEEtran 標準格式逐筆補齊所有引用文獻之完整作者、論文標題、期刊/會議名稱（如 *IEEE Trans. Smart Grid*、*ACM e-Energy*、*Applied Energy*、*IEEE Access*、*Energy and Buildings*）、出版年份、卷期與頁碼。 |

---

## 2. 下一步重構驗證流程
1. 依上述修正方案撰寫重構後完稿 `dic4-overleaf/paper_after.tex`，並補齊八大模組系統架構、端到端決策流程（統一標註 `90% 契約容量臨界值` 與 `Confidence < 0.80`）及 `Algorithm 1`（25 行受限白名單虛擬碼）。
2. 將 `paper_before.tex` 與 `paper_after.tex` 分別於 Overleaf（XeLaTeX）編譯產出修改前與修改後兩份 PDF。
3. 再次執行審稿代理人檢核，確認所有 `CRITICAL` 與 `MAJOR` 項目皆轉為 `PASS`。

