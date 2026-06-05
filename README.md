<h1 align="center">Resume Veloce</h1>
<p align="center">
  <b>Three products, one platform.</b><br/>
  Build resumes. Find or post English-speaking jobs.
</p>

<p align="center">
  <a href="https://resumeveloce.com"><img src="https://img.shields.io/badge/Live-resumeveloce.com-0a66c2?style=for-the-badge" /></a>
  <img src="https://img.shields.io/badge/Status-Production-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Source-Private-lightgrey?style=for-the-badge" />
</p>

> Source code is private. This repo is a public showcase of the architecture, stack, and selected components. For a code walkthrough or demo, [reach out on LinkedIn](https://www.linkedin.com/in/vishva-teja-janne/).

---

## What it is

Resume Veloce is a multi-product platform built around one idea: **make it easier for non-native English speakers to land English-speaking roles abroad.**

| Product | What it does | Who it's for |
|---|---|---|
| 🧠 **Resume Builder** | Free, ATS-ready resume generator with live preview and PDF export | Job seekers |
| 🌍 **Job Board** | International listings for English-speaking roles, visa sponsorship welcome | Candidates relocating across borders |
| 📣 **Job Posting (€19+)** | One post → auto-distributed to LinkedIn, Reddit, Hacker News + 6 more channels | Hiring teams & startups |

Plus **20+ free PDF tools** (merge, split, compress, convert) and **three viral "roaster" tools** as top-of-funnel traffic drivers.

---

## Why it exists

Most resume builders are paywalled, most job boards are noise, and most posting tools cost €200+ per role. Resume Veloce bundles all three in one platform with a free tier large enough to be genuinely useful — monetized through the posting product and PDF/roaster traffic.

---

## Screenshots

<!-- Drop your screenshots here, e.g.: -->
<!-- ![Resume Builder](./screenshots/builder.png) -->
<!-- ![Job Board](./screenshots/jobs.png) -->
<!-- ![Posting Dashboard](./screenshots/posting.png) -->

*(Screenshots coming soon — try the live site at [resumeveloce.com](https://resumeveloce.com))*

---

## Stack

**Frontend**
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/-Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Backend**
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white)

**Data & Infra**
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Firebase](https://img.shields.io/badge/-Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Azure](https://img.shields.io/badge/-Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

**Integrations** — LinkedIn API · Reddit API · Hacker News · Stripe (payments) · PDF generation pipeline

---

## Architecture (high level)

```
        ┌──────────────┐        ┌────────────────┐
        │  React SPA   │ ─────► │  FastAPI API   │
        │ (builder /   │        │  (jobs, auth,  │
        │  jobs / pdf) │        │   payments)    │
        └──────────────┘        └───────┬────────┘
                                        │
              ┌─────────────────────────┼─────────────────────────┐
              ▼                         ▼                         ▼
     ┌────────────────┐       ┌──────────────────┐       ┌──────────────────┐
     │  PostgreSQL    │       │  PDF service     │       │  Distribution    │
     │  (users, jobs) │       │  (resume + tools)│       │  worker          │
     └────────────────┘       └──────────────────┘       │  → LinkedIn      │
                                                        │  → Reddit        │
                                                        │  → Hacker News   │
                                                        │  → 6 more        │
                                                        └──────────────────┘
```

- **Auth & identity** via Firebase
- **Containerized services** on Azure
- **Async distribution worker** decouples posting UX from third-party API latency
- **PDF pipeline** powers both the resume builder and the 20+ standalone PDF tools

---

## Highlights I'm proud of

- Built and shipped solo from idea → production
- Auto-distribution to 9 channels with retry/backoff
- ATS-ready PDF export tuned against real ATS parsers
- Free tier large enough to attract real users; paid tier targeted at hiring teams
- Zero-downtime deploys on Azure with Docker

---

## Roadmap

- [ ] AI cover-letter generator tied to job description
- [ ] Visa-sponsorship filter on job board
- [ ] Analytics dashboard for job posters
- [ ] Multilingual UI (IT, ES, PT)

---

## Get in touch

- 🌐 Live: **[resumeveloce.com](https://resumeveloce.com)**
- 💼 LinkedIn: [vishva-teja-janne](https://www.linkedin.com/in/vishva-teja-janne/)
- 📧 jvishvateja26@gmail.com

If you'd like a code walkthrough, I'm happy to share a screen-share or selected snippets — just reach out.
