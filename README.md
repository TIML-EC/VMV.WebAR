# WebAR 骰子專案 (MindAR + A-Frame)

這是一個專為流動裝置開發的 WebAR 網頁。當相機辨識到特定的 Logo 時，會顯示一個帶有文字的六面骰子。

## 功能特點
- **Logo 追蹤**：辨識指定 Logo 並在其上呈現 AR 內容。
- **3D 骰子**：六面分別帶有「客」、「新」、「科」、「越」、「團」、「精」文字。
- **手勢操作**：支援單指旋轉、雙指縮放骰子。
- **拍照功能**：一鍵捕捉 AR 畫面與相機背景並儲存。

## 部署說明 (GitHub Pages)

1. **準備 Logo 訓練檔**：
   - 由於瀏覽器安全性限制，你需要先將你的 `logo.png` 編譯成 MindAR 可讀取的 `.mind` 格式。
   - 前往 [MindAR Image Target Compiler](https://hiukim.github.io/mind-ar-js-doc/tools/compile)。
   - 上傳你的 `logo.png` 並點擊 "Compile"。
   - 下載編譯後的 `targets.mind` 檔案，並將其放入本專案的根目錄中。

2. **上傳至 GitHub**：
   - 將 `index.html`、`targets.mind` 和 `logo.png` 上傳到你的 GitHub 儲存庫。

3. **啟用 GitHub Pages**：
   - 在 GitHub 儲存庫的 **Settings** > **Pages** 中，選擇 `main` 分支並儲存。
   - 稍等幾分鐘，GitHub 會提供一個 HTTPS 的網址（例如 `https://yourname.github.io/your-repo/`）。

## 如何使用
1. 使用流動裝置（iOS/Android）瀏覽器開啟部署後的網址。
2. 授權使用相機。
3. 將相機對準你的 Logo 圖片。
4. 看到骰子後：
   - **旋轉**：在螢幕上滑動。
   - **縮放**：使用兩指撥動。
   - **拍照**：點擊下方的白色圓形按鈕。

## 技術棧
- [A-Frame](https://aframe.io/) - WebVR/AR 框架
- [MindAR](https://github.com/hiukim/mind-ar-js) - 高效能 Image Tracking 庫
- [aframe-gesture-detector](https://github.com/fcor/aframe-gesture-detector) - 手勢控制組件

## 注意事項
- 必須在 **HTTPS** 環境下執行，否則無法啟動相機。
- 建議使用 Chrome (Android) 或 Safari (iOS)。
