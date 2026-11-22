# BeatStreamPrices site

Static pages for the BeatStreamPrices iPhone app: privacy policy, terms of use and support.
Live at https://beatstreamprices.scheiberintelligence.com

## Layout
- `public/` holds the pages (index, privacy, terms, support) and `_headers`.
- `wrangler.jsonc` serves `public/` as static assets on Cloudflare.

## Before the first deploy
Replace these placeholders in `public/`. Search with: `grep -rn "\[YOUR\|\[the State\|\[Ada" public`
- `[YOUR LEGAL NAME OR BUSINESS NAME]` in privacy.html and terms.html
- `[YOUR SUPPORT EMAIL]` in privacy.html, terms.html and support.html
- `[the State of Idaho]` and `[Ada County, Idaho]` in terms.html

## Deploy (Cloudflare Workers, connected to this repo)
Build command: leave empty. Deploy command: `npx wrangler deploy`.
Then add the custom domain under Settings, Domains and Routes.
