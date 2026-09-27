<div align="center">

<br/>

<img src="frontend/public/LOGO.png" alt="Nori" width="200" />

<br/>

# ✨ N O R I ✨

### *Your Discord server's smartest team member.*

<br/>

> **Nori** is an AI-powered Discord bot and web dashboard that transforms uploaded documents, websites, and files into a living knowledge base — answering your community's questions instantly, accurately, and in any language.

<br/>

<p>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" /></a>
  <a href="https://fastapi.tiangolo.com"><img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" /></a>
  <a href="https://react.dev"><img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" /></a>
  <a href="https://discordpy.readthedocs.io"><img src="https://img.shields.io/badge/Discord.py-2.x-5865F2?style=for-the-badge&logo=discord&logoColor=white" /></a>
  <a href="https://docs.docker.com/compose/"><img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white" /></a>
</p>

<br/>

<p>
  <a href="https://noribot.dev"><strong>🌐 Live Demo</strong></a>&nbsp;&nbsp;•&nbsp;&nbsp;<a href="https://noribot.dev/dashboard"><strong>🖥️ Dashboard</strong></a>&nbsp;&nbsp;•&nbsp;&nbsp;<a href="DEPLOY.md"><strong>🚀 Deploy Guide</strong></a>
</p>

<br/>

---

<br/>

<table>
<tr>
<td>

### 🎯 &nbsp; **What if your Discord bot could actually _read_ your documentation?**

<br/>

Community managers answer the same 50 questions — every single day.  
_"What are the fees?" "Who do I contact?" "What's the process for...?"_

**Nori changes that.** Upload your PDFs, paste your URLs, connect your GitHub repo — and Nori becomes your community's always-on, never-tired, citation-providing support agent.

No hallucinations. No guesswork. Just your documents, delivered as answers.

</td>
</tr>
</table>

</div>

<br/>

---

<br/>

## 🧠 &nbsp; How Nori Thinks

Every message flows through a carefully designed intelligence pipeline:

```
   💬 Member types a message in a watched channel
    │
    ▼
   ╔══════════════════════════════════════════════════════╗
   ║          🔬  QUESTION DETECTOR  (3 tiers)           ║
   ║                                                      ║
   ║   Tier 1 ─── Rule Engine ──── "ends with ?" → YES   ║
   ║   Tier 2 ─── ONNX Model ──── 44MB local classifier  ║
   ║   Tier 3 ─── Groq LLM ────── Llama 3.1 safety net   ║
   ║                                                      ║
   ╚══════════════════╤═══════════════════════════════════╝
                      │
              ┌───────┴───────┐
              │ Is it a       │
              │ question?     │
              └───┬───────┬───┘
                  │       │
              YES ▼       ▼ NO → 🤫 Stay silent
                  │
   ╔══════════════╧══════════════════════════════════════╗
   ║            📚  KNOWLEDGE BASE SEARCH                ║
   ║                                                      ║
   ║   Your PDFs, URLs, docs, videos, GitHub repos        ║
   ║   Powered by Graphlit RAG                            ║
   ║                                                      ║
   ╚══════════════════╤═══════════════════════════════════╝
                      │
              ┌───────┴───────┐
              │ Found an      │
              │ answer?       │
              └───┬───────┬───┘
                  │       │
              YES ▼       ▼ NO
                  │       │
   ╔══════════════╧══╗  ╔═╧════════════════════════════╗
   ║  📨 Reply with  ║  ║  🌐 Web Search Fallback      ║
   ║  cited answer   ║  ║  (Tavily → Exa)              ║
   ║  + 👍 👎        ║  ║  OR                          ║
   ╚═════════════════╝  ║  📢 Escalate to mod channel  ║
                        ╚══════════════════════════════╝
                              │
                              ▼
                    📊 Everything is logged
                    to your analytics dashboard
```

<br/>

---

<br/>

## ⚡ &nbsp; Feature Highlights

<table>
<tr>
<td width="50%" valign="top">

### 💬 &nbsp; For Your Community

<br/>

| | |
|:---:|---|
| 🤖 | **Zero-command Q&A** — just type naturally in any watched channel |
| 🌍 | **Speaks their language** — auto-detects or uses admin-configured language |
| 📎 | **Cites its sources** — every answer references the original document |
| 🎫 | **Private support tickets** — one-click to open a private thread with the bot |
| 🔍 | **Web search fallback** — searches the internet when the KB can't answer |
| 👍👎 | **Feedback loop** — reactions let you rate answers, bad ones notify mods |

</td>
<td width="50%" valign="top">

### 🖥️ &nbsp; For Admins (Dashboard)

<br/>

| | |
|:---:|---|
| 📄 | **Multi-format upload** — PDF, DOCX, images, audio, video, XLSX |
| 🌐 | **Website crawler** — paste a URL, auto-ingests + daily recrawl |
| 🐙 | **GitHub integration** — connect repos, the bot learns your codebase |
| 📊 | **Real-time analytics** — questions/day, answer rate, latency, users |
| ⚙️ | **Per-channel control** — set language, tone, and KB subset per channel |
| 🛡️ | **Mod escalation** — unanswered Qs and 👎 reactions forwarded to mods |
| ⏸️ | **One-click pause** — disable the bot without removing it |
| 💳 | **Auto-billing** — Patreon webhooks handle plan upgrades seamlessly |

</td>
</tr>
</table>

<br/>

---

<br/>

## 🏗️ &nbsp; System Architecture

```
                          ┌─────────────────────────────────────┐
                          │          ☁️  CLOUDFLARE              │
                          │       HTTPS + DNS + Caching          │
                          └──────────────┬──────────────────────┘
                                         │
                          ┌──────────────▼──────────────────────┐
                          │        🖥️  ORACLE CLOUD VM          │
                          │        (4 OCPU · 24 GB RAM)         │
                          │                                      │
                          │  ┌────────────────────────────────┐  │
                          │  │     🐳 DOCKER COMPOSE          │  │
                          │  │                                │  │
                          │  │  ┌──────────────────────────┐  │  │
                          │  │  │   BACKEND CONTAINER      │  │  │
                          │  │  │                          │  │  │
                          │  │  │   🚀 FastAPI  (:12000)   │  │  │
                          │  │  │   🤖 Discord Bot         │  │  │
                          │  │  │   🧠 ONNX Detector       │  │  │
                          │  │  │   🔗 Graphlit Client     │  │  │
                          │  │  │   🌐 Playwright          │  │  │
                          │  │  └──────────────────────────┘  │  │
                          │  │                                │  │
                          │  │  ┌─────────────┐ ┌──────────┐  │  │
                          │  │  │ 🔑 BullMQ   │ │ 🗄️ Redis │  │  │
                          │  │  │ Key Rotator │ │  Cache   │  │  │
                          │  │  └─────────────┘ └──────────┘  │  │
                          │  └────────────────────────────────┘  │
                          └──────────────────────────────────────┘
                                  │         │           │
                         ┌────────┘         │           └────────┐
                         ▼                  ▼                    ▼
                  ┌─────────────┐  ┌──────────────┐   ┌──────────────┐
                  │ 🐘 Supabase │  │ 📚 Graphlit  │   │ 💬 Discord   │
                  │  PostgreSQL │  │  RAG Engine   │   │    API       │
                  └─────────────┘  │ + Groq LLM   │   └──────────────┘
                                   │ + Tavily/Exa  │
                                   └──────────────┘
```

<br/>

<details>
<summary><strong>📋 &nbsp; Full Technology Breakdown</strong></summary>

<br/>

| Layer | Tech | Role |
|:---|:---|:---|
| **🚀 API Server** | FastAPI + Uvicorn | 47 REST endpoints, async Python |
| **🤖 Bot Runtime** | discord.py 2.x | Real-time message handling, reactions, tickets |
| **🎨 Frontend** | React 18 + Vite 5 + Tailwind | Dashboard SPA, served via Caddy |
| **📚 RAG Engine** | Graphlit (hosted) | Ingestion, embedding, semantic search, conversation |
| **🧠 LLM** | Groq (Llama 3.x) | Answer generation + question classification fallback |
| **🔬 Question Detection** | ONNX Runtime | Local binary classifier (44MB, CPU-only, ~5ms) |
| **🌐 Web Search** | Tavily, Exa AI | Fallback when KB has no answer |
| **🐘 Database** | Supabase PostgreSQL | 14 tables via SQLAlchemy + asyncpg |
| **🗄️ Cache** | Redis + BullMQ | API key rotation, rate limiting |
| **🔐 Auth** | Discord OAuth2 + JWT | 15-min access tokens + 7-day HttpOnly refresh cookies |
| **💳 Billing** | Patreon Webhooks | Auto plan upgrades/downgrades |
| **🐳 Deployment** | Docker Compose | Oracle Cloud Always Free tier |
| **☁️ CDN** | Cloudflare | HTTPS termination, DNS, edge caching |

</details>

<br/>

---

<br/>

## 📁 &nbsp; Project Map

> *Every folder has a purpose. Here's the 30-second mental model.*

```
nori/
│
│   ── INFRASTRUCTURE ──────────────────────────────────────
├── docker-compose.yml          ← orchestrates backend + bullmq
├── Dockerfile.backend          ← multi-stage Python image
├── Dockerfile.bullmq           ← lightweight key rotation worker
├── Makefile                    ← shortcuts: make up/down/build/deploy
├── .env.example                ← all 20+ env vars, documented
│
│   ── BACKEND (Python) ────────────────────────────────────
├── backend/
│   ├── app.py                  ← FastAPI entry: CORS, 8 routers
│   ├── controllers/            ← 📦 business logic (8 controllers)
│   │   ├── auth_controller     ←   Discord OAuth + JWT + sessions
│   │   ├── upload_controller   ←   file/URL/FAQ/GitHub ingestion
│   │   ├── query_controller    ←   RAG query proxy
│   │   ├── channel_controller  ←   watch channels, support tickets
│   │   ├── guild_controller    ←   Discord guild management
│   │   ├── server_controller   ←   server config, pause, web search
│   │   ├── analytics_controller←   stats, events, per-channel data
│   │   └── patreon_controller  ←   billing webhooks + plan management
│   ├── middleware/             ← 🛡️ JWT auth, guild guards, rate limiter
│   └── routers/                ← 🔗 thin route → controller wiring
│
│   ── DISCORD BOT ─────────────────────────────────────────
├── bot/
│   └── bot.py                  ← 🤖 the brain: detection → answer → feedback
│
│   ── RAG PIPELINE ────────────────────────────────────────
├── python/
│   ├── ingest.py               ← 📥 ingests PDFs, URLs, docs, media into Graphlit
│   ├── query.py                ← 🔍 KB search + web search fallback
│   ├── deletion.py             ← 🗑️ removes content/feeds from Graphlit
│   ├── sub_urls.py             ← 🕸️ Playwright link crawler
│   └── contacts/               ← 📇 XLSX faculty contact parser
│
│   ── UTILITIES ───────────────────────────────────────────
├── utils/
│   ├── Detection.py            ← 🔬 3-tier question classifier
│   ├── apikeyrotation.py       ← 🔑 round-robin key management
│   ├── BullMQ.py               ← ⏱️ rotates keys every 5 minutes
│   └── model_onnx_2/           ← 🧠 pre-trained ONNX model (44MB)
│
│   ── DATABASE ────────────────────────────────────────────
├── dbhelper/
│   └── db_helper.py            ← 🐘 60+ async DB functions (1200 lines)
│
│   ── FRONTEND (React) ────────────────────────────────────
├── frontend/
│   ├── src/
│   │   ├── App.jsx             ← main app: auth, routing, dashboard
│   │   └── components/         ← 15 tab/page components
│   ├── api/                    ← API client + React hooks
│   ├── Caddyfile               ← reverse proxy for production
│   └── Dockerfile.frontend     ← Node build → Caddy serve
│
│   ── SCRIPTS ─────────────────────────────────────────────
└── scripts/
    ├── download_model.py       ← exports ONNX model at build time
    ├── start-app.sh            ← entrypoint: FastAPI + bot together
    └── oracle-firewall.sh      ← opens ports 80/443 on Oracle VMs
```

<br/>

---

<br/>

## 🚀 &nbsp; Quick Start

### Prerequisites

> You'll need accounts on these platforms (all have free tiers):

| | Service | What you need |
|:---:|---|---|
| 🐘 | **Supabase** | PostgreSQL connection string |
| 💬 | **Discord Developer Portal** | Application with bot + OAuth2 |
| 📚 | **Graphlit** | Environment ID, org key, JWT secret |
| 🧠 | **Groq** | API key (comma-separate multiple for rotation) |
| 🗄️ | **Redis** | Local or hosted instance |
| 🔍 | **Tavily** / **Exa** *(optional)* | Web search API keys |

<br/>

### ① &nbsp; Clone & Configure

```bash
git clone https://github.com/your-org/nori.git
cd nori
cp .env.example .env
```

Open `.env` and fill in your secrets:

```env
# ── Core ───────────────────────────────────
DATABASE_URL=postgresql://user:pass@host:6543/postgres
REDIS_HOST=localhost
JWT_SECRET=your-long-random-secret
BOT_SHARED_SECRET=another-random-secret

# ── Discord ────────────────────────────────
DISCORD_CLIENT_ID=...
DISCORD_CLIENT_SECRET=...
DISCORD_BOT_KEY=your_bot_token
DISCORD_BOT_TOKEN=your_bot_token
DISCORD_REDIRECT_URI=http://localhost:3001/api/auth/discord/callback

# ── Graphlit ───────────────────────────────
GRAPHLIT_ENVIRONMENT_ID=...
GRAPHLIT_ORGANIZATION_ID=...
GRAPHLIT_JWT_SECRET=...

# ── AI & Search ────────────────────────────
GROQ_API_KEY=key1,key2
TAVILY_API_KEY=...
EXA_API_KEY=...
```

<br/>

### ② &nbsp; Run Locally (4 terminals)

```bash
# Terminal 1 ─── Redis
docker run -d -p 6379:6379 redis:7-alpine

# Terminal 2 ─── Backend API
pip install -r requirements.txt
uvicorn backend.app:app --reload --port 8000

# Terminal 3 ─── Discord Bot
python bot/bot.py

# Terminal 4 ─── Frontend Dashboard
cd frontend && npm install && npm run dev
```

> 🎉 Dashboard opens at **http://localhost:3001**  
> Vite auto-proxies `/api/*` → `localhost:8000`

<br/>

### ③ &nbsp; Deploy to Production (Docker)

```bash
docker compose build
docker compose up -d

# Verify
curl http://localhost:12000/     # → {"message": "RAG API running"}
docker compose logs -f backend   # live logs
```

📖 **Full deployment walkthrough** → [**DEPLOY.md**](DEPLOY.md)  
*(Oracle Cloud VM setup, Cloudflare DNS, iptables, Discord config)*

<br/>

---

<br/>

## 📡 &nbsp; API at a Glance

Nori exposes **47 endpoints** across 8 route groups. Every authenticated endpoint expects a `Bearer` JWT.

<details>
<summary><strong>🔐 &nbsp; Auth</strong> — <code>/auth</code> &nbsp;(8 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `GET` | `/auth/discord` | — | Kick off Discord OAuth login |
| `GET` | `/auth/invite` | — | Bot invite + OAuth combined flow |
| `GET` | `/auth/discord/callback` | — | Handle OAuth callback |
| `POST` | `/auth/refresh` | 🍪 | Rotate refresh token → new access token |
| `POST` | `/auth/logout` | 🔑 | Revoke session, clear cookie |
| `GET` | `/auth/me` | 🔑 | Current user profile + guilds |
| `GET` | `/auth/sessions` | 🔑 | List all active sessions |
| `POST` | `/auth/sessions/{id}/revoke` | 🔑 | Kill a specific session |

</details>

<details>
<summary><strong>🖥️ &nbsp; Server</strong> — <code>/server</code> &nbsp;(7 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `POST` | `/server/add` | 🔑 | Register a new Discord server |
| `GET` | `/server/config` | 👑 | Get full server configuration |
| `GET` | `/server/list` | 🔑 | Your servers + config status |
| `GET` | `/server/list-all` | 🔑 | All registered servers |
| `PATCH` | `/server/update-pause` | 👑 | Pause / resume the bot |
| `PATCH` | `/server/update-websearch` | 👑 | Toggle web search fallback |
| `GET` | `/server/get-web-search` | 👑 | Current web search state |

</details>

<details>
<summary><strong>📤 &nbsp; Upload</strong> — <code>/upload</code> &nbsp;(11 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `GET` | `/upload/all` | 👑 | All uploads for a server |
| `GET` | `/upload/sub-urls` | 🔑 | Crawl sub-URLs from a page |
| `GET` | `/upload/my-uploads` | 🔑 | Your personal upload history |
| `POST` | `/upload/website` | 👑 | Website feed (daily recrawl) |
| `POST` | `/upload/url` | 👑 | Single URL ingestion |
| `POST` | `/upload/file` | 👑 | Upload PDF/DOCX/image/audio/video |
| `POST` | `/upload/faq` | 👑 | Submit raw FAQ text |
| `POST` | `/upload/contacts` | 👑 | XLSX contact spreadsheet |
| `DELETE` | `/upload/delete-content/{id}` | 👑 | Remove an upload |
| `POST` | `/upload/channel-messages` | 👑 | Ingest Discord channel history |
| `POST` | `/upload/add-github-repo` | 👑 | Connect a GitHub repository |

</details>

<details>
<summary><strong>🔍 &nbsp; Query</strong> — <code>/query</code> &nbsp;(1 endpoint)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `POST` | `/query/` | 🔑 | Query the knowledge base |

</details>

<details>
<summary><strong>📺 &nbsp; Channels</strong> — <code>/channel</code> &nbsp;(15 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `PUT` | `/channel/add` | 👑 | Watch new channels |
| `DELETE` | `/channel/delete` | 👑 | Stop watching a channel |
| `PUT` | `/channel/add-mod` | 👑 | Set mod notification channel |
| `DELETE` | `/channel/delete-mod` | 👑 | Remove mod channel |
| `GET` | `/channel/list` | 👑 | List watched + mod channels |
| `PUT` | `/channel/add-support-category` | 👑 | Create ticket support channel |
| `POST` | `/channel/add-channel-config` | 👑 | Set channel language & tone |
| `GET` | `/channel/list-all-channel-config` | 👑 | All channel configs |
| `PATCH` | `/channel/update-channel-config` | 👑 | Change language/tone |
| `DELETE` | `/channel/delete-channel-config` | 👑 | Remove channel config |
| `POST` | `/channel/add-channel-knowledge-base` | 👑 | Assign KB sources to channel |
| `GET` | `/channel/get-channel-knowledge-base` | 👑 | Channel's KB sources |
| `DELETE` | `/channel/delete-channel-knowledge-base` | 👑 | Remove a channel KB source |
| `DELETE` | `/channel/delete-all-channel-knowledge-base` | 👑 | Clear all channel KB sources |
| `GET` | `/channel/list-all-channel-knowledge-base` | 👑 | Overview of all channel mappings |

</details>

<details>
<summary><strong>📊 &nbsp; Analytics</strong> — <code>/analytics</code> &nbsp;(5 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `GET` | `/analytics/summary` | 👑 | Totals, rates, avg latency |
| `GET` | `/analytics/recent-analytics` | 👑 | Latest question events |
| `GET` | `/analytics/all-analytics` | 👑 | Daily aggregated breakdown |
| `GET` | `/analytics/analytics-by-channel` | 👑 | Per-channel user stats |
| `GET` | `/analytics/analytics-by-all-channels` | 👑 | Cross-channel comparison |

</details>

<details>
<summary><strong>🏰 &nbsp; Guilds</strong> — <code>/guilds</code> &nbsp;(3 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `GET` | `/guilds/` | 🔑 | Your admin guilds |
| `GET` | `/guilds/{id}/channels` | 🔑 | Guild's Discord channels |
| `GET` | `/guilds/eligible` | 🔑 | Split by bot presence |

</details>

<details>
<summary><strong>💳 &nbsp; Billing</strong> — <code>/patreon</code> &nbsp;(5 endpoints)</summary>
<br/>

| Method | Endpoint | Auth | What it does |
|:---:|---|:---:|---|
| `GET` | `/patreon/checkout` | — | Redirect to Patreon |
| `POST` | `/patreon/webhook` | Sig | Handle member events |
| `POST` | `/patreon/simulate-webhook` | — | Test locally |
| `GET` | `/patreon/plan` | 👑 | Current plan details |
| `GET` | `/patreon/usage` | 👑 | Usage vs. limits |

</details>

> 🔑 = JWT required &nbsp;&nbsp;|&nbsp;&nbsp; 👑 = Guild Admin required &nbsp;&nbsp;|&nbsp;&nbsp; 🍪 = HttpOnly cookie &nbsp;&nbsp;|&nbsp;&nbsp; — = public

<br/>

---

<br/>

## 📂 &nbsp; Supported Uploads

> *Nori eats documents for breakfast.*

| Type | Extensions | How it's processed |
|:---:|---|---|
| 📄 | `.pdf` | Native text extraction + OCR fallback |
| 📝 | `.docx` | Word document parsing |
| 🖼️ | `.png` `.jpg` `.jpeg` `.tiff` `.bmp` `.webp` | OCR via Graphlit cloud |
| 🎬 | `.mp4` `.mp3` `.wav` `.m4a` | Cloud transcription via Graphlit |
| 📊 | `.xlsx` `.xls` | Structured contact record parsing |
| 🌐 | Any URL | Playwright renders → text extracted |
| 🕸️ | Any URL (website mode) | Full site crawl + daily auto-recrawl |
| 🐙 | GitHub repo URL | Recursive code + docs ingestion |
| ✏️ | Raw text | Paste FAQ content directly |

**Max file size:** 10 MB

<br/>

---

<br/>

## 💳 &nbsp; Plans & Limits

Plans upgrade/downgrade automatically via Patreon webhooks — no manual intervention needed.

| | 🆓 Free | ⭐ Starter | 🚀 Pro | 🏢 Enterprise |
|---|:---:|:---:|:---:|:---:|
| **Questions / period** | 50 | 200 | 800 | **Unlimited** |
| **URL sources** | 5 | 10 | 50 | **Unlimited** |
| **File uploads** | 3 | 10 | 50 | **Unlimited** |
| **GitHub repos** | 1 | 1 | 1 | 1 |
| **Web search** | ✅ | ✅ | ✅ | ✅ |
| **Per-channel KB** | ✅ | ✅ | ✅ | ✅ |
| **Analytics** | ✅ | ✅ | ✅ | ✅ |
| **Support tickets** | ✅ | ✅ | ✅ | ✅ |
| **Mod escalation** | ✅ | ✅ | ✅ | ✅ |

<br/>

---

<br/>

## 🐘 &nbsp; Database Design

14 PostgreSQL tables, managed through Supabase:

```
┌──────────────────┐     ┌───────────────────┐     ┌───────────────────┐
│   admin_users    │────▶│  admin_sessions   │     │   guild_admins    │
│                  │     │                   │     │                   │
│  discord_id  PK  │     │  refresh_hash     │     │  guild_id     PK  │
│  username        │     │  expires_at       │     │  discord_id   PK  │
│  email           │     │  revoked          │     │  role (owner/     │
│  oauth_tokens    │     │  user_agent       │     │       admin)      │
└──────────────────┘     └───────────────────┘     └────────┬──────────┘
                                                            │
┌──────────────────┐     ┌───────────────────┐              │
│    servers       │◀────┤   server_plans    │     ┌────────▼──────────┐
│                  │     │                   │     │    channels       │
│  server_id   PK  │     │  plan             │     │                   │
│  server_name     │     │  max_questions    │     │  server_id    FK  │
│  is_paused       │     │  patreon_email    │     │  channel_id       │
│  web_search      │     │  billing_date    │     └───────────────────┘
│  mod_channel     │     └───────────────────┘
└───────┬──────────┘                               ┌───────────────────┐
        │                                          │  channel_config   │
        │     ┌───────────────────┐                │                   │
        ├────▶│    uploads        │                │  channel_id       │
        │     │                   │                │  language          │
        │     │  type, name       │                │  tone              │
        │     │  content_id       │                └───────────────────┘
        │     │  feed_id          │
        │     │  status           │                ┌───────────────────┐
        │     └───────────────────┘                │ channel_knowledge │
        │                                          │ _sources          │
        ├────▶│  server_uploads   │                │                   │
        │     │  content_id → Graphlit             │  channel_id       │
        │                                          │  content_id       │
        ├────▶│  server_feeds     │                │  feed_id          │
        │     │  feed_id → Graphlit                └───────────────────┘
        │
        ├────▶│  question_events  │                ┌───────────────────┐
        │     │  user, answered   │                │ watched_threads   │
        │     │  latency, link    │                │                   │
        │                                          │  thread_id    PK  │
        └────▶│  conversation_    │                │  server_id    FK  │
              │  history          │                │  channel_id       │
              │  graphlit conv IDs│                └───────────────────┘
```

<br/>

---

<br/>

## 🤖 &nbsp; Bot Commands

| Command | Who can use it | What it does |
|:---|:---:|---|
| `-ask <question>` | Everyone | Ask a question directly (4 per 60s cooldown) |
| `-websearch enable` | Admin | Turn on web search fallback for the server |
| `-websearch disable` | Admin | Turn off web search fallback |

> 💡 **Tip:** In watched channels, you don't need any command — just type your question naturally. Nori detects it and responds.

<br/>

---

<br/>

## 🛠️ &nbsp; Contributing

| What you want to change | Where to look |
|---|---|
| Bot behavior & responses | `bot/bot.py` |
| RAG ingestion pipeline | `python/ingest.py` |
| RAG query & retrieval | `python/query.py` |
| API business logic | `backend/controllers/` |
| API routes | `backend/routers/` |
| Database queries | `dbhelper/db_helper.py` |
| Question detection | `utils/Detection.py` |
| Dashboard UI | `frontend/src/components/` |
| API client hooks | `frontend/api/` |

```bash
# Full local dev stack
docker run -d -p 6379:6379 redis:7-alpine
uvicorn backend.app:app --reload --port 8000 &
python bot/bot.py &
cd frontend && npm run dev
```

<br/>

---

<br/>

## 📜 &nbsp; License

Released under the **MIT License**. See [LICENSE](LICENSE) for details.

<br/>

---

<br/>

<div align="center">

<img src="frontend/public/LOGO.png" alt="Nori" width="72" />

<br/>

**Built with ❤️ for communities that deserve smarter support.**

<br/>

<p>
  <a href="https://noribot.dev"><strong>🌐 Website</strong></a>&nbsp;&nbsp;•&nbsp;&nbsp;<a href="https://noribot.dev/dashboard"><strong>🖥️ Dashboard</strong></a>&nbsp;&nbsp;•&nbsp;&nbsp;<a href="https://noribot.dev/api/auth/invite"><strong>🤖 Invite Bot</strong></a>
</p>

<br/>

*"The best support is the one your members don't have to wait for."*

<br/>

</div>
