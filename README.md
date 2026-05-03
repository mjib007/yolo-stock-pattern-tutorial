# 📊 YOLOv8 股票圖形辨識教材

> 用 AI 物件偵測模型,自動辨識 K 線圖中的技術型態(W底、M頭、頭肩頂...)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mjib007/yolo-stock-pattern-tutorial/blob/main/yolo_stock_pattern_tutorial.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)

---

## 🎯 教材簡介

這份教材帶你**用 30 分鐘**體驗一個完整的 AI 應用流程:

```
yfinance 抓股票資料 → mplfinance 畫 K 線圖 → YOLOv8 辨識圖形 → 產出標註結果
```

不需要訓練模型、不需要懂深度學習,**直接用別人訓練好的模型**完成圖形辨識實驗。

<img src="[https://scontent.frmq3-3.fna.fbcdn.net/v/t39.30808-6/516072468_10161540608047966_3151668797035823074_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=13d280&_nc_ohc=_8XUwDZedycQ7kNvwHrPnuA&_nc_oc=Adp1QhAagocX3xfaPVPc8gHWidwDrlwWEvuBeDmw0f391nVyomtnKYlmRrrHGfAeiV4JG5TbJGJz13UIrQLBdkRh&_nc_zt=23&_nc_ht=scontent.frmq3-3.fna&_nc_gid=UH_zeZxtA2zkSzXOKY2Xpw&_nc_ss=7b2a8&oh=00_Af7d28rPRLWBUgDczBbLQoTM_uW5TlknCbplAi-QNfFtCA&oe=69FC9BC8](https://scontent.frmq3-3.fna.fbcdn.net/v/t39.30808-6/690961251_10162792620682966_128958133316489642_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=13d280&_nc_ohc=onbboDMhagkQ7kNvwFLP5uj&_nc_oc=AdrrMXl-1i6XwVoNbVTdpI_X-OJSHCHcVMzx-wrx2sHuO5rlEzIEp_Cr_v5paAjoM2yEwTfiZBKWSeYxqwtrdEBC&_nc_zt=23&_nc_ht=scontent.frmq3-3.fna&_nc_gid=haSMmqm8NEJAcwMcQVXplQ&_nc_ss=7b2a8&oh=00_Af6NfMsRADxVQDHvaa5xmqnxYbsCIllRs8LWsdCG4y3qUA&oe=69FD962B)" width="30%">


## 🚀 一鍵開啟(零安裝)

點擊上方 **"Open in Colab"** 按鈕,在瀏覽器直接執行,**完全不需要在電腦上安裝任何東西**。

## 📋 你會學到什麼

- ✅ 怎麼用 `yfinance` 抓台股、美股資料
- ✅ 怎麼用 `mplfinance` 畫專業 K 線圖
- ✅ 怎麼從 HuggingFace Hub 下載預訓練模型
- ✅ 怎麼用 YOLOv8 做物件偵測推論
- ✅ 三組對照實驗:**期間影響、市場差異、訓練資料分布**對 AI 辨識結果的影響

## 📊 模型可辨識的 6 種圖形

| 英文標籤 | 中文 | 多空意義 |
|---------|------|---------|
| Head and shoulders bottom | 頭肩底 | 看漲反轉 |
| Head and shoulders top | 頭肩頂 | 看跌反轉 |
| M_Head | M 頭 | 看跌反轉 |
| W_Bottom | W 底 | 看漲反轉 |
| Triangle | 三角形 | 整理型態 |
| StockLine | 趨勢線 | 持續性走勢 |

> 💡 模型實際對 Triangle 與 StockLine 的辨識力較弱,教材中會帶你親自驗證這個現象。

## 📚 教材結構

| 章節 | 內容 |
|------|------|
| Step 0~1 | 環境準備 + 套件安裝 |
| Step 2~3 | HuggingFace 授權 + Token 登入 |
| Step 4~6 | 下載模型 + 認識標籤 + 定義函式 |
| Step 7 | 🧪 實驗 A:6 檔台股 6 個月 |
| Step 8 | 🧪 實驗 B:同股票 1 年期間 |
| Step 9 | 🧪 實驗 C:美股對照組 |
| Step 10 | ✏️ 自訂股票測試 |

## 🛠️ 技術堆疊

| 套件 | 用途 |
|------|------|
| [ultralytics](https://github.com/ultralytics/ultralytics) | YOLOv8 模型載入與推論 |
| [mplfinance](https://github.com/matplotlib/mplfinance) | 金融 K 線圖繪製 |
| [yfinance](https://github.com/ranaroussi/yfinance) | Yahoo Finance 資料抓取 |
| [huggingface_hub](https://github.com/huggingface/huggingface_hub) | 模型下載 |

## 📖 使用模型

本教材使用以下預訓練模型(由 FODUU AI 提供):

🤗 [foduucom/stockmarket-pattern-detection-yolov8](https://huggingface.co/foduucom/stockmarket-pattern-detection-yolov8)

> ⚠️ 模型需先到 HuggingFace 接受授權條款才能下載,教材中有完整步驟說明。

## 🎓 適合對象

- 想體驗 AI 物件偵測技術的初學者
- 對「AI + 金融」應用有興趣的學員
- 想學會用預訓練模型解決實際問題的工程師
- 法律、財金背景想踏入 AI 領域的學員

## 💻 兩種執行方式

### 方式一:Google Colab(推薦)

點本頁開頭的 **"Open in Colab"** 按鈕,自動在瀏覽器開啟。

### 方式二:本地 Jupyter

```bash
# 1. 下載 Anaconda
# https://www.anaconda.com/download

# 2. 安裝必要套件
pip install ultralytics mplfinance yfinance huggingface_hub openpyxl

# 3. 開啟 Jupyter Notebook
jupyter notebook yolo_stock_pattern_tutorial.ipynb
```

## 📁 檔案結構

```
.
├── README.md                              ← 你正在看這份
├── yolo_stock_pattern_tutorial.ipynb      ← 主要教材
└── (執行後產生)
    ├── model/             ← YOLO 模型權重
    ├── charts/            ← K 線圖原圖
    └── detect_results/    ← YOLO 標註後的圖
```

## ⚠️ 重要警語

> 本教材僅為 AI 工具操作教學,**不構成任何投資建議**。
> 
> AI 圖形辨識結果存在誤差,實際投資決策請以人工判斷為主,並自負盈虧。
> 
> 特別注意:
> - 同一支股票在不同期間長度下,辨識結果可能完全不同
> - 高信心度結果不保證正確
> - Triangle 與 StockLine 兩種標籤實測上極少出現

## 🤝 回饋與貢獻

如果發現教材有任何錯誤、或有改進建議,歡迎透過 Issues 或 Pull Request 提出。

## 📜 授權

本教材採用 [MIT License](LICENSE)。

YOLO 模型本身的授權請見 [HuggingFace 模型頁面](https://huggingface.co/foduucom/stockmarket-pattern-detection-yolov8)。

## 🦞 關於本教材

本教材為 **MiniClaw(小龍蝦)** 個人 AI 助理生態系的研究成果之一,
從 AI 應用實作中抽取出獨立教材,作為公益教學用途。

## 🔗 相關連結

- 📦 模型來源:[FODUU AI on HuggingFace](https://huggingface.co/foduucom)
- 📚 YOLOv8 文件:[Ultralytics Docs](https://docs.ultralytics.com/)
- 📊 mplfinance 教學:[GitHub](https://github.com/matplotlib/mplfinance)

---

⭐ 如果這份教材對你有幫助,歡迎按個 Star 支持!
