# Portfolio — Md. Anamul Haque

A fast, dependency-free personal site (plain HTML + CSS + a little vanilla JS). No build step, no framework — just open it or drop it on any static host.

## Files
```
portfolio/
├── index.html      # all content + structure
├── styles.css      # design system + responsive dark theme
├── script.js       # mobile nav, scroll reveal, active-link, year
├── assets/
│   ├── resume.pdf  # ← add your CV here (the "Download CV" button links to it)
│   └── og.png      # ← optional 1200×630 social preview image
└── README.md
```

## Preview locally
Open `index.html` directly in a browser, or run a tiny server:
```bash
cd portfolio
python3 -m http.server 5173
# visit http://localhost:5173
```

## Customize (quick)
- **Text/content:** edit `index.html` (search for a phrase and replace).
- **Colors:** edit the `:root` tokens at the top of `styles.css` (`--accent` is the cyan).
- **CV button:** export your CV as PDF → save as `assets/resume.pdf`.
- **Social preview:** add `assets/og.png` (1200×630) and set `<meta property="og:image" content="assets/og.png">` in `index.html`.
- **Photo (optional):** the hero uses a code card instead of a photo. To use your photo, replace the `.hero__card` block in `index.html` with an `<img>` and style it round.

## Deploy (pick one — all free)
- **GitHub Pages:** create a repo (e.g. `dev-Anamul/portfolio`), push these files, then Settings → Pages → deploy from `main` / root. Or name the repo `dev-Anamul.github.io` to serve at your root domain.
- **Netlify / Vercel / Cloudflare Pages:** drag-and-drop the `portfolio` folder, or connect the repo. Zero config.
- **Custom domain:** buy a domain (e.g. `anamulhaque.dev`) and point it at the host. Then add the URL to your LinkedIn, GitHub, and CV.

## After deploying
- Add the live URL to: LinkedIn (Website field), GitHub (profile URL + README), CV header, email signature.
- Keep name + links identical everywhere (recruiters cross-check).

## Accessibility & quality notes (built in)
- WCAG-friendly contrast, visible focus rings, skip link, semantic landmarks, `aria-*` on the menu.
- Mobile-first responsive; 44px+ tap targets.
- `prefers-reduced-motion` respected (animations disabled for users who opt out).
- No external JS/CSS frameworks — loads instantly, works offline.
