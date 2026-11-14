# CLAUDE.md — adamhodges.org

## Project summary

Adam Hodges's academic profile site: a single page introducing his work as a
sociocultural linguist (language and politics, war discourse, race and racism,
social media, discourse studies) with his featured books, publications grouped
by theme, and courses taught.

Plain static files, no build step:

- `index.htm`: the whole page (content, meta tags, structured data, and a few
  lines of inline JavaScript for the mobile menu)
- `styles.css`: all styling; colors, fonts, and sizes are CSS custom properties
  in `:root` at the top
- `images/`: the portrait and book covers
- `docs/`: PDFs linked from the page
- `favicon.svg`, `apple-touch-icon.png`: the AH monogram icons
- `CNAME`: the custom domain
- `_config.yml`: tells GitHub Pages not to publish this file; list any other
  repo-only files there too

## Hosting and publishing

- **GitHub Pages** serves the `main` branch at https://adamhodges.org (the
  domain is set in `CNAME`; don't remove or change it).
- Pushing to `main` publishes the site. Don't commit or push unless Adam asks.
- To check a change locally, open `index.htm` in a browser.
- **Analytics:** Cloudflare Web Analytics only (the beacon at the end of
  `index.htm`). Don't add other tracking.

## Conventions

- Plain HTML, CSS, and a minimum of JavaScript. No frameworks, build tools, or
  new dependencies.
- **Browser support:** use features that are Baseline Widely available freely.
  Newer features only as an enhancement: feature-detect them, and the page must
  still work and read well without them. Fallbacks are short hand-written CSS or
  JavaScript, never a polyfill library or a new dependency.
- Use the existing design tokens in `styles.css` rather than new hard-coded
  colors or sizes. Keep text and background pairs at WCAG AA contrast or better.
- **Keep the metadata in step with the page.** When the job title, affiliation,
  books, or profile links change, update the `<title>`, meta description, Open
  Graph and Twitter tags, and the `Person` structured data in the `<head>` to
  match.
- Every image has alt text; book covers name the book.
- Publication entries keep their existing citation format. Don't reword Adam's
  descriptions of his own work without asking.
- External links open in a new tab, as the existing links do.
- Small commits with clear messages.
