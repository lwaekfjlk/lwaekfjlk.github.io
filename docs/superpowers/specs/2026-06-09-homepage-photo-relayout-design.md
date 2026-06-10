# Homepage Photo Relayout — Design

**Date:** 2026-06-09
**Status:** Approved by user

## Context

User initially asked for a full redesign ("不好看，帮我重新设计"). After reviewing three
style directions (classic serif / modern sans / sidebar) via visual mockups, the user
decided the current design is better than all three and narrowed the request to one
change: **make the profile photo bigger and move it below the intro text**.

Three placement options were mocked up; the user confirmed **Option C** (clicked B in
the browser during exploration, but explicitly confirmed C when asked).

## Decision: Layout C

Page order becomes:

1. **Profile header (text only, full content width):** name, Chinese name (于昊飞),
   affiliation, address, contact links (Email / Scholar / GitHub / LinkedIn / X)
2. **Bio:** the existing three paragraphs, unchanged
3. **Photo block (new):** the Cappadocia photo (`assets/img/self_pic_2.jpg`), centered,
   ~70% of content width, keeping current rounded corners + soft shadow, with the
   existing caption line ("Taken at Goreme, Cappadocia, Turkey. Credit to Naisong.")
   centered below it
4. **News** — unchanged
5. **Publications** (tag filters + list) — unchanged
6. **Visitor map** — unchanged

## Changes

### `_pages/about.md`
- Remove `.profile-photo-col` (photo + caption) from `.profile-header`; the header
  keeps only the info column content, now full width.
- Insert a new photo block between the bio section and the News section:
  `<div class="photo-section">` containing the `<img>` and the caption.

### `_sass/_base.scss`
- Simplify `.profile-header` (two-column flex no longer needed) and drop
  `.profile-photo-col` / now-unused photo-column rules, including the 640px
  breakpoint overrides for the photo column.
- Add `.photo-section`: centered block; image `width: 70%` of the content column,
  natural aspect ratio (no fixed height / no crop — the mockup's height crop was
  preview-only), `border-radius: 12px`, existing soft shadow
  (`0 2px 12px rgba(0,0,0,0.08)`); caption style reuses current
  `.profile-caption` look (small, light gray), centered.
- Mobile (≤640px): image becomes `width: 100%`.

## Not changing

Fonts, colors, navbar, News, Publications (including tag filter JS), visitor map,
all other pages.

## Notes / out of scope

- `_config.yml` `url` is temporarily `http://localhost:4000` for local dev (marked
  TEMP in the file); must be reverted to `https://haofeiyu.me` before deploy.
- `_sass/_base 2.scss` is a stray duplicate file (likely a Finder copy artifact),
  not imported by the build; left untouched.

## Verification

Jekyll serve is watching; after edits, screenshot `http://localhost:4000` (desktop
width and ~640px) and compare against the approved Option C mockup.
