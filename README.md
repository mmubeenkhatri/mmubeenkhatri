# Portfolio — Muhammad Mubeen

A single-page portfolio site. No build step, no dependencies — one HTML file plus your CV.

```
index.html                 the whole site (HTML + CSS + JS inline)
Muhammad_Mubeen_CV.pdf     linked by the "Download CV" button
```

## Publish free on GitHub Pages

1. Create a new public repo — `portfolio` is a good name.
2. Upload `index.html` and `Muhammad_Mubeen_CV.pdf` to the repo root.
3. Repo → **Settings** → **Pages** → Source: *Deploy from a branch*, branch `main`, folder `/ (root)` → **Save**.
4. Wait ~1 minute. Your site is live at `https://mmubeenkhatri.github.io/portfolio/`.

Want it at `https://mmubeenkhatri.github.io` with no path? Name the repo exactly
`mmubeenkhatri.github.io` instead.

### Custom domain (optional)

Buy a domain, add a `CNAME` file to the repo containing just your domain
(e.g. `mubeen.dev`), then point your DNS at GitHub Pages:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  mmubeenkhatri.github.io
```

Then tick **Enforce HTTPS** in Settings → Pages.

## Turning on the contact form

Out of the box, the form opens the visitor's email client with the message pre-filled —
it works everywhere and needs no service. To receive submissions in your inbox instead:

1. Sign up free at [formspree.io](https://formspree.io) and create a form.
2. Copy the form ID from the endpoint they give you (`https://formspree.io/f/**xbljkqwe**`).
3. In `index.html`, find `var FORMSPREE_ID = "";` and paste the ID between the quotes.

The free tier covers 50 submissions a month, which is plenty for a portfolio.

## Editing the content

Everything is plain HTML in one file — search for the text you want to change and edit it.

| What | Where to look |
|:--|:--|
| Headline, intro paragraph | `<h1>` and `.lede` near the top of the body |
| The four metric numbers | `<div class="metrics">` — the `.n` spans |
| Projects | `<article class="project">` blocks |
| Stack chips | `<section id="capabilities">` |
| Colours | the `:root` block at the top of `<style>` — change `--signal` to re-skin the whole page |
| Fonts | the Google Fonts `<link>` and `--f-display` / `--f-body` / `--f-mono` |

## Before you share it

- Replace the placeholder metrics if any number is off — `8 products delivered`,
  `5 industry domains` and `2 as lead developer` are counted from your CV.
- Add a real figure to the LoanClod AI paragraph if you have one (hours saved,
  % faster onboarding). It's the strongest claim on the page and a number would prove it.
- Check the phone number and email render correctly on your phone.
