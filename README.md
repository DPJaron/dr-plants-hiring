# Dr. Plants — Careers / Hiring Site

A single-page, scroll-driven careers site for the **Dr. Plants** YouTube channel. Three stacked sections plus a footer:

1. **Hero** — dark, with a tilted 4-row infinite thumbnail marquee behind a centered brand lockup, headline, and "Apply Now" CTA.
2. **About Us** — cream background, animated count-up stats (Subscribers / Views), hiring blurb, and a second "Apply Now" CTA.
3. **Open Roles** — four role cards (Creative, Producer, Videographer / Editor, Thumbnail Artist), each linking to its Fillout application form.
4. **Footer** — brand lockup, "Watch on YouTube" button, copyright.

Scattered "polaroid" photos float over Sections 2 & 3 on wide screens.

## Stack

Plain static site — one `index.html` with inline `<style>` and `<script>`, plus local `assets/`. No build step, no dependencies. Fonts load from Google Fonts (Sora, Manrope, Caveat).

## Run locally

Any static file server works, e.g.:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

(Opening `index.html` directly via `file://` works too, but a server is recommended so image fetch priorities and the marquee reveal behave as in production.)

## Deploy

Upload the whole folder (`index.html` + `assets/`) to any static host — Netlify, Vercel, Cloudflare Pages, GitHub Pages, S3, etc. No configuration needed.

## Editing the role application links

The four Fillout form URLs live in the `.role-list` anchors in `index.html`. Swap the `href` values to update them.

## Assets

- `assets/logo-circle.png`, `assets/signature.png` — hero + footer brand lockup
- `assets/favicon.png`, `assets/logo.png` — favicon / full logo
- `assets/m/01–13.jpg` — hero marquee thumbnails (16:9)
- `assets/p/*.jpg` — polaroid photos

Implemented from the Claude Design handoff bundle (`dr-plants-hiring-v7`). The reduced-motion media query disables the marquee and CTA shake for users with `prefers-reduced-motion: reduce`.
