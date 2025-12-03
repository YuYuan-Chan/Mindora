# 🚀 Mindora 實施路線圖

> **目標：2 週內推出 MVP，衝刺 Product Hunt Top 5**

---

## 📊 當前狀態評估

### ✅ 已完成
- [x] 項目概念與文檔
- [x] 技術選型（React + Vite）
- [x] 基礎配置檔案

### ⚠️ 需要改進
- [ ] README 需要重寫（參考 README_IMPROVED.md）
- [ ] 技術棧需要升級（參考 package_IMPROVED.json）
- [ ] 沒有實際代碼實現

### 🎯 關鍵缺失
1. **視覺資產：** 無 Logo、Demo、截圖
2. **核心功能：** 無心智圖渲染引擎
3. **AI 整合：** 無 Claude API 串接
4. **UI 實現：** 無任何前端組件

---

## 🗓️ 2 週衝刺計劃

### Week 1: MVP 開發 (Day 1-7)

#### Day 1-2: 基礎架構
```bash
# 任務清單
□ 升級 package.json（添加 Tailwind, Framer Motion, Zustand）
□ 設置 Tailwind 配置
□ 創建基礎文件結構
  └─ src/
     ├─ components/
     │  ├─ Layout.jsx
     │  ├─ Button.jsx
     │  └─ Input.jsx
     ├─ hooks/
     │  └─ useTheme.js
     ├─ store/
     │  └─ mindMapStore.js
     └─ utils/
        └─ claudeAPI.js

# 驗收標準
✓ npm run dev 可成功啟動
✓ Tailwind CSS 正常運作
✓ 基本 Layout 渲染
```

#### Day 3-4: Claude AI 整合
```javascript
// 任務：實現 AI 文章解析
□ 創建 Claude API 客戶端
□ 實現 Prompt Engineering
  - 輸入：文章文本
  - 輸出：JSON 格式的心智圖結構
□ 錯誤處理與重試機制
□ 測試 3 種語言（中/英/日）

// 測試用 Prompt
const MINDMAP_PROMPT = `
Analyze the following article and extract a mind map structure.
Return ONLY valid JSON in this format:
{
  "title": "Main topic (1 sentence)",
  "summary": "Brief summary",
  "branches": [
    {
      "title": "Branch 1",
      "children": [
        { "title": "Sub-item 1" },
        { "title": "Sub-item 2" }
      ]
    }
  ]
}

Article:
{ARTICLE_TEXT}
`;

// 驗收標準
✓ 成功調用 Claude API
✓ 返回正確的 JSON 結構
✓ 處理 API 錯誤（rate limit, 無效 key）
```

#### Day 5-6: 心智圖渲染
```bash
# 任務：實現互動式心智圖
□ 創建 MindMapCanvas 組件
  □ 根節點顯示
  □ 分支節點顯示
  □ 子節點顯示
  □ 連接線渲染

□ 實現基本互動
  □ 節點拖曳（react-draggable 或自行實現）
  □ 畫布縮放（滾輪）
  □ 畫布平移（拖曳空白處）

□ 樣式與動畫
  □ 節點展開動畫（Framer Motion）
  □ Hover 效果
  □ 主題切換（Dark/Light）

# 驗收標準
✓ 渲染包含 3 層結構的心智圖
✓ 可拖曳節點
✓ 主題切換流暢
```

#### Day 7: UI 完善
```bash
# 任務：完成 MVP 所有介面
□ 首頁
  □ Hero section（標題 + CTA）
  □ 文章輸入區（Textarea）
  □ 生成按鈕

□ 導航列
  □ Logo
  □ 主題切換器
  □ GitHub 連結

□ 導出功能
  □ 導出為 PNG（html2canvas）
  □ 導出為 JSON

# 驗收標準
✓ 完整使用流程：輸入 → 生成 → 互動 → 導出
✓ RWD（手機可用）
✓ 無明顯 bug
```

---

### Week 2: 優化與發佈 (Day 8-14)

#### Day 8-9: 美化與細節
```bash
□ 設計與實現 Logo（可用 Figma 或 AI 生成）
□ 錄製 Demo GIF
  - 工具：Screen to GIF (Windows) 或 Kap (Mac)
  - 時長：10 秒
  - 解析度：1200x800
  - 檔案大小：< 10MB

□ 拍攝 5 張產品截圖
  - Dark theme (2 張)
  - Light theme (2 張)
  - 功能特寫 (1 張)

□ 微動畫優化
  - 按鈕 hover 效果
  - 節點展開動畫
  - 頁面過場

□ 色彩調整
  - 確保 WCAG AA 對比度
  - 測試色盲模式（Chromatic 或 ColorOracle）
```

#### Day 10-11: 性能與測試
```bash
□ 性能優化
  □ 代碼分割（React.lazy）
  □ 圖片優化（WebP）
  □ 打包體積分析（vite-bundle-visualizer）
  □ Lighthouse 評分 > 90

□ 測試
  □ 跨瀏覽器測試（Chrome, Firefox, Safari, Edge）
  □ 手機測試（iOS Safari, Android Chrome）
  □ 長文章測試（5000+ 字）
  □ API 錯誤測試

□ Bug 修復
  □ 收集並修復所有已知 bug
```

#### Day 12: 部署與 SEO
```bash
□ 部署到 Vercel
  □ 連接 GitHub repo
  □ 設定環境變數（VITE_CLAUDE_API_KEY）
  □ 自訂域名（mindora.app，可選）

□ SEO 優化
  □ 設定 meta tags（title, description, OG image）
  □ 添加 favicon
  □ 設定 robots.txt 和 sitemap.xml
  □ Google Analytics 埋點

□ 文檔完善
  □ 更新 README（使用 README_IMPROVED.md）
  □ 創建 CHANGELOG.md
  □ 創建 CONTRIBUTING.md
```

#### Day 13: Product Hunt 準備
```bash
□ 註冊 Product Hunt Maker 帳號
□ 準備發佈素材
  □ Tagline: "Turn any article into beautiful mind maps in 3 seconds"
  □ Description (260 字)
  □ First Comment 草稿
  □ 上傳 Logo + Demo GIF + 截圖

□ 預熱
  □ Twitter 發佈 "Building in public" 貼文
  □ 邀請 10 位朋友註冊 PH 帳號
  □ 加入 Indie Hackers Discord

□ 排程發佈
  - 時間：週三 00:01 PST（台灣時間下午 3:01）
  - 檢查清單：所有素材上傳、URL 測試、API 額度充足
```

#### Day 14: 發佈日 🚀
```bash
# 00:01 PST - 發佈
□ 在 Product Hunt 上線
□ 發佈 First Comment

# 發佈後 1 小時
□ 分享到 Twitter（@ProductHunt tag）
□ 分享到 LinkedIn
□ 通知早期用戶投票

# 發佈後 6 小時
□ 回覆所有評論（目標回覆率 100%）
□ 監控 Analytics（修復任何 crash）
□ 在 Reddit r/SideProject 分享

# 發佈後 12 小時
□ 檢查排名（目標：Top 5）
□ 發佈到 Hacker News（Show HN）
□ 更新 README 加上 PH badge

# 發佈後 24 小時
□ 慶祝 🎉
□ 撰寫感謝貼文
□ 開始收集用戶反饋
```

---

## 🎯 各階段驗收標準

### MVP (Week 1 結束)
- [ ] ✅ 核心功能：輸入文章 → AI 生成 → 顯示心智圖
- [ ] ✅ 基本互動：拖曳、縮放、主題切換
- [ ] ✅ 導出：PNG + JSON
- [ ] ✅ RWD：手機可用
- [ ] ❌ 無需：多選、18 色、Chrome Extension

### Product Hunt Launch (Week 2 結束)
- [ ] ✅ 視覺完整度：Logo、Demo、截圖
- [ ] ✅ 性能：Lighthouse > 90
- [ ] ✅ 穩定性：無 critical bug
- [ ] ✅ 文檔：README、CONTRIBUTING
- [ ] ✅ 部署：Vercel + 自訂域名（可選）

---

## 💡 關鍵改進建議總結

### 1. **技術架構**

**❌ 原計劃：**
```javascript
// 純 inline styles
style={{ backgroundColor: '#1e293b', padding: '20px' }}
```

**✅ 建議改用：**
```javascript
// Tailwind CSS + 設計系統
className="bg-slate-800 p-6 rounded-xl shadow-2xl"
```

**理由：**
- 更易維護
- 設計一致性
- 檔案體積更小（Tailwind 自動 purge）
- 社群認可度高（Product Hunt 評委偏好）

---

### 2. **功能優先級**

**❌ 原計劃：**
```
□ Web App + Chrome Extension 同時開發
□ 18 色配色系統
□ 多選批次操作
□ Notion 全格式支援
```

**✅ MVP 優先級：**
```
1. ✅ 核心生成功能（必須）
2. ✅ 基本互動（必須）
3. ✅ 3 種主題（必須）
4. ⏸️ 多選操作（延後）
5. ⏸️ Chrome Extension（延後）
```

**理由：**
- Product Hunt 用戶重視「一個功能做到極致」
- 2 週內完成全功能不現實
- MVP 上線後根據反饋迭代

---

### 3. **視覺設計**

**❌ 原計劃：**
- 無設計系統
- 無 Logo
- 無 Demo

**✅ 必須完成：**
```
□ Logo（可用 AI 生成 + Figma 優化）
□ Demo GIF（10 秒，展示核心流程）
□ 5 張截圖（Dark/Light 各 2 張 + 特寫 1 張）
□ 一致的配色方案（參考 DESIGN_SYSTEM.md）
□ Glassmorphism 效果（毛玻璃卡片）
```

**參考產品（Product Hunt 熱門）：**
- [Linear](https://linear.app) - 極簡設計
- [Raycast](https://raycast.com) - 毛玻璃效果
- [Arc Browser](https://arc.net) - 漸層與動畫

---

### 4. **產品定位**

**❌ 原 README：**
> "Transform articles into beautiful, interactive mind maps with AI"
（太泛泛，缺乏差異化）

**✅ 改進版：**
> "Turn any article into beautiful mind maps in 3 seconds"
（明確數值承諾 + 強調速度）

**或更聚焦：**
> "AI mind maps for Zettelkasten note-takers"
（針對明確受眾）

**Product Hunt Tagline 公式：**
```
[動詞] + [名詞] + [差異化特點] + [數值承諾]

範例：
✅ "Turn articles into mind maps in 3 seconds"
✅ "ChatGPT for visual learners"
✅ "Notion-style mind maps powered by AI"
```

---

### 5. **README 改進**

**❌ 原 README 問題：**
- 功能清單過長（18 種功能）
- 無「Why Mindora?」區塊
- 無 Demo GIF 在最上方
- 缺少 Before/After 對比

**✅ 必須包含：**
```markdown
# 🧠 Mindora

<Demo GIF 在這裡 - 最重要！>

## Why Mindora?
**Before:** 30 minutes manual work
**After:** 3 seconds with AI

## Features (只列 3-5 個)
- AI-powered
- Beautiful by default
- Export ready

## Quick Start (越簡單越好)
npm install && npm run dev

## Demo (多張截圖)

## Tech Stack (簡潔列表)
```

**參考改進版：** `README_IMPROVED.md`

---

## 📦 必須完成的文件

### 優先級 P0（本週完成）
```bash
□ src/App.jsx              # 主應用
□ src/components/
  □ MindMapCanvas.jsx      # 心智圖畫布
  □ ArticleInput.jsx       # 文章輸入
  □ ThemeToggle.jsx        # 主題切換
□ src/utils/claudeAPI.js   # Claude 整合
□ tailwind.config.js       # Tailwind 配置
□ assets/logo.svg          # Logo
□ assets/demo.gif          # Demo
```

### 優先級 P1（下週完成）
```bash
□ README.md                # 更新為 README_IMPROVED.md
□ CHANGELOG.md             # 版本記錄
□ CONTRIBUTING.md          # 貢獻指南
□ assets/screenshots/      # 5 張截圖
```

### 優先級 P2（可選）
```bash
□ DESIGN_SYSTEM.md         # 設計系統文檔
□ PRODUCT_HUNT_STRATEGY.md # PH 策略
□ chrome-extension/        # Chrome 擴充功能（延後）
```

---

## ⚠️ 常見陷阱

### 1. 過度工程
```
❌ 開發一個完美的拖曳系統（花 3 天）
✅ 使用 react-draggable 套件（花 1 小時）

❌ 手刻狀態管理（花 2 天）
✅ 使用 Zustand（花 30 分鐘）
```

### 2. 完美主義
```
❌ Logo 必須完美（花 1 週找設計師）
✅ 用 Midjourney 生成 + Figma 優化（花 2 小時）

❌ 所有功能都要完美
✅ 核心功能可用即可，其他功能可迭代
```

### 3. 忽視行銷
```
❌ 埋頭開發到最後一天才準備素材
✅ 開發過程中同步錄製 Demo、截圖

❌ 發佈後才開始宣傳
✅ 提前 1 週預熱（Twitter、Indie Hackers）
```

---

## 📊 成功指標

### Week 1 結束
- [ ] MVP 可用（核心流程跑通）
- [ ] 至少 3 位朋友測試過
- [ ] 修復所有 critical bug

### Week 2 - Launch Day
- [ ] Product Hunt 發佈成功
- [ ] 前 6 小時獲得 50+ upvotes
- [ ] 24 小時內進入 Top 5

### Week 2 結束
- [ ] 1000+ website visits
- [ ] 100+ GitHub stars
- [ ] 50+ user feedback

---

## 🎁 Bonus: Quick Win Tips

### 1. 善用 AI 工具
```bash
# Logo 生成
Midjourney prompt: "minimalist brain icon logo,
purple gradient, modern tech style, white background"

# Demo GIF
錄製 → CloudConvert 壓縮 → 確保 < 10MB

# 截圖美化
使用 Cleanshot X (Mac) 或 ShareX (Windows)
添加陰影、圓角、背景漸層
```

### 2. 複製成功模式
```
研究 Product Hunt 過去 3 個月的 Top 10
分析共同點：
- Tagline 長度（平均 40-60 字符）
- Demo GIF 時長（8-12 秒）
- 首頁設計（Hero + 3 Features + CTA）
```

### 3. 社群預熱
```
發佈前 1 週：
- Twitter: "Building Mindora, an AI mind map tool..."
- Indie Hackers: "Launching on PH next week, feedback?"
- Reddit: "Show off Saturday" post

目標：累積 50 位關注者 → Launch day 投票
```

---

## 🎯 最終檢查清單（Launch Day 前）

### 技術
- [ ] 所有功能正常運作
- [ ] 手機版可用（RWD）
- [ ] Lighthouse 評分 > 85
- [ ] 無 Console errors
- [ ] API key 正確設定

### 視覺
- [ ] Logo 完成（SVG + PNG）
- [ ] Demo GIF 完成（< 10MB）
- [ ] 5 張截圖完成（1280x800）
- [ ] 設計系統一致（配色、字體、間距）

### 內容
- [ ] README 更新（參考 README_IMPROVED.md）
- [ ] Product Hunt Description 寫好
- [ ] First Comment 草稿完成
- [ ] Twitter 預熱貼文發佈

### 部署
- [ ] 部署到 Vercel（或 Netlify）
- [ ] 自訂域名設定（可選）
- [ ] HTTPS 正常運作
- [ ] 壓力測試（預期 1000+ UV）

---

<p align="center">
  <strong>🚀 Focus + Speed + Polish = Product Hunt Success</strong><br>
  <sub>Done is better than perfect. Ship it!</sub>
</p>
