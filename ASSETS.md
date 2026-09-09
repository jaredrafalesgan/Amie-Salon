# Asset Upload Guide

This document is the single source of truth for where website assets belong in this
repository. Upload files to the **exact paths** below — nothing should be dropped
loose into the project root or scattered across folders.

## Folder structure

```text
/public
  /logo             → Logo files (svg/png)
  /images
    /hero            → Hero/banner image(s)
    /suites          → Suite / interior photos
    /professionals   → Beauty professional / stylist photos
    /gallery         → Any additional gallery/brand photos
  /videos            → Virtual tour or other video assets
  /icons             → Icon files (svg/png)
  /fonts             → Custom font files, if any
```

This mirrors the standard `/public` convention used by static sites and frameworks
like Next.js/Vite, so assets are served directly without extra build config.

## Upload checklist

| # | Asset | Upload path |
|---|-------|-------------|
| 1 | Logo | `/public/logo/` (e.g. `public/logo/amie-salon-logo.svg`) |
| 2 | Hero image *(optional)* | `/public/images/hero/` (e.g. `public/images/hero/hero-salon.jpg`) — the hero now plays the virtual tour video as a full-bleed cinematic background; this image is only used as the `<video poster>` shown for a moment before the video loads |
| 3 | Suite / interior images | `/public/images/suites/` (e.g. `public/images/suites/suite-01.jpg`) |
| 4 | Professional / beauty images | `/public/images/professionals/` (e.g. `public/images/professionals/professional-01.jpg`) |
| 5 | Virtual tour video | `/public/videos/` (e.g. `public/videos/virtual-tour.mp4`) |
| 6 | Icons | `/public/icons/` |
| 7 | Any additional brand assets | `/public/images/gallery/` (or the closest matching folder above) |

## Rules

- **No placeholder/stock images.** Real assets only. If something is missing when
  it's time to build, it will be called out explicitly rather than substituted.
- **No scattering.** Everything lives under `/public`, in the subfolder that matches
  its purpose. If a new asset type doesn't fit an existing folder, a new folder will
  be added under `/public` and documented here — not placed ad hoc.
- Once assets are uploaded, each file will be inspected and mapped to its website
  section (e.g. `hero.jpg → Hero Section`, `logo.svg → Header + Footer`) before the
  build starts.

## Received assets

| File | Maps to |
|---|---|
| `public/logo/a1-fantasybar-logo-horizontal.png` | Horizontal logo lockup — header / footer |
| `public/logo/a1-fantasybar-logo-badge.png` | Circular badge/seal variant of the logo |
| `public/videos/virtual-tour.mp4` | Virtual Tour section (also reused as the hero's full-bleed background video) |
| `public/images/suites/suite-01.mp4` | Suite Rentals section — used as a looping video instead of a static photo, per your request |
| `public/images/gallery/virtual-tour-bg.mp4` | Virtual Tour section's background — looping video behind the dark overlay, instead of a static poster photo |
| `public/images/professionals/professional-01.jpg` | Independent Professionals section photo (renamed from `Gemini_Generated_Image_....jpg`) |
| `public/images/hero/hero-poster.png` | Hero `<video poster>` — shown briefly before the background video loads (renamed from `About image.png`) |
| `public/reference/website-design-reference.png` | Design reference only — **not** used as a site asset |

All planned assets are now filled — icons are handled with the site's own
generated line-icon set (matching the brand's gold/pink line style), no
custom icon files needed.

## Business info

Received and live on the site (Visit A-1 FantasyBar section, `id="visit"`):

- **Address:** 247 W Camp Wisdom Rd., Dallas, TX 75116
- **Phone:** (469) 463-8438 — click-to-call link, plus a "Call Us" button
- **Email:** A1fantasybar@gmail.com — click-to-email link

The map and "Get Directions" button were already wired to the correct
location from the embed you provided earlier; this address/phone/email are
just the plain-text/clickable versions displayed next to them.

## Status

All planned photo/video slots and business info are filled in. Design
reference screenshot is in `/public/reference/` for comparison only.

Testimonials section currently uses sample/placeholder reviews (clearly
marked in `index.html` with `<!-- SAMPLE TESTIMONIALS — REPLACE WITH REAL
CUSTOMER REVIEWS -->`) — swap them for real client testimonials whenever
you have them.
