# Therapy Demo Webpage (Willow & Sage Therapy)

Demo landing page for a therapy-practice prospect (2026-09-15). Everything about the brand is MADE UP: practice "Willow & Sage Therapy", therapist "Dr. Maya Reyes, LMFT", phone (555) 555-0163, email hello@willowandsagetherapy.com. No location or state is named anywhere on purpose. Swap all facts when the real prospect's details arrive.

## Files
- `index.html` — the whole site: single file, no build step. Fonts: Inter (variable) + Caveat (script accent) via Google Fonts.
- `img/` — 4 Higgsfield gpt_image_2_5 stills (quality low; PNG bytes despite .jpg names): `hero.jpg` (golden-hour therapy office), `room.jpg` (cozy corner, reused across the 4 specialty tab panels), `portrait.jpg` (therapist), `calm.jpg` (plant-shadow wall, layered under the umber band rectangles).
- `therapy demo vid 1.mp4` — Ronny's own screen-recorded walkthrough sourcing the design references. NOT a site asset; ignore it.

## Design system
Superhuman style spec (`~/Design Related Resources/Superhuman/Superhuman Style Reference.rtf`) with its wine/violet palette remapped to the warm Compatto reference: cream `#F2EEE6` canvas, ink `#2B2620`, espresso `#3D2E22` (CTAs/announcement/footer), bronze `#A0784A` (inline links only), sand `#E3D5C0` (secondary fill/active tab), umber `#4A3A2C` (dark full-bleed band). Spec rules enforced: headlines weight 460 (never 700), no drop shadows anywhere (depth = photography + backdrop blur), radii 16/8/999, max-width 1200px, minimal motion (0.2s link underlines, nav blur border on scroll, IntersectionObserver fade-rise reveals honoring prefers-reduced-motion).

Sections: announcement pill → sticky blurred nav → full-bleed photo hero with centered 64px headline + two floating glass cards (hidden below 1100px/900px) → 6-cell trust strip → specialties tab strip (4 functional tabs) → 4-step "how it works" → umber full-bleed band with layered translucent rects + Caveat script → about with portrait → FAQ `<details>` accordion → gradient band + demo form → espresso footer with 988 crisis line.

Form is demo-only: JS swaps in a success panel, posts nowhere. Wire to Netlify Forms if this ships.

## Preview / verify
Open `index.html` directly (relative img paths) or any static server. The in-app browser pane won't repaint below the fold; full-page proof shots came from puppeteer-core headless Chrome in the session scratchpad (`shots.mjs`: 1280px + 390px viewports, fullPage, scroll-through first so lazy images load, form submit + tab click assertions).

## Guardrails (grep before any revision)
No em/en dashes or hyphen sentence punctuation in copy; no state names; no client/company names from Ronny's roster; headlines never 700; no `box-shadow`. All were verified clean at build time.
