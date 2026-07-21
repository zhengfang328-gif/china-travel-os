# RULES.md — China Travel OS

English-language guide site for first-time foreign visitors to China.
Static HTML/CSS, mobile-first, deployed via GitHub Pages / Netlify.

## 权威文档（写代码前先读）
- **项目笔记.md** — 完整进度 + 设计规范速查（权威来源，完整 token 见 DESIGN.md）
- **DESIGN.md** — CSS token 快照（从代码自动生成，可重跑）
- **PRODUCT.md** — 品牌人格 + 设计原则 + 反参考

## 不可违反的规则

### 设计系统
- **字体**: Literata（标题 serif）+ Work Sans（正文 sans），Google Fonts 加载。禁止 Inter。
- **色彩**: `--bg: #FAFAFA`（chroma 0），`--accent: #D94838`。所有中性色向红 12° 偏移，禁止纯灰（#1A1A1A / #52525B）。
- **层级**: border 区分，禁止 box-shadow。Nav 纯白实底，禁止毛玻璃 blur。
- **过渡**: 精确属性（`color`, `background-color`, `transform`），`cubic-bezier(.4, 0, 0, 1)`。禁止 `transition: all` / `ease`。
- **无障碍**: 必须含 `@media (prefers-reduced-motion: reduce)`。
- **callout**: 完整 `border: 1px solid` + tint 背景，禁止 `border-left` 侧边条纹。
- **圆角**: `--radius: 10px` / `--radius-l: 16px` / `--radius-pill: 999px`。
- **间距**: 4px 基数；排版比例 ≥1.25 步进。
- **禁用项**: Inter 字体、box-shadow 层级、毛玻璃、emoji 作 UI icon、纯黑/纯灰文字、eyebrow（仅 Anxiety 区保留一条）、格言式否定对仗文案。

### 内容
- **语调**: TikTok Hook + Reddit Honesty。第一人称本地经验，迷你生活细节替代百科式语言。
- **不猜测外部事实**: URL、价格、产品名 → web_search 查证或问用户，禁止凭记忆编造。
- **页面达 80–90 分就上线**，不无限打磨。

### 同步规则
- **修 CSS 后必检查** 项目笔记.md「设计规范」章节是否需要同步更新（数值/策略/禁令描述一致）。
- 新增攻略页 → 更新 项目笔记.md 进度清单 + 文件结构。

### 自动同步
- **每次修改完成后必须自动执行**：`git add` → `git commit` → `git push origin main`，不需要等用户提醒。commit message 用英文简要描述改动。

## 文件结构速查

```
china-travel-os/
├── index.html              ← 首页（Hero + Anxiety + Guide Hub + Cities + Newsletter）
├── guide/
│   ├── alipay.html         ← Alipay 支付教程
│   ├── wechat-pay.html     ← WeChat Pay 教程
│   ├── apps.html           ← 必装 App
│   ├── vpn.html            ← VPN 上网准备
│   ├── esim.html           ← eSIM/Data 指南
│   ├── trains.html         ← 高铁教程
│   ├── checklist.html      ← 互动清单（21 项 + localStorage）
│   ├── metro.html          ← Metro & Bus
│   ├── bike.html           ← 共享单车
│   ├── ride-hailing.html   ← 打车（DiDi）
│   ├── safety.html         ← 安全指南
│   ├── daily-life.html     ← 日常生活指南
│   ├── daily-routines.html ← 本地日常习惯
│   ├── misunderstand.html  ← 常见误解
│   └── images/             ← 截图按子目录组织
├── city/                   ← 杭州城市专题页（已建成）
├── 项目笔记.md              ← 全项目唯一权威笔记
├── DESIGN.md               ← CSS token 快照
├── PRODUCT.md              ← 品牌注册
└── .gitignore
```

## 快速命令
- 预览: 双击 `index.html`
- 部署: Netlify / Vercel（静态站，拖拽即上线）
- GitHub: https://github.com/zhengfang328-gif/china-travel-os
