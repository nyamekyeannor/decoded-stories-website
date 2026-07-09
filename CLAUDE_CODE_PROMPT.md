# Decoded Stories — Claude Code Build Prompt

Paste this into Claude Code once you've got the repo open in the terminal.

---

Build the Decoded Stories podcast website as a static site (plain HTML/CSS/vanilla JS,
no framework, no build step) so it deploys straight to Netlify like my other sites.

I have a fully-approved design mockup at `design-reference.html` in this folder —
use it as the exact visual and structural reference. Match its layout, colors,
fonts, spacing, and component structure closely. Key things to preserve:

- Light theme, Inter font throughout
- Warm/soft gold accent color, with the brand orange reserved specifically for the
  "Stories" word in the wordmark/hero heading (see the CSS variables --accent vs --brand
  in the reference file)
- Unified hero card: rounded container with a portrait host photo on one side and
  title/description/platform badges (real Apple/Spotify/YouTube colored logos) on the other
- Featured Episodes section: minimal card grid (thumbnail, category tag, date/season label, title, view link)
- Listen to Recent Episodes section: tabbed by season (All / Season 3 / Season 2 / Season 1)
  with a Load More button that paginates 6 at a time — see the JS in the reference file
- About section, Newsletter signup section, "Be a Guest" CTA banner, in that order
- Scroll-reveal animation on the Featured cards, About, Newsletter, and Guest banner
  (IntersectionObserver — see reference file JS)
- Soft decorative blurred shapes behind the hero card

Episode content: pull from `content/episodes.json` in this folder. Build the site so
episode data is data-driven from this file (or a JS version of it) rather than
hardcoded per-episode HTML, so it's easy for me to add new episodes later without
touching layout code.

Images: use `assets/logo.png`, `assets/cover.jpg`, and `assets/thumb.jpg` from this
folder. All episode thumbnails currently reuse `assets/thumb.jpg` as a placeholder —
structure the code so swapping in real per-episode thumbnails later is a one-line change
per episode (e.g. an `image` field in the episode data).

Pages/sections needed on the single homepage:
1. Sticky nav (logo + Decoded Stories wordmark, links to Episodes/About/Guest/Newsletter)
2. Hero card
3. Featured Episodes
4. Listen to Recent Episodes (tabbed, paginated)
5. About (bio text below — this is finalized, use it as-is)
6. Newsletter signup (mock form for now — real MailerLite embed comes later, once I have
   the account set up)
7. Be a Guest CTA banner (mock form/mailto link for now)
8. Footer (platform links, social links, contact email annorcode@gmail.com)

Set this up to auto-deploy to Netlify from this repo once pushed to GitHub.

Ask me before assuming anything about content you don't have (real episode
descriptions, guest form destination, etc.) rather than inventing it.

---

## About section copy (finalized, use as-is)

**Hey, I'm Nyamekye**

I'm a front-end engineer and QA analyst by day, and the host of Decoded Stories, where I sit down with creators, developers, and tech professionals to talk about the stories behind their careers.

Every episode digs into the real journey. The pivots, the setbacks, the moments nobody posts about that actually lead to growth. Less highlight reel, more honest conversation.

Outside the mic, I build things under the name AnnorCode. Based in the DC area.

Got a story worth telling? I want to hear it.

