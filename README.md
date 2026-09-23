# Jack Barry: personal site

My personal website. I'm a Service Desk Analyst working on Smart DCC's national smart-metering network, moving into network and security operations (NOC/SOC).

The site is a single static page, built to be read by hiring managers in a couple of minutes.

## Design

The page is laid out as an **auditable incident record**, the kind of document I work with every day:

- **Record header.** A reference number and a live "Viewed" timestamp in UK time sit at the top. Below them is a ruled grid of form fields: state, location, assignment, client, estate size, daily volume, first-contact resolution and contact.
- **Work notes.** Each role is a record with the same fixed row of fields (ref, period, organisation, location, state), followed by its notes.
- **Colour follows one rule.** Blue is only for things you can act on. Red is only for incident priority codes (P1/P2/P3). Everything else is ink on paper.
- **State is shown with ink, not badges.** "Open" and "In progress" are inverted ink stamps. Field rows invert on hover.
- **Three typefaces, each with one job.** [Schibsted Grotesk](https://fonts.google.com/specimen/Schibsted+Grotesk) for labels and headings, [Source Serif 4](https://fonts.google.com/specimen/Source+Serif+4) for reading, and [Martian Mono](https://fonts.google.com/specimen/Martian+Mono) only for data (refs, dates, figures).
- No cards, gradients, pills or glow.

It also supports:
- light and dark mode (dark mode is styled as a carbon copy)
- `prefers-reduced-motion`
- phone layouts (checked at 390px)
- a print stylesheet (hiring managers print CVs)

The full design system (tokens, type scale, components and rules) is in [DESIGN.md](DESIGN.md).

## Tech

- **One file:** `index.html`, with all CSS and JavaScript inline.
- **No build step and no dependencies.** The only external request is Google Fonts, with system font fallbacks.
- **A few dozen lines of plain JavaScript:** the live timestamp, the copy-email button (which falls back to selecting the text if the clipboard is blocked) and the current-section highlight in the nav.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. Go to **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, then pick `main` and `/ (root)`.
3. The site is served at `https://<username>.github.io/<repo>/`.

## Updating content

All content comes from my CV (September 2026 version) and is written directly in `index.html`. When the CV changes, update:

- the header field grid (the figures and the current assignment)
- the Work notes records (each record's `.meta` row and notes)
- the Capabilities table
- the footer's "Compiled from CV" date

## Repository layout

| Path | Purpose |
|---|---|
| `index.html` | The site |
| `DESIGN.md` | Design system: tokens, type, components, rules |
| `PRODUCT.md` | Product brief: audience, purpose, facts the site may use |
| `.impeccable/` | Design-tool state (config, design tokens as JSON, the page's direction brief) |

## How it was built

I designed and built the site with [Claude Code](https://claude.com/claude-code), using the Impeccable design skill:

1. Captured the product brief (audience, constraints, what not to claim) in `PRODUCT.md`.
2. Compared several visual directions on a decision page and chose "The Incident Record".
3. Built the page directly in code from a written direction contract.
4. An independent review agent checked two rounds of desktop and mobile captures against that contract, and I fixed what it found.
5. Recorded the resulting design system in `DESIGN.md`.
