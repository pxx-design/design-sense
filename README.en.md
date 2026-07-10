# Design Sense

> Design judgment for AI agents. — [中文](./README.md)

Design Sense is a polymath designer for AI agents — handcrafted by **shona**, in continuous training across the visual philosophies of gold-standard brands.

Not just colors, fonts, and tokens, but the judgment behind them: what to use, how much to use, what to avoid, and how to reason when the spec does not cover a new scene.

---

## Why

Design taste is not mysticism.

AI can follow parameters, but it often fails at taste.
It adds the wrong things: stock photos, decorative gradients, generic icons.
It overuses brand colors because it knows the color value, but not the dosage.
It falls back to average SaaS patterns when a component or page is not described.

What's missing isn't parameters — every hex value on the web can be scraped. What's missing is the judgment behind them: what to use, how much, what never to touch, how to reason where the spec is silent.

Design Sense is built for that gap. It doesn't hand the AI parameters — anyone can scrape `#faf9f5 ×320`. It hands the AI the judgment above them.

A good design language should not only tell AI what a product looks like.
It should teach AI how that product thinks.

---

## Half human, half AI

This library is co-created. The AI does the extraction — twelve dimensions of measured evidence, every value traceable. The human does the judgment — what is soul and what is surface, what becomes a rule and what stays free for the AI to reason about.

In the age of AI, taste is the part of the system a human leaves behind.

---

## The finished pages, first

The pricing page on the left was built **from scratch by a context-free agent reading nothing but the skill files** — no reference screenshots, no human tweaks. The page on the right is the Anthropic case study itself, typeset in the language it teaches.

<table>
<tr>
<td width="50%"><img src="docs/assets/preview-dna-vercel.png" alt="Pricing page generated with dna-vercel"></td>
<td width="50%"><img src="docs/assets/preview-dna-anthropic.png" alt="Anthropic case study typeset with dna-anthropic"></td>
</tr>
<tr>
<td align="center"><b>dna-vercel</b> · Engineered Restraint 工程克制</td>
<td align="center"><b>dna-anthropic</b> · Vintage Editorial 复古编辑</td>
</tr>
</table>

The bar was never "how many parameters were copied" — it's **"does it look like they made it."** You use the language to build your own thing, not to redraw the reference brand.

Want engineered precision — near-black on paper gray, mono numbers, hairline shadows? Reach for **dna-vercel**.
Want trustworthy vintage warmth — serif body on warm cream, hand-drawn plates, zero shadows? Reach for **dna-anthropic**.

More tastes in training: razor-sharp dark, cinematic product drama, bold gradients.

**One designer. Many tastes — and counting.**

---

## Coverage by domain

|   | Domain                   | Brand reference | Aesthetic                        | Status         |
|---|--------------------------|-----------------|----------------------------------|----------------|
| ✓ | Developer infrastructure | **Vercel**      | Engineered Restraint · 工程克制  | v1.3 · 2026-07 |
| ✓ | AI labs                  | **Anthropic**   | Vintage Editorial · 复古编辑     | v1.2 · 2026-07 |
| ○ | Developer workspace      | Linear          | —                                | training       |
| ○ | Fintech & payments       | Stripe          | —                                | training       |
| ○ | Premium consumer         | Apple           | —                                | training       |
| ○ | B2B SaaS                 | Intercom        | —                                | training       |

*Future training: design tools · e-commerce · media · education · healthcare · gaming · automotive · social · and more.*

---

## Install

Each completed brand is a standard [Claude Code](https://claude.com/claude-code) skill — five files, self-contained:

```bash
git clone https://github.com/pxx-design/design-sense.git

# User-level (all projects)
cp -r design-sense/skills/dna-vercel ~/.claude/skills/
cp -r design-sense/skills/dna-anthropic ~/.claude/skills/

# Or per-project
cp -r design-sense/skills/dna-vercel /your-project/.claude/skills/
```

Then ask Claude:

> "Build me a pricing page using dna-vercel."
>
> "Build me a research index page using dna-anthropic."

The skill activates and the designer reaches for that brand's training.

**中文用户**：完整使用指南（安装、提示词模板、两套 skill 的选用对照、常见问题）见 [docs/dna-vercel-usage.zh.md](docs/dna-vercel-usage.zh.md) 与 [docs/dna-anthropic-usage.zh.md](docs/dna-anthropic-usage.zh.md)。

---

## Anatomy of a skill

Every skill ships the same five files, at five altitudes:

| File | Altitude | Carries |
|------|----------|---------|
| `SKILL.md` | Judgment | Baseline-before-style (seven universal typography checks + compensation discipline), red lines first, negotiation protocol, pre-flight checklist, CJK adaptation |
| `reasoning.md` | Language | Cultural root, counter-intuitive decisions, how to derive new scenes |
| `layouts.md` | Parameters | Per-medium specs — every value tagged *measured* or *derived* |
| `tokens.css` | Implementation | Drop-in CSS variables and base components |
| `specimen.md` | Calibration | Annotated scenes from the reference brand's live site — what good allocation looks like, every claim tied to a measured value |


---

## Methodology

shona builds each brand's training in four layers, in increasing levels of judgment:

### 1. Evidence — machine-extracted

The brand's gold-standard reference is reverse-engineered across 12 dimensions — from color systems and typography to motion language and what is deliberately absent. This is the queryable evidence base — exhaustive but not yet a philosophy.

### 2. Reasoning — designer-judged

shona reads the evidence and articulates the brand's actual thinking: its cultural root, what makes it different, why each parameter takes the value it does, and what it refuses to do. **Machine extraction stops here. Judgment begins.**

### 3. Insight — driven by the brand, not by a template

How many distinct insights a brand carries is decided by the brand itself. Each insight may fuse multiple aspects of the brand into one observation. This is how shona internalizes the brand and encodes it into a skill.

### 4. Validation — cold-run tested

No skill ships until a **context-free agent** — reading nothing but the skill files — passes a set of design-decision probes (both shipped skills: 8/8) and builds a complete page that clears the skill's own pre-flight checklist. Consistency is machine-tested; taste is signed off by human eyes.

---

shona asks not just *"what is this value?"* but *"why is this value this value?"* and *"what does this brand refuse to do?"*

Each new brand sharpens the polymath's training.

---

## Scope

Design Sense teaches **brand-level visual language** — what a page should look and feel like. Generic interface craft (accessibility, forms, performance) is out of scope.

---

## License & Disclaimer

MIT for code and skill text. Brand typefaces are proprietary; skills use officially designated substitutes, clearly noted.

Design Sense is an independent project — not affiliated with or endorsed by Vercel, Anthropic, or any brand listed above. Skill content is based on independent observation of public web pages. Brand names and trademarks belong to their respective owners.

---

## Author

shona · 2026
