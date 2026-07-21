# World Housing Spain — Design System

Brand reference for AI agents building pages for the World Housing Spain website.
All pages use Tailwind CSS via CDN. No build step, no standalone CSS files.

---

## Brand Identity

**Company:** World Housing Spain C.B. — luxury real estate agency, Costa Blanca, Spain.
**Positioning:** Premium, editorial, Mediterranean. Not corporate. Not flashy. Quiet luxury.
**Tone:** Sophisticated, warm, trustworthy. Think Architectural Digest meets coastal living.
**Logo:** `https://worldhousingspain.eu/wp-content/uploads/2024/09/whs-logo-retina-500.png` — render with `brightness-0` (forced black).

---

## Color Palette — Material Design 3 Tokens

The site uses M3 token naming mapped to Tailwind via CSS custom properties.

### Primary
| Token | Hex | Usage |
|---|---|---|
| `primary` | `#2C6E49` | Deep olive green — CTAs, links, active states, badges |
| `on-primary` | `#FFFFFF` | Text on primary backgrounds |
| `primary-container` | `#b7f1c6` | Light green — avatar backgrounds, accent containers |
| `on-primary-container` | `#002110` | Text on primary containers |

### Secondary
| Token | Hex | Usage |
|---|---|---|
| `secondary` | `#745B24` | Deep gold/bronze — secondary accents |
| `on-secondary` | `#FFFFFF` | Text on secondary backgrounds |
| `secondary-container` | `#FFE08C` | Light gold — alternate badges |
| `on-secondary-container` | `#261A00` | Text on secondary containers |

### Tertiary
| Token | Hex | Usage |
|---|---|---|
| `tertiary` | `#1A6666` | Teal — tertiary accent |
| `on-tertiary` | `#FFFFFF` | Text on tertiary |
| `tertiary-container` | `#A4F0EF` | Light teal |
| `on-tertiary-container` | `#002020` | Text on tertiary containers |

### Surface (7-level warm ivory scale)
| Token | Hex | Usage |
|---|---|---|
| `surface` | `#FDF8F0` | Page background — warm off-white |
| `surface-dim` | `#DFD9CD` | Dimmed surface |
| `surface-container-lowest` | `#FFFFFF` | Pure white |
| `surface-container-low` | `#F9F3E7` | Footer, form panels, header default |
| `surface-container` | `#F3EDE1` | Tags, inactive form tabs |
| `surface-container-high` | `#EDE7DB` | Form tab hover |
| `surface-container-highest` | `#E7E2D6` | Image placeholder backgrounds |

### Text & Outline
| Token | Hex | Usage |
|---|---|---|
| `on-surface` | `#1D1B16` | Main text — near-black warm |
| `on-surface-variant` | `#4B4539` | Secondary text |
| `outline` | `#7D7564` | Borders, dividers |
| `outline-variant` | `#CEC5B4` | Light borders, card outlines |

### Hardcoded Accent Colors
| Color | Hex | Usage |
|---|---|---|
| WhatsApp green | `#25D366` | Floating WhatsApp button |
| Google star gold | `#FBBC05` | Review star ratings |
| Selection highlight | `#C9A96A` | `::selection` pseudo-element |
| Dark overlay | `#242321` | Hero overlay (index.html variant) |

---

## Typography

### Font Families
| Role | Font | Tailwind Class |
|---|---|---|
| Headlines / Display | EB Garamond (serif) | `font-display` |
| Body / UI | Manrope (sans-serif) | `font-body` (default) |

Loaded via Google Fonts: EB Garamond 400–700 + italic, Manrope 300–700.

### Type Scale

| Element | Classes | Notes |
|---|---|---|
| Hero H1 | `font-serif text-4xl md:text-[3.375rem] leading-[0.95] font-medium tracking-tight` | |
| Section H2 | `font-display text-4xl lg:text-5xl font-medium tracking-tight` | Second line always `<span class="italic">` |
| Section label | `text-sm font-medium tracking-[0.2em] uppercase text-on-surface/60` | Always above H2 |
| Card H3 | `font-display text-2xl font-medium` | Collection/area cards |
| Property H3 | `font-display text-xl font-medium` | Property cards |
| Stat number | `font-display text-4xl font-medium text-primary` | |
| Stat label | `text-sm text-on-surface/60` | |
| Body | `text-lg text-on-surface/80 leading-relaxed` | |
| Small / meta | `text-sm text-on-surface/50` or `text-xs tracking-[0.15em] uppercase` | |
| Testimonial | `font-display text-2xl lg:text-3xl italic leading-relaxed text-on-surface/90` | |
| Badge | `text-xs font-medium tracking-wide uppercase` | |
| Nav link | `text-sm font-medium tracking-wide uppercase` | |

### Text Color Patterns
- Primary headings: `text-on-surface` (inherited)
- Accent text: `text-primary`
- Subdued: `text-on-surface/60`, `/70`, `/80`, `/85`
- Very subdued: `text-on-surface/50`, `/40`
- On dark: `text-white`, `text-white/80`, `/70`, `/60`

---

## Spacing & Layout

### Container
- Max width: `max-w-7xl` (1280px)
- Horizontal padding: `px-6 lg:px-12` (24px → 48px)

### Section Rhythm
- Standard section: `py-24 lg:py-32` (96px → 128px)
- Footer: `py-16` (64px)
- Section header margin: `mb-16`

### Grid Gaps
- Card grids: `gap-6` or `gap-8`
- Two-column editorial: `gap-16 lg:gap-24`
- Footer columns: `gap-12`
- Form fields: `gap-6`

### Header
- Height: `h-20` (80px)
- Fixed, z-50, backdrop-blur on scroll

---

## Border Radius

| Token | Value | Common Use |
|---|---|---|
| `rounded-lg` | 8px | Buttons, form inputs, form panels |
| `rounded-xl` | 16px | Cards, dropdowns, hero panels |
| `rounded-full` | 9999px | Badges, avatars, chips, social icons |

---

## Elevation (Shadows)

| Token | Definition | Usage |
|---|---|---|
| `shadow-elevation-1` | `0 1px 2px rgba(0,0,0,0.30), 0 1px 3px 1px rgba(0,0,0,0.15)` | Sticky header, form panels |
| `shadow-elevation-2` | `0 1px 2px rgba(0,0,0,0.30), 0 2px 6px 2px rgba(0,0,0,0.15)` | Dropdown menus, card hover |
| `shadow-elevation-3` | `0 4px 8px 3px rgba(0,0,0,0.15), 0 1px 3px rgba(0,0,0,0.30)` | Floating WhatsApp button |

Additional: `shadow-lg shadow-black/5` (header), `shadow-lg shadow-black/10` (CTA buttons).

---

## Component Patterns

### Section Header (used on every section)
```html
<p class="text-sm font-medium tracking-[0.2em] uppercase text-on-surface/60 mb-4">Label</p>
<h2 class="font-display text-4xl lg:text-5xl font-medium tracking-tight mb-16">
  First Line<br><span class="italic">Second Line</span>
</h2>
```

### Card — Property Listing
```html
<a href="#" class="group">
  <div class="relative aspect-[4/3] bg-surface-container-highest overflow-hidden mb-5">
    <img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
    <span class="absolute top-4 left-4 inline-block px-3 py-1.5 text-xs font-medium
      tracking-wide uppercase bg-primary text-on-primary rounded-full">Featured</span>
  </div>
  <p class="text-sm text-on-surface/50 mb-2">Location</p>
  <h3 class="font-display text-xl font-medium mb-3 group-hover:text-primary transition-colors">Name</h3>
  <p class="text-on-surface/70 text-sm leading-relaxed mb-4">3 Bed · 2 Bath · 291 m²</p>
  <p class="font-display text-2xl font-medium">€189,000</p>
</a>
```

### Card — Collection / Area (editorial tall)
```html
<a href="#" class="group relative aspect-[3/4] overflow-hidden bg-surface-container-highest">
  <img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
  <div class="absolute inset-0 bg-gradient-to-t from-surface/90 via-surface/20 to-transparent"></div>
  <div class="absolute bottom-0 left-0 right-0 p-8">
    <p class="text-sm font-medium tracking-wide text-on-surface/60 mb-2">42 Properties</p>
    <h3 class="font-display text-2xl font-medium">Category</h3>
  </div>
</a>
```

### Card — Compact (area grid, content below image)
```html
<a href="#" class="group bg-surface-container-low rounded-xl overflow-hidden
  shadow-elevation-1 hover:shadow-elevation-2 transition-all duration-300 block">
  <div class="aspect-[16/10] overflow-hidden">
    <img class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
  </div>
  <div class="p-5">
    <span class="inline-block px-2.5 py-1 text-[10px] font-medium tracking-wide uppercase
      bg-primary text-on-primary rounded-full mb-2">Badge</span>
    <h3 class="font-display text-2xl font-medium text-on-surface mb-1">Title</h3>
    <p class="text-sm text-on-surface/70 italic mb-3">Subtitle</p>
    <p class="text-sm text-on-surface/60 line-clamp-2">Description text.</p>
    <div class="flex items-center justify-between mt-4 pt-4 border-t border-outline-variant/50">
      <span class="text-xs text-on-surface/50">Meta info</span>
      <span class="text-xs font-medium text-primary tracking-wide uppercase
        group-hover:translate-x-1 transition-transform inline-flex items-center gap-1">
        View Details <span class="material-symbols-outlined text-[14px]">arrow_forward</span>
      </span>
    </div>
  </div>
</a>
```

### Button — Primary CTA
```html
<a class="inline-flex items-center gap-3 px-8 py-4 bg-primary text-white text-sm font-medium
  tracking-wide uppercase rounded-xl hover:bg-[#235a3a] transition-all
  shadow-lg shadow-black/10 hover:shadow-xl hover:shadow-black/15 hover:-translate-y-0.5">
  <span>Label</span>
  <span class="material-symbols-outlined text-[20px]">arrow_forward</span>
</a>
```

### Button — Secondary / Outline
```html
<a class="inline-flex items-center gap-3 px-8 py-4 border-2 border-white/40 text-white/95
  text-sm font-medium tracking-wide uppercase rounded-xl
  hover:bg-white/10 hover:border-white/60 transition-all">
```

### Button — Ghost
```html
<a class="inline-flex items-center gap-3 px-8 py-4 border border-outline-variant
  text-on-surface text-sm font-medium tracking-wide uppercase rounded-lg
  hover:bg-surface-container transition-colors">
```

### Form Input
```html
<input class="w-full px-4 py-3 bg-surface border border-outline-variant rounded-lg
  focus:outline-none focus:border-primary focus:ring-1 focus:ring-primary transition-colors">
```

### Badge / Chip
```html
<span class="inline-block px-3 py-1.5 text-xs font-medium tracking-wide uppercase
  bg-primary text-on-primary rounded-full">Featured</span>
<!-- Alt: bg-secondary-container text-on-secondary-container -->
```

### Review / Testimonial Card
```html
<div class="bg-surface p-6 rounded-xl border border-outline-variant/30">
  <div class="flex items-center gap-3 mb-4">
    <div class="w-10 h-10 rounded-full bg-surface-container-highest flex items-center justify-center">
      <!-- Google SVG -->
    </div>
    <div>
      <p class="font-medium text-sm">Name</p>
      <p class="text-xs text-on-surface/50">N reviews</p>
    </div>
  </div>
  <div class="flex items-center gap-0.5 mb-3">
    <span class="material-symbols-outlined text-[16px] text-[#FBBC05]">star</span> ×5
  </div>
  <p class="text-sm text-on-surface/70 leading-relaxed">Review text</p>
</div>
```

---

## Icons

**System:** Material Symbols Outlined via Google Fonts.

| Icon | Size | Context |
|---|---|---|
| `expand_more` | 16–20px | Dropdown arrows |
| `menu` / `close` | 28px | Mobile nav toggle |
| `arrow_forward` | 14–20px | CTAs, links |
| `star` | 16px | Review ratings (`text-[#FBBC05]`) |
| `sunny` / `pool` / `restaurant` / `golf_course` | 18px | Lifestyle chips |
| `location_on` / `call` / `mail` | 20–24px | Contact info |
| `send` | 20px | Form submit |

**Social icons:** Inline SVGs (Instagram, TikTok, Facebook, LinkedIn, WhatsApp). Size `w-5 h-5` in footer, `w-6 h-6` in mobile nav.

---

## Animations

### Scroll Reveal (IntersectionObserver)
```css
.fade-in { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease-out, transform 0.7s ease-out; }
.fade-in.visible { opacity: 1; transform: translateY(0); }
.fade-in-stagger > * { opacity: 0; transform: translateY(20px); transition: opacity 0.5s ease-out, transform 0.5s ease-out; }
.fade-in-stagger > *.visible { opacity: 1; transform: translateY(0); }
```
Stagger: each child delayed by `i * 100ms`.

### Inline Transitions
- `transition-colors` — all text hover states
- `transition-all duration-300` — header scroll, mobile nav
- `transition-transform duration-700` — image zoom on hover (`group-hover:scale-105`)
- `group-hover:translate-x-1` — arrow slides right on hover
- `hover:-translate-y-0.5` — CTA button lift

---

## Image Patterns

- All images from Unsplash via URL: `?w=800&q=80` (cards), `?w=1920&q=80` (hero)
- Placeholder: `bg-surface-container-highest` behind every image
- Logo: `h-12 w-auto brightness-0` (forced black)
- Hover: `group-hover:scale-105 transition-transform duration-700`

### Gradient Overlays
| Pattern | Context |
|---|---|
| `from-surface/90 via-surface/20 to-transparent` | Collection cards (light) |
| `from-black/70 via-black/20 to-transparent` | Dark overlay cards |
| `from-surface via-surface/40 to-transparent` | Hero (master-template) |
| `from-surface/60 to-transparent` | Editorial images |

---

## Page Structure Pattern

```
<body class="font-body bg-surface text-on-surface antialiased">
  <header fixed, backdrop-blur, border-b>
  <main>
    <section class="py-24 lg:py-32 bg-surface">        ← alternates with
    <section class="py-24 lg:py-32 bg-surface-container-low">  ← these
    ...
  </main>
  <footer class="py-16 bg-surface-container-low border-t border-outline-variant/50">
  <div floating WhatsApp button>
</body>
```

Section backgrounds alternate `bg-surface` ↔ `bg-surface-container-low` for visual rhythm.

---

## WhatsApp Floating Button
```html
<a class="fixed bottom-6 right-6 z-50 flex items-center justify-center w-14 h-14
  bg-[#25D366] text-white rounded-full shadow-elevation-3
  hover:scale-110 transition-transform duration-300"
  href="https://wa.me/34662512994">
  <!-- WhatsApp SVG -->
</a>
```

---

## Contact Information (always present)

- **WhatsApp:** +34 662 51 29 94 (click-to-chat: `https://wa.me/34662512994`)
- **Mobile:** +34 662 51 29 94
- **Landline:** +34 966 14 64 70
- **Email:** worldhousingspain24@gmail.com
- **Address:** Calle Cervantes 25 Bajo, 03130 Santa Pola, Alicante
- **Social:** Instagram `@worldhousingspain`, TikTok `@worldhousing.spain`, Facebook `World Housing Spain`, LinkedIn `world-housing-spain-3a1176385`

---

## Key Rules

1. **EB Garamond for headlines, Manrope for everything else.** Never swap.
2. **Olive green `#2C6E49` is the only primary accent.** Don't introduce new colors.
3. **`rounded-full` for badges, `rounded-xl` for cards, `rounded-lg` for buttons/inputs.**
4. **Images always zoom on hover: `group-hover:scale-105 transition-transform duration-700`.**
5. **Section headers always have an italicized second line.**
6. **Section backgrounds always alternate** between `bg-surface` and `bg-surface-container-low`.
7. **All CTAs are uppercase, tracking-wide, with arrow icons.**
8. **No standalone CSS files.** Everything is Tailwind utilities + inline `<style type="text/tailwindcss">`.
9. **Use `text-on-surface/60` through `/80` for body text hierarchy.** Never use plain gray.
10. **Prices always in `font-display text-2xl font-medium`.**
