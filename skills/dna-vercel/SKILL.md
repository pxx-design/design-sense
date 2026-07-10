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

## 先及格，再风格（通用排版标准 · 全 DNA 共用层）

> 风格之前，先及格。任何风格都站在同一套排版标准上——工程克制不是这套标准的例外，是它的一种「怎么达成」。
> 生成后**能渲染就渲染出来看一眼**，对着下面七问自检；**认出失格，就回去补，别用装饰盖过去。**

### 及格七问 · 每条都教你「失格长什么样」

| 判准 · 扫一眼问自己 | 失格的样子（要认出的 tell） | 工程克制靠什么达成 |
|---|---|---|
| **1 层级**：这一屏有没有一个明确的第一落点？（逐屏问，不是全页平均） | 同屏两三个东西一样重，没有主角 | 字号跨度（display 峰独占它那一屏）+ 留白——不靠颜色、不靠大装饰 |
| **2 亲密**：间距在说「一组 / 分块」吗？ | 到处等距，或忽宽忽窄没逻辑，看不出谁跟谁一组 | 间距按结构角色分三档：组内紧、块间松、区段间更松，差距要看得出 |
| **3 对齐**：都贴着同一套隐形线吗？ | 边缘游离，东西没贴任何线 | 硬边栅格，左缘 / 基线咬死——镜像终端的字符对齐 |
| **4 对比**：要不同，够不够决绝？ | 近似双胞胎（15 挨 16、灰度只差一点），看着像噪声 | 少数几档、每档拉开（官网整页仅 7-12 种字号）；宁可档少，不要一堆挨着的 |
| **5 一致**：同角色同待遇吗？ | 同类卡片这里 padding 一个样、那里一个样 | 同结构角色 → 同一个角色 token，全程复用 |
| **6 节奏**：疏密是有意的吗？ | 一种密度到底，像填表格（文档载体最容易犯） | 该空的地方敢大胆空（hero、区段之间），该紧的地方紧（数据、代码块）；落地页以视口为构图单位（见 layouts.md#Landing）。克制 ≠ 均匀 |
| **7 可读**：行长 / 行距 / 对比够吗？ | 正文行拉太宽、行距太挤、灰得看不清 | 护栏：西文 45-75 字符 / 中文 ~40 字；**行长与行距联动**（行越长行距越宽——官方 docs 行长 90 字符配 1.7 行距），正文行距放宽 |

### 咬合纪律 · 全篇的骨（动杆必补及格）

工程克制是靠「**拿掉**」定义自己的：拿掉颜色（近黑独一）、拿掉装饰、拿掉摄影、拿掉大阴影。

> **每拿掉一个工具，它原本能承担的那条及格，就必须由留下的工具补上——否则就是「套了皮、丢了骨」。**

- 拿掉了「用颜色做层级 / 对比」 → 层级和对比**全压到字号跨度 + 字重 + 留白**。所以工程克制字阶必须陡、留白必须敢——**这不是风格偏好，是在补及格。**
- 拿掉了「用色块 / 装饰做分组」 → 分组**全压到间距 + hairline 线**。所以间距必须携带结构意思、线必须分层（外框 > 内线）。
- 拿掉了「用摄影做视觉焦点」 → 焦点**压到排版本身 + 一个真 mockup / 代码块**。

**反向自检（最常踩的坑）**：你把 Vercel 的皮套上了——灰了、简了、上了 mono——但页面**一片平、没主角、没呼吸**？那就是**拿掉了工具却没补及格**。回去用字号和留白把层级挣回来，**别加装饰回来**。

### 角色词汇 · 咬合的执行面（禁裸值）

字号和间距**不许裸写 px**——全部挂在角色上（值是克制默认，见 tokens.css；载体差异见 layouts.md）：

**字号六声**（对应 tokens.css 现成类）：

| 角色 | 类 / token | 纪律 |
|---|---|---|
| display 峰 | `.text-display` | **全页唯一**（hero 主标题） |
| 区段标题 | `.text-h1` | 每区段一个 |
| 块 / 卡片标题 | `.text-h2` / `.text-h3` | |
| 正文 | `.text-body` / `.text-small` | |
| 辅助说明 | 12-13px caption 档 | |
| eyebrow / 标签 | `.text-caption`（mono uppercase） | 唯一正字距的声 |

**间距三档**：`--gap-element`（组内）< `--gap-block`（块间）< `--gap-section`（区段间）——三档差距要看得出（Q2 的结构化）。

**动笔前先写角色清单**：这页的峰是谁、几个区段、哪些块——先声明，再写 CSS。角色分错时所有值都「合法」、任何校验器都结构性看不见，清单是唯一把这步判断亮出来的地方。真需要第七种字号身份？先写一行理由再加（护栏，不是禁令）。

*具体数字（字阶值、间距档位、量化阈值）不在这一层——它们退到「参数参考」（tokens.css + 下文字距表）当后台默认。这一层只教「看懂什么叫踩住了标准」。好的分配长什么样，看 [`specimen.md`](specimen.md)（官网四现场带批注范例）。*

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

**Dark mode**：Vercel 真身是 Light-first、支持暗色切换。v1.2 起暗版参数已按官方 Geist 暗值落进 tokens.css（见「Dark 模式」节）——用户要暗色整页 → **档 1 软提示后直接做**，不再档 2。

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
- **离线也要真字体？预装即可**：Geist / Geist Mono 是 OFL 开源（Google Fonts 可下载，mac 可 `brew install --cask font-geist font-geist-mono`）——字体栈本地优先，装了自动命中，代码零改动。skill 包不内置字体文件
- **Geist / Inter 都没有中文字形**：中文永远由 PingFang SC / Microsoft YaHei 渲染——这正是栈里显式写 CJK 的原因，也是下面「中文适配」段存在的原因

---

## Dark 模式（v1.2 · 参数=官方 Geist 暗值）

默认浅色（light-first 不变）。用户要暗色整页 → 档 1 软提示后直接做。启用方式：`<html data-theme="dark">`，tokens.css 尾部覆盖块自动切换全部变量。

**映射按 token 角色，不是数值取反**（官方自己就这么做：灰阶中段 700/800 两态共用、主文字停在 #ededed 不到纯白）：

| 角色 | Light | Dark（官方 Geist 实测） |
|---|---|---|
| 页面底 | #fafafa | **#000000** |
| 卡面 | #ffffff | **#0a0a0a**（卡仍比页面亮一档，层级方向不变） |
| 主文字 / 强调 / 按钮 | #171717 | **#ededed（非纯白）** |
| 次文字 | #4d4d4d | #a1a1a1 |
| hairline 边框 | 黑 8% alpha | **白 14% alpha（#ffffff24）** |
| hairline 阴影 | ring 黑 8% + 2px 黑 4% | **ring 白 15% + 1px 2px 黑 16%**（阴影靠更黑不靠更大） |
| code block | #171717 深底 | #1a1a1a 面板 + hairline 分界 |
| 功能色 | 7 色 | **不换 hue**（官方两态同值——身份制跨主题成立） |

**Dark 专属红线**：

- ❌ **纯白文字 `#fff`** —— 官方主文字是 #ededed；纯白在黑底上过曝
- ❌ **数值取反 / `filter: invert`** —— 暗版是按角色重配的另一张表，不是浅色的负片
- ❌ **暗底大阴影提层级** —— 层级 = 表面明度爬梯（#000 → #0a0a0a → #1a1a1a）+ 白 alpha hairline
  暗页卡片 hover 同理：浅色档"第二层阴影扩散加深"在暗底失效——改 **ring 升档**（白 14% → 白 20%）+ translateY 照旧
- ❌ **给品牌色 / 功能色加饱和"提亮"** —— 官方功能色两态同值，不许临场调
- 按钮 primary 反相：#ededed 底 / #0a0a0a 字——行动仍是页面上最重的中性色，仍不用品牌色

暗页里 hero 驯服渐变的 blackoutLines 遮罩填充色跟 `--page-bg` 走（#000）。中文适配、字距、圆角、动效规则与浅色完全一致。

---

## 字距收紧规则（核心签名 · 西文 · 参数参考层）

**字号越大，字距收得越狠。** 这是 Vercel 重量感的来源——不是字重粗细，是密度（新版 hero 64px 仅 w400-450：字更大、字重反而更轻，论点更极端了）。

**主规则用 em**（responsive / clamp() 场景 px 会失调）：大标题 **-0.04 ~ -0.06em**，随字号增强。实测曲线（2026-07 改版复测，整体成立）：

```
font-size  →  letter-spacing（vercel.com 实测）
─────────────────────────────
80px       →  -0.05em ≈ -4.0px   （外推）
64px       →  -0.06em ＝ -3.84px （2026-07 实测 hero，w400-450）
56px       →  -0.06em ＝ -3.36px （2026-07 实测；旧版外推 -0.05em 作废）
48px       →  -0.06em ＝ -2.88px （sans 与 mono display 同值）
40px       →  -0.06em ＝ -2.4px  （docs h1，w600）
32px       →  -0.04em ＝ -1.28px
30px       →  -0.05em ＝ -1.5px  （2026-07 实测）
24px       →  -0.04em ＝ -0.96px
22px       →  -0.02em ＝ -0.44px （2026-07 实测）
16px 正文   →   0
14px UI    →   0                （2026-07 复测归零；旧版实测 -0.02em，两版并存可选）
12px caption →  0
11px eyebrow →  正字距 uppercase（旧版 +0.08em；新版实测 +0.02em w500——带宽内可调）
```

钉死的是**原则**（负字距签名 + 越大越狠）；具体比率是克制默认（-0.04~-0.06em 带宽内可调）。**此表只管西文——中文见下段。**（本段是「先及格」的后台数值，课在顶部，这里只是把课落成数的默认。）

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
| 标题重量感 | 字距收紧（密度），不是加字重——营销页 display 仅 w400-450；docs 标题才用 w600 补小字号的层级 |
| 文档载体页底 | #ffffff 纯白（docs 官方实测 2026-07）；营销页 / 长文才是 #fafafa |
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

- [ ] 页面背景是 `#fafafa` 不是 `#ffffff`（**docs 载体例外**：官方文档用纯白底，2026-07 实测）
- [ ] **动笔前写了角色清单**（这页的峰是谁 / 几个区段 / 哪些块）；无裸值字号 / 间距——全部挂 `.text-*` 角色类与 `--gap-*` 三档
- [ ] **display 峰全页唯一**，且它那一屏没有第二个抢落点的东西
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
- [ ] **（仅暗页）** 页面底 #000 卡面 #0a0a0a；主文字 #ededed **不是 #fff**；hairline 用白 alpha（黑 alpha 在暗底看不见）；无 invert；功能色未加饱和

**渲染目检 · 及格七问**（上面 checklist 之后、交付之前的独立一步——checkbox 查的是代码，这一步查的是眼睛）：
能渲染就渲染出来看一眼，对照顶部「先及格」七问逐条认失格。认出失格 → **回角色 token 重推**，用字号和留白把它挣回来；**不加装饰盖过去、不挪 1px 凑数**。

---

## 何时读子文件

主 SKILL.md 是规则 + 参数 + 核心审美骨架。遇到下列场景，读对应子文件：

| 场景 | 读哪个 |
|---|---|
| 写任何载体（落地页 / 长图 / slides）| [`layouts.md`](layouts.md) |
| 想看「好的分配」长什么样（编排 / 节奏 / 峰谷密读） | [`specimen.md`](specimen.md)（官网四现场带批注 + 实测真值）|
| 写 code block / nav / footer | [`layouts.md`](layouts.md)（Landing 组件规格）|
| 做中文页 | 本文件「中文适配」段 |
| 用户问"为什么 Vercel 这样做" | [`reasoning.md`](reasoning.md)（手法地图 / 五个反直觉决策 / 推理方式 / 锚点参数二分）|
| 想学"如何用 Vercel 语言推导一个新场景" | [`reasoning.md`](reasoning.md)（推导示范）|
| 做完不确定是否符合 Vercel 基因 | [`reasoning.md`](reasoning.md)（锚点参数 [语言本身]）|
| 边界场景：用户要做 layouts.md 没覆盖的载体 | [`reasoning.md`](reasoning.md) + 用三档出口跟用户协商 |

**范围外 · 通用界面工艺**（a11y 细则 / 表单 UX / 性能 / hydration）：不属于本 skill——Vercel 官方有专门的 [web-design-guidelines skill](https://github.com/vercel-labs/agent-skills)（Web Interface Guidelines，80+ 条工艺规则），可与本 skill 叠装：视觉基因归这里，工艺归官方。本 skill 已内建的少数工艺护栏（reduced-motion / transform+opacity only / 触控 ≥44px / focus ring）与官方规则一致。

---

## 来源 + 致谢

逆向拆解自 [vercel.com](https://vercel.com)。

**Version**: v1.3 · 2026-07-10（内部验证中，未发布）
**Skill 整理**: shona · TRUE NAME STUDIO

v1.3（2026-07-10，内部）：顶部新增「先及格，再风格」层（及格七问 + 咬合纪律 + 角色词汇/禁裸值）——教认失格不教参数，数字退「参数参考」；Pre-flight 加角色清单 / 唯一峰两项 + 独立「渲染目检·七问」步骤；新增 specimen.md 官网四现场带批注范例（峰/谷/密/读，2026-07 改版复测：核心基因全部存活；校订 14px 字距归零、docs 纯白底、display w400-450、64/56px 字距实测值）；layouts.md#Landing 新增「一屏一模块」编排规则；tokens.css 新增 --gap-* 间距三档。
v1.2（2026-07，内部）：新增 Dark 模式——tokens.css 暗覆盖块 + 映射表 + dark 红线，参数取自官方 Geist 暗值（vercel.com/geist/colors 实测）；暗色整页从档 2 降为档 1。
v1.1.1（2026-07）：reasoning.md 新增「五个反直觉决策」显式段——重组自推理方式段既有内容，不新增规则。
v1.1（2026-07）：字体切换 Vercel 真字体 Geist（Google Fonts，Inter 兜底）+ 加载指引；新增中文适配段；字距改 em 口径并按实测修正；圆角分级精确化（浮层 12/16px）；新增 code block / nav / footer / 定价卡实测规格与响应式护栏。
