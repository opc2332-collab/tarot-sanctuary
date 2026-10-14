# Tarot Sanctuary v3.0

繁體中文靜態塔羅網站：78 張經典偉特牌、1/3/5/10 張牌陣、正逆位、牌義與行動提示、ChatGPT 解牌提示、localStorage 日誌、回顧、搜尋、JSON 匯入/匯出及 CSV 匯出。無登入、無每日通知、無付費 API。

## 本機啟動

請勿直接以 `file://` 雙擊開啟 `index.html`，因為部分瀏覽器禁止從本機檔案讀取 `cards.json`。

安裝 Python 後，在本資料夾執行：

```bash
python -m http.server 8000
```

然後開啟 `http://localhost:8000`。

## 部署固定網址

**GitHub Pages**：將本資料夾所有檔案上傳至 GitHub repository 根目錄，進入 Settings → Pages，選擇 Deploy from a branch / main / root，儲存後使用 Pages 網址。

**Netlify**：將本資料夾整個拖曳至 Netlify Drop，即可取得 HTTPS 網址。

本網站無需環境變數、資料庫或 build 步驟。請使用 HTTPS 以支援剪貼簿 API 與加密亂數。

## 圖片與授權

卡牌圖片由 Wikimedia Commons 線上載入：
https://commons.wikimedia.org/wiki/Category:Rider-Waite-Smith_tarot_deck_(TaionWC)

此來源為 Pamela Colman Smith 的早期 Rider–Waite–Smith 牌組掃描。每張圖像的具體權利狀態與條款請以 Commons 的檔案說明頁為準；請勿將現代重新上色版本視為公版。**圖片沒有打包在 ZIP 內**，需要網路連線，若外部來源失效則以文字牌面替代。

## 隱私與限制

- 占卜日誌只存本機瀏覽器 localStorage，無跨裝置同步。請定期備份 JSON。
- 只有主動複製並貼至 ChatGPT 時，問題與抽牌結果才會提供給 ChatGPT。
- 無 AI API 串接。網站內提供簡短牌義，深度解讀由使用者貼入 ChatGPT。
- 塔羅屬反思用途，不能作為確定性預測。

## 測試範圍

靜態檔案、牌庫數量與唯一性、JavaScript 語法與 ZIP 完整性可自動檢查；實際 iPhone Safari / GitHub Pages / Netlify 發布需在目標裝置或帳號操作後確認。
