# README Redesign — Sandro Gómez GitHub Profile

**Date:** 2026-03-21
**Status:** Approved

---

## Goal

Refactor the GitHub profile README (`sandrogomez/sandrogomez`) with an updated catalog of experience and career metrics, presented in a unique and modern executive style.

---

## Style Direction

**Executive / Strategic** with a **Narrative / Story-Led** layout.

- Dark background (`#0d1117`) matching GitHub dark theme
- Gradient accent: `#667eea → #764ba2 → #f093fb`
- Clean section headers with horizontal rules
- Two-tone pill system: blue for sectors, purple for tech capabilities
- Cards for current roles, dot-based timeline for career history

---

## Sections (in order)

### 1. Gradient Banner
Use `capsule-render` external SVG:

```
https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Sandro%20Ar
iel%20G%C3%B3mez%20Araya&fontSize=36&fontColor=ffffff&fontAlignY=38&desc=CIO%20%C2%B7%20Founder%20%C2%B7%20Strategic%20Transfor
mation&descAlignY=58&descSize=14
```

Below the banner image, include a centered line:
`📍 Santiago, Chile · Open to Fintech & Open Banking collaboration`

Sector tag badges as shields.io `flat` style in a row:
Finance · Insurtech · Retail · AI & Data · Ecommerce · Fintech

### 2. Tagline
HTML `<blockquote>` or a `<p>` with left border style (`border-left: 3px solid #764ba2; padding-left: 12px`):

> "Driving strategic business transformation through technology — turning AI, data, and digital enablers into real competitive advantage."

### 3. Bio Paragraph
Short 3-sentence paragraph:
- Sectors: finance, insurtech, retail, ecommerce, and education
- Bridge role: business strategy ↔ technical execution, building engineering teams, scaling digital platforms, embedding AI and data
- Human touch: "Founder twice over, failed once (El Manche 🍔), and still going."

### 4. Expertise Pills
Two-color pill system as shields.io `flat` badges rendered via `<img>`:
- **Blue (`#1f6feb` bg label):** Finance · Insurtech · Retail · Ecommerce · Fintech · Edtech
- **Purple (`#8957e5` bg label):** AI Strategy · Data Engineering · Digital Transformation · Innovation · Agile & DevOps · Open Banking

### 5. Current Roles (2×2 card grid)
HTML `<table>` with 2 columns to simulate a card grid (GitHub doesn't support CSS grid/flexbox).

Each cell is styled as a card:
- Background: `#161b22`
- Border: `1px solid #30363d`
- Border-radius: `8px`
- Padding: `12px 16px`
- Company name: bold, `color: #e6edf3`, font-size 14px
- Role title: `color: #8b949e`, font-size 12px
- Tag: small pill — `background: #21262d; border-radius: 4px; padding: 2px 6px; font-size: 11px; color: #8b949e`
- Cards do not link anywhere

| Card | Company | Title | Tag |
|------|---------|-------|-----|
| 🏢 | MetLife Colombia | Hands-on CIO | Insurtech · Strategic Transformation |
| ⚡ | Furio Lab | Founder | AI · Innovation · Ventures |
| 🤝 | SBY Technologies | Tech Advisor | Technology Strategy |
| 🤝 | Somos Pawer | Tech Advisor | Technology Strategy |

### 6. By the Numbers
4-cell HTML `<table>` row. Number cells use `color: #667eea` (solid, no gradient — GitHub strips `background-clip: text`). Center-aligned.

- **15+** Years in Tech
- **6** Ventures Built
- **4** Sectors Led
- **3** Countries

### 7. Career Journey (Condensed Timeline)
HTML `<table>` with 3 columns: dot (●), role/org, sector tag. Newest to oldest based on known order:

| # | Dot | Role | Company | Sector Tag |
|---|-----|------|---------|-----------|
| 1 | `●` `#764ba2` | CTO & Co-Founder | Clever.cl by BICE | Fintech · Digital Banking |
| 2 | `●` `#764ba2` | CTO & Founder | KIIT | B2B SaaS |
| 3 | `●` `#764ba2` | CTO & Co-Founder | Moondo.cl | Ecommerce · Retail Tech |
| 4 | `●` `#764ba2` | CTO & Founder | Codecamp | Edtech |
| 5 | `●` `#764ba2` | Cloud Solution Architect | Seguros Falabella | Insurance · Retail |
| 6 | `●` `#764ba2` | Software Development Director | OW Latam | Digital Consulting |
| 7 | `●` `#484f58` | Software Engineer | Recorrido.cl | Travel Tech |

**Note:** El Manche (Burger House) is referenced as a personality note in the bio paragraph but is intentionally excluded from the career timeline — it was a food venture, not a tech role.

### 8. GitHub Activity
Two widgets side-by-side via HTML `<table>`:
- `github-readme-stats`: `https://github-readme-stats.vercel.app/api?username=sandrogomez&show_icons=true&hide=&count_private=true&title_color=0891b2&text_color=ffffff&icon_color=0891b2&bg_color=1c1917&hide_border=true`
- Streak stats: `https://streak-stats.demolab.com/?user=sandrogomez&stroke=ffffff&background=1c1917&ring=0891b2&fire=0891b2&currStreakNum=ffffff&currStreakLabel=0891b2&sideNums=ffffff&sideLabels=ffffff&dates=ffffff&hide_border=true`
  - Note: prefer `streak-stats.demolab.com` over the old `herokuapp.com` URL which goes offline periodically.

### 9. Connect / Socials
Row of shields.io social badges (`for-the-badge` style) linking to:
- Twitter: `https://www.twitter.com/sandrogomez`
- GitHub: `https://www.github.com/sandrogomez`
- LinkedIn: `https://www.linkedin.com/in/sgomeza`
- Medium: `http://www.medium.com/sandrogomez`
- Personal Blog: `http://sandrogomez.com`

---

## Technical Constraints

GitHub README rendering rules that shape implementation:
- **No CSS classes or external stylesheets** — all styling via inline `style=""` attributes
- **No JavaScript**
- **HTML tables** are the only way to do multi-column layouts
- **`<img>` tags** for shields.io badges and external stat widgets
- **SVG via external services** (capsule-render) for gradient banners
- **No CSS `background-clip: text`** — use solid `color: #667eea` for accent numbers

---

## What's Removed

- Old emoji-heavy role list (replaced by role cards + timeline)
- Skills icon wall — **removed entirely** in this redesign (too long, not needed alongside the expertise pills)
- Duplicate social badges from top of old README (consolidated into Connect section at bottom)
