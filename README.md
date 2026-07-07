# The Paywall Leak — Subscription Funnel Case Study

An interactive product case study modeled on Times Prime–style subscription paywalls, built to diagnose a conversion drop-off and propose a scoped fix — written up as a real PRD, not just a slide.

**Live demo:** _add your deployed URL here_

---

## What this is

Most digital news platforms convert less than 1 in 10 readers who hit a paywall. This project digs into *why*, using a modeled funnel (free article → paywall → checkout → payment), and proposes a single, scoped fix: replacing an 8-field card-only checkout with a one-tap UPI payment.

It's built as a working prototype rather than a static mockup — the funnel numbers and checkout mockups actually respond to user input.

## Features

- **Interactive funnel toggle** — switch between "Current Flow" and "With UPI Upsell" and watch the funnel bars, conversion numbers, and drop-off annotations recalculate live
- **Friction breakdown** — three concrete friction points pulled from typical mobile checkout behavior (form length, missing UPI, ad-heavy pre-paywall load)
- **Before/after checkout mockup** — a side-by-side comparison of the current 8-field card form vs. the proposed one-tap UPI flow
- **Embedded PRD** — problem statement, goal, success metric, requirements, out-of-scope items, and risks, formatted the way it would be handed to an engineering team

## The model

| Stage | Current | Proposed |
|---|---|---|
| Paywall encounters | 50,000 | 50,000 |
| Checkout starts | 10,000 (20%) | 10,500 (21%) |
| Payments completed | 4,000 (8.0% of paywall hits) | 4,600 (9.2% of paywall hits) |
| **Relative lift** | — | **+15%** |

All numbers are modeled for the purpose of this case study, not pulled from real platform data.

## Tech stack

Single-file HTML/CSS/JS — no build step, no dependencies. Fonts load from Google Fonts (Source Serif 4, Space Grotesk, IBM Plex Mono).

## Running locally

Just open `index.html` in a browser. No server or build process required.

## Deploying

This is a static single-file site, so any static host works:

- **Netlify Drop:** drag `index.html` onto https://paywalloptimiser.netlify.app/
- **GitHub Pages:** push to a repo, enable Pages, and point it at the root
- **Vercel:** import the repo and deploy with no build command

## Author

Built by Alice Singhal as a product case study — [LinkedIn](https://www.linkedin.com/in/alicesinghal) · [GitHub](https://github.com/alice-verse)
