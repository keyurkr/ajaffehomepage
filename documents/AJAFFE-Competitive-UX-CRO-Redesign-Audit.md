# A.JAFFE — Luxury eCommerce Competitive UX, CRO & Redesign Audit

**Prepared by:** QualDev — UX / CRO / Digital Strategy

**Client:** A.JAFFE (ajaffe.com)

**Version:** 1.0 — 9 September 2026

**Reference set:** Gabriel & Co. · Michael M · Tacori · VRAI · Verragio · Blue Nile

---

## 0. How to read this document

Every observation in this audit is tagged so the client can see exactly what was seen on a live site and what is professional judgement:

| Tag | Meaning |
|---|---|
| **[VERIFIED]** | Directly observed on the live website during this audit (September 2026). |
| **[INTERPRETATION]** | Our UX / CRO reading of a verified observation. |
| **[RECOMMENDATION]** | What A.JAFFE should change. |
| **[EXPECTED BENEFIT]** | Why we expect the change to help. Never a guaranteed result. |
| **Not verified** | A page or feature we could not access or render during this audit. We do not guess about it. |

We inspected the following surfaces on ajaffe.com: homepage, header/mega menu, Engagement Rings PLP (all + filters + sort), Wedding Bands PLP, one Engagement Ring PDP, the "Schedule a Showing" page, footer, and the SEO/meta layer of each page. On the reference sites we inspected homepages, mega menus, engagement PLPs and PDPs where they rendered server-side. Verragio's homepage, PLP and PDP blocked automated access (HTTP 429) and are marked **Not verified** throughout; only its retailer-locations page and footer architecture were observed.

No conversion data, traffic, analytics, revenue or customer-complaint data is used anywhere in this document. None was available and none has been invented.

---

## 1. Executive summary

A.JAFFE has three assets that none of the six reference brands can copy: a **130-year New York heritage (1892)**, a set of **patented comfort engineering features** (Quilts® interior, Signature Shank®, Expandables™/Flex Fit™) that solve a real, universal ring problem — spinning and poor fit — and a **celebrity/red-carpet proof point** with 38 named wearers on the homepage alone.

The current website does not convert those assets into a premium *shopping* experience. It presents them as brand copy, but the product discovery layer — navigation, category pages, product grid, filters, product page — is structurally behind Gabriel & Co., Tacori and Michael M in ways that directly affect whether a shopper finds a ring she loves and then contacts a retailer.

The ten most consequential findings:

1. **[VERIFIED] No "shop by shape" anywhere in navigation.** Diamond shape is the first decision most engagement shoppers make. Gabriel & Co., VRAI and Blue Nile lead with it; A.JAFFE only exposes shape as a PLP filter ("Center Stone Cut") that a shopper has to discover after landing.
2. **[VERIFIED] The homepage hero says the same thing three times.** All three carousel slides carry the headline "One Of A Kind Craftsmanship" (one H1, two H2s). There is no campaign, no product, no season, no reason to scroll.
3. **[VERIFIED] The homepage has no product discovery section.** After the hero the page is: Quilts® story → Signature Shank® story → 38-celebrity carousel → customization video → heritage → "Connect to a Retailer" → promise icons → newsletter. There is no shop-by-category, shop-by-shape, collection grid or product carousel. Every reference site has at least two of these above the storytelling.
4. **[VERIFIED] Product cards show no price and no save/wishlist.** Cards show style number, name, collection label, four metal swatches and three text links. Gabriel & Co., Tacori, Michael M, VRAI and Blue Nile all show price (or "starting at"); all except Michael M show a wishlist control on the card.
5. **[VERIFIED] The PDP has no price, no metal/shape selector, no breadcrumb and a truncated description.** The metal options are a text line ("Available in: Platinum | White Gold | Yellow Gold | Rose Gold"), the description ends mid-sentence ("…also includes our i"), and the only pricing line contains a typo ("Please contact an authorized retailer other pricing and financing options"). Tacori's equivalent PDP shows a setting price with a "does not include center stone" note, shape/metal/purity selectors and an appointment CTA pre-filled with the product.
6. **[VERIFIED] Filter taxonomy is inconsistent and duplicated.** The Engagement PLP "Collections" filter lists Quilts®, A.JAFFE Quilts®, Iconic Quilts® and Petite Quilts® as four separate values. The Wedding Band PLP lists "Diamond Band" and "Diamond Bands", "Stackable Rings" and "Stacking Rings". Price buckets skip a range on both pages ($15–20k missing on engagement; $10–15k missing on bands).
7. **[VERIFIED] The appointment journey is a generic lead form.** The page is titled "Consumer Leads - A.JAFFE" in the browser tab, asks 9 fields, offers no retailer selection, no date/time and no product context. Tacori passes the product into the appointment URL; Gabriel & Co. pairs "Book viewing" with "Locate a store" directly on the PLP.
8. **[VERIFIED] Pinch-zoom is disabled site-wide** (`user-scalable=0, maximum-scale=1` in the viewport meta on every page). This is a WCAG 2.1 AA failure (1.4.4 Resize Text) and a real usability problem on a site whose product is small and detailed.
9. **[VERIFIED] Trust and craftsmanship content is strong but buried.** The "Learn More" block on the PDP (43 stages of workmanship, RJC and JVC certification, nickel-free, lifetime service, lifetime upgrade) is some of the best proof content in the reference set — and it sits below two lead forms, below the fold, as a wall of bold paragraphs.
10. **[VERIFIED] Mega-menu content and collection taxonomy don't match.** The engagement mega menu links five collections but carries descriptive blurbs for eleven (Classics, Art Deco, Season of Love, Metropolitan, Modern Royals™, Iconic Quilt®, etc.), several of which are not reachable as filters or menu links.

The recommended direction is not "become Gabriel" or "become Tacori". It is: **use Gabriel's discovery architecture, Tacori's product-page decision support and Michael M's brand-house confidence to sell A.JAFFE's unique story — engineered comfort, patented design, 1892 New York — through a retailer-first conversion model.**

---

## 2. Understanding the brand before comparing it

### 2.1 Positioning (from verified site content)

| Dimension | What the site says / shows [VERIFIED] |
|---|---|
| Heritage | Founded New York, 1892; "one of New York City's few remaining 19th-century jewelers"; 130+ years. |
| Craft claim | Every ring passes through "43 meticulous stages of workmanship"; hand-finished by master artisans; "3x the time and precision compared to an average ring". |
| Patented / signature features | Quilts® interior (patented, 19th-century American quilt motif); Signature Shank® (square base, prevents spinning, keeps center diamond upright); Expandables™ / Flex Fit™ / Flex Band™ (expandable bands); A.JAFFE Lotus™; Always by A.JAFFE (A-shaped profile); Gray Gold™; Morse Code bands; Maps by A.JAFFE. |
| Materials & ethics | Natural diamonds only ("rare natural diamonds"); 100% nickel-safe / hypoallergenic (zero nickel, mercury, lead, cadmium); Responsible Jewelry Council certified; Jewelers Vigilance Committee certified; conflict-free. |
| Service | Lifetime service; A.JAFFE Lifetime Upgrade; lifetime warranty; customization ("Design the Ring You've Always Imagined"). |
| Social proof | 38 named celebrities on the homepage carousel; a 25-image "A.JAFFE on the Red Carpet" carousel on every PDP with event captions (Taylor Swift, Sydney Sweeney, Kendall Jenner, Jodie Foster, etc.). |
| Sales model | Retailer-led. PDP says "Please contact an authorized retailer… pricing and financing options." No price, no add-to-cart on rings. Only Maps by A.JAFFE appears to be sold direct (footer: "Track Order (Maps Only)"). A cart icon and account are present in the header. |
| Catalog scale | 388 engagement rings; 378 wedding bands (page counts on PLPs). Fine jewelry and Maps categories exist. |
| Price positioning | PLP price filters run $0–$25,000 (setting price). No prices displayed. Meta layer exposes `product:price:amount 1000` — a placeholder value. |

### 2.2 Customer purchase journey (as the site currently supports it)

Discover (search / social / celebrity) → homepage → mega menu → PLP (388 items, 19 per page) → PDP → **either** "Find the nearest store" (zip form) **or** "Schedule a Showing" (9-field form) → retailer → in-store purchase.

Major conversion actions, in order of business value: (1) appointment / showing request; (2) retailer locator use; (3) product inquiry / "Personalize This Ring"; (4) newsletter; (5) Drop-a-Hint; (6) Maps purchase.

### 2.3 What customers need to know before they will contact a retailer

- Does A.JAFFE make the shape and style I want? (Shape is currently invisible in navigation.)
- Roughly what will it cost? (No price anywhere; a shopper cannot self-qualify.)
- What is different about an A.JAFFE ring versus the same silhouette elsewhere? (The answer — comfort engineering, 43 stages, nickel-free — exists but is presented as brand copy, not product-level proof.)
- Which retailer near me has it, and can I see this specific ring? (Locator and appointment are disconnected from the product.)
- Will it match a wedding band? (A "View Matching Wedding Band" link exists on the PDP — a genuine strength — but is a single text link above the title, not a merchandised pairing module.)

### 2.4 The answer to "why choose A.JAFFE over the reference brands"

> **A.JAFFE is the only house in this set whose signature is engineering, not just ornament.** Quilts®, Signature Shank® and Expandables™ solve the two complaints every ring owner has — spinning and fit — and they have been doing it in New York since 1892, with every ring passing through 43 hand-finished stages and zero nickel. Gabriel sells choice, Tacori sells the crescent, VRAI sells the diamond's origin, Michael M sells the "house". A.JAFFE can own **"the ring that fits like it was made for you — because it was."**

That sentence is the foundation of every recommendation that follows. If a proposed change does not make that story easier to discover, evaluate or act on, it is excluded.

## 3. Competitive experience analysis — site by site

Each site is assessed on the eight lenses from the brief (brand/luxury, navigation/IA, homepage, category landing, PLP, PDP, CRO, mobile). Where a surface could not be rendered it is marked Not verified.

### 3.1 Gabriel & Co. — reference for category organisation and product discovery

**Platform [VERIFIED]:** Magento 2 with a Hyvä-based theme (same stack family as ajaffe.com — relevant because every pattern below is technically achievable on A.JAFFE's current platform).

**A. Brand / luxury experience [VERIFIED]:** Campaign-led hero ("Jessica Alba in Iconic Bujukan®"), a five-item trust strip directly under the hero (Most Awarded Brand · GIA Verified · Recycled Gold Initiative · Unique Serial Number · Since 1989), then editorial edits (Silver Edit, Men's Edit). Perceived level: **accessible-premium** — polished but volume-oriented; price bands in the Gifts menu start "Under $500".

**B. Navigation / IA [VERIFIED]:** Seven primary items (Jewelry, Bujukan®, Engagement Rings, Wedding Rings, Men's, Gifts, About Us) plus utility row (Login, Wishlist, Find a Store, Contact). The Engagement mega menu is the strongest in the set: **Shop by Shape** (9, with shape icons) · **Shop by Style** (11) · **Shop by Metal** (5) · **Premium Collections** (6) · **Featured** (4) · **Knowledge** (Engagement Ring Guide, How to Choose a Diamond, Clarity Chart, Shop Confidently®) · a promo tile ("Discover Your Bridal Style — Take the quiz") · a persistent "Chat with an expert" prompt inside every panel.

**C. Homepage [VERIFIED]:** Hero → trust strip → 5 category icons → campaign story → "Celebrate Forever" with two CTAs (Shop Wedding Rings / Shop Engagement Rings) → Silver Edit → Men's Edit → Store locator + Foundation tiles → Our Story → footer with phone, email, Live Chat, Book Appointment, Find a Store. Appointment is a 7-field modal with reCAPTCHA.

**D. Category landing / PLP [VERIFIED]:** Breadcrumb → hero image + H1 + intro → embedded "Find Partner Stores" widget with "Use my location" → **Shop Rings by Diamond Shape** row → result count ("Showing 4,315 Engagement Rings") → sort (New Arrivals, Best Sellers, Recommended, Price ↑↓) → a one-line disclosure "Price includes setting only, center stone not included" → grid. Below the grid: "View Your Ring In-Store" (Book viewing / Locate a store) → Engagement Ring Collections → blog cards → Chat with an Expert → 8-question FAQ accordion → long-form SEO copy with internal links → "Browse by category" link clusters.

**E. Product cards [VERIFIED]:** Wishlist heart · 4–6 images per card · shape-variant icons on the card (Round / Oval / Marquise "+1") · "4 Metals" indicator · model name + descriptive title ("Reena – 14K Yellow Gold Round Diamond Engagement Ring") · price ($2,025) · "New Arrival" badge.

**Weakness to NOT copy [VERIFIED]:** the filter drawer on the engagement PLP exposes 40+ facets including Earring Closure Type, Enamel Color, Alphabet, Necklace Length and Manufacturer — clearly a global attribute set leaking into a bridal category. This is noise, not choice.

**F. PDP:** Not verified in this audit.

**G. CRO [INTERPRETATION]:** Gabriel's conversion architecture is layered micro-conversions: wishlist on every card, quiz, chat, book viewing, locate a store, appointment modal, email. It never asks the shopper to leave the product context to convert.

**H. Mobile [VERIFIED, from markup]:** Mobile-specific hero assets (`-Mobile` AVIF variants), a "Use My Location" store finder, and the same shape row on mobile PLP. Filter drawer behaviour: Not verified (JS).

### 3.2 Michael M — reference for premium / luxury brand perception

**Platform [VERIFIED]:** Shopify.

**A. Brand / luxury experience [VERIFIED]:** The brand is written as a *house* — "The House of Modern Monarchs", "A Year Worth Celebrating Begins at the House of Modern Monarchs", "The Excellent Deserve Excellence", "Modern Monarchs on the Red Carpet" (with the specific piece named under each celebrity: "Anok Yai — Europa Bypass Ring"). Prices are shown everywhere, including high jewelry at $29,000–$54,880, which itself signals tier. Perceived level: **luxury / high jewelry**.

**B. Navigation / IA [VERIFIED]:** Jewelry · Engagement & Wedding · Men's · Bespoke · The House · Store Locator · The MM World. Engagement panel: Shop by Occasion (All Bridal, New Arrivals, Engagement Rings, Wedding Bands, **Perfect Pairings**, Men's Bands, His & Hers) · Shop by Collection (10 named collections) · Shop by Style (Not-So-Hidden Halo™, Hidden Halo, Halo, Solitaire, Three Stone, Eternity) · **Craft Your Own** · **Shop Complete Rings**. Predictive search surfaces "Popular products" with prices before a query is typed.

**C. Homepage [VERIFIED]:** Campaign hero → "A Perfect Pair / Complete the Look" → New Arrivals product rail with quick-add and prices → "Enter the House" → "Introducing Our Complete Michael M Engagement Rings" → Shop by Category (Bracelets / Earrings / Necklaces / Rings with product rails) → brand manifesto → "Shop the look" → engagement statement → **Book A Private Consultation** → 25 Years of Excellence → Red Carpet.

**E. PLP / cards [VERIFIED via rendered collection pages]:** Cards show multiple metal renders per style, "From $8,820" pricing, and — on engagement collections — a "Locate a retailer" link on the card. This is the clearest example in the set of a **hybrid DTC + retailer** presentation: price shown, purchase routed to retailer.

**Trust / service [VERIFIED]:** Trade-Up Policy (credit up to 75% of original purchase), Register Your Jewelry, Care & Repair, Size Guide.

**F. PDP:** Not verified. **H. Mobile:** Not verified beyond a mobile menu structure identical to desktop.

**G. CRO [INTERPRETATION]:** Michael M's conversion strength is *confidence*: names its trademarked styles, shows prices at every tier, and gives the shopper one premium action ("Book A Private Consultation"). The brand voice does the work Gabriel does with UI density.

### 3.3 Tacori — reference for premium storytelling and presentation

**Platform [VERIFIED]:** Headless (Next.js + Sanity CMS front end, Shopify product data).

**A. Brand / luxury experience [VERIFIED]:** The homepage hero is a *story*, not a product: "The Nervous Suitor — Flowers ready. Ring safely hidden. At least, that was the plan. → Explore the Campaign." Three category tiles each carry one sentence of copy. Photography alt text is written editorially ("angled three-quarter view", "inner face"). Perceived level: **luxury**; the page is short, quiet and confident.

**B. Navigation / IA [VERIFIED]:** Header carries only Concierge · Find a Boutique · Book an Appointment · Search; the shop menu renders client-side (mega-menu contents: Not verified). Footer: The Tacori Story, **The Tacori Crescent** (a dedicated page for the signature design element), Boutiques, Authenticity Registration, Promise of Service, Hand Engraving, Customization, Sourcing & Supply Chain, RJC Internal Audit (PDF).

**E. PLP / cards [VERIFIED]:** Each card: collection eyebrow ("Founder's Collection", "Sculpted Crescent", "Simply TACORI", "Petite Crescent", "Reverie") · descriptive name ("Cushion Wide Band Solitaire Engagement Ring") · "Shown in Yellow Gold" · "starting at $3,590". "View More Designs" load-more. Filters: Not verified (JS-rendered).

**F. PDP [VERIFIED — Oval Solitaire Engagement Ring, HT2580OV]:**

- Gallery: three views with descriptive alt (three-quarter, alternate, inner face).
- Collection eyebrow → H1 → metal line → **"$3,590 *does not include center stone"**.
- Selectors: Shape (Oval / Emerald / Princess / Pear / Round) · Metal (White Gold / Platinum / Yellow / Rose) · Metal Purity (14K / 18K).
- Two CTAs: **Book an Appointment** (URL carries `?product=…`) and **Customize Your Ring**.
- Description uses house vocabulary ("Founder's Signature Crescent at the resting point", "hidden bloom beneath the crown").
- "Additional Style Details": Style, Carat Weight, Crown, Foundation; one line of expectation-setting: "All engagement rings will be crafted and engineered for your center stone."
- Hand Engraving availability note.
- **Recommended Pairings For Her** — matching wedding bands, each link carrying `?metal=14kt-white-gold` so the band opens in the same metal as the ring.
- Related Designs (same style, other shapes) · Gents Bands.

**G. CRO [INTERPRETATION]:** Tacori converts by removing doubt: a price with a clear exclusion note, a product-aware appointment link, and a matching-band module in the selected metal. The shopper arrives at the retailer already decided.

**H. Mobile:** Not verified beyond responsive image `width` parameters.

### 3.4 VRAI — reference for guided discovery (lab-grown DTC, different model)

**A. Brand [VERIFIED]:** Six-item nav (Engagement · Wedding · Diamonds · Jewelry · Gifts · Showrooms). Tone is technical-minimal; trust is built on origin ("first certified true zero-emission diamond producer", "We certify, don't just report GIA grades", "We 100% guarantee the diamond value"). Perceived level: **modern premium**.

**B. Navigation [VERIFIED]:** Engagement panel opens with a **"Begin exploring"** column: Start with a setting · Start with a VRAI created diamond · Speak with a diamond expert · Bespoke · **Ready-to-ship** · Find your ring size · How to buy an engagement ring · Journal. Then By style (10) and By shape (10 + "All 31 shapes"). Showrooms listed by city plus "Virtual appointment".

**C. Homepage [VERIFIED]:** Feature launch ("Tennis Bar") → engagement banner → three proof tiles (Unmatched origin / VRAI created diamonds / Master cutters) → Sought-after styles → **Spotted in VRAI** (Taylor Swift, Emma Watson, Emma Stone, Jennifer Lopez) → world map of showrooms.

**PLP / PDP:** Not verified (client-rendered).

**Relevance [INTERPRETATION]:** VRAI's model (make-to-order lab-grown, DTC) is not A.JAFFE's. The transferable principles are the "Begin exploring" entry column, the ready-to-ship signal, and showroom-plus-virtual appointment routing.

### 3.5 Verragio — Not verified (homepage, PLP, PDP)

verragio.com returned HTTP 429 to automated access on its homepage and catalog pages. **[VERIFIED]** on its Locations page and footer only: state- and country-level retailer location pages (US states, Canadian provinces, London) with breadcrumbs — a strong local-SEO pattern for a retailer-led brand; footer items **Concierge**, Store Locator, Warranty Info, FAQ, Events, Design Philosophy, **Verragio D.N.A**, **Fit Right**, Accessibility statement ("ADA Compliant (WCAG 2.0 AA)"). Third-party retailer listings describe collections (Couture, Insignia, Parisian, Renaissance, Venetian, Tradition) and a "Lumino" setting — **not verified on verragio.com** and used here only to note that Verragio, like A.JAFFE, organises bridal by named collection and by a signature construction feature ("Fit Right").

### 3.6 Blue Nile — reference for funnel mechanics (mass DTC; not a luxury benchmark)

**A. Brand [VERIFIED]:** Promotional (three rotating "Up to 40% Off*" banners, phone number in header, "Today's Deals", "Clear the Vault"). Perceived level: **mass / value**. This is the brand tone A.JAFFE should explicitly *not* adopt.

**B. Navigation [VERIFIED]:** Engagement panel: **Design Your Own Ring** (Start With A Setting / Start With A Diamond / Start With A Gemstone / Creative Studio) · Shop by Shape (10 icons) · Shop by Style (7) · Education (Engagement Ring Guide) · Shop All · Best Selling · Designer · **Ready to Ship — NEW** · **Find Your Ring Size**. Every category panel has an Education link. Header: Stores, **Virtual Appointment**, wishlist, currency selector.

**C. Homepage [VERIFIED]:** Promo hero → 8 category tiles → sale blocks → diamond shapes → collections → "Visit us in store" → "Only at Blue Nile" (4 proof tiles) → customer reviews rail → services footer (Price Match, Diamond Upgrade Program, Lifetime Warranty, Insurance, Protection Plans).

**Transferable [INTERPRETATION]:** ready-to-ship signal, ring-size finder, education inside the menu, virtual appointment as a header action, and the reviews rail — each delivered without the promotional tone.

---

## 4. Competitor matrix

Rating scale: **Strong / Good / Average / Weak / Not Verified.** Ratings are relative to what a luxury bridal shopper needs, not to each brand's own business model. No numeric scores are used.

| Area | A.JAFFE (current) | Gabriel & Co. | Michael M | Tacori | VRAI | Verragio | Blue Nile | Opportunity for A.JAFFE |
|---|---|---|---|---|---|---|---|---|
| Luxury perception | Average | Good | Strong | Strong | Good | Not Verified | Weak | Move from "craft copy" to "house" presentation with campaign hero, restraint and vocabulary. |
| Navigation clarity | Average | Strong | Good | Good (utility-first) | Strong | Not Verified | Good | Reduce 9 top-level items; add shape, metal, price entry points. |
| Category depth / IA | Average | Strong | Good | Not Verified | Good | Not Verified | Strong | Fix collection taxonomy; add shape × style × collection cross-navigation. |
| Product discovery | Weak | Strong | Good | Good | Strong | Not Verified | Strong | Shape row on PLP, quiz/finder, ready-to-ship, best sellers. |
| Homepage hierarchy | Weak | Good | Strong | Strong | Good | Not Verified | Average | Replace repeated hero + story stack with discovery-first, story-second layout. |
| PLP | Average | Strong | Good | Good | Not Verified | Not Verified | Good | Result count, price/"from", wishlist, hover image, sticky filter bar. |
| Filters | Weak (duplicates, gaps) | Average (over-faceted) | Not Verified | Not Verified | Not Verified | Not Verified | Good | Clean, intent-based taxonomy of 7–8 facets. |
| Product cards | Weak | Strong | Good | Good | Not Verified | Not Verified | Good | Price, wishlist, alt image, shape availability, badge. |
| PDP | Weak | Not Verified | Not Verified | Strong | Not Verified | Not Verified | Not Verified | Selectors, price framing, product-aware appointment, pairing module. |
| Storytelling | Good (content) / Weak (delivery) | Good | Strong | Strong | Good | Not Verified | Weak | Keep the content; re-sequence and design it. |
| Trust signals | Good (content) / Weak (placement) | Strong | Good | Strong | Strong | Not Verified | Good | Trust strip under hero; certification block on PDP above the fold. |
| Personalization / customization | Good (offer) / Average (UX) | Good | Strong | Strong | Strong | Not Verified | Strong | Make "Personalize This Ring" a product-aware flow, not a generic form. |
| Store / appointment journey | Weak | Strong | Good | Strong | Strong | Good (location SEO) | Good | Product-aware, retailer-selectable, date-aware appointment. |
| Wishlist / save | Missing | Strong | Not Verified | Not Verified | Not Verified | Not Verified | Good | Add account-optional wishlist + share-with-retailer. |
| Mobile UX | Weak (zoom disabled) | Good | Not Verified | Not Verified | Not Verified | Not Verified | Good | Re-enable zoom; sticky mobile CTA; filter drawer. |
| CRO architecture | Weak | Strong | Good | Strong | Good | Not Verified | Good | Layered micro-conversions inside product context. |
| SEO / content discovery | Average | Strong | Average | Average | Good | Good (locations) | Good | Shape/style/collection landing pages; FAQ schema; location pages. |

**The important differences, in plain terms:**

- **Gabriel wins on *finding*.** Shape-first, style, metal, collection and knowledge all in one panel; the PLP tells you how many rings there are, what the price includes, and lets you save one without leaving.
- **Tacori wins on *deciding*.** One product page answers price, options, pairing and "what happens next" without a single form.
- **Michael M wins on *believing*.** The brand is written as a house with named icons and visible prices, so a shopper trusts the tier before she sees a ring.
- **A.JAFFE currently wins on *proof* — and hides it.** 43 stages, RJC + JVC, nickel-free, patented comfort, lifetime upgrade, 38 celebrities. No reference site has a stronger raw proof set, and none presents it worse.

---

## 5. Competitive gap analysis

### 5.1 What the current site already does well [VERIFIED]

- Icon-led "View by Setting" and wedding-band style menus (13 women's styles, 8 men's) — a genuinely useful visual taxonomy that several competitors lack.
- "View Matching Wedding Band" link on the engagement PDP.
- "Personalize This Ring" and "Find A Retailer" on every product card — the right *intent*, wrong execution.
- Shape icons in the "Center Stone Cut" filter and "Available Diamond Shapes" on the PDP.
- The PDP "Learn More" proof block (43 stages, RJC, JVC, hypoallergenic, lifetime service, lifetime upgrade, investment, heritage).
- Red-carpet carousel with event-level captions.
- A distinct, sellable DTC line (Maps by A.JAFFE) that can carry ecommerce mechanics without conflicting with retailers.
- Hyvä on Magento 2 — a performant, modern front end that can support every recommendation in this document without re-platforming.

### 5.2 What competitors do noticeably better

| # | Gap | Current state [VERIFIED] | Reference | Issue / opportunity [INTERPRETATION] | Recommendation | Customer benefit | Business benefit | Priority | Effort |
|---|---|---|---|---|---|---|---|---|---|
| G1 | Shape-first discovery | No shape in nav or homepage; shape only as PLP filter. | Gabriel, VRAI, Blue Nile menus; Gabriel PLP shape row. | Shape is the first decision for most engagement shoppers; hiding it forces filter-hunting. | Add "Shop by Shape" (9 icons) to the engagement mega menu, the homepage and the top of the ER PLP. Create indexable shape landing pages. | Finds the right rings in one click. | Discovery, SEO (shape keywords), lower bounce. | Critical | Medium |
| G2 | Homepage discovery | Hero ×3 same headline; no category/shape/product modules. | Tacori (3 tiles + product rail), Gabriel (icons + trust), Michael M (rails). | Shopper cannot start shopping from the homepage without opening the menu. | Rebuild homepage per §8. | Immediate paths to engagement, bands, shape, collection. | Engagement, deeper sessions, more PLP entries. | Critical | Medium |
| G3 | Price transparency | No price on card or PDP; placeholder price in meta. | Tacori ("starting at", "does not include center stone"), Michael M ("From $"), Gabriel (setting price + note). | Without any price anchor a luxury shopper cannot self-qualify and may assume "unaffordable" or "cheap". | Show **setting "from" price** with exclusion note; if retailer agreements prohibit, show a **price tier** ("Settings from $X") and financing availability. | Confidence to book. | Better-qualified retailer leads. | Critical | Low–Medium (data) |
| G4 | PDP decision support | Text-only metal line; no selectors; truncated description; typo in pricing line. | Tacori PDP. | The page reads as a catalog entry, not a product page. | Rebuild PDP per §11 with metal/shape selectors that swap imagery, structured details, pairing module, product-aware CTAs. | Evaluate without calling anyone. | Appointment rate, fewer unqualified enquiries. | Critical | High |
| G5 | Appointment journey | Generic 9-field lead form titled "Consumer Leads". | Tacori `?product=`; Gabriel "Book viewing + Locate a store" on PLP; VRAI showroom/virtual choice. | The form is designed for the CRM, not the customer. | Three-step flow: choose retailer (map) → choose date/time or "retailer will contact me" → confirm; carry product and metal from PDP; add virtual option. | Sees the ring she chose, at a store she chose, at a time she chose. | Higher appointment completion; better retailer hand-off. | Critical | Medium |
| G6 | Wishlist / save | None. | Gabriel (heart on card, wishlist in header), Blue Nile. | Engagement shopping is multi-session and multi-person (partner, parents). | Account-optional wishlist with share link and "Send to a retailer near me". | Saves and shares a shortlist. | Return visits, retailer-ready shortlists. | High | Medium |
| G7 | Filter taxonomy | Duplicate/overlapping values; missing price ranges; global sort attributes exposed. | Blue Nile (clean), Gabriel (result count, sort labels). | Duplicates split results and signal poor curation. | Consolidate to 7–8 facets per §10 with a single canonical value per concept. | Fewer wrong turns. | Discovery, perceived quality. | High | Low |
| G8 | Trust placement | Trust icons at page bottom; PDP proof block below forms. | Gabriel trust strip under hero; Tacori PDP details block. | Proof arrives after the decision moment. | Trust strip under hero; certification/comfort block above the fold on PDP. | Reassurance at the moment of doubt. | Conversion, brand tier. | High | Low |
| G9 | Mobile zoom | `user-scalable=0` everywhere. | All references allow zoom. | Accessibility failure and product-inspection barrier. | Remove `maximum-scale`/`user-scalable` from viewport meta. | Can inspect pavé and settings. | ADA risk removed. | Critical | Trivial |
| G10 | Collection storytelling | Eleven collection blurbs in the menu, five links; collection pages not merchandised in nav. | Michael M (10 named collections, each shoppable), Tacori (Crescent page). | The brand's best differentiators (Quilts®, Signature Shank®) have no landing-page hierarchy. | Collection hub + one landing page per signature feature (Quilts®, Signature Shank®, Expandables™, Lotus™, Always). | Understands what makes the ring different. | Brand equity, SEO for branded terms. | High | Medium |
| G11 | Cross-sell / pairing | One text link "View Matching Wedding Band"; "Men's Bands" rail on a women's ER PDP. | Tacori "Recommended Pairings For Her" (metal-matched); Michael M "Perfect Pairings". | Pairing is A.JAFFE's natural second sale. | Pairing module with band shown in selected metal; separate "For him" module. | Completes the set. | AOV at retailer, band attach. | High | Medium |
| G12 | Education / knowledge | None in menu; SEO copy at PLP bottom. | Gabriel Knowledge column + FAQ; Blue Nile education per panel; VRAI guides. | Shoppers research before contacting a retailer. | "Guides" column in menu: Ring fit & comfort, Shapes, Metals, Customization, Care. | Confidence. | SEO/AEO, time on site. | Medium | Medium |
| G13 | Ready-to-ship / availability | Not indicated. | VRAI, Blue Nile "Ready to Ship". | Retailer-led brands still have in-stock styles at partners. | "Available at retailers near you" signal driven by retailer inventory feed (phase 2). | Knows what she can see today. | Retailer traffic. | Future | High |
| G14 | Header hierarchy | 9 top-level items incl. Events, Red Carpet, Schedule a Showing, Store Locator, Customization as peers of categories. | Tacori (3 utility actions + search); VRAI (6). | Category and utility compete. | 5 category items + 3 utility actions (Find a Retailer, Book a Showing, Search). | Scans the menu in one glance. | Navigation success. | High | Low |

### 5.3 What competitors do poorly (do not copy)

- **Gabriel's 40+ filter facets** on a bridal category (Earring Closure Type, Enamel Color, Alphabet). Facets must be scoped per category.
- **Gabriel's triple-repeated PLP intro paragraph** (rendered three times in markup) and very long SEO tail — the tail is useful, but it should be one block, collapsed.
- **Blue Nile's promotional register** ("Up to 40% Off*", "Clear the Vault", phone number in the masthead). Incompatible with luxury perception.
- **Michael M's quick-add density** on the homepage (20+ products with "Quick add"). Appropriate for a DTC fashion-jewelry mix; wrong for a retailer-led bridal journey.
- **A.JAFFE's own 38-celebrity homepage carousel** in its current form — proof is good, a wall of 38 thumbnails is not. Curate to 6–8 with named pieces (as Michael M does).

### 5.4 Opportunities competitors have overlooked

1. **Comfort as a shoppable attribute.** No reference site lets a shopper filter by "won't spin", "expandable/flex", "nickel-free". A.JAFFE has the patents; make "Comfort engineering" a facet and a landing page.
2. **Try-it-at-a-retailer with the exact ring.** Only Tacori passes the product to the appointment. A.JAFFE can pass product + metal + shape + preferred retailer, and email the shopper a "bring this to your appointment" card.
3. **Heritage as a timeline, not a paragraph.** 1892 → Art Deco → Metropolitan → Quilts® patent → today. No competitor has a 130-year story to tell.
4. **Matching-band certainty.** Because A.JAFFE designs bands to match, "Guaranteed to sit flush" is a claim competitors cannot make casually.

## 6. Information architecture and category strategy

### 6.1 Browse dimensions — which ones A.JAFFE needs and why

| Dimension | Include? | Reason (customer intent · catalog · brand · SEO · merchandising) |
|---|---|---|
| Product type (Engagement, Wedding Bands, Fine Jewelry, Maps) | Yes | Primary intent split. Already exists. |
| Shape | **Yes — new** | First engagement decision; catalog already carries "Available Diamond Shapes" per ring [VERIFIED]; high-volume SEO terms ("oval engagement ring"). |
| Style / setting | Yes — clean up | Exists (9 ER settings, 13+8 band styles). Merge "Prong / Vtip-Prong / Flat Prong / Vtip-Claw Prong" into one "Prong" style with sub-filter only on PLP. |
| Collection | Yes — restructure | Five signature collections carry patents/trademarks (Quilts®, Signature Shank®, Lotus™, Always, Expandables™); legacy design collections (Art Deco, Metropolitan, Season of Love, Modern Royals™, Classics) should be a second tier or merged into "Style". |
| Metal | Yes — new as browse path | Every ring is offered in 4 metals [VERIFIED]; "yellow gold engagement ring" is a distinct search intent; Gabriel and Tacori both expose it. |
| Comfort engineering | **Yes — unique** | Quilts® interior, Signature Shank®, Flex/Expandable. No competitor can offer this facet. |
| Gender (bands) | Yes | Already split Women's/Men's; add as a facet on "All Wedding Bands". |
| Price | Yes (setting price tiers) | Self-qualification. Requires business decision on display (see G3). |
| Occasion | Partial | Anniversary / Eternity / Stackable for bands; not needed for engagement. |
| New arrivals · Best sellers | Yes | Both attributes exist in the sort list [VERIFIED: "Best Sellers", "Newest"] but are not exposed as browse paths. |
| Ready-to-ship / at a retailer | Later | Requires retailer inventory feed. Phase 3. |
| Gifts / birthstone | No | Not A.JAFFE's catalog focus; would dilute the bridal positioning. |

### 6.2 Proposed sitemap

```
HOME
├── ENGAGEMENT RINGS
│   ├── All Engagement Rings
│   ├── Shop by Shape        /engagement-rings/shape/{round|oval|cushion|emerald|pear|marquise|princess|radiant|heart}
│   ├── Shop by Style        /engagement-rings/style/{solitaire|hidden-halo|halo|three-stone|pave|bezel|split-shank|wide-band|floral-vine}
│   ├── Shop by Collection   /engagement-rings/collection/{quilts|signature-shank|lotus|always|classics|art-deco|metropolitan|season-of-love|modern-royals}
│   ├── Shop by Metal        /engagement-rings/metal/{platinum|white-gold|yellow-gold|rose-gold}
│   ├── New Arrivals · Best Sellers
│   └── Customize a Ring
├── WEDDING BANDS
│   ├── Women's  → by style (13) · by collection · eternity · anniversary · enhancers · stackable
│   ├── Men's    → by style (8) · Gray Gold™ · Morse Code · Quilts® Interior
│   ├── Matching Sets (his & hers, engagement + band)
│   └── Expandables™ / Flex Fit™
├── FINE JEWELRY  → Necklaces · Bracelets · Rings · Earrings · Quilts® Fine Jewelry
├── MAPS BY A.JAFFE  → Women · Men · How it works · Track order   (DTC)
├── THE HOUSE (brand hub)
│   ├── Our Story (1892 → today timeline)
│   ├── Comfort Engineering  → Quilts® · Signature Shank® · Expandables™
│   ├── Craftsmanship (43 stages)
│   ├── Responsible Sourcing (RJC · JVC · nickel-free)
│   ├── Red Carpet
│   ├── Events · Press · Blog/Journal
│   └── Lifetime Service & Upgrade · Warranty
├── GUIDES  → Ring fit & comfort · Diamond shapes · Metals · Customization · Care · FAQs
├── FIND A RETAILER  (+ state/city location pages)
├── BOOK A SHOWING  (product-aware · retailer-selectable · virtual option)
└── Account · Wishlist · Search
```

### 6.3 Proposed desktop mega menu — Engagement Rings

```
ENGAGEMENT RINGS
├── SHOP BY SHAPE (icons)          ├── SHOP BY STYLE (icons)        ├── SHOP BY COLLECTION          ├── FEATURED TILE
│   Round · Oval · Cushion         │   Solitaire · Hidden Halo     │   A.JAFFE Quilts®           │   [image]
│   Emerald · Pear · Marquise      │   Halo · Three Stone · Pavé   │   Signature Shank®          │   "Rings that never spin.
│   Princess · Radiant · Heart     │   Bezel · Split Shank         │   A.JAFFE Lotus™            │    Discover Quilts®"
│                                  │   Wide Band · Floral/Vine     │   Always by A.JAFFE         │   [Explore]
│  SHOP BY METAL (swatches)        │                               │   Classics · Art Deco       │
│   Platinum · White · Yellow      │  QUICK LINKS                  │   Metropolitan · Modern     │  ─────────────────────
│   Rose                           │   New Arrivals · Best Sellers │   Royals™ · Season of Love  │  Book a complimentary
│                                  │   Customize a Ring            │                             │  showing  [Book]
└── View all engagement rings ──────────────────────────────────────────────────────────────────────  Find a retailer
```

Rules: shape and style columns use the existing SVG icons; the featured tile rotates by campaign; the appointment/retailer footer row is persistent in every panel (the principle behind Gabriel's "Chat with an expert" row, adapted to A.JAFFE's retailer model).

### 6.4 Proposed desktop mega menu — Wedding Bands

```
WEDDING BANDS
├── FOR HER (icons)                ├── FOR HIM (icons)             ├── COLLECTIONS                 ├── FEATURED TILE
│   Pavé · Shared Prong · Channel  │   Classic · Diamond           │   Quilts® · Signature Shank® │   Expandables™ — the band
│   Bezel · Eternity · Curved      │   Two Tone · Gray Gold™       │   Lotus™ · Always           │   that grows with you
│   Enhancers · Open · High Polish │   Black Diamond / Dark Metal  │   Expandables™ / Flex Fit™  │   [Explore]
│   Free Form · Wide · Fancy Cut   │   Morse Code · Quilts® Int.   │                             │  ─────────────────────
│   Larger Melee                   │                               │  MATCHING SETS              │  Book a showing
└── View all women's · View all men's                               │   Engagement + band · His & Hers   Find a retailer
```

### 6.5 Proposed header

```
┌──────────────────────────────────────────────────────────────────────────────────────┐
│  A.JAFFE          Engagement Rings   Wedding Bands   Fine Jewelry   Maps   The House │
│                                                     Find a Retailer · Book a Showing · ⌕ · ♡ · Account │
└──────────────────────────────────────────────────────────────────────────────────────┘
```

Five category items (down from nine). Events, Red Carpet, Customization and Store Locator move: Events and Red Carpet into The House; Customization into a persistent "Customize a Ring" quick link inside Engagement and Wedding panels plus a homepage module; Store Locator becomes the utility action "Find a Retailer".

### 6.6 Mobile navigation structure

```
┌────────────────────────────┐
│ ☰   A.JAFFE      ⌕  ♡  👤  │
├────────────────────────────┤  Drawer (slides from left, full height, body scroll-locked)
│ Engagement Rings        ›  │  ├── level 2: Shape (icon grid 3×3) · Style (icon grid) ·
│ Wedding Bands           ›  │  │             Collection (list) · Metal (swatches) · New · Best · View all
│ Fine Jewelry            ›  │  ├── level 2: For Her · For Him · Collections · Matching Sets
│ Maps by A.JAFFE         ›  │
│ The House               ›  │
├────────────────────────────┤
│ ● Find a Retailer          │  ← pinned bottom actions, always visible in the drawer
│ ● Book a Showing           │
│ Customize a Ring · Guides  │
└────────────────────────────┘
```

Accessibility: drawer is a `dialog` with `aria-modal`, focus trapped, Escape closes, first focusable = close button; level-2 panels announce their heading; icon grids have text labels (no icon-only targets); tap targets ≥ 44×44 px.

---

## 7. Homepage redesign strategy

The current sequence [VERIFIED]: Hero carousel (3 slides, same headline) → Quilts® video → Signature Shank® video → 38-celebrity carousel → Customization video → Our Heritage → Connect to a Retailer → The A.JAFFE Promise → Newsletter → Footer.

**[INTERPRETATION]** The page is a brand brochure with no shopping entry points; it also stacks three autoplay Vimeo embeds. The recommended page keeps every story the current page tells, but re-sequences it so that a shopper can act within the first two screens and meets the story as she scrolls.

### 7.1 Recommended hierarchy

**01 · Hero — campaign, one message**

- Purpose: set tier and season; give one action.
- Content: a single campaign image or 6-second silent loop (not three slides), one headline written as a story line in the Tacori manner (e.g. a proposal moment), one primary CTA. Rotating slides, if kept, must carry different messages.
- Layout: full-bleed 16:9 desktop / 4:5 mobile, text bottom-left, generous safe area.
- Primary CTA: Explore Engagement Rings. Secondary CTA: Book a Showing.
- Reference principle: Tacori's narrative hero; Michael M's "house" voice.
- Why it helps: the first screen currently says "One Of A Kind Craftsmanship" three times; a story headline is more premium and more memorable.
- Mobile: single image, headline ≤ 6 words, CTA full-width.

**02 · Trust strip**

- Purpose: establish credibility before the first scroll.
- Content: Since 1892 New York · 43 stages of hand craftsmanship · Patented comfort (Quilts® & Signature Shank®) · 100% nickel-free · Lifetime service & upgrade.
- Layout: five items, icon + 3-word label, single row; no borders.
- Reference principle: Gabriel's five-item strip under the hero.
- Mobile: horizontally scrollable row with snap.

**03 · Start here — Engagement · Wedding Bands · Fine Jewelry · Maps**

- Purpose: category discovery.
- Content: four editorial tiles, each with one sentence (Tacori's tile copy pattern).
- Layout: 4-up desktop (2×2 on tablet), 2-up mobile.
- CTA per tile: Explore.

**04 · Shop by Shape**

- Purpose: engagement discovery by the first decision.
- Content: 9 shape icons (existing SVGs) with labels, linking to shape landing pages.
- Layout: single row desktop; 3×3 grid mobile.
- Reference principle: Gabriel PLP shape row; Blue Nile shapes module.

**05 · Comfort engineering — "The ring that fits like it was made for you"**

- Purpose: the differentiator, told once, well.
- Content: one section with three tabs or three stacked panels: Quilts® interior, Signature Shank®, Expandables™. Reuse the existing Vimeo loops but lazy-load and mute; add a 2-line "what it solves" per panel (spinning / balance / fit).
- Primary CTA: Shop Quilts®. Secondary: How it works (guide).
- Why: consolidates two homepage sections into one stronger, shoppable module.

**06 · Signature collections**

- Purpose: collection discovery.
- Content: Quilts® · Signature Shank® · Lotus™ · Always by A.JAFFE · Expandables™ — image, name, one line.
- Layout: 5-card rail with scroll-snap.

**07 · New & most-loved**

- Purpose: product-level entry.
- Content: 8 products alternating New Arrivals and Best Sellers (attributes already exist), using the new card design.
- Layout: product rail; on mobile 2 columns × 2 rows + "View all".

**08 · Wedding bands — for her, for him, together**

- Purpose: second category with equal weight; A.JAFFE's band catalog (378) is as large as engagement.
- Content: three tiles (Her / Him / Matching sets) plus Expandables™ callout.

**09 · Customize a ring**

- Purpose: keep the existing customization video, tighten it.
- Content: video (lazy) + 3-step explanation (Choose a style → Choose shape & metal → Meet your retailer) + CTA.

**10 · Spotted on the red carpet**

- Purpose: social proof.
- Content: curate 6–8 of the 38, each captioned with the piece worn (Michael M pattern), link to Red Carpet page.

**11 · Our House since 1892**

- Purpose: heritage.
- Content: one image, 3-line story, timeline teaser (1892 · Art Deco · Quilts® patent · today), CTA to Our Story.

**12 · See it in person**

- Purpose: primary conversion.
- Content: split module — Find a Retailer (zip input inline) | Book a complimentary showing (CTA) | Virtual consultation (if offered).
- Mobile: stacked; zip input first.

**13 · Guides** (3 cards: Ring fit & comfort · Choosing a shape · Metals explained) — supports SEO/AEO without SEO paragraphs.

**14 · Newsletter** — one field (email). The current footer form asks Email, Name, Zip and Phone [VERIFIED]; reduce to email, ask for zip after subscription.

**15 · Footer** — Shop · The House · Services (Customization, Lifetime Upgrade, Warranty, Eternity Band Program) · Retailers (Find a Retailer, Retail Partner Portal) · Support · Legal · Accessibility statement.

### 7.2 Homepage wireframe (desktop)

```
┌──────────────────────────────────────────────────────────────┐
│ HEADER  logo | Engagement · Bands · Fine Jewelry · Maps · House │ Retailer · Showing · ⌕ ♡ 👤
├──────────────────────────────────────────────────────────────┤
│                                                              │
│                CAMPAIGN HERO (single image / loop)           │
│   "Story headline"                                           │
│   [Explore Engagement Rings]  [Book a Showing]               │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│ ◇1892 NY   ◇43 stages   ◇Patented comfort   ◇Nickel-free   ◇Lifetime │
├──────────────────────────────────────────────────────────────┤
│  [Engagement]     [Wedding Bands]   [Fine Jewelry]   [Maps]  │
│   one line         one line          one line        one line│
├──────────────────────────────────────────────────────────────┤
│ SHOP BY SHAPE  ○ ⬭ ▢ ▭ ◊ ◆ ◇ ▣ ♡                             │
├──────────────────────────────────────────────────────────────┤
│ COMFORT ENGINEERING                                          │
│ [video]   Quilts® | Signature Shank® | Expandables™          │
│           "what it solves" · [Shop Quilts®] [How it works]   │
├──────────────────────────────────────────────────────────────┤
│ SIGNATURE COLLECTIONS  [Quilts®][Shank®][Lotus™][Always][Flex]│
├──────────────────────────────────────────────────────────────┤
│ NEW & MOST-LOVED   [card][card][card][card]  → view all      │
├──────────────────────────────────────────────────────────────┤
│ WEDDING BANDS   [For her]   [For him]   [Matching sets]      │
├──────────────────────────────────────────────────────────────┤
│ CUSTOMIZE  [video] 1 style → 2 shape & metal → 3 retailer    │
├──────────────────────────────────────────────────────────────┤
│ RED CARPET  [6 curated, piece named]                         │
├──────────────────────────────────────────────────────────────┤
│ SINCE 1892   image | story | timeline teaser                 │
├──────────────────────────────────────────────────────────────┤
│ SEE IT IN PERSON   [zip ▸ Find]  |  [Book a showing]  |  [Virtual] │
├──────────────────────────────────────────────────────────────┤
│ GUIDES  [fit & comfort] [shapes] [metals]                    │
├──────────────────────────────────────────────────────────────┤
│ NEWSLETTER  [email ▸]                                        │
├──────────────────────────────────────────────────────────────┤
│ FOOTER                                                       │
└──────────────────────────────────────────────────────────────┘
```

---

## 8. Category landing page (Engagement Rings)

Current [VERIFIED]: banner image → H1 → one paragraph → filter bar → grid with two editorial tiles inserted → pagination (19/38/57) → complimentary-viewing form → customization video → three SEO blocks (one with a typo) → footer.

**[INTERPRETATION]** It is a PLP with a banner, not a category landing page; the guided-discovery layer is missing, and the SEO copy is placed where a luxury shopper expects editorial.

### 8.1 Recommended structure (text wireframe)

```
┌──────────────────────────────────────────────────────────────┐
│ Home › Engagement Rings                     (breadcrumb, schema)│
├──────────────────────────────────────────────────────────────┤
│ H1 Engagement Rings                                          │
│ 2-line editorial intro (house voice, not SEO copy)           │
├──────────────────────────────────────────────────────────────┤
│ SHOP BY SHAPE   ○ ⬭ ▢ ▭ ◊ ◆ ◇ ▣ ♡          (sticky on scroll)│
├──────────────────────────────────────────────────────────────┤
│ STYLE ROW  [Solitaire][Hidden Halo][Halo][3-Stone][Pavé][Bezel]…│
├──────────────────────────────────────────────────────────────┤
│ 388 rings · Sort ▾ · Filters (7) ▾ · applied chips ×  Clear all │
├──────────────────────────────────────────────────────────────┤
│ GRID 4-col  card card card card                              │
│             card card [editorial: Quilts® — never spins] card│
│             card card card card                              │
│             … Load more (24 at a time)                       │
├──────────────────────────────────────────────────────────────┤
│ SEE IT IN PERSON   [Find a retailer]  [Book a showing]       │
├──────────────────────────────────────────────────────────────┤
│ COLLECTIONS  Quilts® · Signature Shank® · Lotus™ · Always    │
├──────────────────────────────────────────────────────────────┤
│ GUIDES  Ring fit & comfort · Choosing a shape · Metals       │
├──────────────────────────────────────────────────────────────┤
│ FAQ (accordion, FAQ schema) — 6 questions                    │
│ ▸ About A.JAFFE engagement rings (collapsed SEO copy, 1 block)│
└──────────────────────────────────────────────────────────────┘
```

Shape and style sub-pages (`/engagement-rings/shape/oval`) use the same template with the shape pre-selected, an H1 "Oval Engagement Rings", a shape-specific intro and FAQ, and internal links to the other shapes — the Gabriel principle, executed with A.JAFFE's vocabulary.

---

## 9. PLP, product cards and filters

### 9.1 Grid and card

| Element | Current [VERIFIED] | Recommendation |
|---|---|---|
| Columns | Not verifiable from markup (JS grid) | Desktop 4 (1280+), tablet 3, mobile 2. |
| Page size | 19 / 38 / 57 with numeric pagination | 24 per load, "Load more" + URL `?p=` preserved for SEO and back-button. |
| Image ratio | Square product shots on white | Keep 1:1; add a second image on hover / swipe (profile view or on-hand). |
| Card content | Style no. · name · collection · 4 metal swatches · Personalize · View Details · Find A Retailer | **Image · wishlist ♡ · collection eyebrow · name · "Settings from $X" (or tier) · metal swatches (click swaps image) · shape availability icons · badge (New / Best seller / Quilts® interior).** Remove the three text links; the whole card links to the PDP; "Find a retailer" lives on the PDP and in the sticky bar. |
| Editorial tiles | Two image tiles with no link (`javascript:void(0)`) | Keep the idea; make each tile a real link (collection, guide or showing CTA). |
| Data quality | Some cards missing image and name (e.g. ME2311Q/156B); a band listed under engagement with a mismatched URL | Catalog QA pass before launch: every card must have image, name, collection, shapes, metals. |

### 9.2 Filter taxonomy for this catalog

| Facet | Values | Why customers need it |
|---|---|---|
| Shape | Round · Oval · Cushion · Emerald · Pear · Marquise · Princess · Radiant · Heart (existing icons) | First decision; already in data as "Available Diamond Shapes". |
| Style | Solitaire · Hidden Halo · Halo · Three Stone · Pavé · Bezel · Split Shank · Wide Band · Floral/Vine · Prong (sub: 4-prong / V-tip / claw) | Second decision; collapses the 11 overlapping "Settings" values. |
| Collection | Quilts® · Signature Shank® · Lotus™ · Always · Classics · Art Deco · Metropolitan · Season of Love · Modern Royals™ | One value per collection; "Petite" and "Iconic" become sub-labels within Quilts®. |
| Comfort engineering | Quilts® interior · Signature Shank® · Expandables™/Flex | A.JAFFE-only facet; turns patents into a shopping reason. |
| Metal | Platinum · White gold · Yellow gold · Rose gold · Two-tone | Every ring offers four; swatches already exist. |
| Setting price | Under $3,000 · $3,000–5,000 · $5,000–10,000 · $10,000–15,000 · $15,000+ (continuous, no gaps) | Self-qualification. Current buckets skip a range. |
| Side stones | None · Pavé · Channel · Peek-a-boo / hidden | Frequent product-name attribute ("Peek-A-Boo Diamonds", "Surprise Diamonds"). |
| Band width (bands only) · Gender (bands) · Diamond coverage (bands: plain / half / eternity) | — | Band-specific decisions. |

Sort: Recommended · Newest · Best sellers · Price ↑ · Price ↓. Remove internal attributes from the sort list (Map Color, Map Group, Best Sellers Sort, Available in Platinum?) [VERIFIED in markup].

Behaviour: applied-filter chips with individual × and "Clear all"; result count always visible; filter bar sticky on desktop; URL-encoded filters for shareable/indexable shape and style pages.

### 9.3 Desktop PLP wireframe

```
┌────────────────────────────────────────────────────────────────────┐
│ Home › Engagement Rings                                            │
│ H1 · intro · SHAPE ROW · STYLE ROW                                 │
├──────────────┬─────────────────────────────────────────────────────┤
│ FILTERS      │ 388 rings      Sort: Recommended ▾   [chips × …] Clear│
│ ▸ Shape      ├─────────────┬─────────────┬─────────────┬───────────┤
│ ▸ Style      │ ♡     NEW   │ ♡           │ ♡  QUILTS®  │ ♡         │
│ ▸ Collection │ [image]     │ [image]     │ [image]     │ [image]   │
│ ▸ Comfort    │ Quilts®     │ Classics    │ Lotus™      │ Shank®    │
│ ▸ Metal      │ Ring name   │ Ring name   │ Ring name   │ Ring name │
│ ▸ Price      │ from $2,400 │ from $3,100 │ from $2,900 │ from $4,200│
│ ▸ Side stones│ ●●●●  ○⬭▢+2 │ ●●●●  ○⬭    │ ●●●●  ○⬭◊   │ ●●●●  ○   │
│              ├─────────────┴─────────────┴─────────────┴───────────┤
│              │ … rows …    [editorial tile: "Never spins" → Quilts®]│
│              │                   [ Load more ]                      │
└──────────────┴─────────────────────────────────────────────────────┘
```

### 9.4 Mobile PLP + filter drawer wireframe

```
┌──────────────────────┐        ┌──────────────────────┐
│ ‹ Engagement Rings   │        │ Filters        ✕     │
│ ○ ⬭ ▢ ▭ ◊ ◆ ◇ ▣ ♡ →  │ shape  │ Shape      Round ▾   │
│ 388 · Sort ▾ · Filter (2)│ sticky │ Style      Any ▾     │
├──────────┬───────────┤        │ Collection Any ▾     │
│ ♡ [img]  │ ♡ [img]   │        │ Comfort    Quilts® ✓ │
│ Quilts®  │ Classics  │        │ Metal      ●●●●      │
│ Name     │ Name      │        │ Price      ━━●━━━━   │
│ from $   │ from $    │        │ Side stones Any ▾    │
│ ●●●● +2  │ ●●●●      │        │                      │
├──────────┼───────────┤        │ [Clear all]  [Show 42 rings] │
│ …        │ …         │        └──────────────────────┘
│   [ Load more ]      │        bottom sheet, 90% height, focus-trapped,
└──────────────────────┘        result count updates live on the button
```

---

## 10. PDP redesign

Current PDP [VERIFIED]: "Browse Engagement Rings" link (no breadcrumb) → 18 gallery slots → "View Matching Wedding Band" text link → Style no. → H1 → "Available in: Platinum | White Gold | Yellow Gold | Rose Gold" (text) → retailer pricing line (with typo) → "Find the nearest store" zip form → "Schedule a Showing" 10-field form → complimentary viewing form → Description (truncated mid-sentence) → Details (0.07 ctw, Setting: Prong, 9 shape icons) → "Learn More" (10 bold paragraphs) → Drop A Hint → Share → sourcing statement → Red Carpet carousel (25) → You Might Also Like (8) → Men's Bands (8) → autoplay Vimeo. Meta: `og:image` is a placeholder; `meta title` ("Solitaire Prong Diamond Engagement Ring for Women") does not match the H1.

**[INTERPRETATION]** Three lead forms sit between the product and its description. The metal choice — the one thing every A.JAFFE ring offers — is a sentence, not a control. The best proof content on the site is below the third form.

### 10.1 Recommended information hierarchy

**Above the fold**

- Breadcrumb: Home › Engagement Rings › Oval › [Ring name]
- Gallery (left, 55%): 4–6 real views — three-quarter, top, profile, on-hand, Quilts® interior close-up; zoom on click; video where available; alt text per view.
- Product column (right, 45%, sticky on desktop):
  - Collection eyebrow (Quilts®) + comfort badge ("Never-spin Quilts® interior")
  - H1 ring name · style number (small)
  - **Price framing:** "Setting from $X · center stone not included" *or*, if agreements prohibit, "Settings in this collection from $X · financing through authorized retailers"
  - **Metal selector** (4 swatches, swaps imagery) · **Shape selector** (9 icons, marks availability) · Purity toggle if applicable (14K/18K)
  - Primary CTA: **Book a complimentary showing** (carries product + metal + shape)
  - Secondary: **Find this ring near you** (zip inline) · Tertiary: **Personalize this ring**
  - Wishlist ♡ · Drop a hint · Share
  - Trust micro-row: 43 stages · Nickel-free · RJC & JVC certified · Lifetime upgrade

**Decision support (accordion)**

- The design — full description (fix truncation) in house vocabulary
- Details — total carat weight, setting, available shapes, band width, profile, metals, made in New York
- Comfort engineering — which patent this ring uses and what it solves (2 lines + diagram)
- Sizing & fit — link to guide; note Expandables™ where relevant
- Customization — what can be changed (center stone, metal, shank, engraving)
- Service — lifetime service, Lifetime Upgrade, warranty, authenticity
- Sourcing — natural diamonds, RJC, JVC, nickel-free

**Discovery**

- **Complete the set** — matching wedding band(s) shown in the selected metal (Tacori's `?metal=` principle), "Guaranteed to sit flush" note
- **Same design, other shapes** (the "Related Designs" pattern)
- You may also like (8, same collection or style)
- Recently viewed
- **For him** — men's bands, moved below discovery and labelled so it no longer reads as a mis-targeted rail

**Brand**

- Collection story (one paragraph + image)
- Red carpet — 4 curated images, only if the piece worn belongs to the same collection; otherwise omit from PDP

### 10.2 PDP wireframe — desktop

```
┌────────────────────────────────────────────────────────────────────────┐
│ Home › Engagement Rings › Oval › Solitaire with Surprise Diamonds     │
├──────────────────────────────┬─────────────────────────────────────────┤
│ ┌──────────────────────────┐ │ QUILTS®  · Never-spin interior          │
│ │                          │ │ H1 Solitaire Engagement Ring            │
│ │      MAIN IMAGE          │ │    with Surprise Diamonds   ME2211Q      │
│ │      (zoom on click)     │ │ Setting from $2,400 · center stone not incl.│
│ │                          │ │ Metal  ● ● ● ●   Shape ○ ⬭ ▢ ▭ ◊ ◆ ◇ ▣ ♡│
│ └──────────────────────────┘ │ [ Book a complimentary showing ]        │
│ [thumb][thumb][thumb][thumb] │ [ Find this ring near you  zip ▸ ]       │
│  3/4    top   profile  hand  │  Personalize this ring · ♡ Save · Hint   │
│                              │ 43 stages · Nickel-free · RJC/JVC · Upgrade│
│                              ├─────────────────────────────────────────┤
│                              │ ▸ The design                            │
│                              │ ▸ Details                               │
│                              │ ▸ Comfort engineering (Quilts®)         │
│                              │ ▸ Sizing & fit · ▸ Customization        │
│                              │ ▸ Service · ▸ Sourcing                  │
├──────────────────────────────┴─────────────────────────────────────────┤
│ COMPLETE THE SET   [band in same metal] [band] [band]  "sits flush"    │
├────────────────────────────────────────────────────────────────────────┤
│ SAME DESIGN, OTHER SHAPES   [round][cushion][pear]                     │
├────────────────────────────────────────────────────────────────────────┤
│ YOU MAY ALSO LIKE  [8 cards]          RECENTLY VIEWED                  │
├────────────────────────────────────────────────────────────────────────┤
│ THE QUILTS® STORY  image | 1 paragraph | [Explore]                     │
└────────────────────────────────────────────────────────────────────────┘
```

### 10.3 PDP wireframe — mobile

```
┌──────────────────────┐
│ ‹ Oval               │
│ [ gallery swipe ●○○○ ]│  4:5, pinch-zoom enabled
│ QUILTS® · never spins│
│ H1 Ring name         │
│ Setting from $2,400  │
│ Metal ● ● ● ●        │
│ Shape ○ ⬭ ▢ + more   │
│ ♡ Save   Drop a hint │
│ 43 stages · Nickel-free · Lifetime upgrade │
│ ▸ The design         │
│ ▸ Details            │
│ ▸ Comfort engineering│
│ ▸ Sizing · Customize │
│ ▸ Service · Sourcing │
│ COMPLETE THE SET  →  │
│ SAME DESIGN, SHAPES →│
│ YOU MAY ALSO LIKE  → │
├──────────────────────┤
│ [Book a showing] [Find near me] │ ← sticky bottom bar, appears after hero
└──────────────────────┘
```

**Reasoning behind the major changes:** the three forms collapse into one product-aware CTA and one inline zip field; the metal line becomes a selector because A.JAFFE's four-metal offer is a differentiator only if it can be seen; the proof block moves from the bottom to a trust micro-row plus accordion so it arrives at the moment of doubt; the pairing module turns "View Matching Wedding Band" from a text link into the second sale.

## 11. Luxury visual direction

### 11.1 What "luxury" should mean for A.JAFFE

Not "modern", not "minimal for its own sake". For a 1892 New York house whose signature is engineering, luxury should read as **precision and calm**: the confidence of a maker who has nothing to prove. Three words for the design team: **quiet · exact · warm**.

### 11.2 What currently prevents the experience from feeling as premium as the reference set [INTERPRETATION of verified observations]

1. **Repetition reads as template.** Three hero slides with one headline; the same "Schedule a complimentary viewing" form rendered on the PLP and twice on the PDP; the same collection blurbs duplicated in two menu regions.
2. **Density without hierarchy.** Nine top-level nav items; ten bold "Learn More" paragraphs; 38 celebrity thumbnails; 25 red-carpet images on a product page. Luxury sites show fewer things, larger.
3. **Copy errors at decision points.** "Please contact an authorized retailer other pricing…", "engagament", a description ending "…includes our i", lowercase "heart" among capitalised shapes, "Consumer Leads" as a page title. Each one is small; together they undermine "43 meticulous stages".
4. **Forms where product should be.** Three lead forms interrupt the PDP before the description.
5. **Autoplay video stacked three deep** on the homepage and once more on the PDP — motion without restraint, and a performance cost.
6. **No price signal.** Silence about price does not read as exclusive when the reference luxury brands (Tacori, Michael M) state it plainly.

### 11.3 Specific design changes that create the desired perception

**Typography**

- Two families only: a high-contrast serif for headlines and collection names (the 1892 / Art Deco lineage justifies a Didone-influenced face) and a humanist sans for UI, prices and details. Body 17–18 px, line-height 1.6; product names in the serif at 20–22 px; prices in the sans, tabular figures.
- Scale: 12 / 14 / 16 / 20 / 28 / 40 / 56 / 80 px on desktop; drop two steps on mobile. No all-caps eyebrows; use small-caps only for style numbers.

**Whitespace and rhythm**

- Section spacing on a 8 px base: 96 px between homepage sections on desktop, 64 px on mobile. Product columns have 32 px gutters; cards have no border and no shadow.
- Where: between hero and trust strip (48 px, tighter — they belong together); before "Comfort engineering" (128 px — it is the chapter break).

**Imagery**

- Product: consistent three-quarter hero shot on a warm off-white (#F7F4EF) rather than pure white; second view = profile showing the Quilts® interior or Signature Shank® base — the feature *is* the photography brief. Third view = on-hand.
- Editorial: campaign photography with real skin, real light, one ring; never a collage of celebrity crops.
- Video: one silent loop per page maximum, lazy-loaded, paused under `prefers-reduced-motion`, poster image required.

**Palette**

- Base: warm off-white #F7F4EF; ink #1E1B18 (not pure black); stone grey #8C8680 for meta text; hairline #E4DED6.
- Accent: a deep patina green-blue (#2F4A4E) used only for primary CTAs and focus rings, referencing the brand's existing deep tones rather than a generic gold. Gold appears only in photography.
- Contrast: all text ≥ 4.5:1; CTA text on accent ≥ 7:1.

**UI surfaces**

- Buttons: 48 px tall, 2 px radius, serif label 15 px; primary filled accent, secondary hairline outline, tertiary text link with underline offset. Hover darkens 8%; no scale transforms.
- Cards: image, then text, no container; hover swaps image and underlines the name.
- Icons: keep the existing shape and setting SVGs; redraw at 1.5 px stroke for consistency.
- Borders: hairlines only for tables, accordions and the filter rail.

**Motion**

- One page-load moment (hero image settles, headline fades) and answer-to-action motion (accordion open, drawer slide, image swap). No per-section scroll reveals beyond a single 200 ms opacity/translate on first entry, disabled under `prefers-reduced-motion`.

**Editorial layouts**

- Collection pages use a 2/3 image + 1/3 text split with the text block vertically centred; the comfort-engineering section uses a diagram (cross-section of the shank) — engineering drawn, not described.

---

## 12. CRO strategy

**Primary conversions (retailer-led model):** (1) Book a showing (product-aware); (2) Find a retailer (zip → retailer detail → directions/call); (3) Maps by A.JAFFE purchase (DTC).

**Secondary / micro conversions:** wishlist save · share wishlist / send to retailer · personalize this ring · drop a hint · newsletter · guide read · collection explore · virtual consultation.

### 12.1 Friction by stage

| Stage | Friction observed [VERIFIED → INTERPRETATION] | Change | Customer benefit | Business objective |
|---|---|---|---|---|
| Discovery | No shape entry; homepage has no shopping modules; nine nav items. | Shape row + category tiles on home; 5-item nav; shape/style landing pages. | Finds candidates fast. | Discovery, SEO. |
| Consideration | No price signal; no wishlist; cards need three clicks to do anything. | "From" price or tier; wishlist heart; whole-card link. | Builds a shortlist with confidence. | Return visits, qualified leads. |
| Evaluation | PDP: text-only metal line; description truncated; proof below three forms; pairing is a text link. | Selectors; full description; trust micro-row; pairing module in chosen metal. | Decides without calling. | Appointment rate. |
| Conversion | Appointment = generic form; locator disconnected from product; page title "Consumer Leads". | Product-aware, retailer-selectable, date-aware booking; confirmation email with ring card; retailer notified with product + metal. | Arrives at the retailer with a decision made. | Retailer conversion, partner satisfaction. |
| Post-lead | No follow-up content. | Confirmation page: "What to expect at your showing" + guide links + wishlist reminder. | Feels looked after. | Show-up rate. |

### 12.2 Micro-conversion architecture (the Gabriel principle, adapted)

Every product context offers, in this order: **Save** (no account needed, cookie + optional email) → **Book a showing** → **Find near you** → **Personalize**. Every brand/story context offers **Explore the collection** → **Book a showing**. No context asks for more than one form.

### 12.3 What not to do

No exit-intent popups, no countdown timers, no "X people viewing", no discount capture on entry. These are Blue Nile mechanics and would cost more brand equity than they return.

---

## 13. SEO + AEO + content discovery

**Current [VERIFIED]:** category pages carry `meta keywords` tags (obsolete), long SEO paragraphs at the foot of PLPs, a blog, a canonical PDP URL that drops the category path (fine), a placeholder `og:image` and a placeholder `product:price:amount` on the PDP, and no breadcrumb markup on the PDP.

**Recommendation**

| Item | Action |
|---|---|
| Shape / style / collection / metal landing pages | Real category pages (not filter URLs) with unique H1, 2-line intro, FAQ, internal links to siblings. Target: "oval engagement ring", "hidden halo engagement ring", "Quilts engagement ring", "yellow gold engagement ring". |
| Comfort engineering pages | One page per patent (Quilts® interior, Signature Shank®, Expandables™) answering "why does my ring spin / how to stop an engagement ring from spinning" — an AEO opportunity no competitor owns. |
| Guides | Ring fit & comfort · Shapes · Metals · Customization · Care · "Engagement ring vs wedding band". Written as answers, with FAQ schema. |
| Retailer location pages | State and city pages listing authorized retailers (Verragio's verified pattern), each with LocalBusiness references and a "Book a showing here" CTA. |
| Breadcrumbs | Visible + `BreadcrumbList` schema on PLP, sub-category and PDP. |
| Product schema | `Product` with `brand`, `material`, `offers` (use `PriceSpecification` with `minPrice` if only "from" pricing is shown; omit `price` rather than publish a placeholder), `image` (real, not placeholder). |
| FAQ schema | On category landing pages and guides only; never on PDPs with generic FAQs. |
| Remove | `meta keywords`; SEO paragraphs from above the fold; duplicate menu blurbs. |
| Placement rule | Educational copy sits in a collapsed "About" block below FAQs on category pages, and in Guides. It never appears between the shopper and the grid. |

---

## 14. Accessibility and performance

### 14.1 WCAG 2.1 AA — issues observed and remediation

| Observation [VERIFIED] | WCAG | Fix |
|---|---|---|
| `maximum-scale=1, user-scalable=0` on every page. | 1.4.4 Resize text; 1.4.10 Reflow | Remove both attributes. |
| Header links with `href="javascript:;"` and a malformed `javascrip:;` on the Cart trigger. | 2.1.1 Keyboard; 4.1.2 Name/Role/Value | Use `<button>` for menu, search, store, cart triggers with `aria-expanded` / `aria-controls`. |
| Editorial tiles in the PLP grid link to `javascript:void(0)`. | 2.4.4 Link purpose | Real destinations or `<div>` with no link semantics. |
| Metal swatches on cards are images with title text only. | 1.1.1; 4.1.2 | Radio-group pattern with visible labels on focus and `aria-label` per swatch. |
| Shape icons in filters: one alt is lowercase "heart"; icon `alt="icon"` on many menu items. | 1.1.1 Non-text content | Descriptive alt per icon ("Heart shape"); decorative icons `alt=""`. |
| Duplicate H2 "One Of A Kind Craftsmanship" ×3 in the hero; heading levels skip on PLP ("Shop By" H2 then filter H3s hidden). | 1.3.1 Info and relationships | One H1, distinct H2s, headings only for visible sections. |
| Three lead forms with unlabelled inputs (labels rendered as placeholder text in markup). | 1.3.1; 3.3.2 Labels | Visible `<label>` per field; error messages linked via `aria-describedby`. |
| Autoplay background video ×3 on homepage. | 2.2.2 Pause, stop, hide; 2.3.3 | Pause under `prefers-reduced-motion`; provide a pause control; one video per viewport. |
| Filter accordions and mega menu rendered as lists of links without disclosure semantics. | 4.1.2 | Disclosure buttons with `aria-expanded`; mega menu on hover *and* on click/Enter; Escape closes; arrow-key navigation within panels. |
| Focus states: not verified (CSS not inspected). | 2.4.7 Focus visible | 2 px accent outline, 2 px offset, on all interactive elements. |
| Contrast of stone-grey meta text on white: not verified. | 1.4.3 | Verify ≥ 4.5:1 in the style guide. |

Additional requirements for the redesign: skip link (exists — keep), mobile drawer as modal dialog with focus trap, filter drawer announces result count via `aria-live="polite"`, product option selectors as radio groups, wishlist toggle with `aria-pressed`, alt strategy per gallery view ("three-quarter view", "profile showing Quilts® interior", "on hand"), and every animation wrapped in `@media (prefers-reduced-motion: no-preference)`.

### 14.2 Performance risks observed

| Risk [VERIFIED] | Impact [INTERPRETATION] | Mitigation |
|---|---|---|
| Three Vimeo iframes on the homepage, one on the PDP. | Third-party scripts + heavy media on first load; LCP and CLS risk. | Self-hosted MP4/WebM loops with `poster`, `loading="lazy"`, `preload="none"`, IntersectionObserver play/pause; max one per viewport. |
| Hero markup serves mobile images to all viewports (`homepage_banner_wedding_bands-mobile.jpg`). | Wrong asset for desktop; quality loss or oversize. | `<picture>` with AVIF/WebP sources per breakpoint (Gabriel serves `-Mobile` AVIF variants). |
| PDP renders 18 gallery slots. | DOM weight; lazy images still cost layout. | 4–6 curated views; lazy-load beyond the first two. |
| 25-image red-carpet carousel and 16 recommendation cards on every PDP. | Payload and JS on the highest-value page. | Curate to 4; load recommendation rails on scroll. |
| Full mega menu (with 11 collection blurbs) in the DOM twice (desktop + mobile). | Bloat. | Single source rendered once; blurbs removed from the menu. |
| Placeholder `og:image` on PDP. | Broken social shares. | Real product image. |
| Filter "Apply" step and full page reload (JS not verified). | Slower iteration. | Hyvä-native Alpine filtering with URL state, no full reload. |

---

## 15. Visual evidence

Screenshots are provided as page references for the client presentation; because this audit was compiled from the live markup, each item lists the exact URL and what to capture.

| # | Recommendation | CURRENT (capture) | REFERENCE (capture) | Observation | Proposed direction |
|---|---|---|---|---|---|
| E1 | Shape-first navigation | ajaffe.com → hover "Engagement Rings" (View by Setting / View by Collections) | gabrielny.com → hover "Engagement Rings" (Shop by Shape / Style / Metal / Collections / Knowledge) | A four-dimension menu lets the shopper choose her own path. | A.JAFFE menu with Shape · Style · Collection · Metal columns, featured tile and persistent showing/retailer row. Not a copy: A.JAFFE's collections and comfort story take the place of Gabriel's quiz and chat. |
| E2 | Homepage first screen | ajaffe.com hero (3 slides, same headline) | tacori.com hero "The Nervous Suitor" | One story, one action, then three category tiles. | A.JAFFE campaign hero + trust strip + four category tiles. |
| E3 | Product card | ajaffe.com/engagement-rings (card with Personalize / View Details / Find A Retailer) | gabrielny.com/engagement-rings (heart, shape icons, "4 Metals", price) | Card carries decision data, not links. | A.JAFFE card with price framing, wishlist, shape availability, metal swatches, comfort badge. |
| E4 | PDP decision block | ajaffe.com/engagement-rings/solitaire-engagement-ring-with-surprise-diamonds (metal text line + three forms) | tacori.com/products/engagement-ring-founders-collection-ht2580ov (price note, shape/metal/purity, two CTAs) | Options as controls; one product-aware appointment link. | A.JAFFE PDP with selectors, trust micro-row, product-aware "Book a showing". |
| E5 | Pairing | A.JAFFE PDP "View Matching Wedding Band" text link | Tacori "Recommended Pairings For Her" (bands in selected metal) | Pairing is merchandised. | "Complete the set" module with "sits flush" note. |
| E6 | Appointment | ajaffe.com/bookanappointment (title "Consumer Leads", 9 fields) | gabrielny.com PLP "View Your Ring In-Store: Book viewing · Locate a store"; Tacori `?product=` | Booking starts inside product context. | Three-step product-aware booking with retailer map. |
| E7 | Trust placement | ajaffe.com "The A.JAFFE Promise" at page bottom | gabrielny.com trust strip directly under hero | Proof first, then story. | Trust strip under hero; certification micro-row on PDP. |
| E8 | Brand voice | ajaffe.com "Our Heritage" paragraph | michaelm.com "The House of Modern Monarchs" / "Enter the House" | A house has a name for its world. | "The House" hub, comfort-engineering vocabulary, named signature features on every card. |
| E9 | Location SEO | ajaffe.com/storelocator?zip=10036 (single page) | verragio.com/locations (state/province/city pages) | Indexable retailer pages. | A.JAFFE state and city retailer pages. |

In every case: use the UX principle; adapt it to A.JAFFE's brand, catalog and retailer model. Never copy the layout.

---

## 16. Prioritized recommendations

### P0 — Must fix (blocking usability, accessibility or credibility)

| Recommendation | Impact | Effort | Reason | Reference | Business objective |
|---|---|---|---|---|---|
| Re-enable pinch zoom (remove `maximum-scale`/`user-scalable`). | High | Trivial | WCAG 1.4.4 failure; blocks product inspection. | All references | ADA risk, mobile usability |
| Fix copy defects: PDP pricing sentence, truncated descriptions, "engagament", lowercase "heart", "Consumer Leads" title. | High | Low | Errors at decision points contradict the craft claim. | — | Credibility |
| Consolidate duplicate filter values; fill price-range gaps; remove internal sort attributes. | High | Low | Split results and exposed internals. | Blue Nile, Gabriel | Discovery |
| Fix catalog data: cards missing image/name; mis-categorised band in engagement grid. | High | Low | Broken cards in a luxury grid. | — | Credibility |
| Replace `javascript:;` triggers with buttons; label all form fields. | High | Low | Keyboard and screen-reader access. | — | ADA risk |
| Real `og:image`; remove placeholder `product:price:amount`. | Medium | Trivial | Broken shares; false price signal to crawlers. | — | SEO/social |

### P1 — High impact (the redesign core)

| Recommendation | Impact | Effort | Reason | Reference | Business objective |
|---|---|---|---|---|---|
| New IA: 5-item nav, Shape/Style/Collection/Metal mega menu, mobile drawer with pinned actions. | Very high | Medium | Shape-first discovery; cleaner hierarchy. | Gabriel, VRAI | Discovery, SEO |
| Homepage rebuild (§7). | Very high | Medium | Shopping entry points + re-sequenced story. | Tacori, Gabriel, Michael M | Engagement, PLP entries |
| PLP + card redesign with price framing, wishlist, shape availability, hover image, sticky filters (§9). | Very high | Medium | Cards carry decisions. | Gabriel, Tacori | Consideration |
| PDP rebuild with selectors, trust micro-row, accordion details, pairing module, product-aware CTAs (§10). | Very high | High | Evaluation without forms. | Tacori | Appointment rate |
| Product-aware, retailer-selectable, date-aware Book-a-Showing flow. | Very high | Medium | Conversion built for the customer, not the CRM. | Tacori, Gabriel | Retailer leads |
| Wishlist (account-optional) with share and "send to retailer". | High | Medium | Multi-session shopping. | Gabriel | Return visits |
| Price display decision (from-price or tier). | High | Low (tech) / policy | Self-qualification. | Tacori, Michael M | Lead quality |
| Trust strip under hero; certification micro-row on PDP. | High | Low | Proof at the moment of doubt. | Gabriel, Tacori | Conversion |

### P2 — Enhancement

| Recommendation | Impact | Effort | Reference | Objective |
|---|---|---|---|---|
| Shape / style / collection / metal landing pages with FAQ schema. | High | Medium | Gabriel | SEO |
| Comfort-engineering hub + one page per patent; "Comfort" facet. | High | Medium | Tacori Crescent page | Differentiation, AEO |
| Guides section (fit, shapes, metals, customization, care). | Medium | Medium | Gabriel, Blue Nile | SEO/AEO |
| Retailer state/city pages. | Medium | Medium | Verragio | Local SEO |
| Curated red carpet (6–8 with named pieces). | Medium | Low | Michael M | Proof quality |
| Heritage timeline page. | Medium | Low | — | Brand |
| Self-hosted, lazy video; `<picture>` responsive images. | Medium | Low | Gabriel (AVIF) | Performance |
| Style guide + design-token system (typography, palette, components, motion, accessibility). | High | Medium | — | Consistency |

### P3 — Future

| Recommendation | Impact | Effort | Objective |
|---|---|---|---|
| Retailer inventory feed → "Available at retailers near you" on cards and PDP. | High | High | Retailer traffic |
| Virtual consultation booking with video. | Medium | Medium | Conversion |
| Ring-style finder (3-question quiz) feeding wishlist. | Medium | Medium | Discovery |
| Ring size finder tool. | Low | Low | Confidence |
| A/B programme once analytics baseline exists (hero variants, price-framing variants, CTA order). | High | Medium | Optimisation |
| Personalised "recently viewed / continue where you left off" on return visit. | Medium | Medium | Return conversion |

### 16.1 Quick wins (no redesign required)

1. Remove `maximum-scale=1, user-scalable=0`.
2. Fix the six copy defects listed above.
3. De-duplicate filter values; close price-range gaps; hide internal sort options.
4. Give the hero three different messages or reduce to one.
5. Add a "Shop by Shape" row to the top of the Engagement PLP using the existing icons and the existing "Center Stone Cut" filter URLs.
6. Move "The A.JAFFE Promise" strip directly under the hero.
7. Change the appointment page title and H1; pass the product style number into the form when opened from a PDP.
8. Curate the homepage celebrity carousel to 8 and caption the piece worn.
9. Real `og:image`; drop placeholder price meta; drop `meta keywords`.
10. Lazy-load Vimeo embeds with poster images.

### 16.2 Redesign phase

Style guide → homepage → header/mega menu/mobile drawer → Engagement PLP + cards + filters → PDP → Book-a-Showing flow → Wedding Bands PLP → collection/comfort pages → retailer pages → guides. Delivered as standalone HTML previews per page (375 / 768 / 1280), reviewed on Netlify Drop, then implemented in the existing Hyvä theme.

### 16.3 Future optimisation

Retailer inventory integration, virtual consultations, style finder, analytics baseline and A/B programme, personalisation.

---

## 17. Client-facing summary

### What we found

1. Your best proof — 130 years in New York, 43 stages of hand craftsmanship, patented rings that don't spin, nickel-free metals, certified sourcing, and 38 red-carpet wearers — is all on the site. It is just not where a shopper needs it.
2. A shopper cannot start by choosing a diamond shape, which is how most engagement shoppers start. Gabriel & Co., VRAI and Blue Nile all lead with it.
3. The homepage tells your story three times before it offers a single product or category to explore.
4. Product cards and product pages show no price and no way to save a ring, so a shopper cannot build a shortlist or judge fit for budget.
5. The product page presents metal choices as a sentence, cuts its own description off mid-word, and places three forms between the ring and its details.
6. Filters contain duplicates (four versions of "Quilts®", "Diamond Band" and "Diamond Bands") and skip price ranges.
7. The appointment page is titled "Consumer Leads" and does not know which ring, which retailer or which day the customer wants.
8. Pinch-zoom is switched off on every page — a legal accessibility issue and a real problem when the product is a pavé setting.
9. Your matching-band link and "Personalize this ring" are the right ideas, delivered as small text links.
10. None of this needs a new platform. Gabriel & Co. runs on the same Magento/Hyvä stack you already have.

### What we recommend

- A five-item navigation with Shape, Style, Collection and Metal entry points, and "Find a Retailer" / "Book a Showing" always visible.
- A homepage that opens with one campaign story, a trust strip, four category doors and a shape row — then tells the Quilts® / Signature Shank® story once, well.
- Product cards with a price frame, a save heart, shape availability and metal swatches.
- A product page with metal and shape selectors, the proof block at the top, a "Complete the set" band module in the same metal, and one "Book a showing" button that already knows the ring.
- A booking flow that lets the customer pick the retailer, the date and — optionally — a virtual consultation.
- Pages for each shape, style, collection and patented feature, and retailer pages by state and city, so search engines and AI assistants can find you for "ring that doesn't spin" as well as "oval engagement ring".
- A style guide so every page shares the same quiet, exact, warm look.

### Why this will help

Shoppers who can find, save and evaluate a ring online arrive at your retailers already decided, and retailers receive appointments that name the ring and the metal. The brand reads as the house it is — precise, established, confident — rather than as a catalogue with brochure copy. Search and AI discovery improve because the site finally has pages for the things people search for. Accessibility risk is removed.

### What the new experience should feel like

Opening ajaffe.com should feel like walking into a quiet New York atelier where someone already knows what you came for. The first screen tells one story and offers one door. Every ring you touch shows you its shape, its metals, roughly what it costs and why it will fit better than any other — and the button to see it in person is never more than one tap away. The site shows fewer things, larger, and every word on it is correct.

### Top priorities (first actions)

1. Quick wins this month: zoom, copy fixes, filter clean-up, shape row on the PLP, trust strip under the hero.
2. Decide the price-display policy with your retail partners (from-price vs. tier).
3. Approve the style guide direction (typography, palette, photography brief for the Quilts® / Signature Shank® views).
4. Redesign in this order: homepage → navigation → engagement PLP/cards → PDP → booking flow.
5. Build the comfort-engineering pages and shape/style landing pages alongside the redesign so SEO gains land at launch.

---

## 18. Final principles applied

- Preserve the brand: every recommendation uses A.JAFFE's own collections, patents, vocabulary and retailer model.
- No clone: Gabriel's discovery architecture, Tacori's decision support and Michael M's house voice are principles here, not layouts.
- Every major recommendation states why it matters and what it is expected to do.
- Verified observations are separated from interpretation throughout; anything not seen is marked Not verified.
- Meaningful over decorative: the P0 list contains no visual changes at all.
- Each recommendation answers "does this solve a real customer or business problem for A.JAFFE?" — those that did not (gifts by birthstone, promotional banners, quick-add rails, 40-facet filters) were excluded.

---

*Prepared by QualDev for A.JAFFE. Observations dated 9 September 2026. Sites change; verify any specific claim against the live pages before presenting externally.*
