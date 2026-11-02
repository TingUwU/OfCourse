# 🎓 OfCourse — 智慧選課推薦與動態個人化課程圖譜平台

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![OpenAI](https://img.shields.io/badge/Model-Azure_GPT--4o-orange.svg)](https://azure.microsoft.com/products/ai-services/openai-service)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📌 專案簡介
大學課程體系龐大且先修/後繼關係複雜，學生在安排學期課表時往往缺乏宏觀視野，容易選錯方向或忽略畢業門檻與職涯技能儲備。

**EduVer (OfCourse)** 旨在重新定義大學選課體驗，將「被動選課」轉化為「主動規劃」。結合大型語言模型的語義推理能力與多指標決策演算法，兼顧**學業效率**、**防衝堂排課**與**職涯競爭力**，為每位學生提供量身訂製的個人化學習路徑。

---

## ✨ 核心特色與亮點

1. 🤖 **雙軌智慧推薦引擎 (Dual-Track Recommendation)**
   - **計算推薦 (Calculate Recommendation)**：
     - 基於 **DEA（Data Envelopment Analysis 資料包絡分析法）** 與文字語義相似度演算法。
     - 精確比對學生修課歷史 (`courseHistory`)、學分缺口與課程關聯，找出投報率最高的修課組合。
   - **AI 智慧推薦 (Intelligent Recommendation)**：
     - 整合 **Azure OpenAI GPT-4o**，深度理解學生的自由文字興趣與職涯夢想 (`career.json`)。
     - 提供具備跨領域洞見的客製化選課建議與推薦理由。

2. 🗺️ **多維度互動式可視化導航**
   - **旭日圖 (Sunburst Chart) 課程地圖**：以同心圓階層動態展開學程必選修與領域分佈，點擊即可鑽取各學門細節。
   - **個人能力多維雷達圖 (Radar Chart)**：即時量化分析學生的專業技能分佈，突顯優勢與補足能力短板。
   - **3D 沉浸式知識圖譜 (`3d.html`)**：以 3D 空間力導向圖直觀探索先修條件與學科群網狀關係。

3. ⏰ **智慧時段與衝突檢測 (Time-Slot Scheduling)**
   - 內建時段比對機制（如演算法、人工智慧等熱門模組時段表），自動過濾衝堂時段，確保推薦清單排程合理可行。

---

## 🛠️ 系統技術架構

- **前端展示 (Frontend)**：
  - 原生 HTML5 / CSS3 / JavaScript (ES6+)
  - 互動視覺化：D3.js 旭日圖 (Sunburst)、Three.js 3D 空間圖譜、雷達圖 Canvas
- **後端服務 (Backend)**：
  - Node.js (Express / HTTP REST API) 主服務
  - Python 分析腳本（文字特徵相似度計算 `textSimilarity.py`、DEA 效率評估模型 `dea.py`）
- **AI 與知識推論核心 (AI Core)**：
  - Azure OpenAI Service (GPT-4o Deployment)
