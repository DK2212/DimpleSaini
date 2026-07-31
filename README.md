# Dimple Saini — Portfolio CV

Personal portfolio site for **Dimple Saini**, Senior .NET Full Stack Developer.

Static, dependency-free, self-hosted fonts — no build step, no framework, no external
requests. Deploys as-is to GitHub Pages.

## Files

| Path | Purpose |
|---|---|
| `index.html` | The whole site — markup, styles, and script inline |
| `fonts/` | Self-hosted WOFF2 fonts (Source Serif 4, IBM Plex Sans, IBM Plex Mono) |
| `Dimple-Saini-CV.pdf` | CV served by the Download CV buttons |
| `Dimple-Saini-CV.docx` | Editable source of the CV (not linked from the site) |
| `404.html` | Custom not-found page |
| `robots.txt`, `sitemap.xml` | Search-engine crawl hints |
| `.nojekyll` | Tells GitHub Pages to serve files as-is, skipping Jekyll processing |

## Publishing to GitHub Pages

Repository: `DK2212/DimpleSaini` · Live URL: `https://dk2212.github.io/DimpleSaini/`

1. **Make the repository public.** Pages will not run on a private repo without a paid
   plan. Go to **Settings → General**, scroll to *Danger Zone*, choose
   **Change repository visibility → Make public**, and confirm.
2. Go to **Settings → Pages**.
3. Under *Build and deployment*, set **Source** to `Deploy from a branch`, branch
   `main`, folder `/ (root)`, then **Save**.
4. Wait ~1 minute, then load `https://dk2212.github.io/DimpleSaini/`.

## Using a custom domain (optional)

1. Buy a domain (`dimplesaini.dev` or `dimplesaini.com` — Cloudflare Registrar sells at
   cost).
2. Add a file named `CNAME` in this repo containing only the domain, e.g. `dimplesaini.dev`
3. At your registrar, add a `CNAME` DNS record pointing `www` at
   `dk2212.github.io`, plus `A` records for the apex domain to GitHub's four
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
