# Portfolio Website

Personal portfolio site for Robert Monterroso. Static site highlighting IT operations work, AI tooling, shipped projects, resume access, and a blog section.

## Project Status

- Status: stable
- Last major update: 2026-04-19
- Run: open `index.html`
- Hosting: Cloudflare Pages (auto-deploys from GitHub on push to main)
- Live at: pinchelee.com

## What This Site Does

- Presents a professional landing page with hero stats and positioning
- Highlights featured projects: Advanced Privacy Dashboard, Grabby, Forge AI
- Links out to public repositories where appropriate
- Hosts a downloadable resume PDF
- Includes a blog section for project writeups

## Tech Stack

- Static HTML/CSS
- Google Fonts (Roboto)
- Material Symbols icons
- No build step, no framework

## Structure

```text
Portfolio_Website/
├── index.html                          # Main portfolio page
├── style.css                           # Shared site styling
├── robert-monterroso-resume.pdf        # Resume download
├── Professional Portfolio - Homepage.pdf
├── img/
│   ├── forge-ai-login.png
│   ├── forge-ai-screenshot.png
│   ├── grabby-screenshot.png
│   └── privacy-dashboard-screenshot.png
└── blog/
    ├── forge-ai-launch.html
    ├── ai-bots-on-a-raspberry-pi.html
    ├── i-built-a-trading-bot-and-it-lost.html
    └── local-vs-cloud-llm-routing.html
```

## Local Usage

```bash
open index.html
# or
python3 -m http.server
```
