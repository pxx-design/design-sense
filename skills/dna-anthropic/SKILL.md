---
name: dna-anthropic
description: 为 HTML/CSS 页面注入 Anthropic「复古编辑」视觉基因（别名 anthropic-dna）。Use when：生成或重构研究机构官网、AI 产品页、长文阅读页、技术博客、论文/报告页、文档、公众号长图、翻页 slides、工具台，或用户点名 Anthropic 风 / 复古编辑 / 复古书卷 / 像一本书 / dna-anthropic。核心：#faf9f5 暖纸底、slate #141413 暖黑、长文正文衬线签名、0 阴影明暗分层、天然染料颜料盒、橙不进控件、字距温柔 ≤-0.02em、手绘图版；中文页自带宋黑分轨适配。来源：anthropic.com 逆向实测 + 官方 brand-guidelines 对答案。
---

# Skill · Design DNA · Anthropic

## 一句话哲学

> **复古编辑（Vintage Editorial）**——复古在材料，克制在版面与用量
> 每个设计决策都在回答同一个问题：「这让它更像一本被认真编辑过的书 / 一个克制的研究机构，还是又把它推回了'又一个 AI 创业公司'？」

镜像人文出版传统——旧书纸、衬线正文、铜版图版、天然染料。**内容极度前沿，表达极度古典**：不靠 hype 说服你，靠"被认真编辑过"的样子让你信。

---

## Cultural Root（文化根）

用户是在意 AI 安全与长期主义的思考者，他们的文化记忆是**书**：图书馆、大学出版社、十九世纪的科学图谱（达尔文《物种起源》式的严肃但不冰冷）。

`#faf9f5` 是旧书纸的暖，不是显示器的白；正文排衬线因为书的正文从来是衬线；插画是一只手画的线描配古典图版；整盘颜色用天然染料命名（manilla / kraft / oat / fig / heather）；mono 和 `ANTHROP\C` 反斜杠字标给够技术可信度，让它不至于纯文学。

**跟相邻流派的区分**（同是减法，气质相反）：
- 工程克制（Vercel）＝终端记忆：冷、等宽、字距 -0.06em 狠收、纯灰白
- **复古编辑（Anthropic）＝书的记忆**：暖、衬线、字距最多 -0.02em、一盒暖色极克制地用

---

## 手法地图（主 → 次）

六个手法合起来造"一本被认真编辑过的书"，按离判准轴远近排主次——顶上的最难也最定义它，底下的最显眼却只是表皮：

1. **文案**（天花板）——克制、精确、陈述句、零 hype 词；"编辑"二字首先指文字
2. **排版**——构图（一个峰一片平地 / 左对齐默认 / 640px 阅读列）+ 排字（温柔字距 / lining 数字）
3. **批注**——笔（一根实线下划线）+ 荧光笔（软染料小标签）；颜色只住荧光笔
4. **图版**——默认手绘线描，hero 级才升格点描 / 博物 plate（罕见是生效机制）
5. **材料**——暖奶油纸 + 天然染料颜料盒 + mono 技术可信（颜色是地板，不是全部）
6. **动效**——它是纸不是屏：不浮起、不视差、不发光

**一句排序：文案是天花板，颜色是地板。** 只学到配色字体＝"漆对了、骨没对"。完整推理见 [`reasoning.md`](reasoning.md)。

---

## 设计前自问（一句话 self-check）

写代码前 + 写完后各问一次：

> **"这像一本被认真编辑过的书，还是像又一个 AI 创业公司的营销页？"**

如果它开始像营销页、像 SaaS 模板、像终端、像发布会——退回去，换一个出版物会做的选择。

---

## 意图层（生成前必做）

### 三问

| 问题 | 选项 | 默认 |
|---|---|---|
| **载体** | 机构官网 / 长文阅读页 / 工具台 / 长图 / 翻页 PPT | 机构官网 |
| **表达强度** | 克制端（公司站/编辑层，默认） / 产品端放松（+局部 sans 正文、唯一橙主动作） | 克制端 |
| **动效** | 默认克制（纸感） / 纯静态 | 默认克制 |

### 三档出口

**档 1 · 软提示**（适配性带内 · 提示后直接做）：长图载体、工具台高密度、产品端放松。
**档 2 · 中提示**（不破灵魂 · 给选项等用户拍）：翻页 PPT、暗色整页、需要 attention-grabbing 节奏。
**档 3 · 硬提示**（要改灵魂带 · 明确说"这样就不是 Anthropic 了"再给出口）：sans 正文、加阴影、橙做按钮体系、纯白底、狠字距。

**核心姿态**：敢说"这样做就不是这套语言了"，但**绝不说"我不做"**——永远给出口。

### 灵魂带 / 适配性带 / 红线外

| 带 | 内容 | 处理 |
|---|---|---|
| **灵魂带**（动了 = 不是 Anthropic） | 长文正文衬线 / #faf9f5 暖纸 / 0 阴影 / 字距温柔 / 橙不进控件 / 颜料盒非功能色 | 档 3 |
| **适配性带**（不擅长但能做） | 长图 / 翻页 PPT / 暗色整页 / 工具台 / 产品端放松 | 档 1 或 2 |
| **红线外**（默认不做） | 阴影 / 渐变 / 纯白底 / sans 长文正文 / 摄影 3D / emoji / 霓虹 / SaaS feature 模块 / 逐节居中 | 档 2 或 3 |

**Dark mode**：真身是 Light-first、支持 slate 暗主题反相（按钮反相值有实测：ivory 底 slate 字），但暗色全盘参数未实测——用户要暗色整页走档 2，不要临场编一套暗色板。

---

## 红线（禁止清单 · 先于正面描述）

AI 默认本能是 SaaS 营销页审美 + "AI 感"装饰。这些**全部禁止**：

- ❌ **box-shadow** —— 0 阴影（实测 shadows=[]）。层级靠暖色块明暗混排（一排 1 深卡 + 2 浅卡）+ 1px 边框
  *为什么：纸面是平的，书页没有投影；阴影一来就变 SaaS*
  例外：嵌入的产品截图卡自带阴影是"图的内容"，不破此条

- ❌ **纯白 `#ffffff` 页面背景** —— 用 #faf9f5 暖奶油
  *为什么：白属于显示器，旧书纸是暖的*

- ❌ **Claude 橙当 CTA / 按钮 / 文字色** —— 按钮一律中性高对比反相（slate-dark 底 ivory 字）
  *为什么：出版物的强调是克制的；橙当按钮就从书的火花掉进 SaaS 的转化色*
  橙的合法出场全在**内容**里：编辑层手绘插画底、数据图两支色之一。公司站控件实测 0
  产品层例外：**唯一主动作**（Ask/提交级）可用橙，全站就一处；导航栏 Try 类不算——实测色是深陶土 ~#c6613f（--accent-deep），不是 #d97757 原色

- ❌ **渐变** —— 页面是 flat 暖色块
  *为什么：印刷是实色铺陈，不是屏幕光晕*

- ❌ **sans 长文正文** —— 长文阅读体必须衬线（替身 Lora）
  *为什么：书的正文从来是衬线；sans 正文是这套语言要反的科技产品文化——违反＝丢掉签名*
  精确口径：签名在"长文阅读体"；UI chrome / nav / 短文本 / 表格用 sans 合法

- ❌ **Vercel 式狠字距** —— 只三档 0 / -.005em / -.02em；大号 serif display 接近 0 甚至微正
  *为什么：出版排版温柔留白，狠收紧是终端工程感*

- ❌ **摄影 / 写实照片 / 3D / 等轴测 / 彩色插画** —— 用手绘线描 / 蚀刻图版 / 几何 SVG
  *为什么：百科全书是铜版图版，不是产品摄影*
  ⚠️ 禁手搓"假笔触"：用平滑 SVG 模拟手绘＝把承重的诚实信号降格成装饰——宁可摆真件或不用
  产品截图（真实 UI）不算摄影：产品页语境合法（表达强度旋钮的产品端，可自带柔阴影）；机构页 hero 锚仍首选手绘 / 蚀刻

- ❌ **emoji / 图标库装饰** —— 学术出版物不用表情符号（功能性细线 icon 允许）

- ❌ **亮饱和科技色 / 霓虹** —— 颜料盒是天然染料，饱和天花板 ~55%
  *为什么：物理染料天生不会 neon*
  染料（heather/manilla/kraft…）**不做功能面板底**、不做功能色系统——它们是批注高亮的底色

- ❌ **SaaS feature 区块模块** —— 书是连续阅读流，不是 eyebrow→大标题→卡网格逐节重复的营销模块

- ❌ **逐节居中 / 均匀标题梯** —— 能逐行扫读的内容永不居中；标题层级靠 serif↔sans / 字重 / 位置，不靠尺寸阶梯（条目标题 ≈ 正文字号，约 0.9-1.2×——实测 list H3 16px 配 17-20px 正文；护栏是"绝不放大喊叫"）

- ❌ **阅读区 sidebar** —— 长文是 640px 单一窄列，侧栏挤占阅读轴

- ❌ **控件用 pill 胶囊** —— 按钮 / segmented 一律 8px 方圆角；pill 只给 chip / 徽章小件

- ❌ **"AI-powered" / "Revolutionary" / "Transform" 及中文等价**（革命性 / 颠覆 / 赋能 / 重新定义）
  *为什么：文案是这套语言的天花板——克制、精确、陈述句，说感受不解释道理*

---

## 设计 Tokens（直接复用）

完整 CSS 变量见 [`tokens.css`](tokens.css)。生成新页面第一步引入这套 tokens。核心：

```css
:root {
  --ivory-light:  #faf9f5;   /* 主背景 · 旧书纸（×320）*/
  --ivory-medium: #f0eee6;   /* 次级面板 */
  --oat:          #e3dacc;   /* 暖面板上限 */
  --slate-dark:   #141413;   /* 文字 / 深卡 / 按钮（×543 暖黑非纯黑）*/
  --cloud-medium: #b0aea5;   /* 边框 / 次要（×365）*/
  --border:       rgba(20,20,19,0.3);
  --clay:         #d97757;   /* 橙：插画底 / 数据色——不进控件 */
  --heather:      #cbcadb;   /* 软染料 pill 例 */
  --font-serif:   "Lora", Georgia, "PingFang SC", "Microsoft YaHei", serif;
  --font-sans:    "Poppins", -apple-system, "PingFang SC", "Microsoft YaHei", Arial, sans-serif;
  --font-mono:    "IBM Plex Mono", ui-monospace, monospace;
  --radius-main:  8px;       /* 按钮/控件——方圆角非 pill */
  --radius-large: 16px;      /* 卡片 */
  --section-main: 10rem;     /* 奢侈留白 */
}
```

### 字体加载

真身 Anthropic Serif / Sans / Mono 是**专有字体，不可分发**。skill 用**官方替身**（官方 brand-guidelines 给定 Poppins/Lora）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400..700;1,400..700&family=Poppins:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
```

- 离线 / CSP 禁外联 → 不加，自动落 Georgia / Arial / 系统字，DNA 不碎
- **中文题字**另需 Noto Serif SC w600（全量大——`&text=` 子集只载题字那几个字）；**中文正文不用宋**，见下面「中文适配」
- Lora / Poppins 无中文字形：中文永远由苹方 / 雅黑渲染——栈里已显式写

---

## 字距规则（温柔 · 与 Vercel 相反）

**只三档：`0` / `-0.005em` / `-0.02em`。** 最狠仅到 -0.02em（UI / nav 主力，实测 ×166）；小字标签 -0.005em 档；**大号 serif display 接近 0 甚至微正**（96px 实测 +1.6px ≈ +0.016em——大字号衬线要从容，不是密度）。

三档限的是**负向**——全大写小标签按排版惯例微正拉开（+0.04em 级）不算违规。重量感来自留白（section 10rem）和衬线本身，不来自把字挤在一起。**绝不出现 -0.04em 以下的狠收——那是隔壁 Vercel 的签名。**

---

## 中文适配（做中文页必读 · 宋黑分轨）

serif 签名到中文**不等于**"中文也排宋体"。官方中文界面实测：中文正文落**苹方黑体**，刻意不用宋——中文那份温度由优质人文黑体承载。**开关是"角色/字号"，不是"语言"**：

- **中文正文 / UI / 说明 → 苹方**（字体栈已内建），行距放宽 ~1.7、微开字距 +0.018em（黑体排成编辑式）
- **中文大题字 / 标题板 / "翻开一页书"那一刻 → 思源宋体 Noto Serif SC 加粗到 600**（w400 偏细；系统 Songti/SimSun 冷感，别用）——「宋体标题 + 黑体正文」是中文编辑排版最地道的搭配
  中文题字行高比拉丁 display 放宽一档（1.1 → 1.15-1.2）；「大号 serif 微正」是拉丁实测口径，中文题字字距取 0 不微正（方块字自带满字身）
- 中文不用合成斜体（`em:lang(zh){font-style:normal}`）；强调用**同一根实线下划线**（批注笔），**别用着重号**（另一种设备，破坏整体）
- 高亮（荧光笔）中英同规：软染料 pill 只点小词，绝不刷整句
- 数字 / 代码照常 mono + lining，不受影响

---

## 视觉决策速查

红线管「不做什么」，这里是高频决策的正向答案：

| 决策 | Anthropic 答案 |
|---|---|
| 层级 | 明暗混排（1 深 2 浅）+ 1px 边框 + 留白——不是阴影；每屏至少一处墨色锚 |
| 强调 | 笔（实线下划线 1.36px / offset 3px / 线色 #b0aea5）+ 荧光笔（软染料 pill 点小词） |
| 按钮 | slate-dark 黑底 ivory 字 / 8px 方圆角；secondary 透明底 + 1px slate 边 |
| 标题层级 | serif↔sans 切换 + 字重 + 位置；结构标题 sans 24px w600 恒定，不逐级放大 |
| 居中 | 只给全页唯一的峰（标题板 / 情绪句 / 结尾 dark CTA）；能扫读的永远靠左 |
| 数据图 | 两支数据色（橙 #eb6834 + 蓝 #4a90e2）+ 灰阶/tint 补位；Tufte 式，图题在卡外 |
| 插图 | 默认手绘线描（老物件隐喻 + 留抖）；hero 级才升格点描/博物 plate 且全站罕见 |
| 状态/分类标 | tag 三态（meta 文字 / outline chip / 软染料 pill）+ segmented 轨道——不是彩色徽章系统 |
| 中文标题 | 宋黑分轨：题字 Noto Serif SC w600，正文苹方 |

---

## Layout 按载体分发

| 载体 | 适配度 | 章节 | 触发提示档 |
|---|---|---|---|
| 机构官网 / 产品页 / 文档 | ★★★★★ 原生 | `layouts.md#Landing` | 无 |
| 长文阅读页 / 博客 / 报告 | ★★★★★ 原生（签名场景） | `layouts.md#Article` | 无 |
| 工具台 / Dashboard | ★★★☆☆ 可做 | `layouts.md#Console` | 档 1 |
| 公众号长图 / 竖向滚动 | ★★★☆☆ 可做 | `layouts.md#Longform` | 档 1 |
| PPT 翻页 / 投屏路演 | ★☆☆☆☆ 偏离基因 | `layouts.md#Slides` | 档 2 |
| 强情绪营销页 / 渐变霓虹页 | ☆☆☆☆☆ 红线 | —— | 档 3 |

未在表中的载体：先看能否复用 Landing / Article 的参数，不能复用按档 2 提示。

---

## Motion 默认动效

**原则（实测层）**：它是纸，不是屏——不浮起、不视差、不发光、无 bounce / spring。
**数值（推导默认——官方动效未实测，不杜撰为"实测"）**：微交互 150-200ms / 进入 fade 300-400ms / ease-out；只动 transform + opacity；hover 不 translateY 卡片（纸不浮起），可以极轻变底色 / 边框加深。

```css
/* 进入 fade（锁 html.js——无 JS 内容直接可见）*/
html.js .reveal { opacity: 0; transform: translateY(6px); transition: opacity 400ms ease-out, transform 400ms ease-out; }
html.js .reveal.in-view { opacity: 1; transform: translateY(0); }
@media (prefers-reduced-motion: reduce) { html.js .reveal { opacity: 1; transform: none; transition: none; } }
```

```js
document.documentElement.classList.add('js');
const io = new IntersectionObserver(es => es.forEach(e => e.isIntersecting && e.target.classList.add('in-view')), { threshold: 0.15 });
document.querySelectorAll('.reveal').forEach(el => io.observe(el));
```

- **整页截图 / 导出验证**：IO 在 fullPage 截图不触发——先注入 `.reveal{opacity:1!important;transform:none!important}` 再截，或导出场景直接去 reveal

---

## Pre-flight 自检清单

- [ ] 页面背景 `#faf9f5` 不是 `#ffffff`、不是冷灰
- [ ] **0 box-shadow**；层级靠明暗混排 + 1px 边框；每屏至少一处墨色锚（深卡/黑按钮/重墨标题）
- [ ] 长文正文是 serif（Lora）；UI chrome / 表格才 sans；**中文正文落苹方不落宋，中文题字才 Noto Serif SC w600**
- [ ] 字距在三档内（0 / -.005 / -.02em），大号 serif 微正；**无 -0.04em 以下狠收**
- [ ] 按钮黑反相 8px 方圆角，**没有橙按钮**（除非产品层唯一主动作）；控件无 pill 胶囊
- [ ] 无渐变、无摄影 / 3D / emoji、无霓虹饱和
- [ ] 染料只出现在高亮 pill / 插画底 / 图版卡，**不做功能面板底、不做功能色系统**
- [ ] 强调用下划线（1.36px / offset 3px / #b0aea5）；高亮只点小词不刷整句；中文无着重号、无合成斜体
- [ ] 居中只有全页一处峰；列表 / 可比较内容全部左对齐；长文 640px 单列无 sidebar
- [ ] 数据图两支色相封顶 + 灰阶/tint 补位；无甜甜圈 / 3D 柱 / 彩虹图例
- [ ] 数字 lining 等高（`lnum pnum`），serif 正文也是
- [ ] 动效无 bounce / 视差 / 发光；卡片 hover 不上浮；reveal 锁 html.js
- [ ] 文案零 hype 词（中英），陈述句，标题不对仗目录体
- [ ] section 留白够奢侈（主间距 10rem 级），不是 SaaS 的 64px 挤

---

## 何时读子文件

| 场景 | 读哪个 |
|---|---|
| 写任何载体（官网 / 长文 / 工具台 / 长图 / slides） | [`layouts.md`](layouts.md) |
| 写数据图 / 手绘插画 / tag / segmented | [`layouts.md`](layouts.md)（图版 / Tag 段） |
| 做中文页 | 本文件「中文适配」段 |
| 用户问"为什么 Anthropic 这样做" | [`reasoning.md`](reasoning.md)（六手法 / 五个反直觉决策） |
| 推导 layouts.md 没覆盖的新载体 | [`reasoning.md`](reasoning.md)（判准轴 + 锚点参数二分）+ 三档出口协商 |
| 做完不确定像不像 | [`reasoning.md`](reasoning.md)（锚点参数 [语言本身]）+ 本文件 Pre-flight |

**范围外 · 通用界面工艺**（a11y 细则 / 表单 UX / 性能）：不属于本 skill——可叠装 Vercel 官方 [web-design-guidelines skill](https://github.com/vercel-labs/agent-skills)（通用工艺，与品牌无关）：视觉基因归这里，工艺归它。

---

## 来源 + 致谢

逆向拆解自 [anthropic.com](https://www.anthropic.com)（computed-style 实测 1253 元素 + 编辑层 / 产品层多页校准），色板经官方 [anthropics/skills brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines) 对答案（7/7 全中）；替身字体（Poppins / Lora）为官方 brand-guidelines 给定。

**Version**: v1 · 2026-07-06
**Skill 整理**: shona · TRUE NAME STUDIO

v1（2026-07）：首发——中文宋黑分轨适配、数据图版与插画规格、tag / segmented 控件、批注双笔强调、Console 载体支持。
