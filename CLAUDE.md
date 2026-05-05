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

## Design Context

### Users
- **Primary** — Founders, agency owners, and engineering leaders evaluating Nishil for freelance work (SaaS MVP build, multi-agent AI build, fractional retainer). Technical buyers with a ~30–60s evaluation window.
- **Secondary** — Recruiters and hiring managers scanning for senior FT roles (~8s scan).
- **Tertiary** — Visitors clicking "built by" links from Sivon HQ / StatusLink / MakeToCreate, looking for credibility signals.
- **Job to be done** — In ≤60 seconds, convince a technical buyer that this person ships AI SaaS solo, then convert them to a pre-qualified email enquiry.
- **Emotional goal** — Confidence (he's done this before) + calm (no urgency tactics) + quiet inevitability. Never excitement, never FOMO.

### Brand Personality
**Confident · Technical · Calm.**

- *Confident, not arrogant* — Every claim is backed by a metric or link (10k subs, 29 agents, 3 SaaS shipped, GitHub repos). No hype.
- *Technical, not jargon-laden* — Precise vocabulary for a peer audience ("agent topology," "PII redaction") without gatekeeping.
- *Calm, not flat* — Restrained motion, generous whitespace, no urgency banners. Composure over noise.
- *Voice* — Opinionated where it earns it ("not a demo, a system that ships"), terse, no fluff. The MakeToCreate tagline *"for developers who ship"* is the soul.

### Aesthetic Direction

**Theme:** Dark-only.
- Base `#09090b` (zinc-950), card `#18181b` (zinc-900), borders `#27272a` → `#3f3f46` on hover.
- Accent lime `#D9F99D` (with `#BEF264` hover) — primary action + "available" signal.
- Accent purple `#E9D5FF` — secondary action, retainer/fractional offer.

**Type:**
- Display: Space Grotesk (500/700, tight tracking) for headings.
- Body: Inter (300/400/500/600).
- Eyebrows: monospace UPPERCASE, `0.7rem`, letter-spacing `0.18em`, color `#71717a` (zinc-500).

**Surface:** Glass-morphic bento cards, `1.5rem` radius, mouse-tracking radial glow (white @ 6% opacity, 800px radius), 3% SVG noise overlay fixed to viewport.

**Motion:** Restrained. Card lift `-4px` on hover, 30s marquee, 8s spin-slow on hero blob, shimmer skeleton on blog load. Cubic-bezier `0.25, 0.8, 0.25, 1` easing in 0.3–0.5s windows. Always honor `prefers-reduced-motion`.

**Layout:** Bento grid (`grid-cols-1 md:grid-cols-3 lg:grid-cols-4`), `auto-rows-[180px]` baseline, `gap-4`. Section header cards use `!min-h-0 !row-auto` to act as visual dividers without breaking the rhythm.

**Reference north stars:** Vercel · Linear · Anthropic. Bento-grid portfolio trend (Brittany Chiang, oklch.com, rauno.me).

**Anti-references — what this must NEVER look like:**
1. Generic agency template ("scalable solutions," stock photos, hero-with-blue-gradient)
2. Bro AI-influencer landing page (gradient text, "10x your output," emoji-stuffed CTAs, fake countdowns)
3. Corporate enterprise (deep blue, suit-and-tie photography, certification-soup footers)
4. Maximalist portfolio (3D scenes, scroll-jacking, parallax-everywhere, motion-heavy hero)

### Design Principles

1. **Proof over promise.** Every claim links to a verifiable artifact (live URL, repo, metric). If it can't be linked, it doesn't get said. "Architected platforms" is not allowed; "Scaled an ERP to 10,000 active subs at Fooddarzee" is.
2. **Accent as currency.** Lime and purple are spent, not sprayed. Each card has at most one accent emphasis — the thing that earns the click. If everything is highlighted, nothing is.
3. **Calm motion, never hype motion.** Transitions are restrained, no auto-playing video, no scroll-jacking, no countdown timers. The visitor dictates the pace; the page never demands attention.
4. **Bento as architecture.** Each card is one self-contained unit with one job and one CTA. Section header cards introduce a new chapter; they don't decorate. No card carries two competing actions.
5. **Density without crowding.** Eyebrow + headline + body + proof tag + CTA fit on a card without scrolling. Information is dense, visually quiet. The 1rem gap between cards lets density read as competence, not clutter.

**Accessibility floor:** WCAG AA contrast, fully keyboard-navigable, descriptive `alt` on images, semantic `<main>`/`<footer>`, honor `prefers-reduced-motion` on all animations.
