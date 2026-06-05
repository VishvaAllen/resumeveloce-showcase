<!-- ====== HEADER BANNER ====== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=200&section=header&text=Resume%20Veloce&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Three%20products%2C%20one%20platform.&descAlignY=60&descSize=18" alt="header" />
</p>

<p align="center">
  <b>Build resumes. Find or post English-speaking jobs.</b><br/>
  Browser-first · no signup · no tracking · 9-channel auto-distribution.
</p>

<p align="center">
  <a href="https://resumeveloce.com"><img src="https://img.shields.io/badge/Live-resumeveloce.com-0a66c2?style=for-the-badge" /></a>
  <img src="https://img.shields.io/badge/Status-Production-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Source-Private-lightgrey?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Built-Solo-blueviolet?style=for-the-badge" />
</p>

<p align="center">
  <i>Source is private. This is a public showcase of the architecture and product surface.<br/>For a code walkthrough or demo, <a href="https://www.linkedin.com/in/vishva-teja-janne/">reach out on LinkedIn</a>.</i>
</p>

---

## ✨ The pitch

Most resume builders are paywalled. Most job boards are noise. Most posting tools cost €450+ per role. **Resume Veloce bundles all three** with a free tier large enough to be genuinely useful — monetized through the €19/€89 posting product and SEO traffic from PDF tools + viral roasters.

Built solo. Shipped to production. Designed for **non-native English speakers** chasing English-speaking roles abroad.

---

## 🧩 Three products on one platform

<table>
<tr>
<td width="33%" valign="top">

### 🧠 Resume Builder
*Free, ATS-ready, browser-only*

- 20+ recruiter-tested templates
- Live preview as you type
- Single-column ATS-safe layouts tested against **Workday, Greenhouse, Lever, Taleo**
- Clean PDF export, no watermark
- **Files never leave the device** — fully browser-based

</td>
<td width="33%" valign="top">

### 🌍 Job Board + Aggregator
*Two layers of inventory*

- **Paid board** — verified, English-speaking, visa-sponsorship friendly
- **Free aggregator** searching **8 boards** in one query: Remotive, The Muse, Findwork, USAJOBS, Adzuna, Remote OK, Arbeitnow, Jobicy
- **19 countries** including Italy
- Filter by date, type, remote, experience, visa
- Locally cached for instant repeat searches

</td>
<td width="33%" valign="top">

### 📣 Job Posting
*€19 Basic · €89 Premium*

- **Basic (€19)** — 14-day chronological listing, direct apply link
- **Premium (€89)** — 30-day pinned + featured styling + **9-channel auto-distribution**
- No employer account, Stripe checkout, **live in ~60 seconds**
- Public `/job/:id` page with **Google Jobs JobPosting schema**

</td>
</tr>
</table>

---

## 🚀 The 9-channel Auto-Share kit

> *Post once. Distributed to nine channels in 60 seconds.*

Premium posters get platform-optimized share copy generated the moment Stripe clears, one click per channel, pre-filled share dialog, zero re-typing:

| # | Channel | Format |
|---|---|---|
| 1 | **LinkedIn** | Personal feed post |
| 2 | **X** | Threaded |
| 3 | **Reddit** — /r/forhire | Subreddit-formatted |
| 4 | **Reddit** — /r/remotework | Subreddit-formatted |
| 5 | **Hacker News** | "Who's hiring" formatted |
| 6 | **Telegram** | Group/channel ready |
| 7 | **WhatsApp** | Share dialog |
| 8 | **Slack** | Workspace message |
| 9 | **Warm-intro email** | Personal outreach template |

For comparison: LinkedIn alone charges €450+ for one job slot.

---

## 🛠 Supporting tools (top-of-funnel)

| Tool | What it does |
|---|---|
| **Resume Roaster** | 25+ recruiter-grade checks on uploaded PDFs |
| **LinkedIn Roaster** | Headline, About, skills audit |
| **GitHub Roaster** | 25+ engineering-resume checks against public GitHub |
| **PDF Toolkit** | 22 tools — merge, split, compress, OCR, convert |
| **8-board Job Aggregator** | Single search across 8 boards / 19 countries |
| **Career Guides** | 12+ long-form articles for SEO |

All browser-side, all free, all designed as organic traffic drivers for the paid posting product.

---

## ⚙️ Stack

**Frontend**

<p>
<img src="https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
<img src="https://img.shields.io/badge/-React_Router-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white" />
<img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/-CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
</p>

- Custom scroll-effect hooks (`useInView`, `useCountUp`) — IntersectionObserver-based animations, no heavy deps
- `<Reveal>` + `<PromoPopup>` components with localStorage-based dismissal cooldowns
- Schema.org JSON-LD baked in via custom `<Seo>` component (FAQ + SoftwareApp + JobPosting)

**Backend**

<p>
<img src="https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/-Stripe-635BFF?style=for-the-badge&logo=stripe&logoColor=white" />
</p>

- Stripe checkout sessions for one-time €19 / €89 purchases (no subscription, no employer account)
- Async distribution worker decoupled from posting UX
- Browser-side PDF generation for the resume builder + PDF toolkit

**Data & Infra**

<p>
<img src="https://img.shields.io/badge/-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/-Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
<img src="https://img.shields.io/badge/-Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/-Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white" />
</p>

**Integrations** — Stripe · LinkedIn · X · Reddit · Hacker News · Telegram · WhatsApp · Slack · Remotive · The Muse · Findwork · USAJOBS · Adzuna · Remote OK · Arbeitnow · Jobicy

---

## 🗺 Architecture (high level)

```
        ┌────────────────────────────────┐
        │       React SPA (browser)      │
        │  builder · jobs · pdf · roasts │
        │  scroll-fx · live ATS preview  │
        └───────────────┬────────────────┘
                        │
              ┌─────────┴──────────┐
              ▼                    ▼
     ┌────────────────┐   ┌────────────────────┐
     │   FastAPI API  │   │  Browser-side PDF  │
     │  jobs · auth   │   │   builder + tools  │
     │   Stripe hook  │   │  (no upload, ever) │
     └───────┬────────┘   └────────────────────┘
             │
   ┌─────────┼──────────────────────────┐
   ▼         ▼                          ▼
┌──────┐ ┌──────────┐         ┌───────────────────┐
│ PG   │ │ Job-     │         │  Distribution     │
│ jobs │ │ aggregator│        │  worker (async)   │
│users │ │ 8 boards │         │  → LinkedIn       │
└──────┘ │ 19 ctry  │         │  → X              │
         └──────────┘         │  → Reddit ×2      │
                              │  → Hacker News    │
                              │  → Telegram       │
                              │  → WhatsApp       │
                              │  → Slack          │
                              │  → Warm email     │
                              └───────────────────┘
```

- **Browser-first privacy** — resume content, PDF files, roaster inputs never touch the server
- **Stripe → webhook → distribution worker** — async, retry/backoff, no manual steps
- **Schema.org JSON-LD** on every job page for Google Jobs eligibility

---

## 🧠 Things I'm proud of

- Built and shipped **solo** from idea → revenue-generating production
- **Zero-signup UX** for every free product; payments without an employer account
- **9-channel async distribution** with retry/backoff and Stripe-gated activation
- **ATS-passable PDF exports** tuned against real ATS parsers (Workday, Greenhouse, Lever, Taleo)
- Custom **IntersectionObserver scroll-fx** hooks instead of dragging in Framer Motion
- SEO-engineered: **FAQ schema, SoftwareApp schema, JobPosting schema** on every relevant page
- Italian-localized aggregator (🇮🇹 *Cerca lavoro in Italia*) for the home market

---

## 🛣 Roadmap

- [ ] AI cover-letter generator tied to job description
- [ ] Sponsorship-only filter & visa-status tags on job board
- [ ] Employer analytics dashboard (views / clicks / applies per channel)
- [ ] Multilingual UI (IT, ES, PT, DE)
- [ ] Cron-based re-share for Premium listings at days 7 / 14 / 21

---

## 📬 Get in touch

<p>
  <a href="https://resumeveloce.com"><img src="https://img.shields.io/badge/Live-resumeveloce.com-0a66c2?style=for-the-badge" /></a>
  <a href="https://www.linkedin.com/in/vishva-teja-janne/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:jvishvateja26@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

Happy to share a code walkthrough, screen-share, or selected sanitized snippets. Just reach out.

<!-- ====== FOOTER WAVE ====== -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,2,5,30&height=120&section=footer" alt="footer" />
</p>
