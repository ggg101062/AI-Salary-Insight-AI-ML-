# AI-Salary-Insight：全球 AI / ML 產業薪資結構之量化分析與雙模型預測

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Data Analysis](https://img.shields.io/badge/Focus-Data%20Analysis-orange)
![Machine Learning](https://img.shields.io/badge/Focus-Machine%20Learning-yellow)
![Deep Learning](https://img.shields.io/badge/Focus-Deep%20Learning-red)
![Library](https://img.shields.io/badge/Library-Scikit_Learn%20|%20TensorFlow-green)

## 📌 專案概述 (Project Overview)
本專案為「大一 AI 實驗」課程之核心成果，旨在透過量化分析手段與人工智慧演算法，深度探討並預測全球人工智慧 (AI) 與機器學習 (ML) 產業的薪資結構。

為了完整體現學習與開發的演進過程，本專案依據研究階段區分為兩大核心模組：
1. **`analysis_v1_eda.ipynb` (第一階段：基礎資料探索)**：專注於原始數據的清洗 (ETL) 與多維度視覺化探索，建立產業薪資基礎輪廓，並以簡單線性回歸作為基準線模型 (Baseline)。
2. **`analysis_v2_advanced_ml_dl.ipynb` (第二階段：進階雙模型預測)**：基於前期洞察，引進進階特徵工程，建構隨機森林迴規 (Random Forest) 與深度神經網路 (DNN) 進行模型訓練與效能評比。

## 🛠️ 技術棧 (Tech Stack)
* **Programming Language**: Python
* **Data Manipulation**: `Pandas`, `NumPy`
* **Data Visualization**: `Matplotlib`, `Pyplot`, `Seaborn`
* **Machine Learning**: `Scikit-learn` (Random Forest, Linear Regression, Data Preprocessing)
* **Deep Learning**: `TensorFlow`, `Keras` (Sequential API, Dense, Dropout)
* **Dataset**: [Kaggle: AI/ML Salaries Dataset](https://www.kaggle.com/datasets/cedricaubin/ai-ml-salaries)

---

## 📊 Part 1: 基礎分析與視覺化回顧 ── 對應 `analysis_v1_eda.ipynb`

本階段完成了完整的資料前處理與清理（包含型態轉換、刪除干擾特徵與無缺失值驗證），並透過 `Matplotlib` 實作五大核心圖表分析：
1. **長條圖 (Bar Chart)**：計算各職位平均薪資，發現結合「管理決策」與「數據工程技術」的複合型技術職（如分析工程經理）領跑市場。
2. **折線圖 (Line Chart)**：追蹤 2020-2025 年間各聘僱型態的薪資走勢，呈現 2021-2024 的爆發期與 2025 的健康調整期。
3. **圓餅圖 (Pie Chart)**：分析人才結構，顯示資深等級 (SE) 為市場核心主力 (佔 58.7%)，反映產業的高技術經驗門檻。
4. **直方圖 (Histogram)**：呈現薪資高度集中在 10 萬至 20 萬美元區間的偏態分佈。
5. **散佈圖 (Scatter Plot)**：探討遠端工作比例 (Remote Ratio) 與薪資關係，證實頂尖技術人才的報酬受地域限制較小。

---

## 🚀 Part 2: 進階雙模型建構與薪資預測 ── 對應 `analysis_v2_advanced_ml_dl.ipynb`

為了挑戰預測極限，本階段針對類別特徵進行了深度轉換，並實作了傳統機器學習與深度學習模型的對比。

### 1. 進階特徵工程 (Feature Engineering)
* **標籤編碼 (Label Encoding)**：將有順序關係的 `experience_level` 轉換為有序數值 (0~3)。
* **獨熱編碼 (One-Hot Encoding)**：將 `job_title`、`employment_type` 等無序文字特徵攤平成二元特徵矩陣，欄位由原始的 9 個擴充至 298 個。
* **特徵標準化 (StandardScaler)**：壓縮特徵數值區間，確保深度學習神經網路訓練時的權重穩定性。

### 2. 三大模型效能綜合評比 (Model Performance)
專案以 8:2 劃分訓練集與測試集，並將基礎線性回歸作為 Baseline，與進階模型進行綜合 PK：

| 模型 | MAE (平均絕對誤差) | RMSE (均方根誤差) | R² (解釋力) |
| :--- | :--- | :--- | :--- |
| **線性回歸 (Baseline)** | $47,412 | $64,009 | 0.2455 |
| **隨機森林 (Random Forest)** | $47,015 | $63,455 | **0.2585** |
| **深度神經網路 (DNN)** | **$46,975** | $64,305 | 0.2385 |

* **隨機森林 (Random Forest) 整體最穩定**：成功處理高維度的類別矩陣，取得最高的解釋力 (R² = 0.2585) 與最低的極端誤差。
* **深度神經網路 (DNN) 平均落差最小**：架構包含兩層隱藏層（64 與 32 個神經元）並加入 20% Dropout 層防過擬合，取得最低的平均絕對誤差 (MAE = $46,975)，且驗證集 Loss Curve 收斂極其健康。

### 3. AI 視角的關鍵洞察 (Feature Importance)
* **演算法實證**：隨機森林特徵重要性圖表顯示，**「經驗等級 (Experience Level)」** 的決定性權重高達 35%，壓倒性領先其他特徵。
* **預測極限反思**：雙模型約 26% 的解釋力告訴我們，剩餘 74% 的變異來自於資料集未收錄的個體差異（如：技術廣度、談判技巧、前職底薪等無法被量化的硬實力）。

---

## 📂 檔案結構 (Repository Structure)
* `analysis_v1_eda.ipynb`: 包含基礎資料清洗、五大圖表視覺化探索與線性回歸 Baseline 模型。
* `analysis_v2_advanced_ml_dl.ipynb`: 包含進階特徵工程、隨機森林訓練、DNN 架構建立、雙模型評比與特徵重要性分析。
* `data/`: 存放原始資料與清理後的 CSV 檔案。

## ✍️ 關於作者 (About the Author)
* **作者**：高睿澤 (Jui-Tse Kao)
* **機構**：淡江大學 人工智慧學系 (大一期末專案)
* **專案簡報**：[📊 點此查看 Canva 線上簡報](https://canva.link/jgoke0oio029flj)
