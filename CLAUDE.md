# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file static HTML portfolio website (`personal.html`). No build tools, no package manager, no server-side code.

## Running Locally

Open `personal.html` directly in a browser. No build step or dev server required.

## Architecture

Everything lives in `personal.html`:
- **Lines 1-141**: Head section — metadata, Google Fonts (Inter + Space Grotesk), Tailwind CSS via CDN, custom styles, and Tailwind config
- **Lines 142-376**: Body — bento grid layout with portfolio cards
- **Lines 378-389**: Vanilla JS for mouse-tracking glow effect on `.bento-card` elements

## Key Design Decisions

- **Tailwind CSS via CDN** (`cdn.tailwindcss.com`) with inline config object extending colors, fonts, grid, and animations
- **Dark theme**: Custom palette with lime (`#D9F99D`) and purple (`#E9D5FF`) accent colors
- **Bento grid layout**: CSS Grid with `grid-cols-1 md:grid-cols-3 lg:grid-cols-4` and `auto-rows-[180px]`, cards span multiple rows/cols
- **Glass-morphic cards**: Semi-transparent backgrounds with `backdrop-blur`, border glow on hover
- **Mouse tracking**: JS sets `--mouse-x`/`--mouse-y` CSS custom properties per card for radial gradient glow
- **Marquee animation**: CSS `@keyframes marquee` for horizontal scrolling tech stack (25s loop)
- **No external JS dependencies**: All interactivity is vanilla JavaScript
