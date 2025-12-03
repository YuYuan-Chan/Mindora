# 🎨 Mindora Design System

> **設計理念：** "Beautiful by default, powerful when needed"

---

## 🌈 配色方案

### Primary Colors
```css
/* 主色調 - 紫色代表創意與思考 */
--primary-50:  #faf5ff;
--primary-100: #f3e8ff;
--primary-500: #8b5cf6;  /* 主要按鈕、連結 */
--primary-600: #7c3aed;  /* Hover 狀態 */
--primary-700: #6d28d9;  /* Active 狀態 */
```

### Accent Colors
```css
/* 強調色 - 青色代表科技感 */
--accent-400: #22d3ee;   /* 次要 CTA */
--accent-500: #06b6d4;   /* 圖標、標籤 */
--accent-600: #0891b2;   /* Hover */
```

### Neutral Colors
```css
/* 中性色 - 用於文字和背景 */
--gray-50:  #f9fafb;
--gray-100: #f3f4f6;
--gray-200: #e5e7eb;
--gray-500: #6b7280;  /* 次要文字 */
--gray-700: #374151;  /* 主要文字 */
--gray-900: #111827;  /* 標題 */
```

### Theme-Specific Colors

#### Dark Theme
```css
--bg-primary:   #0f172a;  /* 主背景 */
--bg-secondary: #1e293b;  /* 卡片背景 */
--bg-tertiary:  #334155;  /* 懸停背景 */
--text-primary: #f1f5f9;  /* 主要文字 */
--text-secondary: #94a3b8; /* 次要文字 */
--border: #475569;        /* 邊框 */
```

#### Light Theme
```css
--bg-primary:   #ffffff;
--bg-secondary: #f8fafc;
--bg-tertiary:  #f1f5f9;
--text-primary: #0f172a;
--text-secondary: #64748b;
--border: #e2e8f0;
```

#### Blue Theme (Tech-inspired)
```css
--bg-primary:   #0c1222;
--bg-secondary: #1a2332;
--bg-tertiary:  #2d3748;
--text-primary: #e0f2fe;
--text-secondary: #7dd3fc;
--border: #0ea5e9;
```

---

## 📐 間距系統

```css
/* 基於 8px 網格 */
--spacing-1:  0.25rem;  /* 4px  - 微小間距 */
--spacing-2:  0.5rem;   /* 8px  - 小間距 */
--spacing-3:  0.75rem;  /* 12px - 中小間距 */
--spacing-4:  1rem;     /* 16px - 標準間距 */
--spacing-6:  1.5rem;   /* 24px - 中等間距 */
--spacing-8:  2rem;     /* 32px - 大間距 */
--spacing-12: 3rem;     /* 48px - 特大間距 */
--spacing-16: 4rem;     /* 64px - 區塊間距 */
```

**使用指南：**
- 元素內部間距：`--spacing-3` ~ `--spacing-4`
- 卡片內邊距：`--spacing-6`
- 區塊間距：`--spacing-8` ~ `--spacing-12`

---

## 🔤 字體系統

### Font Family
```css
--font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'Fira Code', 'JetBrains Mono', monospace;

/* 中文優化 */
--font-zh: 'Noto Sans TC', 'PingFang TC', 'Microsoft JhengHei', sans-serif;
```

### Font Sizes
```css
--text-xs:   0.75rem;  /* 12px - 標籤、註釋 */
--text-sm:   0.875rem; /* 14px - 次要文字 */
--text-base: 1rem;     /* 16px - 正文 */
--text-lg:   1.125rem; /* 18px - 強調文字 */
--text-xl:   1.25rem;  /* 20px - 小標題 */
--text-2xl:  1.5rem;   /* 24px - 中標題 */
--text-3xl:  1.875rem; /* 30px - 大標題 */
--text-4xl:  2.25rem;  /* 36px - 主標題 */
```

### Font Weights
```css
--font-normal:  400;
--font-medium:  500;  /* 按鈕、導航 */
--font-semibold: 600; /* 小標題 */
--font-bold:    700;  /* 主標題 */
```

### Line Heights
```css
--leading-tight:  1.25;  /* 標題 */
--leading-normal: 1.5;   /* 正文 */
--leading-relaxed: 1.75; /* 長段落 */
```

---

## 🎭 陰影系統

```css
/* Elevation levels */
--shadow-sm:  0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow-md:  0 4px 6px -1px rgb(0 0 0 / 0.1);
--shadow-lg:  0 10px 15px -3px rgb(0 0 0 / 0.1);
--shadow-xl:  0 20px 25px -5px rgb(0 0 0 / 0.1);
--shadow-2xl: 0 25px 50px -12px rgb(0 0 0 / 0.25);

/* 使用場景 */
.card { box-shadow: var(--shadow-md); }
.modal { box-shadow: var(--shadow-2xl); }
.dropdown { box-shadow: var(--shadow-lg); }
```

**Glassmorphism (毛玻璃效果):**
```css
.glass {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
}
```

---

## 📏 圓角系統

```css
--radius-sm:   0.25rem; /* 4px  - 標籤 */
--radius-md:   0.5rem;  /* 8px  - 按鈕 */
--radius-lg:   0.75rem; /* 12px - 卡片 */
--radius-xl:   1rem;    /* 16px - 面板 */
--radius-2xl:  1.5rem;  /* 24px - Modal */
--radius-full: 9999px;  /* 圓形 - Avatar */
```

---

## 🎬 動畫系統

### Timing Functions
```css
--ease-linear:     linear;
--ease-in:         cubic-bezier(0.4, 0, 1, 1);
--ease-out:        cubic-bezier(0, 0, 0.2, 1);
--ease-in-out:     cubic-bezier(0.4, 0, 0.2, 1);
--ease-spring:     cubic-bezier(0.34, 1.56, 0.64, 1); /* 彈性效果 */
```

### Durations
```css
--duration-fast:   150ms;  /* 懸停效果 */
--duration-normal: 300ms;  /* 一般動畫 */
--duration-slow:   500ms;  /* 大型轉場 */
```

### 常用動畫

**Fade In:**
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

**Slide Up:**
```css
@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
```

**Scale Bounce:**
```css
@keyframes scaleBounce {
  0% { transform: scale(1); }
  50% { transform: scale(1.05); }
  100% { transform: scale(1); }
}
```

**Framer Motion 預設配置:**
```javascript
// 推薦的 Motion 配置
export const fadeInUp = {
  initial: { opacity: 0, y: 20 },
  animate: { opacity: 1, y: 0 },
  transition: { duration: 0.3, ease: "easeOut" }
};

export const staggerChildren = {
  animate: {
    transition: {
      staggerChildren: 0.1
    }
  }
};
```

---

## 🧩 組件規範

### Buttons

```jsx
/* Primary Button */
<button className="
  px-6 py-3
  bg-primary-500 hover:bg-primary-600
  text-white font-medium
  rounded-lg shadow-md
  transition-all duration-150
  hover:shadow-lg hover:scale-105
  active:scale-95
">
  Generate Mind Map
</button>

/* Secondary Button */
<button className="
  px-6 py-3
  bg-gray-100 hover:bg-gray-200
  text-gray-700 font-medium
  rounded-lg
  transition-colors duration-150
">
  Export PNG
</button>

/* Icon Button */
<button className="
  w-10 h-10
  flex items-center justify-center
  rounded-full
  hover:bg-gray-100
  transition-colors duration-150
">
  <Icon size={20} />
</button>
```

### Cards

```jsx
/* Standard Card */
<div className="
  bg-white dark:bg-gray-800
  rounded-xl shadow-md
  p-6
  border border-gray-200 dark:border-gray-700
  hover:shadow-lg
  transition-shadow duration-300
">
  {/* Content */}
</div>

/* Glass Card */
<div className="
  bg-white/10 backdrop-blur-lg
  rounded-xl
  border border-white/20
  p-6
  shadow-xl
">
  {/* Content */}
</div>
```

### Inputs

```jsx
/* Text Input */
<input className="
  w-full px-4 py-3
  bg-gray-50 dark:bg-gray-800
  border border-gray-300 dark:border-gray-600
  rounded-lg
  focus:outline-none focus:ring-2 focus:ring-primary-500
  transition-all duration-150
  placeholder:text-gray-400
" />

/* Textarea */
<textarea className="
  w-full px-4 py-3
  bg-gray-50 dark:bg-gray-800
  border border-gray-300 dark:border-gray-600
  rounded-lg
  min-h-[200px]
  resize-none
  focus:outline-none focus:ring-2 focus:ring-primary-500
  transition-all duration-150
" placeholder="Paste your article here..." />
```

### Mind Map Node

```jsx
/* Node Card */
<div className="
  relative
  bg-gradient-to-br from-primary-50 to-accent-50
  dark:from-primary-900/30 dark:to-accent-900/30
  border-l-4 border-primary-500
  rounded-lg
  p-4
  shadow-md hover:shadow-xl
  transition-all duration-300
  cursor-move
  group
">
  {/* Node Content */}
  <h3 className="font-semibold text-lg mb-2">
    Node Title
  </h3>
  <p className="text-sm text-gray-600 dark:text-gray-300">
    Node description...
  </p>

  {/* Hover Actions */}
  <div className="
    absolute top-2 right-2
    opacity-0 group-hover:opacity-100
    transition-opacity duration-150
  ">
    <button className="p-1 hover:bg-gray-200 rounded">
      <MoreIcon />
    </button>
  </div>
</div>
```

---

## 🎯 Layout Guidelines

### Container Sizes
```css
--container-sm: 640px;   /* Mobile */
--container-md: 768px;   /* Tablet */
--container-lg: 1024px;  /* Desktop */
--container-xl: 1280px;  /* Large Desktop */
--container-2xl: 1536px; /* Ultra Wide */
```

### Responsive Breakpoints
```css
/* Tailwind default */
sm:  640px
md:  768px
lg:  1024px
xl:  1280px
2xl: 1536px
```

### Grid System
```jsx
/* Main Layout */
<div className="min-h-screen bg-gray-50 dark:bg-gray-900">
  {/* Header */}
  <header className="sticky top-0 z-50 bg-white/80 backdrop-blur-lg border-b">
    {/* 64px height */}
  </header>

  {/* Main Content */}
  <main className="container mx-auto px-4 py-8 max-w-7xl">
    {/* Content */}
  </main>
</div>
```

---

## 🎨 Mindora-Specific Components

### Theme Selector
```jsx
<div className="flex gap-2">
  <button className="
    w-12 h-12 rounded-lg
    bg-gradient-to-br from-gray-900 to-gray-700
    border-2 border-transparent
    hover:border-primary-500
    transition-all duration-150
  " aria-label="Dark Theme" />

  <button className="
    w-12 h-12 rounded-lg
    bg-gradient-to-br from-white to-gray-100
    border-2 border-transparent
    hover:border-primary-500
  " aria-label="Light Theme" />

  <button className="
    w-12 h-12 rounded-lg
    bg-gradient-to-br from-blue-900 to-blue-700
    border-2 border-transparent
    hover:border-primary-500
  " aria-label="Blue Theme" />
</div>
```

### Color Picker
```jsx
/* 使用 react-colorful */
import { HexColorPicker } from 'react-colorful';

<div className="popover bg-white dark:bg-gray-800 rounded-xl shadow-2xl p-4">
  <HexColorPicker color={color} onChange={setColor} />

  {/* Preset Colors */}
  <div className="grid grid-cols-6 gap-2 mt-4">
    {presetColors.map(c => (
      <button
        key={c}
        className="w-8 h-8 rounded-lg hover:scale-110 transition-transform"
        style={{ backgroundColor: c }}
        onClick={() => setColor(c)}
      />
    ))}
  </div>
</div>
```

### Loading State
```jsx
/* Skeleton for mind map */
<div className="animate-pulse space-y-4">
  <div className="h-20 bg-gray-200 dark:bg-gray-700 rounded-lg" />
  <div className="grid grid-cols-3 gap-4">
    <div className="h-16 bg-gray-200 dark:bg-gray-700 rounded-lg" />
    <div className="h-16 bg-gray-200 dark:bg-gray-700 rounded-lg" />
    <div className="h-16 bg-gray-200 dark:bg-gray-700 rounded-lg" />
  </div>
</div>

/* AI Generation Animation */
<div className="flex flex-col items-center gap-4">
  <div className="relative w-16 h-16">
    <div className="absolute inset-0 border-4 border-primary-200 rounded-full" />
    <div className="absolute inset-0 border-4 border-primary-500 rounded-full border-t-transparent animate-spin" />
  </div>
  <p className="text-gray-600 dark:text-gray-300">
    AI is analyzing your article...
  </p>
</div>
```

---

## 📱 Mobile Optimization

### Touch Targets
```css
/* Minimum 44x44px for touch targets */
.touch-target {
  min-width: 44px;
  min-height: 44px;
}
```

### Mobile Menu
```jsx
/* Slide-in sidebar */
<motion.div
  initial={{ x: -300 }}
  animate={{ x: 0 }}
  exit={{ x: -300 }}
  className="
    fixed inset-y-0 left-0 z-50
    w-80 bg-white dark:bg-gray-800
    shadow-2xl
  "
>
  {/* Mobile navigation */}
</motion.div>
```

---

## 🎨 Icon System

**推薦使用：** `lucide-react`

```jsx
import {
  Sparkles,      // AI 圖標
  Download,      // 下載
  Share2,        // 分享
  Palette,       // 顏色
  Sun,           // Light mode
  Moon,          // Dark mode
  Zap,           // 快速
  Layout,        // 版面
  GitBranch,     // 分支/心智圖
  Brain          // 大腦
} from 'lucide-react';

<Sparkles className="w-5 h-5 text-primary-500" />
```

---

## ✅ Accessibility Checklist

- [ ] **Color Contrast:** WCAG AA (4.5:1 for normal text)
- [ ] **Keyboard Navigation:** Tab / Shift+Tab / Enter / Esc
- [ ] **Focus Indicators:** 明顯的 focus ring
- [ ] **Screen Reader:** 適當的 `aria-label` 和 `role`
- [ ] **Motion:** `prefers-reduced-motion` support

```css
/* Reduced Motion Support */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 🎁 Design Tips

### 1. **留白的力量**
- 不要填滿每一個空間
- 使用 `--spacing-8` 以上的間距分隔區塊

### 2. **視覺層次**
```
主標題：--text-3xl + --font-bold
次標題：--text-xl + --font-semibold
正文：  --text-base + --font-normal
註釋：  --text-sm + text-gray-500
```

### 3. **顏色使用**
- 主要操作：Primary color
- 次要操作：Gray
- 危險操作：Red
- 成功狀態：Green

### 4. **微互動**
- Hover: scale(1.05) + shadow-lg
- Active: scale(0.95)
- Focus: ring-2 ring-primary-500

---

<p align="center">
  <strong>✨ Beauty is not optional, it's essential ✨</strong><br>
  <sub>Design is how it works, not just how it looks</sub>
</p>
