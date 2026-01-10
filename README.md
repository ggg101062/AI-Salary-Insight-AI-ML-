# AI-Salary-Insight：全球 AI / ML 產業薪資結構之量化與視覺化分析

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Data Analysis](https://img.shields.io/badge/Focus-Data%20Analysis-orange)
![Visualization](https://img.shields.io/badge/Library-Matplotlib-green)

## 📌 專案概述 (Project Overview)
本專案為「大一 AI 實驗」課程之核心成果，旨在透過量化分析手段，探討全球人工智慧 (AI) 與機器學習 (ML) 產業的薪資結構。專案從 Kaggle 獲取原始數據，經過完整的資料前處理 (Data Preprocessing) 與清洗，利用 Python 資料科學工具鏈進行多維度視覺化探索。

本研究不僅關注薪資數字，更深入探討了 **經驗等級、遠端工作比例、職務類別** 與 **報酬** 之間的相關性，為數位轉型浪潮下的職涯規劃提供數據驅動的洞察。

## 📊 核心研究重點 (Key Objectives)
* **數據清洗與 ETL**：處理原始資料集中的遺失值、異常值，並確保薪資單位統整（USD）。
* **多維度量化分析**：針對經驗等級 (EN, MI, SE, EX) 進行分組聚合分析。
* **數據視覺化實踐**：繪製直方圖、散佈圖、折線圖等多種圖表，將枯燥的數字轉化為直觀的趨勢發現。

## 🛠️ 技術棧 (Tech Stack)
* **Programming Language**: Python
* **Data Manipulation**: `Pandas`
* **Data Visualization**: `Matplotlib`, `Pyplot`
* **Dataset**: [Kaggle: AI/ML Salaries Dataset](https://www.kaggle.com/datasets/cedricaubin/ai-ml-salaries)

## 📈 視覺化分析亮點 (Visualization Highlights)
本專案包含五大核心圖表分析：
1. **職位平均薪資分析**：識別 AI 產業中的高薪領頭職務。
2. **經驗等級與薪資關聯**：量化初階與高階主管職位的報酬鴻溝。
3. **工作年份成長趨勢**：觀察近年來 AI 市場薪資的縱向變動。
4. **薪資分佈直方圖**：掌握市場薪資的常態分佈情形。
5. **遠端工作影響力**：探索遠端協作程度對薪酬的實質影響。

## 🔍 關鍵洞察 (Key Insights)
* **年資效應顯著**：數據顯示隨著經驗等級提升，薪資呈現非線性增長，尤其在 Senior (SE) 以上層級有顯著跳躍。
* **數位轉型趨勢**：遠端工作比例 (Remote Ratio) 與高薪職位展現出高度的正相關性，反映出頂尖技術人才的地域限制正在消失。

## 📂 檔案結構
* `期末作業.ipynb`: 包含所有資料處理邏輯與圖表生成的程式碼。
* `AI_Salary_Report.pdf`: 完整的研究報告與口頭簡報投影片。
* `data/`: 存放原始資料與清洗後的 CSV 檔案。

## ✍️ 關於作者
* **作者**：高睿澤
* **機構**：淡江大學 AI 系
* **專案背景**：本專案為 2025 年 AI 實驗課程之期末專案。
* **研究簡報**：[📊 點此查看 Canva 線上簡報](https://www.canva.com/design/DAG9ubtFwTk/LrHapHMgiOg0XVIas3YZPg/edit?utm_content=DAG9ubtFwTk&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

🚀 進階延伸：機器學習與相關性分析
為了更深入探討薪資背後的影響因子，我進行了第二階段的延伸分析：

資料深度前處理：完成了特徵編碼（Encoding）與缺失值精密處理。

關鍵發現：透過 熱力圖 (Heatmap) 證實「經驗等級」與「工作年份」是影響薪資最顯著的因子。

模型預測：建立了 線性回歸 (Linear Regression) 模型，初步實踐薪資預測。

完整程式碼：
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1rmTivqSSig-46zwTHZ0sMrA88LW0hmLx?usp=sharing)

> **專案簡介**：本專案分為基礎資料視覺化 (EDA) 與進階機器學習 (ML) 兩大部分，旨在分析全球 AI 產業薪資趨勢並建立回歸預測模型。
## 🚀 專案更新：機器學習延伸補充 (Part 2)

在完成基礎的資料分析後，我針對資料進行了深度清洗與模型建立，以探索特徵間的相關性。

### 1. 核心處理步驟 (Key Processing)

依據機器學習標準流程，本補充完成了以下任務：

* **目標欄位定義**：鎖定 `salary_in_usd` 為預測目標。
* **缺失值處理**：透過 `dropna` 與 `ffill` 確保資料品質，避免模型偏差。
* **資料型態轉換**：將 `company_size` 等類別資料轉為有序數值 (Order Encoding)。
* **完全編碼 (Encoding)**：針對 `experience_level` 進行標籤編碼，使其具備分析意義。

### 2. 熱力圖分析 (Correlation Insights)

透過熱力圖 (Heatmap) 發現，與薪資相關性最高的前三個特徵為：

1. **薪資排名 (Rank)**：呈極高負相關 (-0.93)，驗證了數據邏輯。
2. **原始薪資 (Salary)**：反映了幣值轉換間的連動性。
3. **經驗等級 (Experience Level)**：具備顯著正相關，證明年資是 AI 產業薪資的決定性因素。

### 3. 模型建立與預測 (Machine Learning)

本專案建立了 **線性回歸模型 (Linear Regression)**：

* **資料切分**：80% 訓練集 / 20% 測試集。
* **模型表現**：R-squared (判定係數) 為 `0.1069`。雖然數據具備高度離散性，但模型成功捕捉到了經驗與薪資成長的基本線性趨勢。

---

## 📊 基礎分析回顧 (Part 1 - EDA)

本專案包含五大核心圖表分析：

1. **長條圖 (Bar Chart)**：比較 Top 10 高薪職位，發現管理型技術職領跑市場。
2. **折線圖 (Line Chart)**：追蹤 2020-2025 年間，各聘僱型態的薪資增長趨勢。
3. **圓餅圖 (Pie Chart)**：分析人才分佈，顯示資深 (SE) 等級為市場主力。
4. **直方圖 (Histogram)**：呈現薪資集中在 10 萬至 20 萬美元區間的偏態分佈。
5. **散佈圖 (Scatter Plot)**：探討遠端工作比例與薪資的弱相關性。

---

## 🛠 使用工具

* **語言**：Python
* **套件**：Pandas, Matplotlib, Seaborn, Scikit-learn
* **資料來源**：Kaggle - AI/ML Salaries

## 💡 結論

透過這次延伸補充，我們不僅視覺化了數據，更透過編碼與熱力圖量化了特徵影響力。已成功建立了一套完整的數據預測流水線。
