# README Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite the GitHub profile README with an executive/strategic narrative layout featuring a gradient banner, role cards, career timeline, and career metrics.

**Architecture:** Single-file rewrite of `README.md` using Markdown + HTML with inline styles. Multi-column layouts use HTML `<table>` elements (the only multi-column layout GitHub renders). External image services (capsule-render, shields.io, github-readme-stats) supply badges, banners, and stat widgets.

**Tech Stack:** GitHub-Flavored Markdown, HTML with inline styles, capsule-render (banner SVG), shields.io (badges), github-readme-stats + streak-stats.demolab.com (activity widgets)

---

## Files

| Action | File | Purpose |
|--------|------|---------|
| Modify | `README.md` | Full rewrite — the only file changed |

---

### Task 1: Scaffold and Banner

**Files:**
- Modify: `README.md` (full replacement)

- [ ] **Step 1: Replace README.md with the banner block only**

  Overwrite the entire file with:

  ```markdown
  <!-- Banner -->
  <p align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Sandro%20Ariel%20G%C3%B3mez%20Araya&fontSize=36&fontColor=ffffff&fontAlignY=38&desc=CIO%20%C2%B7%20Founder%20%C2%B7%20Strategic%20Transformation&descAlignY=58&descSize=14" width="100%" alt="Banner" />
  </p>

  <p align="center">
    📍 Santiago, Chile &nbsp;·&nbsp; Open to Fintech &amp; Open Banking collaboration
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Finance-1f6feb?style=flat&logoColor=white" alt="Finance" />
    <img src="https://img.shields.io/badge/Insurtech-1f6feb?style=flat&logoColor=white" alt="Insurtech" />
    <img src="https://img.shields.io/badge/Retail-1f6feb?style=flat&logoColor=white" alt="Retail" />
    <img src="https://img.shields.io/badge/AI%20%26%20Data-1f6feb?style=flat&logoColor=white" alt="AI and Data" />
    <img src="https://img.shields.io/badge/Ecommerce-1f6feb?style=flat&logoColor=white" alt="Ecommerce" />
    <img src="https://img.shields.io/badge/Fintech-1f6feb?style=flat&logoColor=white" alt="Fintech" />
  </p>
  ```

- [ ] **Step 2: Verify capsule-render renders**

  Open this URL in a browser to confirm the banner image loads (substitute `%20` spaces and accented chars look correct):
  ```
  https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Sandro%20Ariel%20G%C3%B3mez%20Araya&fontSize=36&fontColor=ffffff&fontAlignY=38&desc=CIO%20%C2%B7%20Founder%20%C2%B7%20Strategic%20Transformation&descAlignY=58&descSize=14
  ```
  Expected: a purple-to-blue waving gradient banner with the name and subtitle visible.

- [ ] **Step 3: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add gradient banner and sector badges"
  ```

---

### Task 2: Tagline and Bio

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append tagline block**

  Add after the banner section:

  ```markdown
  <br>

  <p align="center">
    <em>"Driving strategic business transformation through technology — turning AI, data, and digital enablers into real competitive advantage."</em>
  </p>

  <br>
  ```

- [ ] **Step 2: Append bio paragraph**

  Add after the tagline:

  ```markdown
  CIO with a track record of leading technology-driven transformations across **finance, insurtech, retail, ecommerce, and education**. I bridge the gap between business strategy and technical execution — building high-performance engineering teams, scaling digital platforms, and embedding **AI and data capabilities** as core strategic levers. Founder twice over, failed once (El Manche 🍔), and still going.

  <br>
  ```

- [ ] **Step 3: Verify locally**

  Preview `README.md` in any Markdown renderer (VS Code preview, `grip`, or push to a GitHub branch). Confirm the italic tagline renders and the bio paragraph bold text appears.

- [ ] **Step 4: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add tagline and bio paragraph"
  ```

---

### Task 3: Expertise Pills

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append section header and pills**

  Add after the bio:

  ```markdown
  ## 🎯 Expertise

  **Sectors**

  <p>
    <img src="https://img.shields.io/badge/Finance-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Finance" />
    <img src="https://img.shields.io/badge/Insurtech-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Insurtech" />
    <img src="https://img.shields.io/badge/Retail-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Retail" />
    <img src="https://img.shields.io/badge/Ecommerce-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Ecommerce" />
    <img src="https://img.shields.io/badge/Fintech-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Fintech" />
    <img src="https://img.shields.io/badge/Edtech-1f2d3d?style=flat&labelColor=1f6feb&color=1f2d3d&logoColor=white" alt="Edtech" />
  </p>

  **Capabilities**

  <p>
    <img src="https://img.shields.io/badge/AI%20Strategy-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="AI Strategy" />
    <img src="https://img.shields.io/badge/Data%20Engineering-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="Data Engineering" />
    <img src="https://img.shields.io/badge/Digital%20Transformation-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="Digital Transformation" />
    <img src="https://img.shields.io/badge/Innovation-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="Innovation" />
    <img src="https://img.shields.io/badge/Agile%20%26%20DevOps-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="Agile and DevOps" />
    <img src="https://img.shields.io/badge/Open%20Banking-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white" alt="Open Banking" />
  </p>

  <br>
  ```

- [ ] **Step 2: Verify badge colours**

  Open one badge URL in a browser to confirm two-tone rendering:
  ```
  https://img.shields.io/badge/AI%20Strategy-2d1f3d?style=flat&labelColor=8957e5&color=2d1f3d&logoColor=white
  ```
  Expected: purple label on left (`8957e5`), dark right side (`2d1f3d`).

- [ ] **Step 3: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add expertise pills (sectors + capabilities)"
  ```

---

### Task 4: Current Roles Cards

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append section header and 2×2 role card table**

  Add after expertise pills:

  ```markdown
  ## 📌 Currently

  <table>
    <tr>
      <td style="background:#161b22;border:1px solid #30363d;border-radius:8px;padding:12px 16px;width:50%">
        <strong style="color:#e6edf3;font-size:14px">🏢 MetLife Colombia</strong><br>
        <span style="color:#8b949e;font-size:12px">Hands-on Chief Information Officer</span><br>
        <span style="background:#21262d;border-radius:4px;padding:2px 6px;font-size:11px;color:#8b949e">Insurtech · Strategic Transformation</span>
      </td>
      <td style="background:#161b22;border:1px solid #30363d;border-radius:8px;padding:12px 16px;width:50%">
        <strong style="color:#e6edf3;font-size:14px">⚡ Furio Lab</strong><br>
        <span style="color:#8b949e;font-size:12px">Founder</span><br>
        <span style="background:#21262d;border-radius:4px;padding:2px 6px;font-size:11px;color:#8b949e">AI · Innovation · Ventures</span>
      </td>
    </tr>
    <tr>
      <td style="background:#161b22;border:1px solid #30363d;border-radius:8px;padding:12px 16px">
        <strong style="color:#e6edf3;font-size:14px">🤝 SBY Technologies</strong><br>
        <span style="color:#8b949e;font-size:12px">Tech Advisor</span><br>
        <span style="background:#21262d;border-radius:4px;padding:2px 6px;font-size:11px;color:#8b949e">Technology Strategy</span>
      </td>
      <td style="background:#161b22;border:1px solid #30363d;border-radius:8px;padding:12px 16px">
        <strong style="color:#e6edf3;font-size:14px">🤝 Somos Pawer</strong><br>
        <span style="color:#8b949e;font-size:12px">Tech Advisor</span><br>
        <span style="background:#21262d;border-radius:4px;padding:2px 6px;font-size:11px;color:#8b949e">Technology Strategy</span>
      </td>
    </tr>
  </table>

  <br>
  ```

- [ ] **Step 2: Verify card table renders**

  Push to GitHub (or preview locally with `grip`). Confirm two rows of two cards appear. GitHub may strip some inline styles — check that border and background are visible. If GitHub strips `border-radius`, that is acceptable.

- [ ] **Step 3: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add current role cards"
  ```

---

### Task 5: By the Numbers

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append metrics section**

  Add after role cards:

  ```markdown
  ## 📊 By the Numbers

  <table>
    <tr>
      <td align="center" style="background:#161b22;border:1px solid #21262d;border-radius:10px;padding:14px 10px;width:25%">
        <strong style="color:#667eea;font-size:22px">15+</strong><br>
        <span style="color:#8b949e;font-size:10px;text-transform:uppercase;letter-spacing:0.5px">Years in Tech</span>
      </td>
      <td align="center" style="background:#161b22;border:1px solid #21262d;border-radius:10px;padding:14px 10px;width:25%">
        <strong style="color:#667eea;font-size:22px">6</strong><br>
        <span style="color:#8b949e;font-size:10px;text-transform:uppercase;letter-spacing:0.5px">Ventures Built</span>
      </td>
      <td align="center" style="background:#161b22;border:1px solid #21262d;border-radius:10px;padding:14px 10px;width:25%">
        <strong style="color:#667eea;font-size:22px">4</strong><br>
        <span style="color:#8b949e;font-size:10px;text-transform:uppercase;letter-spacing:0.5px">Sectors Led</span>
      </td>
      <td align="center" style="background:#161b22;border:1px solid #21262d;border-radius:10px;padding:14px 10px;width:25%">
        <strong style="color:#667eea;font-size:22px">3</strong><br>
        <span style="color:#8b949e;font-size:10px;text-transform:uppercase;letter-spacing:0.5px">Countries</span>
      </td>
    </tr>
  </table>

  <br>
  ```

- [ ] **Step 2: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add career metrics section"
  ```

---

### Task 6: Career Journey Timeline

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append timeline section**

  Add after metrics:

  ```markdown
  ## 🗂️ Career Journey

  <table>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">CTO &amp; Co-Founder</strong> · Clever.cl by BICE<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Fintech · Digital Banking</span>
      </td>
    </tr>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">CTO &amp; Founder</strong> · KIIT<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">B2B SaaS</span>
      </td>
    </tr>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">CTO &amp; Co-Founder</strong> · Moondo.cl<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Ecommerce · Retail Tech</span>
      </td>
    </tr>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">CTO &amp; Founder</strong> · Codecamp<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Edtech</span>
      </td>
    </tr>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">Cloud Solution Architect</strong> · Seguros Falabella<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Insurance · Retail</span>
      </td>
    </tr>
    <tr>
      <td style="color:#764ba2;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0;border-bottom:1px solid #21262d">
        <strong style="color:#e6edf3">Software Development Director</strong> · OW Latam<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Digital Consulting</span>
      </td>
    </tr>
    <tr>
      <td style="color:#484f58;font-size:16px;padding:8px 12px 8px 0;vertical-align:top">●</td>
      <td style="padding:8px 0">
        <strong style="color:#e6edf3">Software Engineer</strong> · Recorrido.cl<br>
        <span style="color:#6e7681;font-size:12px;font-style:italic">Travel Tech</span>
      </td>
    </tr>
  </table>

  <br>
  ```

- [ ] **Step 2: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add career journey timeline"
  ```

---

### Task 7: GitHub Activity Stats

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append stats section**

  Add after timeline:

  ```markdown
  ## 📈 GitHub Activity

  <table>
    <tr>
      <td>
        <a href="http://www.github.com/sandrogomez">
          <img src="https://github-readme-stats.vercel.app/api?username=sandrogomez&show_icons=true&count_private=true&title_color=0891b2&text_color=ffffff&icon_color=0891b2&bg_color=1c1917&hide_border=true&show_icons=true" alt="GitHub stats" />
        </a>
      </td>
      <td>
        <a href="http://www.github.com/sandrogomez">
          <img src="https://streak-stats.demolab.com/?user=sandrogomez&stroke=ffffff&background=1c1917&ring=0891b2&fire=0891b2&currStreakNum=ffffff&currStreakLabel=0891b2&sideNums=ffffff&sideLabels=ffffff&dates=ffffff&hide_border=true" alt="Contribution streak" />
        </a>
      </td>
    </tr>
  </table>

  <br>
  ```

- [ ] **Step 2: Verify both widgets load**

  Open each image URL directly in a browser and confirm they return an SVG image (not a 404 or error card). Especially verify the streak-stats domain — if it returns an error, fall back to: `https://github-readme-streak-stats.herokuapp.com/?user=sandrogomez&...` with the same parameters.

- [ ] **Step 3: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add GitHub activity stats"
  ```

---

### Task 8: Connect / Socials + Footer Banner

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Append socials and footer**

  Add after stats section:

  ```markdown
  ## 🤝 Connect

  <p>
    <a href="https://www.twitter.com/sandrogomez" target="_blank" rel="noreferrer">
      <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter" />
    </a>
    <a href="https://www.linkedin.com/in/sgomeza" target="_blank" rel="noreferrer">
      <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
    <a href="http://www.medium.com/sandrogomez" target="_blank" rel="noreferrer">
      <img src="https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white" alt="Medium" />
    </a>
    <a href="https://www.github.com/sandrogomez" target="_blank" rel="noreferrer">
      <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
    </a>
    <a href="http://sandrogomez.com" target="_blank" rel="noreferrer">
      <img src="https://img.shields.io/badge/Blog-667eea?style=for-the-badge&logo=safari&logoColor=white" alt="Personal Blog" />
    </a>
  </p>

  <!-- Footer -->
  <p align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=80&section=footer" width="100%" alt="Footer" />
  </p>
  ```

- [ ] **Step 2: Final end-to-end review**

  Push to GitHub and view the live profile at `https://github.com/sandrogomez`. Scroll through the full README and check:
  - [ ] Banner loads and displays name + subtitle
  - [ ] Tagline renders in italic
  - [ ] Bio bold text visible
  - [ ] Expertise pills show two colours (blue vs purple)
  - [ ] Role cards render as a 2×2 grid
  - [ ] Metrics row shows 4 numbers in `#667eea` colour
  - [ ] Timeline shows 7 entries with purple dots
  - [ ] Both stat widgets load (not error cards)
  - [ ] Social buttons render with logos
  - [ ] Footer wave visible

- [ ] **Step 3: Commit**

  ```bash
  git add README.md
  git commit -m "feat: add socials section and footer — README redesign complete"
  ```

---

### Task 9: Push to GitHub

- [ ] **Step 1: Push**

  ```bash
  git push origin main
  ```

- [ ] **Step 2: Verify live profile**

  Open `https://github.com/sandrogomez` in a browser and confirm the new README is rendering correctly as the public profile page.
