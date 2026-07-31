# Dimple Saini — Portfolio CV

Personal portfolio site for **Dimple Saini**, Senior .NET Full Stack Developer.

Static, dependency-free, self-hosted fonts — no build step, no framework, no external
requests. Deploys as-is to GitHub Pages.

## Files

| Path | Purpose |
|---|---|
| `index.html` | The whole site — markup, styles, and script inline |
| `fonts/` | Self-hosted WOFF2 fonts (Source Serif 4, IBM Plex Sans, IBM Plex Mono) |
| `Dimple-Saini-CV.txt` | ATS-friendly plain-text CV, linked from the Download CV buttons |
| `404.html` | Custom not-found page |
| `robots.txt`, `sitemap.xml` | Search-engine crawl hints |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, skipping Jekyll processing |

## Publishing to GitHub Pages

1. In GitHub Desktop, click **Publish repository** (keep it **public** — private repos
   need a paid plan for Pages).
2. On github.com, open the repo → **Settings** → **Pages**.
3. Under *Build and deployment*, set **Source** to `Deploy from a branch`, branch
   `main`, folder `/ (root)`, then **Save**.
4. Wait ~1 minute. The site goes live at:
   `https://YOUR-USERNAME.github.io/DimpleCV/`

## Before you publish — replace the placeholder URL

Three files contain `YOUR-USERNAME`. Swap in your real GitHub username so canonical
tags and the sitemap point at the live site:

- `index.html` — the `<link rel="canonical">` tag
- `robots.txt` — the `Sitemap:` line
- `sitemap.xml` — the `<loc>` element

## Using a custom domain (optional)

1. Buy a domain (`dimplesaini.dev` or `dimplesaini.com` — Cloudflare Registrar sells at
   cost).
2. Add a file named `CNAME` in this repo containing only the domain, e.g. `dimplesaini.dev`
3. At your registrar, add a `CNAME` DNS record pointing `www` at
   `YOUR-USERNAME.github.io`, plus `A` records for the apex domain to GitHub's four
   Pages IPs (documented in GitHub's custom-domain guide).
4. In **Settings → Pages**, enter the domain and tick **Enforce HTTPS**.

## Editing content

Everything lives in `index.html`. Content sections in document order: hero and
at-a-glance panel, profile, focus areas, expertise, experience timeline, selected
work, background, contact.

Colours and spacing are CSS custom properties defined once in the `:root` block at the
top of the `<style>` element, with matching light and dark overrides. Change a value
there and it updates everywhere.

## Notes

- The page adapts to the visitor's light/dark system preference.
- A print stylesheet is included — `Ctrl`+`P` → *Save as PDF* produces a clean,
  recruiter-ready document with navigation and buttons stripped out.
- Schema.org `Person` structured data (JSON-LD) is embedded for search engines.
