# Handoff: WEnDyS Landing Page v1

**Date**: 2026-02-17 21:57
**Context**: ~60%

## What We Did
- Created WEnDyS Oracle landing page from scratch
- Started as plain HTML/CSS/JS, then converted to Astro 5 + Cloudflare Workers to match sibling Oracle pattern
- Learned from `Soul-Brews-Studio/landing-oracle` (gallery repo) — understood content collections, palette system, deployment pattern
- Redesigned UI inspired by Phukhao's cyberpunk aesthetic but with unique dewdrop identity:
  - Deep ocean dark bg (`#060d15`) with ambient glow
  - Space Grotesk (display) + JetBrains Mono (code) + Kanit (Thai)
  - Flowing gradient text animation (blue→teal)
  - Status line (`DEWDROP_NODE::ACTIVE`), stats grid, principle rows, node badges
  - Glass cards with glow-border effects
- Created public repo: https://github.com/AmDewSaroota/wendys-landing
- Created registration issue on landing-oracle: https://github.com/Soul-Brews-Studio/landing-oracle/issues/5
- 3 commits pushed to master

## Pending
- [ ] Add `account_id` and `routes` to `wrangler.toml` for actual deployment (needs Cloudflare config)
- [ ] Deploy to `wendys.buildwithoracle.com` via `npx wrangler deploy`
- [ ] Take screenshot for gallery card (landing-oracle needs `/public/screenshots/wendys.png`)
- [ ] i18n toggle needs testing — LangToggle labels in `nav.who`, `nav.principles`, `nav.family` use English terms ("Story", "Protocol", "Network") that don't switch
- [ ] Add OG image (`public/og.png`) for social sharing
- [ ] Mobile responsive testing (nav links hidden on mobile but no hamburger menu)
- [ ] Consider adding CLAUDE.md for Oracle identity
- [ ] The `ψ/` brain directory structure (resonance, memory, etc.) not yet set up

## Next Session
- [ ] Test full build: `bun run build` — verify dist/ output
- [ ] Fix i18n nav labels to properly switch TH/EN
- [ ] Add mobile hamburger menu or simplify nav
- [ ] Deploy to Cloudflare Workers (coordinate with landing-oracle issue #5)
- [ ] Screenshot the deployed page → submit to landing-oracle for gallery card
- [ ] Set up CLAUDE.md with WEnDyS identity + 5 principles

## Key Files
- `src/pages/index.astro` — Main page (hero, soul modes, principles, family, footer)
- `src/styles/global.css` — Dewdrop theme tokens, glass/glow effects, animations
- `src/components/LangToggle.astro` — i18n system with full TH/EN dictionaries
- `src/components/Nav.astro` — Fixed glass nav bar
- `src/layouts/Base.astro` — Root layout (fonts, meta, FOUC prevention)
- `wrangler.toml` — Cloudflare Workers config (needs account_id + routes)
- `ψ/learn/Soul-Brews-Studio/landing-oracle/origin/` — Gallery source (cloned)
