# SaveAny — AI 万能视频下载器

**SaveAny** 是一款全栈 AI Web 应用，支持从 1800+ 视频平台（YouTube、Bilibili、抖音、TikTok 等）下载视频，并集成 AI 视频内容总结、思维导图生成、字幕下载及会员支付体系。

## 技术栈

| 层级 | 技术 |
|------|------|
| 前端 | Vue 3、Vite、Tailwind CSS |
| 后端 | Python、FastAPI、SQLite |
| 核心库 | yt-dlp（视频解析）、DeepSeek API（AI 总结） |
| 支付 | Stripe Checkout + Webhook |
| 认证 | JWT |

## 核心功能

- **多平台视频下载**：基于 yt-dlp，支持 1800+ 平台，多清晰度（360p ～ 4K）
- **抖音无水印下载**：内置专用解析模块，无需登录 Cookie
- **AI 视频总结**：调用 DeepSeek 大模型，自动生成摘要、思维导图，支持多轮问答
- **字幕下载**：支持 SRT / VTT / TXT 三种格式
- **会员体系**：Stripe 在线支付，JWT 认证，免费 / VIP 分级权限控制
- **SEO / GEO 优化**：结构化数据、Open Graph、AI 爬虫友好的 noscript 内容

## 本地运行

详见 [docs/保姆级本地运行指南.md](docs/保姆级本地运行指南.md)，核心步骤：

```bash
# 克隆项目
git clone https://github.com/WenzeZhang/free-video-downloader.git

# 后端
cd backend && cp .env.example .env   # 填写 DEEPSEEK_API_KEY 等
pip install -r requirements.txt
python main.py                        # http://localhost:8000

# 前端（另开终端）
cd frontend && npm install
npm run dev                           # http://localhost:5173
```

---

# SaveAny — AI-Powered Universal Video Downloader

**SaveAny** is a full-stack web application for downloading videos from 1800+ platforms (YouTube, Bilibili, Douyin/TikTok, etc.), with an integrated AI summarization pipeline, mind-map generation, subtitle export, and a membership payment system.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vue 3, Vite, Tailwind CSS |
| Backend | Python, FastAPI, SQLite |
| Core libs | yt-dlp (video parsing), DeepSeek API (AI summary) |
| Payments | Stripe Checkout + Webhook |
| Auth | JWT |

## Key Features

- **Multi-platform download** — yt-dlp engine, 1800+ sites, 360p–4K quality selection
- **Douyin watermark-free download** — dedicated parser, no login/cookie required
- **AI video summary** — DeepSeek LLM generates structured summaries, mind maps, and supports multi-turn Q&A
- **Subtitle export** — SRT / VTT / TXT formats
- **Membership system** — Stripe online payments, JWT auth, free / VIP permission tiers
- **SEO / GEO optimization** — structured data, Open Graph, AI-crawler-friendly noscript fallback

## Quick Start

See [docs/保姆级本地运行指南.md](docs/保姆级本地运行指南.md) for the full guide.

```bash
git clone https://github.com/WenzeZhang/free-video-downloader.git

# Backend
cd backend && cp .env.example .env   # set DEEPSEEK_API_KEY etc.
pip install -r requirements.txt
python main.py                        # http://localhost:8000

# Frontend (new terminal)
cd frontend && npm install
npm run dev                           # http://localhost:5173
```
