# Portfolio — nishilbhave.github.io

Single-file static portfolio site. Deployed via GitHub Pages at https://nishilbhave.github.io/.

Positioning: AI-native senior builder. Three productized freelance offers (SaaS MVP build, multi-agent AI system, fractional senior engineer retainer). All CTAs route to `mailto:nishilbhave@gmail.com`.

## Stack

- Single `index.html` — no build tools, no package manager, no server-side code
- Tailwind CSS via CDN (`cdn.tailwindcss.com`) with inline config
- Vanilla JS for mouse-glow tracking and blog post fetching
- Space Grotesk + Inter (Google Fonts)
- Hosted on GitHub Pages

## Running Locally

`index.html` fetches the WordPress REST API at `https://maketocreate.com/wp-json/wp/v2/posts`, which has CORS allowed only for `https://nishilbhave.github.io`. The `file://` origin is blocked, so serve over HTTP:

```bash
python3 -m http.server 8765
# open http://localhost:8765/index.html
```

## Layout

Single bento grid (`grid-cols-1 md:grid-cols-3 lg:grid-cols-4`, `auto-rows-[180px]`):

1. **Hero** — Profile + Sivon HQ feature card
2. **Stats strip** — 11 yrs / 3 SaaS / 10k subs / 29 agents
3. **Work with me** — SaaS MVP, Multi-agent, Fractional retainer
4. **Proof** — StatusLink, MakeToCreate, Experience, GitHub repos
5. **Latest writing** — 3 dynamic posts via WP REST API (with skeleton + fallback)
6. **Stack + meta** — Tech marquee, location, LinkedIn
7. **Bottom CTA** — Resume, GitHub, Email

## Design

Dark-only theme. Base `#09090b`, card `#18181b`, accent lime `#D9F99D` and purple `#E9D5FF`. Glass-morphic cards with mouse-tracking radial glow. Restrained motion — honors `prefers-reduced-motion`.

See [CLAUDE.md](./CLAUDE.md) for the full design system, brand personality, and editing notes.

## Files

- `index.html` — entire site
- `resume/Nishil_Bhave_Senior_Backend_Dev.pdf` — resume served from the bottom CTA
- `CLAUDE.md` — project instructions and design context
