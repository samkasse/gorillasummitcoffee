# Gorilla Summit Coffee – 2026 Website Redesign

Clean, modern static website for **Gorilla Summit Coffee** (specialty coffee social enterprise from the highlands of Uganda).

**Repo purpose:** Redesign + redeploy on Cloudflare Pages while preserving the vibrant coffee-farming vibe and official logo colours.

---

## Official Brand Colours (from logo guidelines)

| Role | Hex | Usage |
|------|-----|-------|
| Forest Green | `#3E6B35` | Primary green, accents, tags |
| Fresh Leaf Green | `#79B84A` | Bright accents, highlights |
| Coffee Brown | `#5A3825` | Secondary brown |
| Dark Espresso | `#2A1B14` | Main text / dark accents |
| Cream | `#E7D2A5` | Warm supporting |
| Warm Beige | `#D8C19B` | Borders / soft backgrounds |
| Ivory | `#F6F2EA` | Main page background |
| Gold | `#C9A227` | Optional luxury accent |
| Rich Black | `#111111` | Strong text |

These are now live in `styles.css` as CSS variables.

---

## Current Status (Aug 2026)

- [x] GitHub repository created
- [x] Clean multi-section single-page site with real content from the old website
- [x] Official brand colour palette applied
- [x] Logo reference wired into header (place `logo.png` in `assets/images/`)
- [ ] Upload final logo.png (and other photos) into `assets/images/`
- [ ] Domain fully pointed / active on Cloudflare
- [ ] Cloudflare Pages project connected and live
- [ ] Final content & image polish
- [ ] Old site taken offline / redirects set

---

## Asset Folder Structure

```
gorillasummitcoffee/
├── index.html
├── styles.css
├── README.md
├── assets/
│   └── images/
│       ├── logo.png          ← official circular logo (required)
│       ├── favicon.png
│       ├── hero.jpg          (highland landscape)
│       ├── kanungu.jpg
│       ├── kisoro.jpg
│       ├── bwindi.jpg
│       └── ...other photos
└── (future: robots.txt, sitemap.xml)
```

**Action needed:** Upload the clean circular logo as `assets/images/logo.png` (PNG with transparent background preferred, or the versions you already shared).

---

## Deployment – Cloudflare Pages

1. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git
2. Select repo `samkasse/gorillasummitcoffee`
3. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: `/`
4. Deploy
5. Custom domains → add `gorillasummitcoffee.com` + `www`

---

## Migration Checklist

### Content & Assets
- [x] Extract core story, locations, impact and contact details
- [x] Official colour palette locked from logo guidelines
- [ ] Place final `logo.png` in `assets/images/`
- [ ] Collect / organise photography
- [ ] Open Graph / social meta images

### Technical
- [ ] Confirm domain nameservers point to Cloudflare and status is Active
- [ ] Connect this GitHub repo to Cloudflare Pages and deploy
- [ ] Attach custom domain(s) and verify HTTPS
- [ ] Test mobile + desktop

### Launch
- [ ] Final content review
- [ ] Soft launch / preview URL testing
- [ ] Announce new site
- [ ] Decommission old site + redirects

---

## Next Immediate Step

1. Upload the official logo as **`assets/images/logo.png`** (you already have clean versions).
2. Tell me the Cloudflare domain status (or share a screenshot).
3. I will then finalise any remaining wiring and we deploy together.
