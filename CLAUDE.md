# Portfolio Website

Personal portfolio site for Robert Monterroso — static HTML/CSS site with featured projects, mini project cards, blog posts, resume, and contact section. No build step, no framework.

## Live URL

- Site: https://pinchelee.com
- Hosting: Cloudflare Pages (auto-deploys from GitHub main branch)
- Repo: github.com/pincheleee/portfolio-website

## Architecture

```
Portfolio_Website/
├── index.html                              # Single-page portfolio — hero, featured projects, mini projects, blog grid, about, contact
├── style.css                               # All styles — CSS custom properties, glass morphism, responsive, dark sections
├── robert-monterroso-resume.pdf            # Downloadable resume (linked from hero)
├── Professional Portfolio - Homepage.pdf   # Design reference
├── img/
│   ├── forge-ai-login.png
│   ├── forge-ai-screenshot.png
│   ├── grabby-screenshot.png
│   ├── polybot-screenshot.png
│   └── privacy-dashboard-screenshot.png
├── blog/
│   ├── sarb-tracker-mvp.html               # Building a FERPA-Compliant SARB Tracker
│   ├── aeries-assistant.html               # Chat Interface for Aeries SIS
│   ├── aeries-mcp-server.html              # Giving Claude Direct Access to Student Records
│   ├── i-built-a-trading-bot-and-it-lost.html  # 27K-Line Trading Bot Postmortem
│   ├── local-vs-cloud-llm-routing.html     # Local vs Cloud LLM Routing
│   ├── forge-ai-launch.html                # SaaS + Chrome Extension Build Log
│   └── ai-bots-on-a-raspberry-pi.html      # AI Bots on Raspberry Pi
├── AGENTS.md                               # Agent handoff doc (blog conventions, section order, rules)
└── CLAUDE.md
```

### Homepage sections (in order)

1. **Hero** — name, title ("I make school tech work"), stat grid (500+ devices, 320+ users, 5+ sites), CTA buttons
2. **Featured Projects** — bento grid: Advanced Privacy Dashboard, Forge AI, Grabby
3. **Mini Projects** — card grid (8 projects)
4. **Blog** — card grid with all posts (newest first)
5. **About** — skills, certifications, education
6. **Contact** — email, GitHub, LinkedIn links

### Blog post conventions

- Each post is a standalone HTML file (no shared template engine)
- Posts include their own `<style>` block for post-specific layout
- Code blocks use Catppuccin Mocha color scheme (dark background, colored spans)
- Stats strip at top for key numbers
- Callout boxes: `.callout` (blue, positive) and `.callout-warning` (yellow, honest limitations)
- Tags at bottom as pill-shaped spans
- Back link to `../index.html#blog`
- Style: honest build-in-public tone — show code, admit what is stubbed, tell the bug story

## Stack

- Vanilla HTML5 + CSS3 (no framework, no build step, no JavaScript framework)
- Google Fonts: Roboto (300/400/500/700/900)
- Material Symbols Outlined icons
- CSS custom properties with glass morphism design system (frosted glass cards, backdrop-filter blur)
- Semantic HTML with ARIA attributes, skip-to-content link, scroll progress indicator
- Open Graph + Twitter Card meta tags for social sharing
- Responsive: mobile nav toggle, fluid grid

## Key Conventions

- **Liquid Glass design system**: CSS custom properties define the entire palette — `--surface`, `--glass-border`, `--glass-blur`, `--elevation-1/2/3`. Cards use `rgba()` backgrounds with `backdrop-filter: blur()`.
- **No JavaScript framework**: Scroll progress, nav toggle, and section highlighting are vanilla JS in `index.html`.
- **Blog posts are self-contained**: Each HTML file includes its own styles. No shared template engine — copy an existing post as a template when adding new ones.
- **Featured projects have real screenshots**: All images in `img/` are actual application screenshots, not mockups.
- **Resume is in the repo root**: `robert-monterroso-resume.pdf` is linked directly from the hero section.

## Adding a New Blog Post

1. Create `blog/your-slug.html` using any existing post as template
2. Add a card to the `<div class="blog-grid">` in `index.html` (newest first)
3. Commit both files, push to main — Cloudflare auto-deploys

## Adding a New Project

1. Add screenshot to `img/` (use actual app screenshot, not mockup)
2. Add a card to the featured projects bento grid or mini projects card grid in `index.html`
3. Commit and push

## Commands

- `open index.html` -- preview locally in browser
- `python3 -m http.server` -- local dev server at http://localhost:8000
- `git push origin main` -- deploy to Cloudflare Pages (auto-deploy on push)

## Don't

- Don't add React, Tailwind, or any build tools — keep it vanilla HTML/CSS
- Don't add emojis unless explicitly requested
- Don't create blog posts without code blocks — technical credibility requires showing real code
- Don't force an AI angle in blog posts — frame around the actual problem being solved
- Don't remove hashtags from YouTube/social descriptions (only from titles)
- Don't forget to push after changes — Cloudflare deploys from main
