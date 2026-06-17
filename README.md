<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,4&height=120&section=header&text=&animation=fadeIn" width="100%" />
</p>

<h1 align="center">Tharun Stryker</h1>

<p align="center">
  <a href="https://readme-typing-svg.demolab.com">
    <img src="https://readme-typing-svg.demolab.com?font=Syncopate&weight=700&size=24&pause=1000&color=00D4FF&center=true&vCenter=true&width=820&lines=Founder+%26+Engineer;AI+%26+Data+Science;Building+Production+Systems" alt="Typing Animation" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/B.Tech%20AI%20%26%20Data%20Science-7C3AED?style=flat-square&labelColor=0D0D1A" />
  <img src="https://img.shields.io/badge/Location-Krishnagiri%2C%20Tamil%20Nadu-00D4FF?style=flat-square&labelColor=0D0D1A" />
  <img src="https://img.shields.io/badge/Entity-Naeris-7C3AED?style=flat-square&labelColor=0D0D1A" />
</p>

<p align="center">
  <a href="https://naeris.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-naeris.vercel.app-00D4FF?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D0D1A" />
  </a>
  <a href="mailto:tharunstryker@gmail.com">
    <img src="https://img.shields.io/badge/Email-tharunstryker%40gmail.com-7C3AED?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D0D1A" />
  </a>
  <a href="https://github.com/tharunstryker">
    <img src="https://img.shields.io/badge/GitHub-tharunstryker-00D4FF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D0D1A" />
  </a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=tharunstryker&style=flat-square&color=7C3AED&label=Profile+Views&labelColor=0D0D1A" />
  <img src="https://img.shields.io/github/followers/tharunstryker?style=flat-square&color=00D4FF&label=Followers&labelColor=0D0D1A" />
  <img src="https://img.shields.io/github/stars/tharunstryker?style=flat-square&color=7C3AED&label=Stars&labelColor=0D0D1A" />
</p>

---

## Professional Overview

I am an **AI & Data Science engineer** and founder of **Naeris**, focused on shipping production-grade systems that solve real problems. My work spans open-source libraries, SaaS platforms, and ML infrastructure—all built with a commitment to code quality, security, and user impact.

**Currently Open To:**
- AI/ML freelance engagements and consulting
- Early-stage technical partnerships
- Significant open-source contributions
- Speaking and technical writing opportunities

---

## Core Competencies

| **Dimension** | **Expertise** |
|---|---|
| **Languages** | Python, JavaScript, TypeScript, HTML, CSS, Bash |
| **Backend Systems** | Node.js, Supabase, PostgreSQL, REST APIs, Serverless |
| **Cloud & DevOps** | Vercel, GitHub, Linux, CI/CD pipelines, Edge functions |
| **AI/ML** | Drift detection, multi-provider LLM orchestration, fallback chains, embeddings |
| **Security** | Row-level security (RLS), authentication, API key management, data isolation |

---

## Featured Projects

### psiwatch — ML Drift Detection

**A zero-dependency Python library for detecting data drift in production ML pipelines.**

Most data science teams discover model degradation *after* it causes business impact. `psiwatch` detects drift early by comparing production data against training distributions.

**Why It Matters:**
- Production models fail silently when data distributions shift
- Existing solutions require heavy dependencies or complex setup
- `psiwatch` provides immediate, actionable insights

**Distinguishing Features:**
- **Zero external dependencies** — ~15KB install, works on any Python environment (Windows, Mac, Linux, Android/Termux, Google Colab)
- **Multiple detection methods** — PSI, Chi-Square test, mean shift analysis
- **CLI + Python API** — Integrate however suits your workflow
- **CI/CD ready** — JSON output, `--fail-on-drift` flag for automated gates
- **Rich output formats** — Terminal reports, HTML dashboards, webhook alerts (Slack, Discord, custom)

**Quick Example:**
```bash
pip install psiwatch
psiwatch compare train.csv prod.csv --output report.html
```

| Feature | psiwatch | Competitors |
|---|---|---|
| **Zero dependencies** | Supported | Not supported |
| **CLI tool** | Supported | Not supported |
| **CI/CD integration** | Supported | Not supported |
| **Runs on Android** | Supported | Not supported |
| **Rich output formats** | Supported | Partial |

**Links:** [GitHub Repository](https://github.com/tharunstryker/psiwatch) · [PyPI Package](https://pypi.org/project/psiwatch) · [Documentation](https://github.com/tharunstryker/psiwatch#readme)

---

### Neeti by Aevra — AI-Powered Education SaaS

**Production SaaS platform delivering AI-powered education tools at scale.**

Neeti comprises two integrated products designed for modern students:

**CareerKit** — Five AI-powered career guidance modules
- Personalized career path recommendations
- Skill gap analysis and learning roadmaps
- Industry insights and market positioning

**CardStudio** — Interactive greeting card engine
- Animated templates and customizable themes
- Real-time preview and instant sharing
- Scalable delivery and asset optimization

**Technical Highlights:**
- **Full-stack ownership** — Frontend, backend, deployment, AI orchestration (solo)
- **Security** — Row-level security on all tables, two-cookie authentication, tier-gated asset bundling
- **AI Reliability** — 4-provider fallback chain (Gemini → Groq → GitHub Models → OpenRouter) with automatic key rotation
- **Scalability** — Vercel Edge functions for sub-100ms response times, Supabase vector queries for retrieval

**Stack:** Vanilla JavaScript · Supabase · Vercel Edge · Gemini API · Groq · GitHub Models · OpenRouter

**Visit:** [naeris.vercel.app](https://naeris.vercel.app)

---

### PromptLens — LLM Response Comparison Toolkit

**Prompt engineering toolkit for evaluating and comparing LLM responses across multiple providers side-by-side.**

Built to accelerate the prompt optimization workflow—test variations, compare outputs, benchmark providers in real-time.

**Visit:** [GitHub Repository](https://github.com/tharunstryker/PromptLens)

---

## Professional Experience

### Founder & Engineer — Naeris
**January 2026 — Present**

Leading all technical and product decisions for Naeris. Key accomplishments:

- Shipped `psiwatch` to PyPI as a production-ready package with comprehensive documentation
- Architected and deployed production SaaS platform serving multiple AI-powered products
- Engineered fault-tolerant AI orchestration with 4-provider fallback chain and dynamic key rotation
- Implemented enterprise-grade security: RLS, admin authentication, rate limiting, asset CDN
- **Built production systems on Android (Termux)** — no traditional desktop development

**Technical Stack:** Python · JavaScript · Supabase · PostgreSQL · Vercel · Edge Functions · Gemini API · Groq API

---

## GitHub Activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=tharunstryker&theme=tokyonight&background=070714&border=00D4FF&stroke=00D4FF&ring=7C3AED&fire=00D4FF&currStreakLabel=00D4FF" alt="GitHub Streak Stats" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=tharunstryker&layout=compact&theme=tokyonight&bg_color=070714&border_color=7C3AED&title_color=7C3AED&text_color=FFFFFF" alt="Top Languages" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=tharunstryker&bg_color=070714&color=00D4FF&line=7C3AED&point=FFFFFF&area=true&area_color=7C3AED&hide_border=false" alt="Activity Graph" />
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/tharunstryker/tharunstryker/output/github-contribution-grid-snake-dark.svg" alt="Contribution Snake" />
</p>

---

## Current Initiatives

**Short-term Focus (Q2 2026):**
- Scaling Neeti user base through partnerships and community engagement
- Expanding `psiwatch` feature set based on production feedback
- Developing advanced monitoring capabilities for ML systems

**Medium-term Vision:**
- Building a comprehensive ML observability platform
- Contributing high-impact open-source libraries to the AI/ML ecosystem
- Establishing Naeris as the go-to platform for AI-powered education

```
interests:
  - Advanced ML monitoring and observability
  - Scalable AI orchestration patterns
  - Education technology and accessibility
  - Open-source community building
  - Production systems architecture
```

---

## Collaboration & Partnerships

I actively seek opportunities to collaborate on:

- **AI/ML Infrastructure** — Designing systems that scale intelligently
- **EdTech Innovation** — Building tools that democratize education
- **Open-Source Impact** — Creating libraries that solve industry-wide problems
- **Consulting & Advisory** — Guiding early-stage teams on technical architecture

**Preferred engagement model:** Results-focused, long-term partnerships with clear technical ownership and autonomy.

---

## Technical Philosophy

```
Principles:
  ├─ Simplicity over complexity
  ├─ Pragmatism over perfection
  ├─ Security from the ground up
  ├─ Performance by design
  └─ Code that teaches
```

*"No framework shortcuts. No bloat. No excuses."*

---

## Get In Touch

<p align="center">
  <a href="mailto:tharunstryker@gmail.com">
    <img src="https://img.shields.io/badge/Email-tharunstryker%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0D0D1A" />
  </a>
  <a href="https://github.com/tharunstryker">
    <img src="https://img.shields.io/badge/GitHub-tharunstryker-00D4FF?style=for-the-badge&logo=github&logoColor=white&labelColor=0D0D1A" />
  </a>
  <a href="https://naeris.vercel.app">
    <img src="https://img.shields.io/badge/Portfolio-naeris.vercel.app-7C3AED?style=for-the-badge&logo=vercel&logoColor=white&labelColor=0D0D1A" />
  </a>
</p>

<p align="center">
  Open to meaningful conversations about AI, engineering, and building things that matter.
</p>

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,4&height=100&section=footer&text=&animation=fadeIn" width="100%" />
</p>
