# AI/ML 薪資分析與預測專案 (AI/ML Salary Analysis & Prediction)

這個專案旨在分析全球 AI/ML 產業的薪資結構，並透過機器學習模型預測未來的薪資趨勢。本專案分為兩個主要部分：基礎視覺化分析與進階機器學習前處理。

# AI/ML 薪資分析與預測專案 (AI/ML Salary Analysis & Prediction)

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
