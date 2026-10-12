# Skill: article-to-json

## 說明
收集文章網址、內容或截圖，解析出文章的網址 (url)、標題 (title)、作者 (author)、發佈日期 (published_at) 與繁體中文標籤 (tags)。

## 輸出格式
將解析結果寫入工作區根目錄的 `articles.json`，格式如下：
```json
[
  {
    "url": "文章網址",
    "title": "文章標題",
    "author": "作者",
    "published_at": "YYYY-MM-DD",
    "tags": ["標籤1", "標籤2"]
  }
]
