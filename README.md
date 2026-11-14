# 一郎宴會館 一頁式網站

網站只有一個檔案 `index.html`，照片都放在 `images` 資料夾。所有更新都可以在 GitHub 網頁上直接完成，不用安裝軟體。

---

## 基本步驟：改文字

1. 在儲存庫首頁點 `index.html`。
2. 按右上角的**鉛筆圖示**（Edit this file）。
3. 按 `Ctrl + F`（Mac 用 `Cmd + F`）搜尋要改的文字或標記。
4. 改好後，按右上角綠色的 **Commit changes**，再按一次確認。
5. 等 1 到 2 分鐘，重新整理網站，就會看到更新。

> 只改中文字、價格和日期，`<` `>` 符號和英文代碼都不要動。改壞了也沒關係，GitHub 會保留每一個舊版本，可以還原。

---

## 菜單 PDF（menu 資料夾）

每份菜單一個固定檔名。要換菜單，只要上傳**同檔名**的新 PDF 到 `menu` 資料夾，不用改程式碼。

| 檔名 | 內容 | 何時換 |
|---|---|---|
| menu.pdf | 當季桌菜菜單 | 換季時（春夏、秋冬） |
| weiya.pdf | 尾牙春酒特別菜單 | 每年尾牙季前 |

PDF 請控制在 2MB 以下。換菜單時，網頁上同一張卡片的價格文字也要一起改（見下方）。

---

## 新年專區

搜尋 `新年專區 開始`。這一區在 `data-end` 的日期（目前是 2027-02-10，初五）過後會自動隱藏。

每年要做的事：

1. 換三張海報：`images/51-cny-eve.jpg`、`52-cny-day3-5.jpg`、`53-cny-takeout.jpg`（整張海報顯示，不裁切，點擊可放大）
2. 在 `index.html` 改標題年份，並把 `data-end` 改成新一年的初五

---

## 時令專區（目前是大閘蟹）

搜尋 `時令專區 開始`。換菜時改 `<h3>` 的菜名和 `<p>` 的說明、價格；照片上傳同名檔 `images/17-seasonal.jpg`。
這一區不會自動隱藏，換菜或下架都要手動改。要暫時拿掉，從 `▼ 時令專區 開始` 選到 `▲ 時令專區 結束` 整段刪除。

---

## 頂端公告列

搜尋 `頂端公告 開始`。改 `<b>` 和 `</b>` 中間的文字、`href`（要跳到哪一區），以及 `data-end` 的日期。過了結束日會自動隱藏。

---

## 首屏輪播

首屏兩張照片每 3 秒自動切換，先出現 `images/02-hero.jpg`（門口造景），再換 `images/01-hero.jpg`（主宴會廳）（直式 4:5，建議 1200×1500）。

---

## Google 評分

首屏的「★ 4.1｜Google 評論 2,642 則」是手動更新的數字，不會自動變動。
建議每季到 Google 地圖看一次，在 `index.html` 搜尋 `Google 評論` 修改分數和則數。

---

## 換照片

照片都已對應檔名，**上傳同檔名的照片就會自動換上**。完整清單見 `一郎宴會館網站_照片管理清單.xlsx`。
還缺照片的位置（目前顯示灰色框）：`23-family.jpg`（家族聚餐）、`25-catering.jpg`（外燴）、`41-building.jpg`（大樓外觀）。

上傳方法：打開 `images` 資料夾 → **Add file** → **Upload files** → 拖進照片 → **Commit changes**。

- 檔名要完全一樣，包括小寫和 `.jpg`。
- 每張照片壓縮到 300KB 以下（squoosh.app 或 tinypng.com）。
- 照片裡有客人正臉的，要先取得同意。

---

## 頁尾社群圖示

頁尾的 Facebook、Instagram、LINE 目前顯示文字。到各品牌官方的品牌資源頁下載 Logo，存成以下檔名、上傳到 `images` 資料夾，就會自動換成 Logo，Facebook、Instagram 會統一顯示成白色，LINE 保留原本的綠色：

- `icon-facebook.svg`
- `icon-instagram.svg`
- `icon-line.svg`

（也可以用 `.png`，但要把 `index.html` 裡對應的 `.svg` 改成 `.png`。）

---

## 個資蒐集告知

在 `index.html` 搜尋 `個資蒐集告知`，可以修改公司名稱、保存期間與聯絡信箱。

---

## 正式上線前

- [ ] 搜尋 `noindex`，把那一行改成 `<meta name="robots" content="index,follow,max-image-preview:large">`，Google 才會開始收錄。
- [ ] 搜尋 `G-XXXXXXXXXX`（共兩處），換成 GA4 評估 ID。
- [ ] 決定網域後，把所有 `https://yslu-prog.github.io/ichiro-site/` 換成新網址。
- [ ] 確認 `robots.txt`、`sitemap.xml` 已一起上傳；換網域時，這兩個檔案裡的網址也要改
- [ ] 搜尋 `todo`，換好照片後通知 Claude 拿掉紅色「待更新」框
- [ ] 上線後到 Google Search Console 提交網址（含 sitemap.xml），並在 Google 商家檔案填入網站連結。
