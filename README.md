# 漂浮性水生植物 AR 課堂平台

四上自然 2-2「探索水生植物」的一節課活動。學生以小組操作浮萍水槽 AR、完成一張觀察學習單，再各自完成三題測驗。

## 課堂流程（40 分鐘）

| 時間 | 活動 |
| --- | --- |
| 3 分鐘 | 看任務問題並先預測浮萍會不會固定在原處 |
| 12 分鐘 | 小組掃描 AR 圖卡，觀察低、中、高水位 |
| 15 分鐘 | 小組完成並送出學習單 |
| 10 分鐘 | 個人完成三題測驗並看即時回饋 |

學習單與測驗都只處理漂浮性水生植物：浮萍隨水面升降、根沒有固定在水底，以及通氣組織如何幫助植物漂浮。

## 部署

### 1. 發佈 AR 素材到 GitHub Pages

GitHub 公開儲存庫已建立：<https://github.com/siasilvalining-max/nutn115-floating-plants>。
預定 Pages 網址：<https://siasilvalining-max.github.io/nutn115-floating-plants/>。

1. 將 `github-pages` 資料夾裡的 `index.html`、`duckweed_tank.glb`、`targets.mind` 和 `1029arcode.jpg` 放在儲存庫根目錄。
2. 到儲存庫 **Settings → Pages**，選擇 `main` 分支和根目錄發佈。
3. 發佈後學生可用上述 Pages 網址開啟 AR。Apps Script 的 `AR_BASE_URL` 已設為此網址。

GitHub Pages 是靜態網站服務，網站檔案會公開供學生讀取。此儲存庫只放 AR 網頁、3D 模型和 AR 圖卡，不放班級名冊或學生作答資料。

### 2. 設定並發佈 Google Apps Script 平台

1. 在 Apps Script 專案新增或替換 `Code.gs`、`Index.html`，並啟用 `appsscript.json` 的資訊清單檢視後貼入同名檔案。
2. `Code.gs` 的 `AR_BASE_URL` 已設為本專案的 GitHub Pages 網址；若改用其他帳號或儲存庫，才需要同步更新。
3. 在 Apps Script 編輯器選取 `setupTeacherStorage` 並執行一次。授權後，執行紀錄會顯示私有的作答試算表網址。
4. 選 **部署 → 新增部署作業 → 網頁應用程式**；以「我」身分執行，並設定學生可存取。Apps Script 部署完成後會提供平台網址。
5. 開啟部署網址，首頁的學生 QR code 會依平台網址自動產生。更新 Apps Script 後，請建立新版本再部署。

Apps Script 只記錄組別、學習單選項、簡短結論和測驗答案／分數，不收學生姓名。作答試算表由執行 `setupTeacherStorage` 的教師帳號建立；請由教師保管，不需分享給學生。

## AR 圖卡

`github-pages/1029arcode.jpg` 是 AR 圖卡。請原樣列印或顯示在另一台裝置上，再用平板開啟 AR 頁面掃描。AR 頁面會要求使用相機；需在 HTTPS 網址中開啟並允許相機權限。

## 教材依據

依使用者提供的南一版四上自然第 2 單元課本與習作「2-2 探索水生植物」設計：課本第 49 頁說明漂浮性水生植物的通氣組織，第 50–51 頁呈現水位變化下沉水植物的觀察對照；本平台把操作與題目集中在所選的漂浮性植物浮萍。未將課本頁面或其他組別作品放入網站。
