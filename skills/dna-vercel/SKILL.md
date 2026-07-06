---
name: dna-vercel
description: 为 HTML/CSS 页面注入 Vercel「工程克制」视觉基因（别名 vercel-dna）。Use when：生成或重构 SaaS / 开发者工具 / AI 工具的落地页、定价页、产品文档、技术博客、changelog、公众号长图、翻页 slides，或用户点名 Vercel 风 / 工程克制 / dna-vercel。核心：#fafafa 纸底、#171717 近黑唯一强调、Geist + Mono 双声（Inter 兜底）、大标题负字距、hairline 阴影、无渐变无摄影无 bounce；中文页自带 CJK 字距适配。来源：vercel.com 逆向实测。
---

# Skill · Design DNA · Vercel

## 一句话哲学

> **工程克制（Engineered Restraint）**
> 每个设计决策都在回答同一个问题：「这让信息更清晰了吗？」

镜像开发者的文化记忆——终端、代码、像素屏。文字、代码、内容是主角，设计是精确控制，不是展台。

---

## Cultural Root（文化根）

镜像**开发者文化的视觉记忆**：终端、代码编辑器、像素屏幕、命令行——黑底白字、等宽字体、精确到字符的对齐、没有多余装饰。

近黑 `#171717` 是终端文字色；`#fafafa` 是早期显示器的纸质温度；JetBrains Mono 把代码工程化为品牌字体；代码块享有和标题同等的视觉地位；没有摄影因为终端里没有照片；没有 bounce 动效因为终端是静态精确的。

> **Vercel 不是在做"极简设计"，而是在说："我们知道你是谁，我们和你一样。"**

**跟相邻流派的区分**：
- 产品极简（Apple）= 镜像消费者对"精致物件"的记忆 · 界面消失，产品图主导
- 暗色极简（Linear）= 镜像专业工具使用者对 IDE/Photoshop 的记忆 · 深色制造专业感
- **工程克制（Vercel）= 镜像开发者对终端的记忆** · 文字代码是主角，设计是精确控制

详细推理框架 + 锚点参数二分 + 推导示范，见 [`reasoning.md`](reasoning.md)。

---

## 手法地图（主 → 次）

五个签名手法挂在同一根判准轴上（「这让信息更清晰了吗」），按离轴心远近排主次——顶上的改了就不是 Vercel，底下的最显眼却只是表皮：

1. **排版 / 字距**（灵魂 ·「排版即设计」）—— 重量来自密度不是字重：大标题负字距，Sans + Mono 两种声音
2. **色彩按身份管理** —— 灰阶做层级、功能色做状态、品牌色只在 hero，三者严格不混
3. **Material 分级压声量** —— hairline 阴影 + 圆角分级，每级都不喊；按钮近黑不用品牌色
4. **影像＝代码与界面** —— 不摄影不插画，「图」就是 UI mockup / 代码块本身
5. **Hero 渐变被工程驯服** —— 最感性的时刻也要过结构过滤（blackoutLines 刮到只剩缝）

**一句排序**：排版是天花板（最难、最定义 Vercel），hero 渐变是地板（最显眼、只在首页一处）。只学到渐变和灰阶，是「漆对了、骨没对」。完整表见 [`reasoning.md`](reasoning.md)。

---

## 设计前自问（一句话 self-check）

写代码前 + 写完代码后各问一次：

> **"这让信息更清晰了，还是在信息之外加了什么？"**

如果是后者——去掉它，或者让它退到感知边缘。

---

## 意图层（生成前必做）

在写第一行代码前，先识别场景三问，然后按"灵魂带 / 适配性带 / 红线外"决定如何提示用户。

### 三问

| 问题 | 选项 | 默认 |
|---|---|---|
| **载体** | 落地页 / 长文 / 文档 / 仪表盘 / 定价页 / 长图 / 翻页 PPT | 落地页 |
| **场景** | 自看（电脑/网页） / 投屏汇报 / 路演大屏 | 自看 |
| **动效** | 默认克制（见下文 Motion 段） / 纯静态 / 更夸张 | 默认克制 |

如果用户没说，按默认走；如果用户的需求落到下面三档之外的位置，按对应档语气提示。

### 三档出口

**档 1 · 软提示**（适配性带内 · 提示后直接做）
> "{载体/场景} 不是 Vercel 站的原生形态，成品会偏向 {预期感}。如果接受，我开始做。"

**适用**：长图载体、投屏汇报需要稍高密度、克制范围内的动效定制。

---

**档 2 · 中提示**（适配性带外、不破灵魂 · 给选项等用户拍）
> "{需求} 会让 Vercel 的 {核心特征} 变成 {副作用}。
> (a) 接受偏差，做 {方案 A}
> (b) 折中：{方案 B}
> (c) 推荐切换 {更合适的 DNA}"

**适用**：路演大屏 sparse 密度、翻页 PPT 路演、需要 attention-grabbing 节奏。

---

**档 3 · 硬提示**（用户要改灵魂带 · 明确告知"这样做就不是 Vercel 了"）
> "你要改 {核心 token}。这一改成品就不再是 Vercel——{核心 token 在 Vercel 中承担的角色}。
> (a) 坚持改：保留其他基因，但成品观感接近 {另一种 DNA}
> (b) 折中：只在 {局部} 用，主体保持 Vercel
> (c) 取消"

**适用**：换配色、换字体、换字距规则、换 hairline shadow 为大阴影、换圆角档位。

---

### 灵魂带 / 适配性带 / 红线外

| 带 | 内容 | 处理 |
|---|---|---|
| **灵魂带**（动了 = 不是 Vercel） | 三色 / 双字体 / 字距收紧（西文签名） / hairline shadow / 6-8-pill 圆角 | 用户坚持改 → 档 3 提示，确认后照做 |
| **适配性带**（Vercel 不擅长但能做） | 长图载体 / 翻页 PPT / sparse 密度 / 范围外动效 / 暗色整页 | 档 1 或档 2 提示 |
| **红线外**（默认不做） | 渐变（除驯服 hero）/ 大 shadow / 衬线 / 摄影 / 多彩品牌按钮 / outline 按钮 / bounce 动效 / 页面表面中间档圆角 / emoji 装饰 / AI 营销话术 | 用户主动要 → 档 2 或档 3 提示 |

**Dark mode**：Vercel 真身是 Light-first、支持暗色切换，但本 skill 只实测了浅色系。用户要暗色整页 → 走档 2 提示（暗色灰阶参数未实测，不要临场编一套）。

**核心姿态**：dna-vercel 敢于说"这样做的话，成品就不是纯 Vercel 了"，但**绝不该说"我不做"**。永远给用户出口。

---

## 红线（禁止清单 · 先于正面描述）

AI 默认本能是 SaaS 营销页审美，会自动加：渐变、彩色按钮、大阴影、bounce 动效、衬线装饰、emoji 图标。这些**全部禁止**：

- ❌ **`background: linear-gradient(...)` 渐变背景** —— 除 hero 区可考虑被 blackoutLines SVG 遮罩驯服的渐变，其他位置一律纯色
  *为什么：渐变带视觉情绪，违反"信息清晰优先"——即使在品牌最感性时刻，色彩也必须经过工程结构过滤*
  档位：hero 内驯服渐变＝合规；hero 内不驯服的渐变＝档 2；整页 / 大面积情绪渐变＝档 3

- ❌ **大 box-shadow** —— 合规阴影是 hairline：`rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px 0px`
  *为什么：提升感阴影让界面变 SaaS 营销风，违反开发者文化*

- ❌ **衬线字体** —— Geist + Geist Mono（Inter / JetBrains Mono 兜底）双声足够
  *为什么：衬线带文学感，这套语言是工程感*

- ❌ **摄影图片 / 写实插画** —— 用 UI mockup / 代码块 / 几何 SVG 替代
  *为什么：开发者产品的"图"是界面和代码，不是摄影；有温度的插画不是开发者工具的语言*
  ⚠️ mockup 必须画成**真产品**（真菜单栏 / 侧栏 / 真内容文字），不做「灰框 + 占位文字」的 wireframe——检验标准：单看这块 mockup，像不像 Vercel 做的真界面
  时间不够画不了完整 mockup → 降级用**深底 code block** 当配图（合规的快路径），而不是降级成占位框

- ❌ **多彩品牌按钮** —— primary = #171717，secondary = 白底实色边框
  *为什么：行动本身就是重量，不需要品牌色"说服"开发者*

- ❌ **outline / ghost 按钮** —— secondary 用白底实色，不用 outline 边框感
  *为什么：outline 是工具感的廉价版本，实色边框更精确*

- ❌ **bounce / spring / 大幅 transform 动效** —— 克制范围内的动效（hover lift / fade-in / scroll reveal）默认开启，规范见下文 Motion 段；超出范围的弹跳、spring、大 scale、大 rotate 一律禁止
  *为什么：开发者不需要动效表演，克制是专业感的一部分*

- ❌ **`background: #ffffff` 纯白页面背景** —— 用 #fafafa（印刷纸底）
  *为什么：纯白太强，#fafafa 有印刷纸质感，降低视觉噪声*

- ❌ **页面表面的中间档圆角** —— 卡片 6px / 容器 8px / 按钮 100px pill 钉死；页面卡片和容器不出现 12-20px
  *为什么：精密分级才有工程感，档位之间不发明新值*
  例外（另一层级，不算破格）：浮层组件按官方 Geist Material 口径——tooltip 6px / menu·modal 12px / fullscreen 16px（实测 menu 12px 相符）；大容器 64px（实测 ×6）；textarea 类 24px——都是分级里的档位，不是「随手挑个圆角」

- ❌ **emoji 装饰 / 图标库装饰** —— 真正功能性的几何 SVG 可以；emoji ✨💎🚀 等装饰一律去掉
  *为什么：emoji 是消费者文化语言，跟工程感冲突*

- ❌ **"AI-powered" / "Revolutionary" / "Transform your..."** 营销话术 —— 开发者文化不接受夸张承诺；中文等价物同禁：「革命性 / 颠覆 / 赋能 / 重新定义 / 开启新时代」
  *为什么：开发者文化要求精确和证据，营销话术是反信任；文案写成可验证的事实句*

---

## 设计 Tokens（直接复用）

完整 CSS 变量见 [`tokens.css`](tokens.css)。**生成新页面时，第一步是引入这套 tokens 或内嵌等效 CSS 变量**。核心如下：

```css
:root {
  --page-bg:        #fafafa;        /* 不是纯白 */
  --surface:        #ffffff;
  --text-primary:   #171717;        /* 近黑 = 强调色 = 按钮色 */
  --text-secondary: #4d4d4d;
  --text-tertiary:  #666666;
  --border:         rgba(0,0,0,0.08);
  --shadow-card:    rgba(0,0,0,0.08) 0px 0px 0px 1px,
                    rgba(0,0,0,0.04) 0px 2px 2px 0px;
  --font-sans:      "Geist", "Inter", -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;
  --font-mono:      "Geist Mono", "JetBrains Mono", ui-monospace, monospace;
  --radius-sm:      6px;             /* 卡片 / code block */
  --radius-md:      8px;             /* 容器 / 大卡片 */
  --radius-pill:    100px;           /* 按钮 CTA */
}
```

### 字体加载

Geist 是 Vercel 真字体（Google Fonts 免费，OFL 开源）。联网页面在 `<head>` 加：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Geist:wght@100..900&family=Geist+Mono:wght@100..900&display=swap" rel="stylesheet">
```

- 离线 / CSP 禁外联（如 artifact）→ 不加这行，字体栈自动落 Inter → 系统字，DNA 不碎
- **Geist / Inter 都没有中文字形**：中文永远由 PingFang SC / Microsoft YaHei 渲染——这正是栈里显式写 CJK 的原因，也是下面「中文适配」段存在的原因

---

## 字距收紧规则（核心签名 · 西文）

**字号越大，字距收得越狠。** 这是 Vercel 重量感的来源——不是字重粗细，是密度。

**主规则用 em**（responsive / clamp() 场景 px 会失调）：大标题 **-0.04 ~ -0.06em**，随字号增强。实测曲线：

```
font-size  →  letter-spacing（vercel.com 实测）
─────────────────────────────
80px       →  -0.05em ≈ -4.0px   （外推，实测最大字号 48px）
56px       →  -0.05em ≈ -2.8px   （外推）
48px       →  -0.06em ＝ -2.88px （多数 ×18；hero H1 特例 -0.05em ×2）
40px       →  -0.06em ＝ -2.4px
32px       →  -0.04em ＝ -1.28px
24px       →  -0.04em ＝ -0.96px
16px 正文   →   0               （×831）
14px UI    →  -0.02em ＝ -0.28px （×623）
12px caption →  0
11px eyebrow →  +0.08em uppercase
```

钉死的是**原则**（负字距签名 + 越大越狠）；具体比率是克制默认（-0.04~-0.06em 带宽内可调）。**此表只管西文——中文见下段。**

---

## 中文适配（做中文页必读）

字距收紧是**西文签名**。中文由苹方 / 雅黑渲染，方块字字身已满，吃不了大负字距（会挤压变形）。中文页用双轨制：

- **默认值写中文友好**：大标题 `letter-spacing: -0.005em ~ 0`，行高比西文放宽一档（标题 1.15-1.25，正文 1.6-1.7）
- **英文段 / 短语标 `lang="en"`**，用 `:lang(en)` 恢复西文 DNA（负字距 + 紧行高）——同一份 CSS 双语各得其所
- 标题字重 600 在苹方上稳定，不用降
- 中文不用合成斜体（`em:lang(zh) { font-style: normal; }`），强调靠字重和层级
- 数字 / 单位 / 代码永远是拉丁字符——照常吃 Geist Mono，mono 签名不受影响

```css
/* 默认中文友好（html lang="zh-CN"）*/
.hero-h1 { font-size: 56px; letter-spacing: -0.005em; line-height: 1.2; }
/* 英文段恢复西文 DNA */
.hero-h1:lang(en), .hero-h1 :lang(en) { letter-spacing: -0.05em; line-height: 1.08; }
```

---

## 视觉决策速查

红线管「不做什么」，这里管高频决策的正向答案（与红线不重复的部分）：

| 决策 | Vercel 答案 |
|---|---|
| 标题重量感 | 字距收紧（密度），不是加字重 |
| 数字 / 单位 / 状态 / 代码 | Geist Mono（精确数据的声音，作用域自行判断——例如：按钮「14 天试用」这类叙述句保持 sans）；大号 mono 数字字距 -0.04 ~ -0.05em |
| 段落标题 caption / eyebrow | 11px mono uppercase +0.08em #666（实测另有 sans caption 一声，skill 默认 mono） |
| 分区方式 | border-bottom hairline + 留白，不用色块 |
| 浮层（tooltip / menu / modal / fullscreen） | Material 更高档：圆角 6 / 12 / 12 / 16px（官方口径），阴影仍克制 |
| 产品「配图」 | 深底 code block / 真产品 mockup（规格见 layouts.md#Landing） |

---

## Layout 按载体分发

Vercel 对不同载体有不同适配度——载体参数全部见 [`layouts.md`](layouts.md)。先看下表选章节：

| 载体 | 适配度 | 章节 | 触发提示档 |
|---|---|---|---|
| 落地页 / 定价页 / 文档 / 长文 | ★★★★★ 原生 | `layouts.md#Landing` | 无 |
| 公众号长图 / 竖向滚动 | ★★★☆☆ 可做 | `layouts.md#Longform` | 档 1 软提示 |
| PPT 翻页 / 投屏汇报 / 路演 | ★☆☆☆☆ 偏离基因 | `layouts.md#Slides` | 档 2 中提示 |
| 营销情绪页 / 品牌色渐变页 | ☆☆☆☆☆ 红线 | —— | 档 3 硬提示 |

**未在表中的载体**（仪表盘、邮件模板、移动 app 等）：先看是否能复用 Landing 的 card/stat 参数，不能复用时按档 2 提示用户。

---

## Motion 默认动效

Vercel 本来就有动效，只是克制。**默认开启，不询问用户**——除非用户要更夸张的动效（bounce / spring / 大 transform），走档 3 提示。

**总原则**：动效是为了让信息呈现得更顺，不是为了被看见。如果用户能"注意到"动效在发生，多半已经过头了。

### 白名单

| 项 | 数值 |
|---|---|
| 缓动 | `ease-out` / `cubic-bezier(0.16, 1, 0.3, 1)` / `linear`（仅 hero 渐变流动）|
| 微交互时长（hover / focus）| 150-200ms |
| 进入动效时长（fade-in / reveal）| 300-400ms |
| 翻页过渡 | 300ms ease-out（横向 translateX ≤ 2%）|
| 数字 stat 滚动 | 400-600ms |
| 性能 | 只用 `transform` 和 `opacity`（GPU 加速）|

### 最常用 2 种动效代码

```css
/* Hover 卡片：极小幅上浮 + shadow 加深（加深靠第二层扩散，ring 透明度不越 0.08 上限）*/
.card { transition: transform 200ms ease-out, box-shadow 200ms ease-out; }
.card:hover {
  transform: translateY(-1px);                /* 上限 -2px */
  box-shadow: rgba(0,0,0,0.08) 0 0 0 1px, rgba(0,0,0,0.06) 0 4px 12px;
}

/* 进入视口 fade-in + 上移
   ⚠️ 必须锁在 html.js 下——无 JS / JS 失败时内容直接可见，不许隐形 */
html.js .reveal {
  opacity: 0;
  transform: translateY(8px);
  transition: opacity 400ms ease-out, transform 400ms cubic-bezier(0.16, 1, 0.3, 1);
}
html.js .reveal.in-view { opacity: 1; transform: translateY(0); }
@media (prefers-reduced-motion: reduce) {
  html.js .reveal { opacity: 1; transform: none; transition: none; }
}
```

```js
document.documentElement.classList.add('js');
const io = new IntersectionObserver(
  (entries) => entries.forEach(e => e.isIntersecting && e.target.classList.add('in-view')),
  { threshold: 0.15 }
);
document.querySelectorAll('.reveal').forEach(el => io.observe(el));
```

### 关键约束

- **按钮 hover 不 translate**（按钮是行动本身，不该"飘"），只改 background + shadow
- **禁 `ease-in-out`** 在小尺寸交互上拖沓 / **禁 `ease-in`** 开始迟缓
- **超 600ms 的非装饰动效需要理由**
- **整页截图 / 导出验证时**：IntersectionObserver 在 fullPage 截图里不触发，reveal 元素会被截成空白——先注入 `.reveal{opacity:1!important;transform:none!important}` 再截，或导出场景直接去掉 reveal

---

## Pre-flight 自检清单

输出 HTML 之前逐条核对：

- [ ] 页面背景是 `#fafafa` 不是 `#ffffff`
- [ ] 强调/按钮色是 `#171717` 不是任何蓝/绿/品牌色
- [ ] 西文大标题字距是负值且用 em（48px → -0.06em 那种）；clamp()/responsive 场景**绝不用固定 px 字距**
- [ ] **中文页**：中文标题没吃西文负字距（默认 -0.005em ~ 0，`:lang(en)` 才恢复），正文行高 ≥1.6
- [ ] 字体只用 Geist/Inter + Geist Mono/JetBrains Mono（中文落系统苹方/雅黑），**没有衬线字体**；联网页面带了 Google Fonts 引入行
- [ ] 卡片用 hairline shadow（`rgba(0,0,0,0.08) 0px 0px 0px 1px, rgba(0,0,0,0.04) 0px 2px 2px 0px`），**无大 box-shadow**
- [ ] **无渐变**（除非 hero 区做了 blackoutLines 遮罩）
- [ ] 按钮 secondary 是**白底实色边框**，不是 outline/ghost
- [ ] **无摄影 / 写实插画** —— 用 UI mockup / 代码块 / SVG 替代
- [ ] mockup 是**真产品画法**：无灰框占位、无「主角位」类 placeholder 文字
- [ ] code block 按规格：`#171717` 深底白字 13px mono（或 docs 浅底语法色板），见 layouts.md#Landing
- [ ] 动效在 Motion 段白名单内（缓动 ease-out / 时长 150-400ms / hover 卡片 translateY ≤ -2px / 按钮 hover 不 translate），**无 bounce / spring / 大幅 scale / rotate**
- [ ] 数字 / 单位 / code / 标签性 mono 用 Geist Mono / JetBrains Mono
- [ ] 圆角：卡片 6px / 容器 8px / 按钮 pill，页面表面**无 12-20px 中间档**（浮层 menu/modal 12-16px 是另一层级，允许）
- [ ] eyebrow caption 用 11px uppercase letter-spacing 0.08em
- [ ] **无 emoji 装饰**
- [ ] **无"AI-powered" / "Revolutionary" / "Transform"** 营销话术

---

## 何时读子文件

主 SKILL.md 是规则 + 参数 + 核心审美骨架。遇到下列场景，读对应子文件：

| 场景 | 读哪个 |
|---|---|
| 写任何载体（落地页 / 长图 / slides）| [`layouts.md`](layouts.md) |
| 写 code block / nav / footer | [`layouts.md`](layouts.md)（Landing 组件规格）|
| 做中文页 | 本文件「中文适配」段 |
| 用户问"为什么 Vercel 这样做" | [`reasoning.md`](reasoning.md)（手法地图 / 推理方式 / 锚点参数二分）|
| 想学"如何用 Vercel 语言推导一个新场景" | [`reasoning.md`](reasoning.md)（推导示范）|
| 做完不确定是否符合 Vercel 基因 | [`reasoning.md`](reasoning.md)（锚点参数 [语言本身]）|
| 边界场景：用户要做 layouts.md 没覆盖的载体 | [`reasoning.md`](reasoning.md) + 用三档出口跟用户协商 |

**范围外 · 通用界面工艺**（a11y 细则 / 表单 UX / 性能 / hydration）：不属于本 skill——Vercel 官方有专门的 [web-design-guidelines skill](https://github.com/vercel-labs/agent-skills)（Web Interface Guidelines，80+ 条工艺规则），可与本 skill 叠装：视觉基因归这里，工艺归官方。本 skill 已内建的少数工艺护栏（reduced-motion / transform+opacity only / 触控 ≥44px / focus ring）与官方规则一致。

---

## 来源 + 致谢

逆向拆解自 [vercel.com](https://vercel.com)。

**Version**: v1.1 · 2026-07-06
**Skill 整理**: shona · TRUE NAME STUDIO

v1.1（2026-07）：字体切换 Vercel 真字体 Geist（Google Fonts，Inter 兜底）+ 加载指引；新增中文适配段；字距改 em 口径并按实测修正；圆角分级精确化（浮层 12/16px）；新增 code block / nav / footer / 定价卡实测规格与响应式护栏。
