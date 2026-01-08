# AI-Salary-Insight：全球 AI / ML 產業薪資結構之量化與視覺化分析

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Data Analysis](https://img.shields.io/badge/Focus-Data%20Analysis-orange)
![Visualization](https://img.shields.io/badge/Library-Matplotlib-green)

## 📌 專案概述 (Project Overview)
本專案為「大一 AI 實驗」課程之核心成果，旨在透過量化分析手段，探討 2023 年全球人工智慧 (AI) 與機器學習 (ML) 產業的薪資結構。專案從 Kaggle 獲取原始數據，經過完整的資料前處理 (Data Preprocessing) 與清洗，利用 Python 資料科學工具鏈進行多維度視覺化探索。

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
