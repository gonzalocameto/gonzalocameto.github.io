# gonzalocameto.github.io

Personal site. Plain static HTML + CSS, no build step, no Jekyll (`.nojekyll`).

```
index.html            the page
assets/style.css      styles (light/dark follow the OS)
assets/favicon.svg
qr/qr-ciarp26.svg     QR for the last CIARP slide → https://gonzalocameto.github.io/hyena-lai/?ref=ciarp26 (project page)
```

## Preview locally

```bash
python3 -m http.server 8000      # open http://localhost:8000
```

## Deploy (first time)

1. Create an **empty public** repo on GitHub named exactly `gonzalocameto.github.io`.
2. Push:
   ```bash
   git remote add origin git@github.com:gonzalocameto/gonzalocameto.github.io.git
   git push -u origin main
   ```
3. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
4. After ~1 min the site is live at https://gonzalocameto.github.io/

Afterwards every push to `main` redeploys.

## Analytics (GoatCounter)

GitHub Pages has no visitor analytics (repo *Insights → Traffic* only counts views of the repo on github.com).
GoatCounter is free for personal sites, cookieless (no consent banner) and needs one script tag.

1. Sign up at https://www.goatcounter.com/signup and pick a code, e.g. `gcameto` → dashboard at `https://gcameto.goatcounter.com`.
2. Done: the script at the bottom of `index.html` uses the code `gcameto`.
3. Push. Visits appear within seconds.

What you get:
- **Visits from the talk**: the QR points to `?ref=ciarp26`; GoatCounter reports `ref` / `utm_*` parameters as the
  referrer/campaign, so CIARP scans show up separately from other traffic.
- **Clicks**: links with `data-goatcounter-click="…"` (emails, code, BibTeX, LinkedIn…) are counted as events.

## Pending

- [ ] Slides: the only PDF is `docs/slides/hyenalai-ciarp2026.pdf` in the `hyena-lai` repo (written there by `build_handout.sh` in the talk sources). Push that repo before the talk; the Slides button here links to it and appears by itself from Thu Nov 26 (Mexico City time), only if the file is published.
- [ ] Google Scholar link, if a profile is created.
- [x] `github.com/gonzalocameto/hyena-lai` is public (checked 2026-11-15).
- [ ] Enable GitHub Pages on `hyena-lai` (Settings → Pages → main / `/docs`) so the
      **Project page** button on this page resolves.
