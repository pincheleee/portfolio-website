# Portfolio Website — Agent Handoff

**Live at:** pinchelee.com
**Hosting:** Cloudflare Pages (auto-deploys from GitHub main branch)
**Repo:** github.com/pincheleee/portfolio-website

## Stack

- Vanilla HTML/CSS (no framework, no build step)
- Google Fonts: Roboto + Material Symbols Outlined
- Single `style.css` for the entire site
- Blog posts are standalone HTML files in `blog/`

## Structure

```
index.html          ← Homepage (hero, projects, blog grid, about, contact)
style.css           ← All styles (CSS custom properties, responsive)
blog/               ← Individual blog post pages (self-contained HTML+CSS)
img/                ← Screenshots and assets
```

## Blog Posts (newest first)

| File | Title | Date |
|------|-------|------|
| `blog/sarb-tracker-mvp.html` | Building a FERPA-Compliant SARB Tracker From Scratch | May 2026 |
| `blog/aeries-assistant.html` | I Built a Chat Interface for a 1990s Student Database | March 2026 |
| `blog/aeries-mcp-server.html` | Giving Claude Direct Access to Student Records (Safely) | March 2026 |
| `blog/i-built-a-trading-bot-and-it-lost.html` | I Built a 27,000-Line Trading Bot and It Lost Every Dollar | April 2026 |
| `blog/local-vs-cloud-llm-routing.html` | Local vs Cloud LLM Routing from Production Experience | April 2026 |
| `blog/forge-ai-launch.html` | I Built a SaaS and Chrome Extension in One Session | March 2026 |
| `blog/ai-bots-on-a-raspberry-pi.html` | Building AI Bots That Run 24/7 on a Raspberry Pi | February 2026 |

## Blog Post Conventions

- Each post is a standalone HTML file (no shared template engine)
- Posts include their own `<style>` block for post-specific layout (blog-post, callout, code blocks)
- Code blocks use Catppuccin Mocha-ish color scheme (dark background, colored spans for syntax)
- Stats strip at top for key numbers
- Callout boxes: `.callout` (blue, positive) and `.callout-warning` (yellow, honest limitations)
- Tags at bottom as pill-shaped spans
- Back link to `../index.html#blog`
- Style: honest build-in-public tone. Show code. Admit what's stubbed. Tell the bug story.

## Adding a New Blog Post

1. Create `blog/your-slug.html` using any existing post as template
2. Add a card to the `<div class="blog-grid">` in `index.html` (newest first)
3. Commit both files, push to main — Cloudflare auto-deploys

## Homepage Sections (in order)

1. Hero (name, title, tagline)
2. Featured Projects (bento grid — currently: Privacy Dashboard, Forge AI, Grabby)
3. Mini Projects (card grid — 8 projects)
4. Blog (card grid — all posts)
5. About (skills, certs, education)
6. Contact

## Rules

- No emojis unless user asks
- No React/Tailwind/build tools — keep it vanilla
- Blog posts must include code blocks for technical credibility
- Posts must be honest about current state (what works vs what's stubbed)
- Always `git push` at end of session — Cloudflare deploys from main
- Featured project screenshots go in `img/`
- Resume PDF kept in root (linked from hero)

## Recent Session (2026-05-03)

Added 3 Aeries cluster blog posts (SARB Tracker, Aeries Assistant, MCP Server). All follow the build-in-public pattern with code snippets, stats strips, and honest state callouts. SARB post went through 3 rewrites to get the tone right — no AI angle forced, compliance engineering framing, bug story included.
