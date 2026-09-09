# Using `index.html` in GoHighLevel (GHL)

`index.html` is a single self-contained file — all CSS and JS are inlined, there's
no build step and no external framework, so it drops straight into a GHL page.

## How to paste it in

1. In GHL, open the page/funnel step you want this on.
2. Add a **Custom Code / Custom HTML** element (full-width section).
3. Open `index.html` in a text editor, select all, copy.
4. Paste the entire contents into the Custom HTML element and save.

If GHL's editor strips out the `<head>` (some custom-code elements only accept
body content), move the `<link>` Google Fonts tag and the `<style>` block into
the page's **Settings → Custom CSS / Head Tracking Code** area instead, and paste
only everything from `<header>` down through the closing `</script>` into the
Custom HTML element.

## Images and video

All images/video currently point at this GitHub repo's raw file URLs, e.g.:

```
https://raw.githubusercontent.com/jaredrafalesgan/Amie-Salon/claude/repo-asset-setup-i8cy81/public/logo/a1-fantasybar-logo-badge.png
```

This means:
- **You don't need to re-upload assets to GHL.** As you upload real photos to
  the exact paths listed in `ASSETS.md`, they'll appear on the live GHL page
  automatically on next load — no code changes needed.
- Missing images currently show a clearly labeled "upload here" placeholder box
  instead of a broken image or stock photo (see below).

**Before this goes fully live**, two things worth doing:
1. **Merge this branch to `main`** (or your default branch) and update the URLs
   from `claude/repo-asset-setup-i8cy81` to `main` — a feature branch isn't a
   stable long-term image host.
2. **Move the virtual tour video off raw GitHub hosting.** It works for now, but
   a 15MB `.mp4` served from `raw.githubusercontent.com` isn't ideal for
   production load times. Consider GHL's own media library, or an embed from
   YouTube/Vimeo, once you're ready to launch.

## Missing assets

Per `ASSETS.md`, these are still needed — until uploaded, their sections show a
dashed placeholder box naming the exact path to upload to:
- `public/images/hero/hero-salon.jpg` — hero section photo
- `public/images/suites/suite-01.jpg` — suite rental section photo
- `public/images/professionals/professional-01.jpg` — professionals section photo
- `public/images/gallery/virtual-tour-poster.jpg` — virtual tour background photo
- `public/icons/` — not yet wired up; the site currently uses generated line-icon
  SVGs (scissors, comb, lock, diamond, etc.) as stand-ins. Send real icon files
  if you want your own set used instead.
