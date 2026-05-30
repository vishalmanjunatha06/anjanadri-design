# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static marketing website for **Anjanadri Elite Boys PG** — a premium student paying-guest accommodation near NMIT, Yelahanka, Bangalore.

## Running Locally

No build step required. Serve the HTML file directly:

```bash
# Option 1: Python built-in server
python3 -m http.server 8080 --directory anjanadri-elite-pg

# Option 2: Open directly in browser
open anjanadri-elite-pg/index.html
```

## Architecture

Single-file design — the entire site lives in `anjanadri-elite-pg/index.html` (~864 lines):
- All CSS is embedded in a `<style>` block at the top of the file
- No JavaScript, no build tooling, no external dependencies
- Images stored in `anjanadri-elite-pg/images/` (QR codes for WhatsApp and Google Reviews)

**Page sections (in order):** Nav → Hero (stats) → About → Amenities → Food/Mess → Rooms (3 tiers) → Contact → Footer

## Design System

CSS custom properties defined in `:root`:
- `--navy: #0F1F3D` — primary background/text
- `--gold: #C9A84C` — accent/headings
- `--whatsapp: #25D366` — CTA buttons

Typography uses Google Fonts (Inter + Playfair Display) loaded via CDN. Responsive breakpoint at `768px` using media queries. Font sizes use `clamp()` for fluid scaling.

## External Links

All CTAs link to:
- WhatsApp: `https://wa.me/919353222222` (floating button + contact section)
- Phone: `tel:+919353222222`
- Google Reviews: linked via QR code image
