# Gorilla Summit Coffee – 2026 Website Redesign

Clean, modern static website for **Gorilla Summit Coffee** (specialty coffee social enterprise from the highlands of Uganda).

**Repo purpose:** Redesign + redeploy on Cloudflare Pages while preserving the vibrant coffee-farming vibe and logo colours of the original site.

---

## Current Status (Aug 2026)

- [x] GitHub repository created (`samkasse/gorillasummitcoffee`)
- [x] Clean multi-section single-page site with real content from the old website
- [x] Earthy + highland green colour palette (ready to refine with official logo colours)
- [ ] Logo + photography assets added
- [ ] Domain fully pointed / active on Cloudflare
- [ ] Cloudflare Pages project connected and live
- [ ] Final content & image polish
- [ ] Old site taken offline / redirects set

---

## Colour Palette (Suggested – refine with logo)

Based on the original earthy coffee feel + vibrant highland farming vibe:

| Role              | Hex       | Notes                              |
|-------------------|-----------|------------------------------------|
| Background        | `#faf8f5` | Warm off-white / cream             |
| Alt background    | `#f0ebe3` | Soft parchment                     |
| Primary (coffee)  | `#2c1810` | Deep roasted brown                 |
| Accent brown      | `#4a2f23` | Hover / secondary brown            |
| Highland green    | `#2d4a3e` | Leaf / forest / sustainability     |
| Green light       | `#3d6354` | Supporting green                   |
| Text              | `#1a1a1a` | Near black                         |
| Muted text        | `#5c5c5c` | Secondary copy                     |
| Border            | `#e5dfd6` | Soft warm border                   |
| Dark footer       | `#1f140f` | Deep brown-black                   |

**Next step:** Share the official logo (PNG/SVG or clear photo). We will extract exact brand colours and update the CSS variables.

---

## Recommended Asset Folder Structure

```
gorillasummitcoffee/
├── index.html
├── styles.css
├── README.md
├── assets/
│   ├── images/
│   │   ├── logo.png              (or logo.svg – primary logo)
│   │   ├── logo-white.png        (for dark backgrounds if needed)
│   │   ├── favicon.png / .ico
│   │   ├── hero.jpg              (highland farm / landscape hero)
│   │   ├── about-farmers.jpg
│   │   ├── kanungu.jpg
│   │   ├── kisoro.jpg
│   │   ├── bwindi.jpg
│   │   ├── processing.jpg
│   │   ├── cherries.jpg
│   │   └── packaging.jpg
│   └── fonts/                    (optional – currently using Google Fonts)
└── (future: robots.txt, sitemap.xml, etc.)
```

**Tips**
- Optimise images (WebP preferred, or compressed JPG/PNG). Aim for <200–300 KB for hero, smaller for cards.
- Keep logo as SVG if possible for crisp scaling.
- Name files clearly and use lowercase + hyphens.

Once you upload the logo and key photos into `assets/images/`, we can wire them into the HTML (hero background, location cards, about section, favicon).

---

## Deployment Instructions – Cloudflare Pages

### 1. Prerequisites
- Domain `gorillasummitcoffee.com` added in Cloudflare (nameservers updated).
- GitHub account connected to Cloudflare (this repo is already under `samkasse`).

### 2. Create the Pages Project
1. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com).
2. Go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Select the repository: `samkasse/gorillasummitcoffee`.
4. Configure build settings:
   - **Framework preset:** None (or Static HTML)
   - **Build command:** leave empty
   - **Build output directory:** `/` (root)
   - **Root directory:** `/`
5. Click **Save and Deploy**.

Cloudflare will pull the `main` branch and publish the static files.

### 3. Custom Domain
1. In the Pages project → **Custom domains** → **Set up a custom domain**.
2. Add `gorillasummitcoffee.com` and `www.gorillasummitcoffee.com`.
3. Cloudflare will guide you to create the required CNAME / A records (usually automatic if the domain is already on Cloudflare).
4. Wait for SSL to provision (usually a few minutes).

### 4. Optional Improvements
- Enable **Always Use HTTPS**.
- Add a simple `_redirects` or Cloudflare Redirect Rules if old Wix URLs need 301s.
- Later: Cloudflare Images or R2 for larger media libraries.

---

## Migration Checklist

### Content & Assets
- [x] Extract core story, locations, impact and contact details from old site
- [ ] Obtain high-resolution official logo (and any colour guidelines)
- [ ] Collect / organise photography (farms, farmers, cherries, processing, Bwindi/Kanungu landscapes)
- [ ] Write or refine any missing copy (e.g. specific lot descriptions, current harvest notes)
- [ ] Add Open Graph / social sharing meta tags + images

### Technical
- [ ] Confirm domain nameservers point to Cloudflare and status is Active
- [ ] Connect this GitHub repo to Cloudflare Pages and deploy
- [ ] Attach custom domain(s) and verify HTTPS
- [ ] Test mobile + desktop thoroughly
- [ ] Add favicon and logo to the live site
- [ ] (Optional) Set up basic analytics (Cloudflare Web Analytics is free and privacy-friendly)

### Launch
- [ ] Final content review with stakeholders
- [ ] Soft launch / preview URL testing
- [ ] Point DNS fully if not already done
- [ ] Announce new site
- [ ] Decommission old Wix (or other) site and set any necessary redirects

---

## Local Development

Simply open `index.html` in a browser, or use any static server:

```bash
# Python
python3 -m http.server 8000

# Node (if you have npx)
npx serve .
```

Then visit `http://localhost:8000`.

---

## Next Actions (Recommended Order)

1. **Share the logo** (file or clear description of main colours) so we can lock the palette and replace the text logo.
2. Upload key images into `assets/images/`.
3. Confirm Cloudflare domain status (screenshot of the domain overview is perfect).
4. We will then wire images into the HTML, polish any remaining sections, and walk through the Pages deploy together.

---

**Contact for the project:** This redesign is being managed in collaboration with the Gorilla Summit Coffee team / technical support.

Questions or ready for the next step? Just reply with the logo / images / Cloudflare status and we continue.
