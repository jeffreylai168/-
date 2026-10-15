# 事審救星｜健保給付條件速查（PWA）v2.1.0

## 檔案
| 檔案 | 用途 |
|---|---|
| index.html | App 主程式 |
| rules-builtin.js | 內建健保署藥品給付規定全文（1150922 版）：通則、630 條條文、86 份附表 |
| manifest.webmanifest | 安裝設定（名稱、圖示、全螢幕） |
| sw.js | Service Worker，離線快取 App 本體 |
| icons/ | PNG 圖示（iOS 180、Android 192/512、maskable） |

## 部署到 GitHub Pages
1. GitHub 建一個新 repo（例：`shishen`），把本資料夾全部檔案（含 icons/）上傳到根目錄。
2. Settings → Pages → Source 選 `Deploy from a branch`，Branch 選 `main` / `(root)` → Save。
3. 約 1 分鐘後網址為 `https://<帳號>.github.io/shishen/`。
4. 手機開啟該網址安裝：iPhone 用 Safari「分享 → 加入主畫面」；Android Chrome 點「安裝」。

## 改版
- 更新內容後，把 `sw.js` 的 `CACHE` 版本號加一（例 `shishen-v2.1.1`），使用者開啟時會出現「有新版本可用」。
- 健保署改版條文：不必改程式，在 App「離線條文庫」貼上新版全文即可（匯入內容優先於內建原文）。

## 注意
- 直接雙擊 index.html（file://）可以瀏覽，但不能安裝、不能離線快取；需放在 HTTPS 網址。
- 收藏與匯入的條文存在各裝置本機，不會跨裝置同步；清除瀏覽器網站資料會一併清除。
