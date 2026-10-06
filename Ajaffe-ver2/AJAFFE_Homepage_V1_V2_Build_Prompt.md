# A.JAFFE Homepage Redesign: Build Prompt (Version A + Version B)

> Copy everything below this line into Claude (or give it to the design/dev team) as the brief.

---

## ROLE

You are a senior luxury e-commerce UI designer and front-end developer. Build **two standalone, self-contained HTML homepage previews** for **A.JAFFE** (ajaffe.com), a New York fine-jewelry house founded in 1892. The two files will be shared with the client for review, so they must look finished and premium. They are not wireframes.

- **Version A**: `ajaffe-home-v1.html`, with a classic top navigation
- **Version B**: `ajaffe-home-v2.html`, with a Tacori-style left-side navigation

Both versions use the **same homepage content, sections and design system**. Only the navigation and the header/layout frame are different, so the client can compare the two navigation approaches directly.

---

## 1. CONTEXT: WHY WE ARE REDOING THIS

The client (Sumay and team) reviewed our first preview. Their feedback, in priority order:

1. **Hero.** They no longer want one video hero. Sumay wants the hero to **rotate frequently between product categories and collections**. The reference is the **Tiffany-style hero, about a 1:2 split**: text on the narrower left third, a wide product image or video on the right two-thirds.
2. **Page rhythm.** **Michael M's grid and layout are the strongest reference.** The page should move between a wide hero, a 2-column section, a 4-column section, a full-width visual, and then back to divided layouts. The rhythm should feel clean, sharp and intentional.
3. **Three feature videos: Quilts®, Signature Shank®, Expandables.** The two wide videos in our first preview did not explain these product features. Each video must clearly tell the customer what the feature is and why it matters. Follow Michael M's presentation style.
4. **Featured Categories.** **Four categories across the full width of the screen**, with images flush left to right and **no borders, gutters or extra spacing**.
5. **Signature Collections.** Remove the hover-to-reveal and auto-rotate concept. Quilts and Signature Shank are already covered by the videos, so this becomes a **three-part visual section: Lotus, Classics, Modern Royals**.
6. **Navigation font.** The current sans-serif isn't working. Use something more distinctive. **A serif in the navigation is acceptable, and preferred** if it looks more refined.
7. **Typography overall.** Refine the font pairing and the size relationships so the hierarchy feels cohesive.
8. **Identity.** Don't make A.JAFFE look like other jewelry sites. Take the strongest ideas from **Michael M, Tacori and Tiffany**, but make the result **custom and distinctive to A.JAFFE**.
9. **Left-side navigation (Tacori)** keeps the top of the desktop page open for imagery and carries over naturally to mobile. This becomes **Version B**.

### Internal direction (from QualDev leadership)

- The client mainly wants a **better luxury look**, plus a few functional improvements. **Do not** redesign their business model or push hard on "shop now" e-commerce patterns.
- **Use A.JAFFE's real imagery and videos** from ajaffe.com. Do not use stock photos or unrelated images. The previous hero image looked "strange" to the client.
- **Do not add busier product cards**, prices or data the client may not have.
- **Never reference B2C/online-only brands** (VRAI, Blue Nile) in copy, notes or comments.
- **Nothing important may be hidden behind hover.** Users miss it, and it fails on touch devices.
- **Every design decision must be explained** (see §8, Review Notes layer).

---

## 2. DELIVERABLES

1. `ajaffe-home-v1.html`: Version A (top navigation)
2. `ajaffe-home-v2.html`: Version B (left-side navigation)
3. `/assets/` folder with the real A.JAFFE images and videos used, optimized as WebP/MP4 plus poster frames
4. A short `README.md` that lists the asset sources (the original ajaffe.com URL for each file), the fonts used, and how to switch versions

Each HTML file contains **all CSS and JS inline**. The only external dependency allowed is Google Fonts. Both files must be ready to drag into Netlify Drop.

Add a **small fixed version switcher** in the bottom-left corner of both files ("Version A · Top Nav" / "Version B · Side Nav") so the client can jump between them. Also add a **"Show design notes"** toggle (see §8).

---

## 3. BRAND ASSETS: USE THE REAL ONES

Pull from the live ajaffe.com site:

- A.JAFFE logo (SVG preferred)
- Current homepage hero banners. Use these for the rotating hero slides.
- Category imagery: Engagement Rings, Wedding Bands, Fine Jewelry, Men's
- Videos or clips for **Quilts®**, **Signature Shank®** and **Expandables**. If a clean Expandables video doesn't exist, use a high-quality still with a subtle Ken Burns motion and label it `[PLACEHOLDER – client video needed]` in the design notes.
- Collection imagery for **Lotus**, **Classics** and **Modern Royals**
- Red-carpet/celebrity imagery that is already on their site

Rules:

- **Do not upscale low-resolution images** or put mismatched backgrounds side by side. Where an asset is weak, still use it, but flag it in the design notes with a specific recommendation. Example: "Reshoot on seamless warm-white (#F4F1EC) background, 3/4 angle, 2400px min."
- Keep **one consistent background tone across product shots** in a row. If sources don't match, sit them on a shared tinted panel.
- Compress to WebP at ~80 quality. Serve 2x sizes with `srcset`/`sizes`.

---

## 4. DESIGN SYSTEM (same for both versions)

### 4.1 Color tokens (CSS custom properties on `:root`)

```css
--color-ink: #141414;          /* primary text, logo */
--color-ivory: #F7F4EF;        /* page background */
--color-porcelain: #FFFFFF;    /* cards, panels */
--color-stone: #E6E0D6;        /* dividers, subtle fills */
--color-taupe: #8C8275;        /* secondary text (check contrast ≥4.5:1 on ivory) */
--color-champagne: #B39A6B;    /* accent: hairlines, small caps labels, focus rings; never body text */
--color-overlay: rgba(20,20,20,.38);
```

The palette stays restrained: mostly ivory, ink and imagery. Champagne is used sparingly. **No jewel-tone blocks.** The luxury feel comes from whitespace, type and photography.

### 4.2 Typography: distinctive and editorial

Build **Pairing 1 as the default**, and add a hidden dev toggle (in the notes panel) to preview Pairings 2 and 3:

| Pairing | Display / Headings | Navigation | Body / UI |
|---|---|---|---|
| **1 (default)** | Cormorant Garamond 300/500 | Cormorant Garamond 500, uppercase, letter-spacing .14em | Jost 300/400 |
| 2 | Bodoni Moda 400 (optical) | Bodoni Moda small caps, .12em | Manrope 300/400 |
| 3 | Playfair Display 400 italic accents | Marcellus, uppercase, .16em | Figtree 300/400 |

**Type scale** (fluid with `clamp()`, ratio ~1.333):

```css
--fs-eyebrow: clamp(.72rem, .68rem + .15vw, .8rem);   /* small caps label, champagne, tracking .2em */
--fs-body:    clamp(.95rem, .9rem + .2vw, 1.05rem);
--fs-lead:    clamp(1.1rem, 1rem + .4vw, 1.3rem);
--fs-h3:      clamp(1.35rem, 1.2rem + .6vw, 1.75rem);
--fs-h2:      clamp(1.9rem, 1.5rem + 1.6vw, 3rem);
--fs-h1:      clamp(2.4rem, 1.8rem + 2.6vw, 4.25rem);
--lh-tight: 1.1; --lh-body: 1.65;
```

Rules: headings in light weights with generous size contrast; eyebrow → heading → one-line lead → text-link CTA. **No all-caps body copy. No more than two typefaces on screen at once.**

### 4.3 Spacing and grid

- 12-column grid, max content width 1440px, side gutters `clamp(16px, 4vw, 64px)`
- Section vertical rhythm: `--space-section: clamp(64px, 9vw, 140px)`
- Full-bleed sections break out of the container to 100vw

### 4.4 Components

- **CTA style:** understated text link with an animated underline ("Discover Quilts →"), or a thin 1px outlined button. **One primary CTA per section at most.**
- **Buttons:** 48px minimum height; ink fill for primary and outline for secondary; no rounded pills (2px radius max).
- **Hairline dividers** in `--color-stone`.

---

## 5. HOMEPAGE SECTIONS (same content in A and B)

Follow the Michael M-style rhythm: **wide → 4-col → 2-col → full-width → 3-col → 2-col → full-width → divided**. Each numbered section below gets a matching `data-note` marker for the design-notes layer.

### 1. Hero: rotating split (Tiffany-inspired, about 1:2)

- **Layout (desktop ≥1024px):** left column 1/3 with text on ivory; right column 2/3 with full-height image or video. Height: `min(88vh, 860px)`.
- **4 slides** rotating every **6s** with a slow crossfade and a subtle image scale of 1.04 → 1:
  1. **Engagement Rings**: eyebrow "Since 1892", headline "Engineered for a Lifetime", CTA "Explore Engagement"
  2. **Quilts® Collection**: headline "The Art of the Quilt", CTA "Discover Quilts"
  3. **Wedding Bands**: headline "Bands Made to Be Worn Every Day", CTA "View Wedding Bands"
  4. **Fine Jewelry / Seasonal**: headline editable, CTA "Shop Fine Jewelry"

  (Headlines are placeholder copy for client approval. Every slide must have a **different** headline.)
- **Controls:** numbered progress indicators (01 / 02 / 03 / 04) with a thin progress bar, prev/next arrows, and a **visible Pause/Play button** (WCAG 2.2.2). Pause on hover and on keyboard focus. Support swipe on touch.
- **Mobile (<768px):** image on top (4:5 ratio), text block below. Do not overlay text on the image.
- Each slide's image comes from the **real ajaffe.com hero banners and category imagery**.
- `prefers-reduced-motion`: no autoplay, no crossfade scale. Show slide 1 with manual controls.

### 2. Featured Categories: 4-up, full-bleed, flush

- 4 tiles, **100vw wide, zero gap, no borders**, portrait ratio 3:4
- Engagement Rings · Wedding Bands · Fine Jewelry · Men's
- Label sits at the bottom-left of each tile over a soft gradient (serif, white, `--fs-h3`) with a small "Explore →" link
- Hover (desktop only, as enhancement): image scales to 1.03 over 900ms. **The label is always visible, never hover-only.**
- Tablet: 2×2 grid, still flush. Mobile: 2×2 flush, or a horizontal scroll-snap row with a visible peek of the next tile.

### 3. Heritage statement: 2-column

- Left: an atelier or craftsmanship image from ajaffe.com. Right: eyebrow "New York · Since 1892", H2 "Four Generations of Uncompromising Craft", a 2–3 line lead, and a text link "Our Story".
- Below: an **inline proof strip** of 4 small-caps facts separated by hairlines. Content: "Est. 1892 New York · 43 Stages of Craftsmanship · Patented Comfort Engineering · Lifetime Care". The client must verify the exact claims; flag this in the notes.

### 4. Feature videos: Quilts®, Signature Shank®, Expandables

This section must **explain the features clearly**, which was the client's main complaint about the first preview.

- **Layout (Michael M rhythm):**
  - Row 1: **Quilts®** as a full-width video (21:9), with a text panel overlapping the lower-left corner on an ivory card
  - Row 2: **Signature Shank®** and **Expandables** in a 2-column split (each 4:5 video)
- **Each video block contains:**
  - Eyebrow: "Signature Innovation"
  - Name: "Quilts®" / "Signature Shank®" / "Expandables"
  - **One-sentence "what it is"**. Example: "A patented shank that curves to the natural shape of the finger, so the ring sits upright and never spins."
  - **One-sentence "why it matters"**, framed as a customer benefit
  - CTA: "See How It Works →"
- Videos: `muted`, `playsinline`, `loop`, `preload="none"`, poster image, and autoplay **only when in the viewport** (IntersectionObserver), pausing when out of view. Include a visible play/pause toggle on each video.
- Reduced motion: show the poster only, with a play button.
- **Visible separation** between videos: `--space-section / 2` spacing and consistent alignment. No two videos stacked edge to edge.

### 5. Signature Collections: 3-part visual

- Heading: "Signature Collections", followed by a 1-line intro
- **3 equal columns, all visible at once:** **Lotus · Classics · Modern Royals**
- Each column: a tall image (2:3), the collection name in serif, a 1-line description, and a "Discover →" link
- **No hover-to-reveal and no auto-rotate.** Everything is visible by default.
- Mobile: stacked, or a horizontal scroll-snap row with the next card peeking

### 6. Full-width visual: Customize / Bespoke

- Full-bleed editorial image (16:7 desktop, 4:5 mobile) with centered or left-aligned copy: eyebrow "Bespoke", H2 "Designed with You, Made by Hand", CTA "Begin Your Design"
- Light overlay only as strong as needed for 4.5:1 text contrast

### 7. Red Carpet: curated 2-column

- Left: one large hero celebrity image. Right: a 2×2 grid of 4 more.
- Each image has a caption: *who* + *what they're wearing* (e.g. "Worn by ___ · Quilts® Diamond Band")
- 5 images total, curated. No endless carousel.
- CTA: "View the Red Carpet Gallery →"

### 8. See It in Person: divided section

- 2-column split. Left: **Find a Retailer**, with a zip/city input and "Search" button. Right: **Book a Complimentary Showing**, with a single CTA button.
- This is the brand's main conversion goal (retail partners). Keep it elegant, not salesy.

### 9. Newsletter + Footer

- Slim newsletter row ("Join the A.JAFFE World"), email field with a visible label
- Footer on ink background with 4 link columns, social icons (with accessible names), and the legal row

---

## 6. NAVIGATION: THE ONLY DIFFERENCE BETWEEN A AND B

### Version A: refined top navigation (`ajaffe-home-v1.html`)

- **Structure:** a thin utility bar (Find a Retailer · Book a Showing · account/search/wishlist icons), then a main bar with the **centered logo** and primary links split left/right:
  `Engagement · Wedding Bands · Fine Jewelry` | LOGO | `Collections · Bespoke · Our Story`
- **Nav font:** the serif from the active pairing, uppercase, letter-spacing .14em, 13–14px
- **Transparent over the hero** only if the hero image allows contrast. Otherwise ivory. It turns solid ivory with a hairline after 80px of scroll. It hides on scroll down and reveals on scroll up.
- **Mega menu:** a full-width ivory panel opening on **click and keyboard** (hover-intent is an enhancement), 4 columns:
  - *Engagement:* Shop by Shape (icons: Round, Oval, Cushion, Emerald, Princess, Pear, Radiant, Marquise) · Shop by Style (Solitaire, Halo, Three-Stone, Vintage, Pavé) · Shop by Collection (Quilts®, Signature Shank®, Lotus, Classics, Modern Royals) · a feature image tile
  - Other menus use the same pattern with their own content
- **Mobile:** hamburger button → full-height drawer with accordion sections, a focus trap, and Esc to close

### Version B: Tacori-style left-side navigation (`ajaffe-home-v2.html`)

- **Desktop (≥1200px):** a **fixed left rail 260px wide**, ivory, with a hairline right border:
  - Top: A.JAFFE logo
  - Middle: primary categories stacked vertically in the serif nav font, 18px spacing (Engagement, Wedding Bands, Fine Jewelry, Collections, Bespoke, Red Carpet, Our Story)
  - Bottom: Find a Retailer, Book a Showing, and search/account/wishlist icons
  - Clicking a category slides out a **flyout panel** (about 380px) to the right of the rail over the content, with the subcategories (same shape/style/collection structure as Version A) and one feature image. Close with Esc, a click outside, or a close button.
- **The top of the page is fully open.** The hero starts at `top: 0` in the content area to the right of the rail, which gives imagery the maximum room. **This is the main selling point of Version B, so call it out in the notes.**
- All full-bleed sections span the **content area** (100vw − rail), not the whole window.
- **Tablet (768–1199px):** the rail collapses to a 72px icon strip (logo mark + menu button + search). The menu button opens the full rail as an overlay.
- **Mobile (<768px):** a slim top bar (logo + menu + search). The menu opens a **left drawer that reuses the exact same rail structure**. This is the "natural mobile transition" the client mentioned.
- Rail and flyout: `nav` landmark, `aria-expanded` on triggers, focus moves into the flyout, focus returns to the trigger on close.

---

## 7. TECHNICAL AND ACCESSIBILITY STANDARDS (non-negotiable)

- **Responsive:** test and look polished at **375px, 768px, 1280px** (plus 1440px for Version B's rail). No horizontal scroll at any width.
- **WCAG 2.1 AA:** semantic landmarks (`header`, `nav`, `main`, `footer`); one H1 (the active hero headline, or a visually hidden brand H1); skip-to-content link; contrast ≥4.5:1 for text and ≥3:1 for UI; visible focus rings (2px champagne outline + 2px offset); all interactive items keyboard-operable; 44×44px minimum touch targets; descriptive `alt` text for every product image; `aria-live="polite"` on the hero slide status; pause controls on all moving content.
- **Performance:** `loading="lazy"` and `decoding="async"` on all below-the-fold images; the first hero image eager with `fetchpriority="high"`; WebP with `srcset`; `preload="none"` + posters on videos; JS inline at the end of body or `defer`; fonts with `display=swap` and preconnect.
- **CSS:** all design tokens as custom properties; **BEM class naming** (`.hero__slide--active`, `.category-grid__tile`, `.side-nav__flyout`).
- **Animation:** scroll reveals via **IntersectionObserver** (opacity 0→1 + translateY(24px)→0, 700ms, cubic-bezier(.2,.7,.2,1), staggered 80ms). **All animation is wrapped in `@media (prefers-reduced-motion: no-preference)`.**
- No frameworks, no jQuery.

---

## 8. DESIGN NOTES LAYER (explain every decision)

Leadership's biggest criticism was that **we suggest things without explaining them**. Add a **"Show design notes"** toggle (bottom-left, next to the version switcher). When it's on:

- Numbered champagne pins appear on each section (1–9, plus "N" for navigation).
- Clicking a pin opens a small side card with:
  - **What changed** from the current ajaffe.com
  - **Why**: which client feedback point it answers, or which reference inspired it (Michael M / Tacori / Tiffany only)
  - **Asset note** where relevant, e.g. "Current Expandables video is low-res. Recommend a 10–15s macro clip showing the band expanding, shot on warm-white seamless."
- Notes are **off by default**, so the design is judged clean first.

Include a notes entry covering **photography and image recommendations** for the client: consistent backgrounds, live-model vs. product-shot ratio, minimum resolution, and video length and format. This was promised but missing last time.

---

## 9. DO NOT

- Do not use stock or unrelated imagery, or an invented hero image
- Do not hide content behind hover, or rely on auto-rotation to reveal key content (except the hero, which has controls)
- Do not add prices, swatches, badges or extra data to product displays
- Do not mention or visually imitate VRAI or Blue Nile
- Do not copy any competitor's layout pixel for pixel. Take the principle, make it A.JAFFE's own.
- Do not use more than one primary CTA per section
- Do not use generic "One of a Kind Craftsmanship" repeated across slides

---

## 10. ACCEPTANCE CHECKLIST (verify before sharing)

- [ ] Both files open offline, drag into Netlify Drop, and switch to each other via the switcher
- [ ] Hero rotates through 4 **different** category/collection slides with a working Pause
- [ ] Featured Categories: 4 tiles, flush, full width, no gaps
- [ ] 3 feature videos (Quilts®, Signature Shank®, Expandables), each with a "what it is" and a "why it matters" line, and visible spacing between them
- [ ] Signature Collections shows Lotus, Classics and Modern Royals, all visible without hover
- [ ] Section rhythm alternates wide / 4-col / 2-col / full-width / 3-col / 2-col
- [ ] Serif navigation, refined type scale, max 2 typefaces visible
- [ ] Version B: top of the page open, left rail + flyout on desktop, same structure in the mobile drawer
- [ ] Checked at 375 / 768 / 1280 (and 1440 for Version B)
- [ ] Keyboard-only walkthrough passes; Lighthouse Accessibility ≥ 95
- [ ] Reduced-motion mode: no autoplay, no reveals
- [ ] Design notes toggle works and every section has a rationale + asset note
- [ ] Only real A.JAFFE assets; weak assets flagged with specific reshoot guidance
