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
- [x] Clean multi-section site with real content from the old website
- [x] Official brand colour palette applied
- [x] Logo (`logo.png`) present and wired into header + favicon
- [x] Hundreds of photos already in `assets/images/` (image_001 … image_380+)
- [x] Media page expanded to show more of the existing photography
- [x] Hero background set to a working existing image
- [ ] Domain fully pointed / active on Cloudflare Pages
- [ ] Cloudflare Pages project connected and live on gorillasummitcoffee.com
- [ ] Final image selection & compression (optional cleanup of very large originals)
- [ ] Old site taken offline / redirects set

---

## Asset Folder

Photos live in `assets/images/`. Many large original files are already committed. The site currently uses a selection of them on the homepage, locations, media and impact pages.

**Note on file sizes:** Cloudflare Pages allows max **25 MiB per individual file**. Most current images are under this limit. For best performance, compress the largest ones later (target ~300–800 KB for web display).

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

## Next Steps

1. Connect this repo to Cloudflare Pages and deploy (see steps above).
2. Point the domain (nameservers or CNAME) so the new site is live.
3. (Optional) Select the best 20–30 photos, compress them, and we can replace the bulk originals for faster loading.
4. Once live, we can decommission the old Wix-style site.

Tell me when the Cloudflare Pages project is connected or if you want more photos organised / renamed.
