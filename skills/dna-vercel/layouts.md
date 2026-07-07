# Layout · 按载体分发

> dna-vercel 在不同载体上的具体参数。**载体适配度和提示档的路由表只在主 SKILL.md 一份**（避免双源漂移），按那边选好章节后来这里查参数。
> 章节：[Landing](#landing-落地页--文档--长文)（原生）/ [Longform](#longform-竖向长图)（档 1）/ [Slides](#slides-翻页演示)（档 2）。
> 中文页的字距 / 行高口径见 SKILL.md「中文适配」段，本文件参数默认是西文值。
> **暗页**：本文件所有颜色参数以 token 角色书写时自动随 `data-theme="dark"` 切换（映射表见 SKILL.md「Dark 模式」节）；写死的 hex 按该表手动换档。nav 暗版底 = rgba(0,0,0,.85) + blur；code block 在暗页配 hairline 分界。

---

## Landing（落地页 / 文档 / 长文）

适配度：★★★★★ 原生 · 无需触发提示
适用：落地页、定价页、产品文档、技术博客、changelog、developers 子站。

### Hero（首屏）

```
- 居中或左对齐 + 大量留白
- 上方可放 caption（11px uppercase #666）当 eyebrow
- 主标题  56–80px / weight 600 / letter-spacing -0.05em（西文；中文见 SKILL.md 中文适配）/ line-height 1.05–1.08
- 副标题  17px / color #4d4d4d / max-width 560–720px / line-height 1.55
- 双 CTA: primary (#171717 pill) + secondary (白底实色 pill)
- 背景：#fafafa 纯色 或加 dot grid
  background-image: radial-gradient(circle, rgba(0,0,0,0.04) 1px, transparent 1px);
  background-size: 24px 24px;
- 高度 min-height: 88vh ~ 100vh —— 这是**首页 hero** 口径
  内页（定价 / 文档 / changelog）hero 用紧凑档：padding 上 96px 下 64px、无 min-height，
  让核心内容（如定价卡）进首屏
```

### Nav（导航 · 实测参数）

```
- 高度 64px / z-index 75 / sticky
- 背景：rgba(250,250,250,0.85) + backdrop-filter blur(12px) + border-bottom hairline
- nav 链接 14px / #4d4d4d / nav-item 圆角 9999px / padding 8px 12px / 高 30px
- ⚠️ nav 内的 secondary 按钮是例外：6px 圆角 / 32px 高 / 14px w500（非 pill）
  ——同一按钮在 hero 区是 100px pill / 16px / ~40px 高，两种 secondary 因上下文分化（实测）
```

### Footer（页脚 · 实测较薄，标注为准）

```
- 顶部 border-top: 1px solid var(--border) 与正文分隔
- 分类标签：Geist Mono 12px / w500（实测）
  中文页的分类标签直接用英文 mono uppercase（PRODUCT / LEGAL…）——mono 无中文字形，
  中文标签会破 mono 声；链接文字可中文
- 链接：14px / #666（tertiary，footer 链接主力色，实测 ×134）
- 结构未做全站实测：默认多列链接 + 底行 logo/版权，不加装饰
```

### 响应式（最小护栏）

```
- ≤960px：多列卡片收单列（或 2col），容器 padding 32→20px
- ≤700px：nav 收起链接（保留 logo + primary CTA；汉堡菜单可选），hero 字号靠 clamp() 自适应
- 字距一律 em（px 字距在 clamp 缩放下失调）；触控目标 ≥44px
- 断点数值是克制默认，可按内容调；原则钉死：小屏不出横向滚动、不缩小点按目标
```

### Code block / Terminal（代码块 · 摄影的替代品，规格必须对）

**默认档 · 深底 terminal 块**（营销页 / hero 配图语境）：

```css
.code-block {
  background: var(--text-primary);   /* #171717——代码块就是终端，用终端的墨色 */
  color: #ffffff;
  border-radius: 6px;                /* 实测 --code-block-radius */
  padding: 16px 20px;
  font-family: var(--font-mono);
  font-size: 13px;
  line-height: 1.6;
}
.code-comment { color: rgba(255,255,255,0.4); }   /* 层级靠白色透明度，不靠彩色 */
.code-key     { color: rgba(255,255,255,0.7); }
.code-val     { color: rgba(255,255,255,0.9); }
```

**docs 档 · 浅底语法高亮**（文档 / 长文语境，实测色板）：

```
底色 #fff 或 #fafafa + hairline 边框 + 6px 圆角，语法色板（vercel.com 实测）：
keyword #bd2864 · string #297a3a · function #7820bc · value #0068d6 · string 高亮底 #cce6ff
```

两档共同红线：**不用 VS Code 暗紫主题、不用彩虹色 token、不加 macOS 红绿灯装饰条**（除非做的就是「窗口」mockup）。

### Section

```
- 上下 padding 64px / 96px（spacious 用 96px）
- 章节标题之上加 caption（11px uppercase eyebrow #666）
- 主标题 28–32px / letter-spacing -0.04em（实测 32px → -1.28px）
- 描述 14–15px / color #4d4d4d / max-width 720px / line-height 1.6
- 上下 section 之间用 border-bottom: 1px solid var(--border) 分隔
  （不用色块/背景区分）
```

### Card / Bento Grid

```
- background: #ffffff
- box-shadow: hairline
  rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px 0px
  （实测主力卡片影还带第三层微投影 rgba(0,0,0,0.04) 0 4px 8px，可加可不加；
  **投影层**透明度永不越 0.08——1px ring 属边界层，强调卡可用 --border-strong 0.14）
- border-radius: 6px
- padding: 24px
- 卡片边界首选 shadow ring；1px 实线 hairline（rgba(0,0,0,0.08) ×48 / #ebebeb ×8 实测）
  用于分隔线、输入框、容器也合规——禁的是 2px+ 粗边框，全站只有 1px
- bento 2col 或 3col 网格，gap 12–16px
```

### Stat / Number Card

```
- 数字用 Geist Mono / JetBrains Mono
- font-size: 28–32px / weight 600 / letter-spacing -0.04em
  （大号 mono 数字字距统一走 -0.04 ~ -0.05em 带，不套 sans 标题的 -0.06em 曲线）
- 数字下方 caption: 12px color #4d4d4d
- 底部可加 11px mono 来源标签
  border-top: 1px solid var(--border)
```

### 定价三卡（Pricing）

```
- 三卡等高网格 gap 16px；hero 用内页紧凑档（见上文 Hero）
- 推荐档标记：badge = gray-100 底 / 11px mono uppercase / 9999px pill，置于 tier 名旁
  推荐卡 ring 用 --border-strong rgba(0,0,0,0.14)（边界层强调，非投影）
- 价格数字：mono 36-40px / -0.04 ~ -0.05em；非数字价（Custom）同规格同字号对齐
- CTA：推荐卡用唯一 primary（#171717 pill），其余卡 secondary 白底 pill——尺寸从上下文自行推
- 不用色块高亮推荐档、无彩色对比标记（见 reasoning.md 定价页推导示范）
- 对比表：未实测，不立参数——从判准轴、色彩身份（布尔值别用绿✓红✗）、hairline 分区自行推导
```

### Hero 渐变（高级 · 默认不用）

Vercel 在 hero 区允许色彩，但**色彩不是直接铺陈，而是被 SVG 遮罩"驯服"**：

```
conic-gradient（紫橙蓝多色）+ blackoutLines SVG 遮罩 + 白色三角形
→ 背景色填充的密集线条刮掉大部分渐变
→ 只留 ~1px 缝隙透出彩色
→ 效果像等高线地形图或示波器波纹，而非泼墨渐变
```

**这是 Vercel 的极致体现：即使在品牌最感性时刻，色彩也经过工程结构过滤。**

落地参数（**推导默认**，真站参数级实测未做、真件一到就让位）：线条周期 ~7px 留 ~1px 缝（开缝比 ≤1/7）、渐变带高 ~280px + 径向 mask 收边、色相取功能色系、流动 60-90s linear（白名单内唯一 linear 场景）。**暗页声量**：遮罩填充跟 `--page-bg`（#000），缝隙彩色靠边缘渐隐压到感知边缘——暗底彩色比浅底更"发光"，声量只紧不松。

如果不会做这个效果，**就不要用渐变**——直接 `#fafafa` 纯色或 dot grid 永远 safe。

---

## Longform（竖向长图）

适配度：★★★☆☆ 可做 · 档 1 软提示
适用：公众号头图、产品发布长图、技术 changelog 长图、年终总结竖图。
不适用：需要交互的网页内容（请用 Landing）。

### 触发档 1 提示

生成前告诉用户：

> "公众号长图不是 Vercel 站的原生形态——Vercel 是 web 翻页节奏，长图是无翻页的瀑布。
> 成品会保留 Vercel 的工程克制（字距、配色、hairline、mono 数字），
> 但会失去 web 上的'页面感'。如果接受，我开始做。"

提示后直接做，不等用户回。

### 整体节奏

```
- 无 hero（公众号封面已经是 hero）
- 无 navigation / footer
- 顶部可选小卡片：标题 + 副标题 + 日期 + 作者，作为正文起点
- 章节顺接，**不靠色块切换**，靠 hairline 分隔 + 留白
- 末尾：单独章节作为 outro，加一行 mono 落款（日期 / 版本号 / 链接）
```

### 容器与尺寸

```
- 整体宽度：750px（公众号原生宽度）或 1080px（小红书图文）
- 左右 padding：48px（750 宽时）/ 64px（1080 宽时）
- 整体背景：#fafafa
- 章节之间间距：80px / 96px / 120px（按节奏由密到疏）
```

**关键**：长图无翻页，节奏感来自**章节间距的递进**，不是色块切换。

### 章节标题块

```css
.section-head { margin-top: 96px; margin-bottom: 32px; }
.section-head .eyebrow {
  font: 600 11px/1 var(--font-mono);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #666;
  margin-bottom: 12px;
}
.section-head h2 {
  font: 600 32px/1.25 var(--font-sans);
  letter-spacing: -0.005em;   /* 中文默认——公众号长图多为中文，方块字不吃西文负字距 */
  color: #171717;
}
.section-head h2:lang(en),
.section-head h2 :lang(en) {
  letter-spacing: -0.04em;    /* 英文标题恢复西文 DNA（实测 32px 档） */
  line-height: 1.15;
}
```

### 内文段落

```
- 字号 16px（750 宽）/ 17px（1080 宽）
- 行高 1.7（长图阅读距离比网页远，行距适当放大）
- 段落间距 24px
- 颜色 #171717
- 字距 0（小字号不收）
- 段落最大行宽：650px（即使容器更宽，正文也要收窄保证可读）
```

### 引用块 / 强调段（长图唯一允许的左边线）

```css
.quote {
  border-left: 2px solid #171717;
  padding: 4px 0 4px 20px;
  margin: 32px 0;
  font: 400 18px/1.55 var(--font-sans);
  letter-spacing: 0;   /* 中文引用不收；纯英文引用可标 lang="en" 收 -0.017em */
}
```

### 章节分隔（三种合规方式）

```
1. 纯留白：章节间距 96-120px，无视觉元素
2. Hairline：1px solid var(--border)，宽度 = 内文容器宽度，居中
3. Mono 序号：「01 / 04」样式 11px mono #666，居中
```

按节奏从弱到强：纯留白 → hairline → mono 序号。

### 长图特有的红线

- ❌ **不要 hero 大渐变**（长图没有 hero）
- ❌ **不要 sticky 导航**（导出图片后没意义）
- ❌ **不要任何 hover / scroll 触发动效**（导出为静态图，动效会丢失）
- ❌ **不要满铺色块**（章节切换靠间距，不靠色块）

---

## Slides（翻页演示）

适配度：★☆☆☆☆ 偏离基因 · 档 2 中提示
适用：投屏汇报、内部 review、路演 demo。
不适用：自看 / 网页阅读（请用 Landing）。

### ⚠️ 触发档 2 提示（必做）

生成前先告诉用户：

> "PPT 翻页路演违背 Vercel 的 web-native 节奏——Vercel 是连续滚动的工程克制，
> PPT 是离散翻页的演讲节奏。成品会保留 Vercel 的字体/配色/字距/hairline，
> 但整体观感更接近 Linear 或 Stripe，而不是 vercel.com。
>
> (a) 接受偏差，做 Vercel 风的 slides
> (b) 折中：做成「投屏自看」而非「路演大屏」，密度按 dense
> (c) 推荐切换其他 DNA
>
> 你要哪个？"

只有用户选 (a) 或 (b) 才继续。

### 三档密度

| 密度 | 适用 | 字号策略 | 一屏论点 |
|---|---|---|---|
| **dense** | 投屏自看 / 屏幕分享 | 同 Landing | ≤ 5 |
| **normal** | 投屏汇报 / 中等会议室 | 标题 +20% / 正文 +10% | ≤ 4 |
| **sparse** | 路演大屏 / 大会议室 | 标题 +40% / 正文 +25% / **正文下限 24px** | ≤ 3 |

sparse 是适配性带边缘——密度下降到这一档，Vercel 的"工程克制"会被稀释成"空"。

### 屏幕自适应（必做）

slides 是固定 16:9 的"画布"——**必须在窗口里居中 + 等比缩放**，不能让内容堆在角落（用户在大屏上打开会看到内容堆在左上）。

**默认用 CSS aspect-ratio + flex 居中**：

```css
.slide-wrapper {
  width: 100vw;
  height: 100vh;
  background: #fafafa;
  display: flex;
  align-items: center;            /* 垂直居中 */
  justify-content: center;        /* 水平居中 */
  overflow: hidden;
}

.slide {
  aspect-ratio: 16 / 9;
  width: 100%;
  max-width: 100vw;
  max-height: 100vh;
  padding: 5% 6%;                 /* 百分比内边距，跟着 slide 缩放 */
  display: flex;
  flex-direction: column;
  justify-content: center;        /* 内容垂直居中 */
}
```

**关键约束**：
- slide 内部的尺寸用 `vw / vh / %` 或 `em / rem`，**不要用绝对 px**
- 字号用 `clamp()` 自适应，例如 `clamp(32px, 4vw, 80px)` 作为大标题
- slide 容器用 flex 垂直居中，内容自然分布，**不要靠绝对定位**
- 翻页过渡的 `translateX` 用 `%` 而不是 `px`

**为什么不用 px**：px 在大屏上会让内容堆在左上角，slide 不会跟着窗口缩放。用相对单位让 slide 跟着屏幕走。

**导出固定像素 PDF / 长图时**——改用 JS `transform: scale()` 方案（保留 1920×1080 设计稿尺寸，按容器比例缩放）。本 skill 默认不展开，需要时按需实现。

### 内容布局（三段式锁定 · 防溢出必做）

slide 内部必须用 **flex 三段式**：页眉 / 主体 / 页脚分开锁定，避免内容超出 viewport 或重叠：

```css
.slide {
  aspect-ratio: 16 / 9;
  width: 100%;
  padding: 4% 5%;
  display: flex;
  flex-direction: column;
  overflow: hidden;                  /* 兜底：超出裁剪，不蔓延 */
}

.slide__header { flex-shrink: 0; }   /* 04/10 · 章节标签 → 锁定顶部 */

.slide__body {                        /* 主标题 + 内容 → 自适应剩余空间 */
  flex: 1 1 0;
  min-height: 0;                     /* 关键 - 允许子元素收缩 */
  display: flex;
  flex-direction: column;
  justify-content: center;
  overflow: hidden;
}

.slide__footer { flex-shrink: 0; }   /* METHODOLOGY · 数据 metadata → 锁定底部 */
```

**为什么必须三段式**：
- AI 默认会把内容一股脑塞进 slide → 总高度超过 viewport → 页脚被挤压到主体上方甚至重叠
- 三段式让顶部和底部"锁定"，中间主体自适应剩余高度
- `overflow: hidden` 是兜底防御，超出就裁剪不蔓延到下一屏

**配套规则**：
- 主体内容字号用 `clamp()` 自适应：`font-size: clamp(28px, 3.5vw, 64px)`
- **如果主体仍然超出**：减少卡片数 / 切换到更稀疏密度档，**不要让 slide 滚动**
- 主体卡片之间用 `gap` 不用 `margin`，便于 flex 布局收缩

### 整体节奏

```
- 单页比例 16:9（aspect-ratio + flex 居中，见上文「屏幕自适应」）
- 设计尺寸参考 1920×1080，导出时按此比例
- 横向 translateX 翻页用 % 不用 px（见 SKILL.md Motion 段）
- 每页 padding 按密度档：5% (dense) → 6% (normal) → 8% (sparse)
- 不要 footer、不要"slide 12/24"那种页码角标
```

### 4 种页面类型

**1. 封面页（Cover）** — 左对齐 + 大量留白
```
[ 11px mono eyebrow ]    ← 项目 / 日期 / 版本
[ 80-120px 大标题 ]      ← 字距 -0.05em（slides 全用 em——clamp 缩放下固定 px 字距会失调；中文标题 -0.005em）
[ 17-22px 副标题 ]       ← 一句话价值
[ 11px mono 署名 ]
```

**2. 内页（Content · 最高频）**
```
[ 11px mono eyebrow ]    ← 章节名 / 页编号
[ 32-48px 页标题 ]       ← dense/normal/sparse 按密度档
[ 内容主体 ]             ← 文字 / 卡片 / 数据 / mockup
[ (可选) 11px mono 注脚 ]
```

**3. 章节分隔页（Section Break）** — 全屏极简
```
[ 11px mono SECTION 02 ]
[ 96px 章节名 #171717 ]   ← 字距 -0.05em（中文 -0.005em）
```

**4. 结尾页（Outro）**
```
[ 80px Thanks. 或 Q&A ]
[ 17px 联系方式 ]
[ 11px mono 链接 ]
```

### Slides 特有的红线

- ❌ **不要 bullet list**（• ○ ▪）—— 用空行 + 段落分隔代替
- ❌ **不要"AGENDA"页** —— 用章节分隔页代替
- ❌ **不要页码角标 / slide master 装饰** —— 极简 mono 数字即可
- ❌ **不要 zoom / morph / spring 转场** —— 只用横向位移
