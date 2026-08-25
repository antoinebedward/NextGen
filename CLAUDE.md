# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

This repository holds the source for the Fallingbrook Health and Wellness
website (Acupuncture, Cosmetic Acupuncture, and Registered Massage Therapy —
Orléans, ON), under `website/`. It's a static, framework-free HTML/CSS/JS
site with no build step, package manager, or test suite.

## Commands

There is no build/lint/test tooling. To preview the site locally:

```
cd website
python3 -m http.server 8000
```

Or just open `website/index.html` directly in a browser.

## Architecture

- Each page under `website/` (`index.html`, `services.html`, `about.html`,
  `policies.html`, `contact.html`) is fully self-contained — its own
  `<head>`, header/nav, and footer are duplicated in every file rather than
  assembled from includes, since there's no build step to stitch partials
  together. When changing shared chrome (nav links, footer contact info),
  update it in all five pages.
- `website/css/style.css` is the single shared stylesheet for all pages —
  CSS custom properties at the top (`--color-*`, `--font-*`) define the
  palette/typography site-wide.
- `website/js/main.js` is the single shared script (mobile nav toggle,
  active-nav-link highlighting via current filename, footer year, contact
  form client-side validation). The contact form has no backend wired up.
- `website/assets/images/` holds site images.

## Content status

Much of the current copy (exact phone/email/address, hours, service
pricing, social links, and the practitioner photo) is placeholder text
marked with `TODO` comments in the HTML, pending the real values from the
site owner. See `website/README.md` for the full list and for which facts
are already verified vs. placeholder.
