# trm-website

Marketing site for **The Rhythm Messengers** (Chicago drumline), rhythmmessengers.com. Single-page vanilla HTML/CSS/JS inline (~45KB), no framework or build step. Replaced an old Wix multi-page site.

## Deploy
- Repo: GitHub `DerekDalton/trm-website`, branches `main` (prod) + `staging`.
- Cloudflare Pages: build preset None, empty build command, output `/`. Branch = environment.
- Domain: GoDaddy registrar, DNS on Cloudflare; CNAME `@` + `www` → `trm-website.pages.dev`. **Canonical host = apex** — canonical tag, OG, schema, robots, and sitemap must all agree.
- Old Wix URLs 301 to `#anchors` via `_redirects`.

## Rules
- GSC keyword to protect: **"drumline chicago"** — don't change headings/copy that rank for it without checking.
- Design "taste" skills are vendored in `.agents/skills/` here, pinned in `skills-lock.json` — keep local, don't globalize.
- `min-height:100dvh` (not `100vh`); descriptive `alt` text on all images.
