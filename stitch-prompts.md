# Stitch Prompt — World Housing Spain Refinements

Use these prompts in your Google Stitch project to regenerate/improve each screen. Copy and paste the relevant prompt for each screen.

---

## Screen 1: Homepage

```
Refine the World Housing Spain homepage with these improvements:

ACCESSIBILITY:
- Add a skip-to-content link at the very top of the page (sr-only, visible on focus)
- Add proper ARIA labels to all interactive elements
- Add alt text to all images (descriptive, not generic)

NAVIGATION:
- Add id="open-mobile-nav" to the hamburger menu button
- Add aria-expanded, aria-controls attributes to mobile nav toggle
- Implement scroll-aware sticky header that adds shadow on scroll
- Add body scroll lock when mobile nav is open
- Add Escape key support to close mobile nav

TYPOGRAPHY:
- Change hero title from text-[3.25rem] to text-4xl md:text-[3.25rem] for mobile
- Ensure all headings scale properly on mobile (max-width constraints)

FORMS:
- Add required attribute to First Name, Last Name, Email, and Message fields
- Add proper form labels (visible, not just placeholder)
- Add focus ring styles on all form inputs

FOOTER:
- Update copyright year to 2026
- Ensure all footer links are present: Properties, Company, Legal sections
- Add social media links (Instagram, LinkedIn)

IMAGES:
- Replace generic alt text with descriptive text (e.g., "Luxury villa with infinity pool overlooking the Mediterranean Sea")
- Add loading="lazy" to below-fold images

LOGO:
- Use the single logo URL from the Global section below
- Header (light bg): logo should be black — class="h-12 w-auto brightness-0"
- No other logo variants or images

CONTENT:
- Keep "The Azure Sanctuary" editorial tone
- Maintain warm neutral color palette (#fdf8f0 surface, #2c6e49 primary, #745b24 secondary gold)
- Keep EB Garamond for headlines, Manrope for body text
```

---

## Screen 2: Luxury Collection

```
Refine the Luxury Collection page with these improvements:

LOCALIZATION (CRITICAL):
The current page shows non-Spain properties. Replace with Spain/Costa Blanca locations:

1. Replace "Japanese Zen Retreat" with:
   - Title: "Andalusian Cortijo"
   - Location: Moraira
   - Stats: 6 Bed · 5 Bath · 750 m² · 12,000 m² Plot
   - Price: €4,800,000
   - Features: Private Vineyard, Guest Cottage, Wine Cellar, Olive Grove
   - Description: "A meticulously restored Andalusian estate nestled among ancient olive trees, with panoramic views stretching from the mountains to the Mediterranean."

2. Replace "Greek Island Villa" with:
   - Title: "Costa Blanca Clifftop Villa"
   - Location: Jávea
   - Stats: 4 Bed · 4 Bath · 380 m² · Direct Sea Access
   - Price: €3,200,000
   - Features: Glass Elevator, Rooftop Lounge, Home Cinema, Smart Home
   - Description: "Perched dramatically on the cliffs of Jávea, this architectural marvel offers uninterrupted 270-degree views of the Mediterranean."

3. Replace "Alpine Chalet" with:
   - Title: "Mallorcan Finca"
   - Location: Altea Hills
   - Stats: 5 Bed · 5 Bath · 520 m² · 8,000 m² Plot
   - Price: €2,900,000
   - Features: Pool House, Tennis Court, Orchard, Staff Quarters

4. Replace "Tropical Beach Villa" with:
   - Title: "Ibizan White Villa"
   - Location: Benissa Coast
   - Stats: 7 Bed · 6 Bath · 680 m² · Beachfront
   - Price: €5,500,000
   - Features: Beach Access, Spa Suite, Outdoor Kitchen, DJ Booth

ACCESSIBILITY:
- Add skip-to-content link
- Add descriptive alt text to all images

FOOTER:
- Update copyright to 2026
- Ensure full footer with all sections

TYPOGRAPHY:
- Use responsive text-4xl sm:text-5xl md:text-7xl for hero

NAVIGATION:
- Implement working mobile hamburger menu with body scroll lock

LOGO:
- Use the single logo URL from the Global section
- Header (light bg): black logo → class="h-12 w-auto brightness-0"
- Remove any other logo variants
```

---

## Screen 3: Property Listings

```
Refine the Property Listings page with these improvements:

ACCESSIBILITY:
- Add skip-to-content link
- Add descriptive alt text to all property images

FILTER BAR:
- Add toggle functionality for "More Filters" button
- Add expanded filter panel with additional options (area, pool, sort)
- Add aria-expanded state to filter toggle button
- Add focus ring styles to all select elements

PROPERTY CARDS:
- Ensure consistent hover effects: shadow-elevation-1 hover:shadow-elevation-2 transition-all duration-300
- Add rounded-xl to all cards for consistency
- Featured card should span 2 columns on desktop

NAVIGATION:
- Add working mobile hamburger menu
- Add aria-expanded, aria-controls to toggle button
- Implement body scroll lock and Escape key support

FOOTER:
- Update copyright to 2026
- Ensure full 4-column footer

TYPOGRAPHY:
- Maintain editorial headline style with EB Garamond
- Keep Manrope for body and UI elements

LOGO:
- Use the single logo URL from the Global section
- Header (light bg): black logo → class="h-12 w-auto brightness-0"
- Remove any other logo variants

COLORS:
- Primary green: #2c6e49
- Secondary gold: #745b24
- Surface: #fdf8f0
- Maintain Material Design 3 token system
```

---

## Screen 4: Property Detail

```
Refine the Property Detail page with these improvements:

CRITICAL FIX:
- In the <style> block, replace the hardcoded color #C9A96A with var(--md-sys-color-secondary)
  Change: background: #C9A96A;
  To: background: var(--md-sys-color-secondary);

ACCESSIBILITY:
- Add skip-to-content link
- Add descriptive alt text to all gallery images
- Add ARIA labels to gallery navigation

GALLERY:
- Ensure first image spans 2 columns on desktop, 1 on mobile
- Add "View all photos" button functionality hint

INQUIRY FORM:
- Add required attribute to First Name, Last Name, Email, and Message fields
- Add proper form labels
- Add focus ring styles

STICKY SIDEBAR:
- Ensure price/inquiry card sticks on scroll (lg:sticky lg:top-28)
- Add border separation from main content

NAVIGATION:
- Add working mobile hamburger menu
- Implement scroll-aware header shadow

FOOTER:
- Update copyright to 2026
- Ensure full footer with all sections

MAP:
- Replace hardcoded #C9A96A with CSS variable reference
- Keep the decorative map pin style

LOGO:
- Use the single logo URL from the Global section
- Header (light bg): black logo → class="h-12 w-auto brightness-0"
- Remove any other logo variants

STRUCTURED DATA (for SEO):
- Add JSON-LD schema for RealEstateListing:
  - name, description, price, address
  - image, numberOfBedrooms, numberOfBathroomsTotal
  - floorSize, lotSize
```

---

## Screen 5: Area Guide

```
Refine the Area Guide page with these improvements:

ACCESSIBILITY:
- Add skip-to-content link
- Add descriptive alt text to all images
- Add ARIA labels to interactive elements

CONTENT:
- Keep Altea as the focus area
- Maintain editorial/lifestyle tone
- Keep statistics: Population 24,000+, 300+ Sunny Days, 6 km Coastline
- Maintain market overview with price data

NAVIGATION:
- Add working mobile hamburger menu
- Implement scroll-aware header shadow
- Add proper ARIA attributes to mobile nav

BENTO GRID:
- Ensure first item spans 2 columns and 2 rows on desktop
- Maintain consistent hover effects on all highlight cards

PROPERTY CARDS:
- Keep consistent card styling with other screens
- Ensure hover effects match: shadow-elevation-1 hover:shadow-elevation-2

FOOTER:
- Update copyright to 2026
- Ensure full 4-column footer with all sections

TYPOGRAPHY:
- Use responsive text scaling for hero: text-5xl md:text-7xl
- Keep EB Garamond for display/headlines
- Keep Manrope for body text

COLORS:
- Maintain Material Design 3 token system
- Primary: #2c6e49 (green)
- Secondary: #745b24 (gold)
- Surface: #fdf8f0 (warm cream)

LOGO:
- Use the single logo URL from the Global section
- Header (light bg): black logo → class="h-12 w-auto brightness-0"
- Remove any other logo variants
```

---

## LOGO (Critical — Apply to All Screens)

```
LOGO USAGE:
- Use ONLY this logo URL across all screens (remove any other logo variations):
  https://lh3.googleusercontent.com/aida-public/AB6AXuC0bjVRvUGRZirTpt7Q2kYcHsi0-oH8D6Fl5WKbqzATDyyRzDThLCX2G6YUsBtdymKG4Kf3_gLbyTsw1Z2Zx6_nbGX2QJsQ0jfV_MTWOXh4LwruhNhdFcGAWpaIZOmDbo_3Dr4DyH1cc6MbhDkDoSuNkm-M3-FrBHLNKXCqw9Nv2gVR7mtCMhEP_wtBP8IcHluqmVjAY7ET1ogv4IQlskwvH0BILvzv3YF2GDanT9dCA52ML5s6flvg3unk9GS8eSczCkAPW52BXSL3

- On LIGHT backgrounds (header, footer, surface containers):
  Logo must appear BLACK → set class="h-12 w-auto brightness-0"
  
- On DARK backgrounds (hero overlays, dark sections):
  Logo must appear WHITE → set class="h-12 w-auto brightness-0 invert"

- In the header (always light bg): logo stays black at all times
- Remove any other logo images or variants from all screens
```

---

## Global Design Tokens (Apply to All Screens)

```
COLOR PALETTE:
- Primary: #2c6e49 (forest green)
- Secondary: #745b24 (warm gold)
- Tertiary: #1a6666 (teal)
- Surface: #fdf8f0 (warm cream)
- Surface Container: #f3ede1
- On Surface: #1d1b16

TYPOGRAPHY:
- Headlines: "EB Garamond", serif
- Body: "Manrope", sans-serif

SPACING:
- Section padding: py-24 lg:py-32
- Container max-width: 7xl (80rem)
- Container padding: px-6 lg:px-12

COMPONENTS:
- Cards: rounded-xl, shadow-elevation-1, hover:shadow-elevation-2
- Buttons: rounded-lg, tracking-wide, uppercase, text-sm
- Inputs: rounded-lg, border-outline-variant, focus:border-primary
- Badges: rounded-full, text-xs, tracking-wide, uppercase

INTERACTIONS:
- Image hover: scale-105 transition-transform duration-700
- Button hover: opacity/90 transition-colors
- Link hover: color transition-colors
- Card hover: shadow-elevation-2 transition-shadow

ANIMATIONS:
- Intersection Observer for fade-in on scroll
- Staggered reveal for grid items
- Smooth scroll for anchor links
```

---

## Usage Instructions

1. Open your Stitch project (ID: 14331507145566872330)
2. Select the screen you want to refine
3. Click "Edit with AI" or the equivalent prompt input
4. Copy and paste the relevant prompt from above
5. Review the generated output
6. Iterate as needed

**Note:** The most critical fix is the Luxury Collection localization (replacing non-Spain properties) and the Property Detail hardcoded color (#C9A96A → CSS variable).
