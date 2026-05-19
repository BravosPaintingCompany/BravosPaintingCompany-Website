# Bravo's Painting Company — Project Notes

## Tech Stack
- Astro v6 (static output)
- Tailwind CSS v3 (@astrojs/tailwind)
- Hosted on Netlify (with Netlify Forms for contact)
- Node.js v22.14.0 installed at ~/.local/nodejs/node-v22.14.0-darwin-arm64/bin/

## Dev Server
```
export PATH="$HOME/.local/nodejs/node-v22.14.0-darwin-arm64/bin:$PATH"
cd ~/Sites/bravos-painting
npm run dev
```
Then visit http://localhost:4321

## ⚠️ Reviews Page — Temporarily Hidden
The Reviews page has been intentionally removed while waiting for real customer reviews.

**To restore it when real reviews are ready:**

### Step 1 — Re-enable the page
```
mv ~/Sites/bravos-painting/src/pages/_reviews.astro ~/Sites/bravos-painting/src/pages/reviews.astro
```

### Step 2 — Add back to Header nav
In `src/components/Header.astro`, add this line back after Service Areas:
```
{ href: '/reviews', label: 'Reviews' },
```

### Step 3 — Add back to Footer
In `src/components/Footer.astro`, add this line back after Service Areas:
```
{ href: '/reviews', label: 'Reviews' },
```

### Step 4 — Add real reviews
Open `src/pages/reviews.astro` and update the `reviews` array with real customer names, locations, ratings, and quotes.

---

## Business Info
- Owner: Diego Bravo
- Phone: (657) 433-4791
- Email: info@bravospaintingcompany.com
- License: #1149855
- Service Area: Orange County, CA
- Brand color: #2E6DB5

## Image Locations
- Team photo: /public/team-photo.png (two-person shot)
- Diego portrait: /public/diego-portrait.png (solo — used in About section)
- Logo wide (header): /public/logo-wide.png
- Logo square (footer): /public/logo-square.png
- Service images: /public/images/services/
- Gallery images: /public/images/gallery/

## Temp Files to Clean Up
- /public/images/temp-preview/ — preview images used during image selection, safe to delete
- ~/Sites/hero-preview.html — preview HTML file used during design, safe to delete
