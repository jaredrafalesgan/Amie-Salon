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

## Status

Repository currently contains only the folder scaffold (`.gitkeep` placeholders,
no real assets yet). Waiting on asset upload before the build begins.
