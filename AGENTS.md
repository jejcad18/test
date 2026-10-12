# Copilot Instructions
- 專案：test，AI 測試小助手專案
- 技術堆疊：Next.js (App Router)、TypeScript (Strict)、Tailwind CSS、shadcn/ui、Supabase
- 動手前先讀 ARCHITECTURE.md：第 3 節查檔案位置，第 4 節查新增功能的流程
- 畫面元件只負責顯示；Supabase 查詢一律寫在 `lib/[feature_name]/`
- 安全：遵守 ARCHITECTURE.md 第 5 節三條紅線；金鑰與 `.env*` 不可提交
- 介面文字與註解用繁體中文與台灣用語（對照表在 ARCHITECTURE.md 第 8 節）
- 不新增 ARCHITECTURE.md 第 2 節以外的套件，需要時先詢問
- 開 PR 前執行 `npm run lint`、`npm run test:unit`、`npx playwright test`
- Commit 採 Conventional Commits（`feat:`、`fix:`、`refactor:`、`test:`）
