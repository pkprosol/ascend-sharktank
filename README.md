# ASCEND Shark Tank Landing Page

Static landing page for the ASCEND Shark Tank — held at the ASCEND Agency Growth & Leadership Summit 2026, Music City Center, Nashville, TN, June 8–11, 2026 (exact pitch slot TBD within program).

Cloned from `sharktank-nabip` per the "fill-in-the-blanks" approach Al outlined — same format, same prize structure, same Stripe payment link, just retargeted to the ASCEND audience.

## Wired

- **Stripe payment link** (entry fee, $10,000): `https://buy.stripe.com/4gM3cw4rk84lf4v6Tq57W0K` (ASCEND-specific link)
- All "Apply to Compete" CTAs route directly to Stripe checkout.
- `SPOTS_REMAINING` env var controls the live scarcity counter in the top banner (default `5`).

## TBD before final launch

Search `public/index.html` for `TBD:` to find every deferred item:

- Final panel of judges beyond Al Lewis
- Application deadline date (recommend ~3 weeks pre-event, e.g., mid-May 2026)
- Date and time slot for the pitch within the ASCEND June 8–11 program
- Specific room / area within Music City Center, Nashville

## Updating the spots counter

Edit `SPOTS_REMAINING` in `render.yaml` (or the value in the Render dashboard env vars), then redeploy. `build.sh` substitutes the value into the page at build time.

## Deploy to Render

1. Push this repo to GitHub.
2. In Render dashboard → **New** → **Static Site**, connect the repo.
3. Render auto-detects `render.yaml`. Publish directory is `./public`.
4. Custom domain: point DNS (e.g. `ascend-sharktank.validationinstitute.com`) to Render per their docs.
