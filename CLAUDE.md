# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file static portfolio site at `index.html`. Deployed via GitHub Pages at https://nishilbhave.github.io/. No build tools, no package manager, no server-side code.

Positioning: AI-native senior builder. Three productized freelance offers (SaaS MVP build, multi-agent AI system, fractional senior engineer retainer). All CTAs route to `mailto:nishilbhave@gmail.com` with pre-filled subjects.

## Running Locally

`index.html` cannot be opened via `file://` because it fetches the WordPress REST API at `https://maketocreate.com/wp-json/wp/v2/posts` (CORS allowed for `https://nishilbhave.github.io` only — local file:// origin will be blocked). Serve over HTTP for local preview:

```
python3 -m http.server 8765
# then open http://localhost:8765/index.html
```

## Architecture

Everything lives in `index.html`. The page is a single bento grid with sections separated by full-width header cards:

1. **Hero** — Profile (2×2) + Sivon HQ feature card (2×2)
2. **Stats strip** — 4 metric cards (11 yrs / 3 SaaS / 10k subs / 29 agents)
3. **§ Work with me** — Services A (SaaS MVP), B (Multi-agent), D (Fractional retainer wide)
4. **Proof** — StatusLink + MakeToCreate (2×1 each), Experience (2×2) + GitHub repos showcase (2×2)
5. **§ Latest writing** — 3 dynamic posts via WP REST API with skeleton loading + fallback
6. **Stack + meta** — Tech stack marquee, location, LinkedIn
7. **Bottom CTA strip** — Resume PDF download, GitHub link, Email Me lime CTA

The blog section uses an HTTP fetch on page load. Skeleton shimmer placeholders show during fetch; on success, 3 cards render and get the mouse-glow listener attached. On failure, a single fallback card links to maketocreate.com.

## Key Design Decisions

- **Tailwind CSS via CDN** (`cdn.tailwindcss.com`) with inline config extending colors, fonts, animations
- **Dark theme** — Custom palette with lime (`#D9F99D`) and purple (`#E9D5FF`) accents
- **Bento grid** — `grid-cols-1 md:grid-cols-3 lg:grid-cols-4 auto-rows-[180px]`, cards span via `md:col-span-*` / `md:row-span-*`. Section header cards use `!min-h-0 !row-auto` to break out of the fixed row height
- **Mouse-tracking glow** — JS sets `--mouse-x`/`--mouse-y` CSS custom properties per `.bento-card`, drives a `radial-gradient` overlay
- **Marquee animation** — CSS `@keyframes marquee` (30s loop), tech list duplicated for seamless scroll
- **Skeleton loading** — `@keyframes shimmer` for blog posts placeholder
- **WP REST API** — `https://maketocreate.com/wp-json/wp/v2/posts` (CORS configured server-side for the GitHub Pages origin)
- **No external JS dependencies** — All interactivity is vanilla JS

## Editing Notes

- The resume PDF served at the bottom is `Nishil_Bhave_Senior_Backend_Dev.pdf`. If renamed, update the `<a href>` accordingly.
- The GitHub avatar URL is hard-coded: `https://avatars.githubusercontent.com/u/13285272?v=4`. Stable as long as the GitHub user ID doesn't change.
- Service CTAs use `mailto:` with `subject=` and `body=` URL-encoded — keep encoding consistent if editing.
- All three productized offer prices are intentionally hidden from the page (the user's choice). Don't add public pricing without confirming.
- New blog posts surface automatically (latest 3); no manual update needed when MakeToCreate publishes.
