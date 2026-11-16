# AGENTS.md

## Architecture
Static site, no build step. Netlify publishes `public/` (see `netlify.toml`).

- `public/index.html` – the entire presentation: inline `<style>` and `<script>`, DE/EN copy switched via `data-i` attributes and a JS dictionary.
- `public/img/` – photography referenced as `img/<name>.jpg` (some lazy-loaded via `data-src`).
- `public/_headers` – sends `X-Robots-Tag: noindex, nofollow` for all paths.
- `public/robots.txt` – disallows all crawlers.

## Conventions and decisions
- The site was supplied complete by the client; keep edits minimal and preserve the design and copy.
- It is intentionally private/unindexed (confidential offer for a named owner). Do not remove the noindex headers, robots meta or robots.txt.
- Share-card metadata (`description`, `og:site_name`, `og:title`, `og:description`) was added to the head; no `og:image` is set on purpose.
- Contact is via `mailto:` links only; there is no backend or form.
