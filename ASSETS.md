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
| 2 | Hero image | `/public/images/hero/` (e.g. `public/images/hero/hero-salon.jpg`) |
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
| `public/videos/virtual-tour.mp4` | Virtual Tour section |
| `public/reference/website-design-reference.png` | Design reference only — **not** used as a site asset |

Still needed per the checklist above: hero image, suite/interior photos,
professional/beauty photos, icons.

## Business info still needed

- **Street address** — the "Visit A-1 FantasyBar" section (`index.html`,
  `id="visit"`) has a Google Maps embed and a working "Get Directions" button
  already wired to the correct location (from the map embed you provided),
  but the plain-text address label next to the map pin icon is a placeholder
  until you send the actual mailing address.
- **Phone number** (optional) — not currently in the site anywhere. Send it
  if you want a click-to-call link added near the map.

## Status

Logo and virtual tour video received and renamed to descriptive filenames
(originals had auto-generated names like `Screenshot 2026-09-09 122647.png`
from the upload). Design reference screenshot is in `/public/reference/` for
comparison only. Still waiting on hero image, suite photos, professional
photos, icons, and the business street address before the build is fully
finished.

Testimonials section currently uses sample/placeholder reviews (clearly
marked in `index.html` with `<!-- SAMPLE TESTIMONIALS — REPLACE WITH REAL
CUSTOMER REVIEWS -->`) — swap them for real client testimonials whenever
you have them.
