# t3chnicallyinclined.github.io

Personal site for Tristan Rega — a status board rather than a portfolio.

`index.html` is a single static page with no build step and no dependencies beyond a
Google Fonts stylesheet. It reads the public GitHub REST API from the visitor's
browser on load (no token, no backend) to show current stars, per-release asset
download totals and the date of the most recent release for each tracked repository.

If GitHub rate-limits the visitor's IP (60 unauthenticated requests per hour), the page
falls back to figures recorded on 16 November 2026 and says on screen that it has done so.

## Publishing

GitHub Pages, from the default branch root. The site is then served at
https://t3chnicallyinclined.github.io

Add `resume.pdf` to this directory to make the footer link work.

## Adding a project

Edit the `TRACKED` array near the top of the inline script. Each entry needs the
repository name, a display name, one sentence, which metrics to show, and the fallback
figures used when the API is unavailable.
