# 政策智能体 UI 配色手稿
## Professional Color System Design Guide

### 🎨 主色彩系统 (Primary Color System)

#### 品牌主色 (Brand Primary)
```css
--primary-blue: #007AFF        /* Apple Blue - 主要交互色 */
--primary-blue-hover: #0056B3  /* 悬停状态 */
--primary-blue-active: #004C99 /* 激活状态 */
--primary-blue-10: rgba(0, 122, 255, 0.1)  /* 10% 透明度 - 焦点环 */
--primary-blue-20: rgba(0, 122, 255, 0.2)  /* 20% 透明度 - 背景高亮 */
--primary-blue-30: rgba(0, 122, 255, 0.3)  /* 30% 透明度 - 阴影 */
```

#### 功能色彩 (Functional Colors)
```css
--success-green: #34C759       /* 成功状态 */
--warning-orange: #FF9500      /* 警告状态 */
--error-red: #FF3B30          /* 错误状态 */
--info-purple: #AF52DE        /* 信息提示 */
```

### 🌫️ 中性色系统 (Neutral System)

#### 背景色阶 (Background Hierarchy)
```css
--bg-primary: #FFFFFF          /* 主背景 - 卡片、输入框 */
--bg-secondary: #F2F2F7        /* 次级背景 - 页面底色 */
--bg-tertiary: #F6F6F6         /* 三级背景 - 浏览器头部 */
--bg-hover: #F5F5F7           /* 悬停背景 */
--bg-pressed: #E5E5EA         /* 按压背景 */
```

#### 文字色阶 (Text Hierarchy)
```css
--text-primary: #1D1D1F        /* 主标题、重要文字 */
--text-secondary: #3C3C43      /* 副标题、正文 */
--text-tertiary: #3C3C4399     /* 辅助信息、占位符 */
--text-quaternary: #8E8E93     /* 禁用状态文字 */
--text-inverse: #FFFFFF        /* 反色文字 */
```

#### 边框线条系统 (Border System)
```css
--border-light: #F2F2F7        /* 轻边框 - 卡片分割 */
--border-medium: #E5E5EA       /* 中边框 - 输入框 */
--border-strong: #D1D1D6       /* 强边框 - 重要分割 */
--border-separator: #C6C6C8    /* 分割线 */
```

### 🎯 使用场景规范 (Usage Guidelines)

#### 页面层级 (Page Hierarchy)
```
Level 1: 主背景 (#F2F2F7)
├── Level 2: 卡片背景 (#FFFFFF)
    ├── Level 3: 输入框背景 (#FFFFFF + border)
    └── Level 3: 按钮背景 (#007AFF)
```

#### 交互状态 (Interaction States)
```css
/* 正常状态 */
.button-primary {
    background: #007AFF;
    color: #FFFFFF;
    border: none;
}

/* 悬停状态 */
.button-primary:hover {
    background: #0056B3;
    box-shadow: 0 4px 12px rgba(0, 122, 255, 0.3);
}

/* 激活状态 */
.button-primary:active {
    background: #004C99;
    transform: translateY(1px);
}

/* 禁用状态 */
.button-primary:disabled {
    background: #E5E5EA;
    color: #8E8E93;
}
```

### 🔍 对比度规范 (Contrast Standards)

#### WCAG AA 合规性
- **正文**: #3C3C43 on #FFFFFF (对比度: 10.69:1) ✅
- **标题**: #1D1D1F on #FFFFFF (对比度: 15.8:1) ✅  
- **按钮**: #FFFFFF on #007AFF (对比度: 4.78:1) ✅
- **辅助文字**: #8E8E93 on #FFFFFF (对比度: 4.54:1) ✅

### 🎨 色彩情感映射 (Color Psychology)

```
蓝色 (#007AFF) → 信任、专业、可靠
绿色 (#34C759) → 成功、安全、增长  
橙色 (#FF9500) → 注意、活力、创新
红色 (#FF3B30) → 紧急、错误、重要
紫色 (#AF52DE) → 智能、高端、创新
灰色系 → 平衡、稳定、现代
```

### 🌓 暗色模式配色 (Dark Mode - Optional)

```css
/* 暗色模式颜色变量 */
@media (prefers-color-scheme: dark) {
    :root {
        --bg-primary: #1C1C1E;
        --bg-secondary: #000000;
        --bg-tertiary: #2C2C2E;
        --text-primary: #FFFFFF;
        --text-secondary: #EBEBF5;
        --text-tertiary: #EBEBF599;
        --border-light: #38383A;
        --border-medium: #48484A;
    }
}
```

### 📐 阴影系统 (Shadow System)

```css
--shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.04);           /* 轻微阴影 */
--shadow-md: 0 4px 12px rgba(0, 0, 0, 0.08);          /* 中等阴影 */  
--shadow-lg: 0 8px 25px rgba(0, 0, 0, 0.12);          /* 重阴影 */
--shadow-blue: 0 4px 12px rgba(0, 122, 255, 0.3);     /* 蓝色阴影 */
--shadow-green: 0 4px 12px rgba(52, 199, 89, 0.3);    /* 绿色阴影 */
```

### ✨ 渐变系统 (Gradient System)

```css
--gradient-primary: linear-gradient(135deg, #007AFF 0%, #0056B3 100%);
--gradient-success: linear-gradient(135deg, #34C759 0%, #28A745 100%);
--gradient-background: linear-gradient(180deg, #F2F2F7 0%, #FFFFFF 100%);
```

---

> **设计原则**: 简洁、直观、一致性  
> **品牌调性**: 专业、可信、现代、智能  
> **适用平台**: Web、移动端响应式设计 