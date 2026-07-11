# Align & Scale Solutions — Website Redesign Audit

**Date:** 12 July 2026
**Repository:** https://github.com/mthairu254/alignandscale-site.git
**Branch:** main

---

## 1. Factual Risks Found in the Former Website

| Issue | Location | Action Taken |
|-------|----------|--------------|
| Fake client logo images referenced (client-hashi.png, etc.) | experience.html | Removed; replaced with text-based cards |
| Invented tagline: "transformative healthcare consultancy" | clients.html old | Removed; page converted to redirect |
| Copyright year 2025 | clients.html old | Updated to 2026 in all pages |
| External AOS animation library loaded from CDN | clients.html old | Removed; not used in redesigned site |
| Invented social media links in footer | Multiple pages | Removed; no social links displayed |
| No invented testimonials, statistics, or performance claims found | All redesigned pages | Verified clean |

---

## 2. Unsupported Content Removed

- Fake client logo images (client-hashi.png, client-hope.png, client-robins.png, client-maua.png, client-caremark.png, client-springcrest.png) — none existed in the images/ directory
- AOS animation library dependency
- Old clients.html content (invented tagline, outdated structure)

---

## 3. Inaccurate Information Corrected

- **Location reference:** Changed "institutions outside Nairobi" to "institutions requiring flexible engagement models or located outside major urban centres" in services.html
- **Copyright year:** Confirmed 2026 across all pages
- **Footer link text:** Changed "Terms of Service" to "Terms of Use" for consistency with page title

---

## 4. Technical Issues Identified and Fixed

| Issue | Fix Applied |
|-------|-------------|
| Favicon references pointed to non-existent files (favicon-32.png, favicon-16.png, favicon-180.png) | Updated to reference existing files: favicon.png, favicon-192x192.png |
| No robots.txt | Created with crawl directives |
| No sitemap.xml | Created with 7 public pages |
| No custom 404 page | Created 404.html |
| clients.html had old content | Converted to redirect page to experience.html |
| Missing Twitter card metadata on about.html, services.html | Added |
| Missing og:site_name on some pages | Added |
| Manifest.json referenced non-existent icon filenames | Updated to match existing files |

---

## 5. Accessibility Concerns Identified and Fixed

| Concern | Fix Applied |
|---------|-------------|
| Missing focus-visible styles | Added `a:focus-visible`, `button:focus-visible`, `input:focus-visible`, `textarea:focus-visible`, `select:focus-visible` with 2px teal outline |
| No prefers-reduced-motion handling | Added `@media (prefers-reduced-motion: reduce)` — disables animations, transitions, and hero slideshow |
| Mobile menu missing aria-controls | Added `aria-controls="navLinks"` to all hamburger buttons |
| Mobile menu missing Escape key handling | Added keydown listener — Escape closes menu, returns focus to hamburger |
| Mobile menu links don't close menu | Added click handlers on all nav links to close menu |
| Body scrolling not prevented when menu open | Added `document.body.style.overflow = 'hidden'` when menu active |
| Decorative emoji icons not hidden from screen readers | Added `aria-hidden="true"` to all decorative elements |
| Breadcrumb missing ARIA labels | Added `aria-label="Breadcrumb"` and `aria-current="page"` |
| Nav links missing role attributes | Added `role="menubar"` to nav container, `role="menuitem"` to links |
| Heading hierarchy on thank-you page | Verified logical h1 → h2 flow |

---

## 6. SEO Gaps Identified and Fixed

| Gap | Fix Applied |
|-----|-------------|
| No robots.txt | Created with Allow/Disallow rules and sitemap reference |
| No sitemap.xml | Created with 7 public URLs |
| Sitemap missing privacy.html and terms.html | Added both pages |
| Missing Twitter card metadata on about.html, services.html | Added summary_large_image cards |
| Missing og:site_name on multiple pages | Added to all public pages |
| clients.html should not be indexed | Set `noindex, follow` meta robots; added to robots.txt Disallow |
| No schema.org on experience.html | Added WebPage schema |
| No schema.org on privacy.html | Not needed for policy pages (no business data to expose) |
| Canonical URLs verified | All pages have correct canonical tags |
| Unique title tags verified | All pages have unique, descriptive titles |
| Meta descriptions verified | All pages have unique meta descriptions |

---

## 7. Improvements Implemented

### Design
- Premium corporate design system with Playfair Display + Inter typography
- White content backgrounds with light-grey alternates
- Navy reserved for hero, navbar, footer, CTA sections
- Teal accents for buttons, links, and highlights
- Clean card layouts with subtle borders and hover states
- Professional, executive, timeless appearance
- No glassmorphism, neon, gaming aesthetics, or excessive animation

### Content
- All content uses only verified information
- No invented testimonials, statistics, client numbers, or performance claims
- Experience page uses only confirmed client names
- Confidentiality statement included on Experience page
- Privacy Policy and Terms of Use pages created

### Technical
- Semantic HTML5 with ARIA attributes
- Schema.org structured data on key pages
- Open Graph and Twitter Card metadata on all public pages
- Canonical URLs on all pages
- Custom 404 page
- robots.txt and sitemap.xml
- PWA manifest updated

### Accessibility
- Visible keyboard focus indicators
- prefers-reduced-motion support
- Keyboard-accessible mobile menu (Escape, focus management)
- Meaningful alt text on all images
- ARIA labels on navigation, breadcrumbs, and interactive elements
- Logical heading hierarchy
- Sufficient colour contrast (verified against WCAG AA)

### Forms
- Netlify form with honeypot spam protection
- Full name, email, phone, organisation, service selection, preferred contact method, message
- Privacy consent checkbox required
- Information usage statement displayed
- Action points to thank-you.html

---

## 8. Unresolved Matters Requiring Confirmation

| Item | Status | Action Needed |
|------|--------|---------------|
| Client names: Hashi Medical Centre, Maua Cottage Hospital, Robins Healthcare, Caremark Hospital | Retained per user instruction | Confirm these 4 are correct; Hope Renal Centre and Springcrest Medical Centre removed from named list |
| og-image.png | Referenced but does not exist in images/ | Create or provide OG image for social sharing |
| Hero stock images (hero1-4.jpg) | Exist in images/ | Confirm they reflect African healthcare professionals |
| logo.png | Exists | Confirm it is current and correct |
| favicon.png | Exists | Confirm it is current and correct |
| Privacy Policy / Terms of Use legal review | Not reviewed by legal counsel | Recommend professional legal review before publication |

---

## 9. Temporary Stock-Image Locations

| File | Location | Purpose |
|------|----------|---------|
| hero1.jpg | images/hero1.jpg | Hero slideshow slide 1 |
| hero2.jpg | images/hero2.jpg | Hero slideshow slide 2 |
| hero3.jpg | images/hero3.jpg | Hero slideshow slide 3 |
| hero4.jpg | images/hero4.jpg | Hero slideshow slide 4 |
| hero-bg.jpg | images/hero-bg.jpg | Hero background (unused in current design) |

All stock images should be replaced with photographs showing African healthcare professionals, hospital leadership, board meetings, strategic planning, healthcare operations, organisational development, and professional collaboration.

---

## 10. Client Names Retained and Why

| Client Name | Retained | Reason |
|-------------|----------|--------|
| Hashi Medical Centre | Yes | Explicitly confirmed by user |
| Maua Cottage Hospital | Yes | Explicitly confirmed by user |
| Robins Healthcare | Yes | Explicitly confirmed by user |
| Caremark Hospital | Yes | Explicitly confirmed by user |
| Hope Renal Centre | Removed from named list | Not in the confirmed list for this iteration; engagement described generically |
| Springcrest Medical Centre | Removed from named list | Not in the confirmed list for this iteration; engagement described generically |

---

## 11. Files Created, Modified, Redirected, or Removed

### Modified
| File | Changes |
|------|---------|
| index.html | Full redesign — 7-section homepage, updated nav/footer, improved JS, fixed favicons, added ARIA |
| about.html | Full redesign — mission/vision/values/methodology, updated nav/footer, improved JS, fixed favicons |
| services.html | Full redesign — 10 expanded services, updated nav/footer, improved JS, fixed favicons |
| experience.html | Full redesign — text-based client cards, required sections, confidentiality statement |
| contact.html | Full redesign — service dropdown, preferred contact method, privacy consent, info statement |
| thank-you.html | Updated nav/footer, improved JS, fixed favicons |
| styles.css | Complete design system — premium corporate theme, accessibility improvements |
| manifest.json | Updated theme color, icons, description |
| sitemap.xml | Added privacy.html and terms.html |
| robots.txt | Added clients.html to Disallow |

### Created
| File | Purpose |
|------|---------|
| privacy.html | Privacy Policy page |
| terms.html | Terms of Use page |
| 404.html | Custom error page |
| AUDIT.md | This audit document |

### Redirected
| File | Redirects To | Method |
|------|-------------|--------|
| clients.html | experience.html | Meta refresh + canonical + JavaScript |

---

## 12. Verification Summary

- **No DNS, Netlify, or Zoho settings changed** — confirmed
- **No commits or pushes made** — confirmed
- **No invented testimonials, statistics, or performance claims** — verified across all pages
- **All client names verified against user-provided list** — confirmed
- **Location references: Murang'a, Kenya** — verified across all pages
- **Copyright year: 2026** — verified across all pages
- **Navigation consistent across all 9 pages** — verified
- **Footer consistent across all 9 pages** — verified
- **Form action points to thank-you.html** — verified
- **Honeypot field present** — verified
- **Form-name hidden input present** — verified
