# 倍數判別法 動畫教學 🔢 Divisibility Rules Interactive Animation

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=for-the-badge&logo=github)](https://cconecone-cmyk.github.io/divisibility-rules/)
[![Language](https://img.shields.io/badge/Language-繁體中文%20%7C%20English-blue?style=for-the-badge)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Zero Dependency](https://img.shields.io/badge/Dependencies-Zero-orange.svg?style=for-the-badge)](#)

<p align="center">
  <img src="divisibility_by_9.gif" alt="9 的倍數判別法幾何動畫演示 (Divisibility by 9 Animation)" width="760" style="max-width: 100%; border-radius: 12px; box-shadow: 0 4px 16px rgba(0,0,0,0.15);" />
</p>

> 國中／國小數學《倍數判別法》幾何動態視覺化教學工具（支援**繁體中文**與**全英文**雙語切換）！  
> 將抽象的十進位位值與代數拆解，轉換為生動的**幾何積木方塊分組**與**逐步算式推導動畫**，讓學生一眼看懂「為什麼倍數判別法會成立」。
> 
> *An interactive visual proof and animation tool for Divisibility Rules (2, 4, 8, 3, 9, 11, and 7), featuring geometric block grouping, step-by-step algebraic derivations, and bilingual (English / Traditional Chinese) support.*

🔗 **線上即時體驗網址 (Live Demo)**：[https://cconecone-cmyk.github.io/divisibility-rules/](https://cconecone-cmyk.github.io/divisibility-rules/)  
🌐 **Direct English Link (直接開啟英文版)**：[https://cconecone-cmyk.github.io/divisibility-rules/?lang=en](https://cconecone-cmyk.github.io/divisibility-rules/?lang=en)

---

## ✨ 核心特色 (Key Features)

1. **雙語一鍵即時切換 (Instant Bilingual Switching)**
   - 頂部導航列內建 `🌐 EN` / `🌐 中文` 語系切換按鈕。
   - 所有介面、按鈕、提示、數學口訣、幾何圖卡與逐步算式皆提供道地繁體中文與全英文雙語，並會自動記憶於 `localStorage`。
   - 支援網址參數直接指定語系：`?lang=en` 或 `?lang=zh`。
2. **幾何方塊視覺化拆解 (Geometric Visual Proofs)**
   - **個位、十位（長條）、百位（百數板）、千位以上（3D 立體方塊 SVG）** 實體呈現。
   - 動態演示「整除部分分組打包」與「多出來或不足的方塊進行飛行動畫集中統計」。
3. **算式同步逐步推導 (Step-by-Step Algebraic Proofs)**
   - 右側同步顯示嚴謹代數拆解步驟（例如 $100 = 99 + 1$、$1000 = 1001 - 1$）。
   - 步驟間具備平滑過渡高亮，老師講課免板書、學生理解無門檻。
4. **雙展示模式（響應式佈局）(Projector & Mobile Dual Layouts)**
   - 📺 **投影模式（Projector）**：左右分欄（大方塊圖 ＋ 大字體算式），適合電子白板與教室大型觸控螢幕。
   - 📱 **手機模式（Mobile）**：垂直最佳化排版，學生平板或家長手機隨開即練。
5. **手勢縮放與大圖／大算式切換 (Pan, Zoom & Focus Modes)**
   - 支援滑鼠滾輪、觸控雙指縮放（Pinch-to-zoom）與平移拖曳。
   - 一鍵切換「⤢ 大圖模式」或「⤢ 大算式模式」，聚焦細節。
6. **自由輸入與智慧隨機出題 (Custom Numbers & Random Generator)**
   - 可直接在輸入框輸入任意數值（支援 6 位數，7 的倍數支援至 12 位數）。
   - 內建精選題庫按鈕與 🎲 隨機出題功能（自動包含整除與不整除對照案例）。
7. **URL 參數直接分享題型 (Shareable URL Deep Linking)**
   - 老師可直接產生特定題目的連結分享至 Google Classroom、Padlet 或 LINE：
     - `?lang=en&r=11&n=9724`（英文版 11 的倍數演示）
     - `?r=7&n=366415`（7 的三位分節法）
     - `?r=3&n=1234`（3 的倍數餘數原理）

---

## 📐 數學判別法原理總覽 (Divisibility Rules Overview)

| 規則 (Rule) | 判別口訣 (Criterion) | 幾何與十進位拆解原理 (Mathematical Rationale) |
| :--- | :--- | :--- |
| **2 的倍數**<br>*(Divisible by 2)* | 個位數是 $0, 2, 4, 6, 8$（偶數）<br>*Last digit is even* | $10 = 2 \times 5$、$100 = 2 \times 50$，十位以上的數一定能被 $2$ 整除，故只需檢視個位。<br>*Since $10^k$ is divisible by 2 for $k \ge 1$, all higher places drop out.* |
| **4 的倍數**<br>*(Divisible by 4)* | 末兩位數是 $4$ 的倍數（或 $00$）<br>*Last 2 digits form a multiple of 4* | $100 = 4 \times 25$、$1000 = 4 \times 250$，百位以上的數必能被 $4$ 整除，故只需檢視末兩位。<br>*$100$ is divisible by 4; only the tens and ones places matter.* |
| **8 的倍數**<br>*(Divisible by 8)* | 末三位數是 $8$ 的倍數（或 $000$）<br>*Last 3 digits form a multiple of 8* | $1000 = 8 \times 125$，千位以上的數必能被 $8$ 整除，故只需檢視末三位。<br>*$1000$ is divisible by 8; only the hundreds, tens and ones matter.* |
| **3 的倍數**<br>*(Divisible by 3)* | 各個數位數字和是 $3$ 的倍數<br>*Sum of digits is a multiple of 3* | $10 = 9 + 1$、$100 = 99 + 1$、$1000 = 999 + 1$，將每個位值拆出 $3$ 的倍數後，各剩下 $1$ 個方塊，集合後即為「數字和」。<br>*$10^k = (10^k - 1) + 1$; each unit leaves an extra 1.* |
| **9 的倍數**<br>*(Divisible by 9)* | 各個數位數字和是 $9$ 的倍數<br>*Sum of digits is a multiple of 9* | 原理同 $3$ 的倍數：$9, 99, 999$ 皆為 $9$ 的倍數，剩下的方塊總數就是各位數字和。<br>*Analogous to 3: $10^k \equiv 1 \pmod 9$.* |
| **11 的倍數**<br>*(Divisible by 11)* | 「奇數位和」與「偶數位和」之差為 $11$ 的倍數或 $0$<br>*(Odd sum − Even sum) is divisible by 11* | $10 = 11 - 1$（偶數位少 1）、$100 = 99 + 1$（奇數位多 1）、$1000 = 1001 - 1$（偶數位少 1），「多出來的」與「不足的」互相抵消。<br>*$10 \equiv -1 \pmod{11}$, causing alternating signs $+1, -1, +1, -1$.* |
| **7 的倍數** *(補充)*<br>*(Divisible by 7)* | **三位分節法**：從個位起每三位一節，「奇數節和 − 偶數節和」為 $7$ 的倍數或 $0$<br>*3-digit blocks alternating sum* | $1001 = 7 \times 11 \times 13$，而 $1000 = 1001 - 1$、$10^6 = 1001 \times 999 + 1$，一加一減交替抵消！同一個差亦可用於判別 $11$ 與 $13$。<br>*Since $1000 \equiv -1 \pmod{1001}$, 3-digit blocks alternate signs modulo 7, 11, and 13.* |

---

## ⌨️ 鍵盤快捷鍵指南 (Keyboard Shortcuts)

| 快捷鍵 (Key) | 功能 (Action) |
| :---: | :--- |
| `→` / `PageDown` / `Space` / `Enter` | **下一步 (Next step)**（觸發分組與飛行動畫） |
| `←` / `PageUp` / `Backspace` | **上一步 (Previous step)** |
| `P` | **自動連續播放 / 暫停 (Play / Pause)** |
| `+` / `=` | 放大視圖 (Zoom in) |
| `-` / `_` | 縮小視圖 (Zoom out) |
| `0` | 還原 100% 縮放比例 (Reset zoom) |
| `G` | 切換 **大圖模式 (Diagram layout)** |
| `E` | 切換 **大算式模式 (Formulas layout)** |
| `F` | 切換 **全螢幕模式 (Fullscreen)** |

---

## 🚀 本地端運行 (Local Running)

本專案為零依賴的純原生 Web 應用（HTML5 + CSS3 + Vanilla JavaScript），無須 Node.js 或建置打包流程：

```bash
# 複製專案
git clone https://github.com/cconecone-cmyk/divisibility-rules.git

# 進入資料夾
cd divisibility-rules

# 直接用任何瀏覽器打開 index.html
start index.html # Windows
open index.html  # macOS
```

---

## 📄 授權條款 (License)

MIT License - 歡迎各級學校教師、學生與教育工作者自由分享與教學使用。
