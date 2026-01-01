# NCKU_CHE-process-design
[題目](114年度化工程序設計競賽題目.pdf)
# 114年度化工程序設計競賽 - 10萬公噸 VAM 製程設計
# Project: 100,000 MTA Vinyl Acetate Monomer Process Design

## 📖 專案背景 (Background)
本專案為 **台灣化學工程學會 114年度 (2025-2026)** 化工程序設計競賽題目 [cite: 1, 2]。
目標是設計一個年產能 **10萬公噸 (100,000 MTA)** 的醋酸乙烯酯單體 (Vinyl Acetate Monomer, VAM) 製程 [cite: 3]。

鑑於環保與能耗考量，本設計採用 **乙烯法 (Ethylene Process)**，其碳排 (2.5 t-CO2e/t VAM) 遠低於乙炔法 (6.0 t-CO2e/t VAM)，為目前主流生產技術 [cite: 4, 6]。

## ⚙️ 製程概述 (Process Description)
* **反應類型**：氣相氧化反應 (Gas-phase oxidation) [cite: 5]。
* **主要原料**：乙烯 (Ethylene)、醋酸 (Acetic Acid)、氧氣 (Oxygen) [cite: 5]。
* **催化劑系統**：金 (Au)、鈀 (Pd) 觸媒，並以醋酸鉀 (Potassium Acetate) 為活化促進劑 [cite: 5]。
* **反應方程式**：
    $$C_2H_4 + CH_3COOH + \frac{1}{2}O_2 \rightarrow CH_3COOCH=CH_2 + H_2O$$

## 🚀 設計要求與目標 (Design Requirements)
本專案報告涵蓋以下 12 項核心設計要求 [cite: 10]：

1.  **製程模擬**：包含反應、蒸餾、吸收、壓縮等單元，需提供詳細敘述 [cite: 11]。
2.  **質能平衡**：計算 Mass/Energy Balance，並處理汽-液平衡 (VLE) 與不互溶液-液平衡 (LLE) [cite: 12]。
3.  **流程圖繪製**：PFD (Process Flow Diagram) 及控制流程圖，需標示物流編號及單位 (mass basis) [cite: 13]。
4.  **反應器安全設計**：反應器進出口氧氣濃度不得超過容許濃度的 **75% (安全餘裕)** [cite: 14]。
5.  **安全連鎖系統**：設計 Interlock System 以避免反應失控或燃燒爆炸 [cite: 15]。
6.  **熱移除系統**：設計氧化反應熱之移除機制 [cite: 16]。
7.  **CO2 移除**：設計系統移除因過度氧化產生的二氧化碳 [cite: 17]。
8.  **原料回收循環**：
    * 移除不反應氣體 (Inert gas) [cite: 18]。
    * 未反應之乙烯與醋酸需經過處理後循環使用 [cite: 18]。
9.  **副產物移除**：需從產品中移除醋酸甲酯、醋酸乙酯、乙醛及聚合物，以達產品純度 [cite: 19]。
10. **聚合抑制**：設計添加適量抑制劑 (Inhibitor) 以防止 VAM 水解或聚合 [cite: 20]。
11. **儲槽設計**：設計 VAM 產品儲槽，需考量避免自身聚合 [cite: 21]。
12. **材質選用**：考量醋酸腐蝕性，選用適合的合金鋼材質 [cite: 22]。

## 📊 規格需求 (Specifications)

### [cite_start]1. 產品規格 (VAM Product Spec) [cite: 23, 24]
| 項目 | 規格 | 備註 |
| :--- | :--- | :--- |
| **VAM 純度** | **≥ 99.9 wt%** | |
| 水分 | ≤ 500 ppm | (0.05 wt%) |
| 醋酸含量 | ≤ 0.03 wt% | |
| 乙醛 | ≤ 20 ppm | |
| 醋酸乙酯 | ≤ 20 ppm | |
| 醋酸甲酯 | ≤ 20 ppm | |
| 抑制劑 (MEHQ) | 5 ppm | |
| 色度 (Pt-Co) | ≤ 10 | |

### [cite_start]2. 原料規格 (Feed Specs) [cite: 25-30]
| 原料 | 純度要求 | 關鍵雜質限制 |
| :--- | :--- | :--- |
| **乙烯** | ≥ 99.9 vol% | O2 ≤ 5 ppm, CO2 ≤ 10 ppm, 硫/氯 ≤ 50 ppb |
| **氧氣** | ≥ 99.5 vol% | N2/Ar ≤ 0.5 vol%, 水分 ≤ 2 ppm |
| **醋酸** | ≥ 99.8 wt% | 水分 ≤ 0.15 wt%, 金屬離子 ≤ 0.1 ppm |

## 💰 經濟數據 (Economic Parameters)

### [cite_start]原料與產品單價 [cite: 31, 32]
* **VAM**: 740 - 1,150 USD/MT
* **Ethylene**: 800 - 1,200 USD/MT
* **Oxygen**: 350 - 400 USD/MT
* **Acetic Acid**: 350 - 450 USD/MT

### [cite_start]公用流體 (Utilities) [cite: 33-52]
| 項目 | 價格 | 備註 |
| :--- | :--- | :--- |
| **電** | 4.5 NTD/kWh | |
| **蒸汽 (MP)** | 900 NTD/MT | 4 kg/cm²G |
| **蒸汽 (HP)** | 1,000 NTD/MT | 20 kg/cm²G |
| **冷卻水** | 0.1 NTD/kkcal | 供 33°C / 回 < 43°C |
| **冰水** | 1.0 NTD/kkcal | 供 7°C / 回 < 12°C |
| **純水** | 20 NTD/MT | |
| **廢水處理** | 15 NTD/MT | |

## 📚 參考文獻 (References)
[cite_start]本專案設計依據以下核心文獻 [cite: 53-58]：
1.  **Dimian, A. C.; Bildea, C. S.** (2008). *Chemical Process Design: Computer-Aided Case Studies*. Chapter 10: Vinyl Acetate Monomer Process. Wiley-VCH.
2.  **Chemical Engineering** (Nov. 2021). *Production of Vinyl Acetate*.
3.  **Han, Y. F. et al.** (2005). *A kinetic study of vinyl acetate synthesis over Pd-based catalysts*. Journal of Catalysis 232, 467-475.

---
*Disclaimer: This project is for the 2025-2026 Student Chemical Process Design Competition.*
