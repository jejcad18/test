# Skill: article-to-json

## Description
收集文章網址、文字內容或網頁截圖，解析出文章的元資料（URL、標題、作者、發布日期），並提取合適的標籤，最後結構化寫入工作區根目錄的 articles.json。

## Target File
`articles.json`（位於專案根目錄）

## Output JSON Schema
[
  {
    "url": "string (文章網址)",
    "title": "string (文章標題)",
    "author": "string (作者姓名)",
    "published_at": "string (格式: YYYY-MM-DD)",
    "tags": ["string (標籤1)", "string (標籤2)"]
  }
]

## Instructions & Rules
1. 資訊收集與驗證：
   - 優先從使用者提供的網址讀取內容；若網站有反爬蟲機制（如 Medium / Towards Data Science），改以使用者上傳的文字或截圖為準。
   - 若使用者未提供 URL 或截圖，或截圖內容模糊不完整，必須主動提問並請使用者補齊資訊。
2. 標籤與摘要處理：
   - 根據文章內容或截圖主題提煉 2~5 個繁體中文或英文核心標籤（tags）。
   - 去除長篇摘要（summary），專注於元資料與標籤提取。
3. 寫入規範：
   - 讀取現有的 articles.json 檔案。
   - 將新解析出的物件追加（Append）到 JSON 陣列中，避免覆蓋既有資料。
   - 格式必須為標準 JSON，保持縮排與逗號正確性。
