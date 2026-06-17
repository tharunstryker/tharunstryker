<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,4&height=120&section=header&text=&animation=fadeIn" width="100%" />
</p>

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=Syncopate&weight=700&size=26&pause=1000&color=00D4FF&center=true&vCenter=true&width=820&lines=Tharun;Founder+%26+Engineer;Building+Naeris;Neeti[...]
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/B.Tech%20AI%20%26%20Data%20Science-7C3AED?style=flat-square&labelColor=0D0D1A" />
  &nbsp;
  <img src="https://img.shields.io/badge/Location-Krishnagiri%2C%20Tamil%20Nadu-00D4FF?style=flat-square&labelColor=0D0D1A" />
  &nbsp;
  <img src="https://img.shields.io/badge/Entity-Naeris-7C3AED?style=flat-square&labelColor=0D0D1A" />
</p>

<p align="center">
  <a href="https://naeris.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-naeris.vercel.app-00D4FF?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D0D1A" />
  </a>
  &nbsp;
  <a href="mailto:tharunstryker@gmail.com">
    <img src="https://img.shields.io/badge/Email-tharunstryker%40gmail.com-7C3AED?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D0D1A" />
  </a>
  &nbsp;
  <a href="https://github.com/tharunstryker">
    <img src="https://img.shields.io/badge/GitHub-tharunstryker-00D4FF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D0D1A" />
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=tharunstryker&style=flat-square&color=7C3AED&label=Profile+Views&labelColor=0D0D1A" />
  &nbsp;
  <img src="https://img.shields.io/github/followers/tharunstryker?style=flat-square&color=00D4FF&label=Followers&labelColor=0D0D1A" />
  &nbsp;
  <img src="https://img.shields.io/github/stars/tharunstryker?style=flat-square&color=7C3AED&label=Stars&labelColor=0D0D1A" />
</p>

---

## ◈ About

<img align="right" width="340" src="https://github-readme-stats.vercel.app/api?username=tharunstryker&show_icons=true&theme=tokyonight&bg_color=070714&border_color=00D4FF&title_color=00D4FF&icon_color[...]

B.Tech AI & Data Science engineer and solo founder. Building **Naeris** — shipped real products: a published PyPI package, an open-source AI tooling suite, and a production SaaS platform — entirely on Android via Termux.

**Open To:**
- AI/ML freelance contracts
- Early-stage technical collaboration
- Open-source contributions

---

## ◈ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,javascript,html,css&theme=dark" /><br/>
  <sub><b>Languages</b></sub>
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=supabase,postgres,nodejs&theme=dark" /><br/>
  <sub><b>Backend & Databases</b></sub>
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=vercel,git,github,linux,bash&theme=dark" /><br/>
  <sub><b>Cloud, DevOps & Tooling</b></sub>
</p>

---

## ◈ Featured Projects

<details>
<summary><b>⚡ psiwatch — Zero-Dependency ML Drift Detection</b></summary>
<br/>

**Dataset drift detection for production ML pipelines.** Detects covariate drift, distribution shift, and data quality degradation between training and production data using PSI, Chi-Square, Mean Shift, and Standard Deviation analysis.

**Why it matters:** Models trained on historical data silently fail when production data drifts. Most teams discover this *after* the model breaks. psiwatch alerts you *before* it's too late.

### Core Features
- **Zero dependencies** — pure Python, standard library only. ~15KB install. Works anywhere Python runs (Windows, Mac, Linux, Termux/Android, Google Colab).
- **CLI tool** — `psiwatch compare train.csv production.csv` outputs formatted reports with severity flags.
- **Multiple I/O modes** — CSV files, pandas DataFrames, Python dicts, lists of dicts.
- **4 detection methods** — PSI (Population Stability Index), Mean Shift (std deviations), Std Deviation Shift, Chi-Square test.
- **Rich output** — Terminal (ANSI colored), HTML (shareable), JSON (CI/CD), TXT (logs).
- **Trend direction** — Numeric columns show trend as ↑ ↓ → (increasing, decreasing, stable).
- **Vanished category detection** — Flags categories that disappeared from production vs training.
- **CI/CD integration** — `--fail-on-drift` flag exits with code 1 on drift (block deployments).
- **Baseline locking** — Lock training data as a statistical fingerprint, ship with model, check in production.
- **Directory watching** — Poll new CSV files and auto-check against a locked baseline.
- **Webhook alerts** — Send Slack/Discord/custom JSON alerts when drift detected.
- **Config files** — `psiwatch.toml` or `.psiwatchrc` for persistent settings.
- **Trend analysis** — Track drift across time sequences (`psiwatch trend day1.csv day2.csv day3.csv`).

### Quick Start
```bash
pip install psiwatch
psiwatch compare old.csv new.csv --output report.html
```

### CLI Commands
```bash
psiwatch compare train.csv prod.csv              # Compare two datasets
psiwatch compare train.csv prod.csv --fail-on-drift  # Fail if drift > threshold
psiwatch compare train.csv prod.csv --webhook https://hooks.slack.com/...  # Alert on drift
psiwatch lock train.csv                          # Lock baseline
psiwatch check prod.csv --fail-on-drift          # Check against lock
psiwatch trend day1.csv day2.csv day3.csv        # Track drift over time
psiwatch watch data/ --once                      # Check directory (cron-safe)
psiwatch summary train.csv prod.csv              # Health score only (scripts)
```

### Python API
```python
import psiwatch

# CSV or DataFrame
psiwatch.compare("old.csv", "new.csv", output="report.html")

# Raw results
result = psiwatch.analyze("old.csv", "new.csv")
print(result["health_score"])  # 0-100

# Catch drift in code
from psiwatch import DriftDetected
try:
    psiwatch.compare("old.csv", "new.csv", fail_on_drift=True)
except DriftDetected:
    # send alert, stop deploy, etc.
```

### Comparison with Competitors
| Feature | psiwatch | evidently | alibi-detect |
|---|---|---|---|
| **Dependencies** | ✓ Zero | ✗ Heavy | ✗ Heavy |
| **Install size** | ✓ ~15KB | ✗ ~50MB+ | ✗ ~100MB+ |
| **CLI tool** | ✓ Yes | ✗ No | ✗ No |
| **CI/CD `--fail-on-drift`** | ✓ Yes | ✗ No | ✗ No |
| **Works on Android (Termux)** | ✓ Yes | ✗ No | ✗ No |
| **Pure Python** | ✓ Yes | ✗ No | ✗ No |
| **Vanished category detection** | ✓ Yes | ✗ No | ✗ No |
| **Trend direction (↑↓→)** | ✓ Yes | ✗ No | ✗ No |
| **Self-upgrade via CLI** | ✓ Yes | ✗ No | ✗ No |

### Example Report
```
══════════════════════════════════════════════════════════════
  PSIWATCH REPORT
  baseline: train.csv  →  new: production.csv
══════════════════════════════════════════════════════════════

  [ALERT] credit_score [numeric] — HIGH DRIFT
     → Mean shifted by 2.20 std devs (752 → 624)  ↓
     → PSI = 11.12 (significant drift)
     ┌ Mean:    752 → 624  ↓
     ├ Std:     48 → 71
     ├ PSI:     11.12
     └ Min:     600 → 420

  [ALERT] loan_type [categorical] — HIGH DRIFT
     → New categories found: ['BNPL', 'Crypto']
     → Categories vanished: ['Personal']
     → PSI = 4.19

  ──────────────────────────────────────────────────────────────
  Health Score: 11/100 (Significant Drift — Action Required)
══════════════════════════════════════════════════════════════
```

### Health Score Thresholds
| Score | Status | Action |
|---|---|---|
| 80–100 | ✓ Stable | Model is fine, no action needed |
| 50–79 | ⚠ Moderate | Monitor closely, investigate root cause |
| 0–49 | ✗ Significant | Retrain model immediately |

| Repository | Links |
|---|---|
| **Source** | [github.com/tharunstryker/psiwatch](https://github.com/tharunstryker/psiwatch) |
| **PyPI** | [pypi.org/project/psiwatch](https://pypi.org/project/psiwatch) |

</details>

<details>
<summary><b>🔍 PromptLens — Open-Source AI Response Comparator</b></summary>
<br/>

Developer utility for comparing LLM responses across multiple providers side-by-side. Built for prompt engineers evaluating model behavior at the output level.

| Attribute | Detail |
|---|---|
| **Stack** | Vanilla JS · Multi-provider LLM APIs |
| **Scale** | Public open-source |
| **Repository** | [github.com/tharunstryker/PromptLens](https://github.com/tharunstryker/PromptLens) |

</details>

<details>
<summary><b>🎯 Neeti by Aevra — AI SaaS Platform for Indian Students</b></summary>
<br/>

Production-grade dual-product SaaS. CareerKit: five AI career tools. CardStudio: interactive greeting card engine with gates, themes, animations, and hosted share links. Every layer sole-authored — architecture, design, backend, frontend, DevOps, security audit.

| Attribute | Detail |
|---|---|
| **Stack** | Vanilla JS · Supabase · Vercel Edge · Cloudinary · Gemini/Groq/GitHub Models/OpenRouter |
| **AI** | 4-provider fallback chain · 5 rotating Gemini keys · server-side prompt isolation |
| **Security** | RLS on all 5 tables · two-cookie admin auth · `_buildEFILES(cfg)` per-tier asset bundling |
| **Link** | [naeris.vercel.app](https://naeris.vercel.app) |

</details>

---

## ◈ Experience

**Founder & Engineer** · **Naeris**
`Jan 2026 — Present`

- Published `psiwatch` to PyPI — zero-dependency Python ML monitoring library
- Built and shipped Neeti: CareerKit + CardStudio, production SaaS on Vercel + Supabase
- 4-stage AI fallback chain with 5-key Gemini rotation across all tools
- Full security audit: RLS across 5 tables, tier-gated asset bundling, two-cookie admin auth
- Built entirely on Android via Termux — no laptop, no PC

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PyPI-3775A9?style=flat-square&logo=pypi&logoColor=white" />
  <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" />
  <img src="https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/Termux-000000?style=flat-square&logo=android&logoColor=white" />
</p>

---

## ◈ GitHub Analytics

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=tharunstryker&theme=tokyonight&background=070714&border=00D4FF&stroke=00D4FF&ring=7C3AED&fire=00D4FF&currStreakLabel=00D4FF&sideLabel[...]
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=tharunstryker&layout=compact&theme=tokyonight&bg_color=070714&border_color=7C3AED&title_color=7C3AED&text_color=FFFFFF&hide_b[...]
</p>

---

## ◈ Contribution Activity

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=tharunstryker&bg_color=070714&color=00D4FF&line=7C3AED&point=FFFFFF&area=true&area_color=7C3AED&hide_border=false&border_colo[...]
</p>

---

## ◈ Contribution Snake

<p align="center">
  <img src="https://raw.githubusercontent.com/tharunstryker/tharunstryker/output/github-contribution-grid-snake-dark.svg" />
</p>

---

## ◈ Current Focus

```yaml
status:
  building:
    - psiwatch — ML drift detection library (PyPI live)
    - Neeti by Aevra — CareerKit + CardStudio (Razorpay KYC pending)
  open_to:
    - AI/ML freelance contracts
    - Early-stage technical collaboration
```

---

## ◈ Connect

<p align="center">
  <a href="mailto:tharunstryker@gmail.com">
    <img src="https://img.shields.io/badge/Gmail-tharunstryker%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D0D1A" />
  </a>
  &nbsp;
  <a href="https://github.com/tharunstryker">
    <img src="https://img.shields.io/badge/GitHub-tharunstryker-00D4FF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D0D1A" />
  </a>
  &nbsp;
  <a href="https://naeris.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-naeris.vercel.app-7C3AED?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D0D1A" />
  </a>
</p>

---

<p align="center">
  <i>"No framework. No build step. No shortcuts."</i>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,4&height=100&section=footer&text=&animation=fadeIn" width="100%" />
</p>
