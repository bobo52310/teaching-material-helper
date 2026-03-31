# 教材小幫手 ✂️📸

> 上傳照片，AI 幫你把物件一個一個切出來，生成雙語教學圖卡！

一款 **100% 在瀏覽器端運行** 的 AI 教學圖卡工具，使用 [Transformers.js](https://huggingface.co/docs/transformers.js) 進行物件偵測，完全免費、不需註冊、不會上傳任何照片。

## 功能特色

### AI 自動偵測
- 辨識照片中 80+ 種常見物件（COCO 資料集）
- 可調整偵測靈敏度（30% - 95%）
- 自動裁切並生成獨立圖片
- 原圖偵測框視覺化（彩色 bounding box + 名稱標籤）

### 多圖批次處理
- 一次上傳多張照片，AI 逐張分析
- 縮圖預覽管理：新增、刪除、追加
- 所有偵測結果合併顯示

### 雙語教學圖卡
- 中英文對照顯示
- 內建語音發音（TTS）：先唸英文再唸中文
- 可點擊編輯名稱，老師可自訂修改

### 學習模式（Flashcard）
- 翻牌式學習：先看圖猜名稱，翻轉揭曉答案
- 支援鍵盤操作（← → 切換、Space 翻轉、Esc 關閉）
- 內建發音功能

### 匯出與分享
- 單張下載 / 全部下載 PNG 圖片
- 一鍵複製詞彙清單到剪貼簿
- **Quizlet 匯出**：TSV 格式，可直接匯入 Quizlet
- **Anki 匯出**：含圖片的 HTML 格式，匯入 Anki 建立閃卡
- **測驗卷生成器**：自動生成「看圖寫名稱」測驗卷（含字庫）
- 列印友善模式（自動隱藏非必要元素）

### 隱私與安全
- 100% 瀏覽器端執行，照片不會上傳
- 不需 API Key、不需註冊帳號
- AI 模型首次下載後自動快取（約 40 MB）
- PWA 支援：可安裝到手機桌面

## 使用方式

1. 開啟 `index.html`（或部署到任何靜態網頁空間）
2. 上傳照片（可多選）或用相機拍照
3. 調整偵測靈敏度（預設 70%）
4. 點擊「AI 自動偵測並切割物件」
5. 使用結果：
   - 下載圖片 / 複製詞彙清單
   - 進入學習模式複習
   - 匯出到 Quizlet / Anki
   - 生成測驗卷列印

## 技術架構

| 項目 | 技術 |
|------|------|
| 前端 | Vanilla HTML/CSS/JavaScript（單一檔案，無需建構工具） |
| AI 模型 | DETR ResNet-50 via Transformers.js |
| 語音 | Web Speech API (SpeechSynthesis) |
| 離線支援 | Service Worker + PWA Manifest |
| 部署 | 靜態檔案（GitHub Pages / Vercel / 任何 HTTP 伺服器） |

## 本地開發

無需任何建構工具，直接開啟即可：

```bash
# 方法一：直接開啟
open index.html

# 方法二：使用本地伺服器（推薦，避免 CORS 問題）
npx serve .
```

## 瀏覽器支援

需要支援 WebAssembly 的現代瀏覽器：
- Chrome 80+
- Firefox 80+
- Safari 15+
- Edge 80+

## 授權

MIT License
