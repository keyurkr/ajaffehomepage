# A.JAFFE Homepage Redesign — Preview Build

Standalone HTML homepage previews for client review. Each file is fully self-contained (all CSS/JS inline); the only external dependencies are **Google Fonts** and the **real A.JAFFE media** referenced from the live CDN.

## Files

| File | Version | Nav | Status |
|---|---|---|---|
| `ajaffe-home-v1.html` | **A** | Refined top navigation | ✅ Built |
| `ajaffe-home-v2.html` | **B** | Tacori-style left-side navigation (fixed 260px rail + slide-out flyouts on desktop; 72px icon strip on tablet; slim top bar + drawer on mobile — same content/design system) | ✅ Built |
| `ajaffe-home-v3.html` | **V3** | Same header, navigation, mega menu, hero and footer as `ajaffe-home-v1.html` (byte-identical). Everything between hero and footer revised for space, pacing and editorial composition — see "V3 revision" below. | ✅ Built |

### V3 revision (below the hero only)
Order: Categories → **Quilts®** editorial (video | text, 50/50) → **Signature Shank®** editorial (text | video, 50/50) → **Expandables™** full-width moment → **Discover A.JAFFE** (scrolling rail, 3½ cards) → **Signature Collections** (Lotus™ · Classics™ · Modern Royals™) → **Customization** full-width video → **A.JAFFE Favorites** (1 sticky featured + 6) → **Maps by A.JAFFE** full-width band (same height as Customization; desktop `images/maps-banner-wide.jpg`, mobile `images/maps-banner.jpg` stacked above the copy) → **Celebrities** (curated 4) → **Crafted in New York Since 1892 · Find a Retailer · Schedule a Showing** (one row of 3 cards: `ourstory01.png`, `images/find-retailer.jpg`, `images/schedule-showing.jpg`) → **The A.JAFFE Promise** (kept from V2) → footer.
One layout system: full-width container with 64px side margins · 12px gutter between all tiles · section header title-left / link-right · one card caption style · lifestyle 4:5, products 1:1, editorial video boxes at the video's own ratio (1920:2165).
Spacing tokens: `--v3-s` 48–72px · `--v3-m` 64–96px · `--v3-l` 80–128px (larger break after the full-width moment). Only two full-width media moments (Expandables, Customization).
**Before production:** celebrity photos are placeholders (several carry Getty Images watermarks) · Expandables™ uses an A.JAFFE campaign still with slow motion until a video exists · confirm "43 stages of craftsmanship" and "100% nickel-free" claims · heritage archive image (`ourstory01.png`) is only 799px wide — a higher-resolution scan would let it run larger.

Switch between versions with the **bottom-left switcher** ("A · Top Nav" / "B · Side Nav").
Toggle the rationale layer with **"Show design notes"** — champagne pins (1–9 + N) open a card explaining *what changed*, *why* (which feedback point / Michael M · Tacori · Tiffany reference), and *asset recommendations*. Notes are **off by default**. The notes card also carries a hidden dev **type-pairing toggle** (1 default / 2 / 3).

## How to run
- Open `ajaffe-home-v1.html` directly in a browser, or drag the folder into **Netlify Drop**. It needs internet access to load the fonts and A.JAFFE media.
- To make it fully offline/portable, download the assets below into a local `/assets/` folder (WebP for images, MP4 + poster for videos) and repoint the URLs. This is the recommended next step before a formal handoff.

## Fonts (Pairing 1 — default)
- **Display / Headings:** FreightDispPro — Light 300 (+ Light Italic) / Medium 500, the same files as ajaffe.com, self-hosted in `fonts/` (licensed A.JAFFE web font; keep it on the brand license in production)
- **Navigation:** FreightDispPro Medium 500, uppercase, letter-spacing .14em
- **Body / UI:** Jost (300 / 400)
- Alt pairings previewable via the dev toggle: **2** Bodoni Moda + Manrope · **3** Playfair Display + Marcellus + Figtree.
- Loaded from Google Fonts with `display=swap` + preconnect.

## Real A.JAFFE assets used (source = ajaffe.com CDN)

| Where | Source URL |
|---|---|
| Logo | `…/static/…/images/ajaffe-bill-logo.svg` |
| Hero slides (4) | `…/media/frontblock/images/n/e/newhomebanner1_1.jpg`, `…/newhomebanner2_2.jpg`, `…/frontblock/images/h/o/homepage_banner_wedding_bands.jpg`, `…/media/images/homebannerweb/f2423273592491e0ea7cc4943b0e046e.jpg` |
| Featured categories | `ajaffe.com/media/images/explore-women.jpg`, `…/explore-ring-img.jpg`, `…/explore-necklaces.jpg`, `ajaffe.com/media/images/explore-men.jpg` |
| Heritage | `…/media/frontblock/images/o/u/our_craftmanship.jpg` |
| Quilts® video | Vimeo `1133785947` (background loop) |
| Signature Shank® video | Vimeo `1133785305` (background loop) |
| Expandables still | `…/media/catalog/product/x/g/xgr3891-8_pl_c.jpg` |
| Collections | Lotus `ajaffe.com/media/catalog/category/AJAFFE_Lotus.jpeg` · Classics `…/our_story.jpg` (stand-in) · Modern Royals `…/Modern-Royals-Mega-Menu-Banners2.jpg` |
| Bespoke | `…/media/images/homebannerweb/c920a2c199a96a6b53ba2298b0826126.jpg` |
| Red carpet (5) | `…/media/mageplaza/blog/post/a/j/ajaffe_celebrity_image_…_may_2025_{carrie_underwood, jennifer_hudson, kerry_washington, mindy_kaling, jasmine_tookes}.jpg` |
| Shape icons | `…/media/images/icons/*.svg` |

CDN host: `https://eadn-wc01-15840335.nxedge.io` (and `https://ajaffe.com` for a few `/media/images` files).

## Asset flags (see in-page design notes for full detail)
- **Expandables** — no clean feature video exists; shown as a still with subtle Ken Burns. *Client video needed:* 10–15s macro clip of the band expanding over a knuckle, warm-white seamless, 1080p+.
- **Classics** — collection tile reuses a heritage image as a stand-in; a dedicated 2:3 warm-white Classics still is recommended.
- **Featured categories** — sources vary slightly in tone; recommend one seamless warm-white (#F4F1EC) reshoot at 3:4, 2400px min, for a perfectly matched flush row.
- **Proof-strip claims** ("43 Stages", "Patented Comfort Engineering", etc.) must be client-verified.

## Standards
Semantic landmarks, one H1, skip link, keyboard-operable nav + mega menu + drawer (focus trap, Esc), hero Pause/Play (WCAG 2.2.2) with `aria-live`, visible focus rings, `prefers-reduced-motion` support (no autoplay/reveals), lazy-loaded below-the-fold imagery, videos autoplay only in viewport (IntersectionObserver). No frameworks, no jQuery.

## V4 — `ajaffe-home-v4.html` (one-gutter layout)

V4 = V3 + a spacing override (`v4.css`, injected by `build4.py` from the built V3 page). Content, order and header/hero/footer are the same as V3.

- The 12px gap between the category tiles is the only spacing: page side margins 12px, and 12px between every section.
- Full-width bands (Expandables™, Customization, Maps by A.JAFFE) are inset 12px, so they read as boxes.
- Quilts® / Signature Shank®: video box and an ivory text panel (#F7F4EF), 12px apart and 12px from the edges.
- The A.JAFFE Promise has a white background, 12px from the edges and 12px above the footer.
- Section titles (Discover, Favorites, Celebrities) keep their own inner space above the title, so text never sits 12px under an image.
- Rebuild: run `build.py` (V3), then `build4.py` (V4).

## V5 — `ajaffe-home-v5.html` (full-screen hero, header over hero)

V5 = V4 + `v5.css` + a small header-state script (injected by `build5.py` from the built V4 page). Everything below the hero is the same as V4.

- Hero: each slide image fills the full width and the whole first screen (100svh); the header sits on top of it.
- Header: same layout, logo, items and placement. The black promotion bar (Find a Retailer · Book a Showing · Our Story · Events) always stays dark. While over the hero, the main bar is transparent with a white logo, menu and icons (a soft top shade keeps them readable). Hover, keyboard focus, an open mega menu, or scrolling past the hero bring back the current ivory main bar.
- Hero copy, link, arrows and play/pause keep the current format, on the left side of the image with no box: white text over a soft dark fade from the left. On phones the copy sits at the bottom in white over a dark fade.
- Rebuild order: `build.py` (V3) → `build4.py` (V4) → `build5.py` (V5).
- Motion layer (V5 only, `v5-motion.css` + `v5-motion.js`, injected by `build5.py`): hero copy staggers in and the title unveils on every slide change; hero images zoom slowly; headings rise ahead of their content; cards rise one after another; large images unveil with a soft wipe; full-width bands (Expandables™, Customization, Maps) have subtle parallax; consistent hover zoom. All switched off for visitors who prefer reduced motion.

## V6 — `ajaffe-home-v6.html`

V6 = the built V5 page + `build6.py`. Only change: A.JAFFE Quilts® and A.JAFFE Signature Shank® sit side by side in one row (two video boxes, 12px apart), with the eyebrow, title, one line and "Discover…" link laid over the bottom-left of each video on a soft dark fade. On phones the two stack. Rebuild order: `build.py` → `build4.py` → `build5.py` → `build6.py`.
