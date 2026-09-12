# 兒童發展敏感期互動甘特圖

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

蒙特梭利敏感期互動甘特圖 — 以年齡滑桿觀察 0–7 歲兒童的 14 個發展敏感期，即時顯示爆發高峰期、行為訊號、家長引導建議及居家活動。單一 HTML 檔案，零依賴、可離線列印。

## 功能

- 🕰️ **互動觀測時光機** — 滑桿或快速焦點按鈕，切換孩子年齡（0–7 歲，精確至月）
- 📊 **甘特時序圖** — 14 個敏感期的全期與高峰範圍，紅色垂直指示線即時連動
- 🗂️ **類別篩選** — 身體動作 / 感官秩序 / 語言讀寫 / 社交情緒 / 數學認知
- 🔥 **爆發高峰標記** — 高峰項目置頂排序、脈動動畫，可「僅顯示高峰期」
- 📋 **深度行為解碼** — 點擊長條或卡片，開啟行為訊號 / 發展密碼 / Do & Don't / 教具建議
- 🖨️ **列印／存檔** — 原生 print，適合製成育兒參考表

## 架構

```
index.html   — 單一檔案應用（Tailwind CDN + 內嵌 CSS / 資料 / 邏輯）
```

- 資料：`SENSITIVE_PERIODS_DATA`（14 個情境，含 `startAge/endAge/peakStart/peakEnd`）
- 邏輯：`renderGanttRows()` → `renderActiveCards()` → `openDetailModal()`
- 範疇參考：蒙特梭利（Maria Montessori）與現代發展心理學；年齡為統計常模，個體差異屬正常

## 運行

直接開啟或任何靜態伺服器：

```bash
python3 -m http.server 8000
# 瀏覽 http://localhost:8000/index.html
```

無需構建、無需 API key、無後端。

## License

MIT © 2026 forumdata-collab — 詳見 [LICENSE](LICENSE)