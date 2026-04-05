# Design System: Active Theory

## 1. Visual Theme & Atmosphere

Active Theory's website is a full-screen WebGL 3D experience that treats the browser as a cinematic portal — not a document. There are no traditional HTML elements visible; the entire interface is rendered on a WebGL canvas with custom shaders, particle systems, and metallic 3D objects floating in deep space. The design operates on an absolute black void (`#000000`) with iridescent, holographic 3D forms (metallic rings, organic structures, jellyfish) that catch light with chromatic aberration and PBR reflections. Text is rendered as 3D geometry within the scene, not as DOM elements.

The typography uses NBArchitektStd — a monospaced, industrial, architect-blueprint typeface loaded in three weights (Light 300, Regular 400, Bold 700). ALL text is uppercase with generous letter-spacing, creating a terminal/command-line aesthetic that feels like interfacing with a high-tech system. The monospaced character of NBArchitekt means every character occupies equal width, reinforcing the technical, engineered feel — text looks plotted rather than typeset.

What makes Active Theory distinctive is its total rejection of traditional web design. There are no cards (in the DOM sense), no grids, no backgrounds, no borders, no shadows — everything exists in 3D space. Project thumbnails float as rounded-corner planes in a 3D carousel, the navigation is a floating pill with a frosted-glass effect, and category links use an arrow prefix (`->`) like terminal commands. The "Ask me anything..." input field has a thin border with rounded corners, sitting over the 3D scene. The entire experience is scroll-driven, with the camera moving through a 3D environment as the user scrolls — from a hero scene with a metallic logo and particles, through an underwater-like transition zone, past the "CREATIVE DIGITAL EXPERIENCES" text wall, and into the work gallery.

**Key Characteristics:**
- Pure black void (`#000000`) with WebGL-rendered 3D content — zero traditional layout
- NBArchitektStd — monospaced architect-blueprint typeface, all uppercase
- Iridescent, holographic 3D objects with chromatic aberration and PBR materials
- Floating particle systems (green-gold and purple-white palettes)
- 3D project card carousel with rounded-corner planes in perspective
- Frosted-glass pill navigation with glow effect
- Terminal-style category links with `->` arrow prefix
- Scroll-driven 3D camera movement through scenes
- Purple/violet accent for interactive category links
- Ambient music player integrated into the experience

## 2. Color Palette & Roles

### Primary
- **Void Black** (`#000000`): The infinite background — pure black, the canvas of space
- **Pure White** (`#ffffff`): Primary text, navigation labels, headings — high contrast on void

### Interactive & Accent
- **Violet Link** (`#b8a0d4`): Category navigation links (`-> WEBSITES`, `-> INSTALLATIONS`) — a muted lavender-violet
- **Violet Hover** (`#d4c4e8`): Hover state for category links — brightened violet
- **Glow Cyan** (`#00e5ff`): Subtle accent glow on 3D logo ring and navigation pill edge — electric cyan highlight
- **Warm Amber** (`rgba(200, 180, 100, 0.6)`): Particle system warm tones — gold-green particles in hero scene

### Surface
- **Frosted Glass** (`rgba(255, 255, 255, 0.08)`): Navigation pill background — barely visible, glass-like
- **Frosted Border** (`rgba(255, 255, 255, 0.2)`): Navigation pill and input border — subtle white outline
- **Input Surface** (`rgba(255, 255, 255, 0.05)`): "Ask me anything" input background
- **Input Border** (`rgba(180, 160, 210, 0.4)`): Input field border — violet-tinted

### 3D Material Colors
- **Holographic Base** (`#8090a0`): Base metallic color for 3D objects — cool steel
- **Chromatic Red** (`#ff3050`): Chromatic aberration highlight — red channel split
- **Chromatic Blue** (`#3050ff`): Chromatic aberration highlight — blue channel split
- **Iridescent Teal** (`#40e0d0`): Surface iridescence on metallic rings
- **Particle Green** (`#80a040`): Green-tinted particles in hero environment
- **Particle Purple** (`#c080d0`): Purple-tinted particles in transition zone

### Text Opacity Scale
- **Full** (`rgba(255, 255, 255, 1.0)`): Navigation labels, headings
- **Strong** (`rgba(255, 255, 255, 0.85)`): Body descriptions, "FOUNDED IN 2012"
- **Medium** (`rgba(255, 255, 255, 0.5)`): "SCROLL DOWN" indicator
- **Subtle** (`rgba(255, 255, 255, 0.3)`): Placeholder text, disabled states

## 3. Typography Rules

### Font Family
- **Universal**: `NBArchitektStd`, fallbacks: `"Courier New", Courier, monospace`
- **Weights**: Light (300), Regular (400), Bold (700)
- **Format**: WOFF2 primary, WOFF and OTF fallbacks

*Note: NBArchitektStd is a custom monospaced typeface by Neubau Berlin. For external implementations, `IBM Plex Mono`, `Space Mono`, or `JetBrains Mono` serve as close substitutes.*

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | NBArchitektStd | 96px+ (6rem+) | 700 | 0.95 (tight) | 8px+ | `text-transform: uppercase`, 3D-rendered text |
| Section Heading | NBArchitektStd | 48px (3rem) | 700 | 1.00 (tight) | 4px | `text-transform: uppercase` |
| Nav Label | NBArchitektStd | 14px (0.88rem) | 700 | 1.00 (tight) | 2px | `text-transform: uppercase`, "WORK", "CONTACT" |
| Category Link | NBArchitektStd | 14px (0.88rem) | 400 | 1.70 | 1.5px | `text-transform: uppercase`, violet color, `->` prefix |
| Body Description | NBArchitektStd | 13px (0.81rem) | 300 | 1.60 | 1.2px | `text-transform: uppercase`, company description text |
| Input Placeholder | NBArchitektStd | 12px (0.75rem) | 300 | 1.00 | 1.5px | `text-transform: uppercase`, "ASK ME ANYTHING..." |
| Scroll Indicator | NBArchitektStd | 12px (0.75rem) | 400 | 1.00 | 3px | `text-transform: uppercase`, "SCROLL DOWN" |
| Project Title | NBArchitektStd | 36px (2.25rem) | 700 | 1.00 | 3px | `text-transform: uppercase`, rendered on 3D card |
| Micro Label | NBArchitektStd | 10px (0.63rem) | 300 | 1.00 | 1.5px | `text-transform: uppercase`, metadata, year |

### Principles
- **Universal uppercase**: Every single text element uses `text-transform: uppercase`. There is no sentence case or title case anywhere in the design. This creates a systematic, engineered voice.
- **Monospaced identity**: NBArchitektStd's fixed-width characters mean text aligns in columns naturally. The "architect blueprint" aesthetic makes every label feel precisely plotted.
- **Generous letter-spacing everywhere**: Even body text has positive letter-spacing (1.2px+). Display text pushes to 8px+. This wide tracking is the defining typographic gesture — text breathes across the void.
- **Three weights, strict roles**: Bold (700) for navigation and headings, Regular (400) for interactive labels, Light (300) for body descriptions. No weight blending or medium weights.
- **3D text rendering**: Hero text ("CREATIVE DIGITAL EXPERIENCES") is rendered as actual 3D geometry with depth, not as DOM text. The 3D text catches light and has subtle materiality.

## 4. Component Stylings

### Navigation Pill

**Frosted Glass Pill**
- Background: `rgba(255, 255, 255, 0.08)` (frosted glass)
- Border: `1px solid rgba(255, 255, 255, 0.2)`
- Radius: 40px (full pill)
- Padding: 12px 32px
- Position: Fixed top-right
- Backdrop-filter: `blur(12px)` (glass effect)
- Glow: subtle `box-shadow: 0 0 20px rgba(0, 229, 255, 0.1)` on bottom edge
- Contains: "WORK" and "CONTACT" labels separated by a horizontal line
- Divider: thin horizontal line (`rgba(255, 255, 255, 0.3)`) between labels

### Category Navigation

**Terminal-Style Links**
- Text: Violet (`#b8a0d4`)
- Size: 14px NBArchitektStd Regular
- Prefix: `->` arrow before each category name
- Spacing: ~30px vertical gap between items
- Hover: brightens to `#d4c4e8`, slight glow
- Position: Fixed left side, vertically stacked
- Categories: WEBSITES, INSTALLATIONS, XR / VR / AI, MULTIPLAYER, GAMES

### Cards & Containers

**3D Project Cards**
- Shape: Rounded rectangle planes in 3D space
- Radius: ~20px (visible rounded corners on 3D planes)
- Content: Full-bleed project screenshot/video as texture
- Arrangement: 3D carousel — cards fan out in perspective depth
- Active card: centered, largest, facing camera
- Inactive cards: rotated, scaled down, fading into depth
- No border, no shadow — depth comes from 3D perspective
- Project title overlaid on card in white uppercase text

### Input Field

**AI Chat Input**
- Background: `rgba(255, 255, 255, 0.05)`
- Border: `1px solid rgba(180, 160, 210, 0.4)` (violet tint)
- Radius: 30px (pill shape)
- Padding: 10px 20px
- Text: NBArchitektStd Light 12px, uppercase, white
- Placeholder: "ASK ME ANYTHING..." in `rgba(255, 255, 255, 0.4)`
- Position: Below category navigation

### Scroll Indicator

**"SCROLL DOWN" Label**
- Text: Pure white at 50% opacity
- Size: 12px NBArchitektStd Regular
- Letter-spacing: 3px
- Position: Center-top of viewport
- Animation: subtle fade pulse

### Music Player

**Ambient Audio Controls**
- Previous/Next buttons: minimal, icon-based
- Song info: "Song--Artist" format
- Position: Bottom of viewport
- Style: minimal, near-invisible controls

## 5. Layout Principles

### Spacing System
- No traditional spacing system — content is positioned in 3D space
- Screen-space UI elements use generous margins from viewport edges
- Navigation pill: ~40px from top, ~40px from right
- Category nav: ~50px from left, ~630px from top
- Input field: ~50px from left, below category list

### Grid & Container
- **No grid.** The site has no 2D layout grid. Content exists in 3D space with camera-relative positioning.
- Screen-space HUD elements (nav pill, category links, input) are positioned absolutely relative to viewport edges
- The 3D scene itself is a continuous environment — no sections, no containers

### Whitespace Philosophy
- **The void IS the design**: The pure black background is not empty space — it's the infinite void of a 3D environment. Traditional whitespace concepts don't apply because the "empty" areas are actually 3D depth filled with particles, distant objects, and atmospheric fog.
- **Cinematic framing**: Content is framed by the 3D camera, not by CSS margins. The camera positions text and objects relative to each other in 3D space.
- **HUD overlay pattern**: The only screen-space elements (nav, categories, input) are positioned like a heads-up display — minimal, peripheral, never competing with the 3D content.

### Border Radius Scale
- Pill (40px): Navigation container — fully rounded
- Input (30px): Chat input field — rounded pill
- Card (20px): 3D project card planes — softened corners
- No other radius values — the design uses only these three

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| 3D Environment (Level 0) | WebGL-rendered 3D scene | The entire background — particles, objects, fog |
| 3D Objects (Level 1) | PBR materials, iridescence, chromatic aberration | Logo, organic structures, jellyfish, spine |
| 3D Cards (Level 2) | Perspective-projected planes with rounded corners | Project showcase carousel |
| 3D Text (Level 3) | Extruded 3D typography with material properties | "CREATIVE DIGITAL EXPERIENCES" hero text |
| HUD Overlay (Level 4) | Screen-space elements with frosted glass | Nav pill, category links, input, scroll indicator |

**Shadow Philosophy**: Active Theory uses ZERO CSS shadows. Depth is entirely created by the WebGL 3D engine — perspective projection, lighting, fog, and particle layering provide all depth cues. The frosted-glass navigation pill creates its own sense of elevation through `backdrop-filter: blur()` and subtle glow, not through box-shadow. In a fully 3D environment, CSS shadows are meaningless — depth is real, not simulated.

## 7. Do's and Don'ts

### Do
- Use pure black (`#000000`) as the only background — the void is sacred
- Apply uppercase + generous letter-spacing to ALL text — no exceptions
- Use NBArchitektStd exclusively — the monospaced blueprint aesthetic is core identity
- Use frosted glass (`rgba(255,255,255,0.08)` + `backdrop-filter: blur`) for overlaid UI
- Use violet/lavender (`#b8a0d4`) for interactive navigation links
- Prefix category links with `->` arrow — the terminal command aesthetic
- Use pill-shaped containers (40px radius) for navigation elements
- Keep HUD elements minimal and peripheral — the 3D content is the hero
- Use opacity scaling for text hierarchy (1.0 → 0.85 → 0.5 → 0.3)
- Add subtle glow effects (cyan or violet) on interactive elements

### Don't
- Don't add background colors to sections — everything floats over the void
- Don't use shadows — depth comes from 3D perspective, not CSS effects
- Don't use sentence case or lowercase — everything is uppercase
- Don't use traditional card layouts with backgrounds and borders
- Don't use a grid system — position elements as HUD overlays
- Don't introduce warm colors (orange, yellow) into the UI — the palette is cool (white, violet, cyan)
- Don't use sans-serif or serif fonts — the monospaced typeface is non-negotiable
- Don't add heavy borders — all borders are `rgba(255,255,255,0.2)` or thinner
- Don't use solid backgrounds for inputs or buttons — everything is semi-transparent
- Don't create traditional navigation bars — the floating pill is the only navigation pattern

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <768px | Simplified 3D scene, reduced particles, touch scroll |
| Tablet | 768–1024px | Standard 3D with touch interaction |
| Desktop | 1024–1440px | Full 3D experience |
| Large Desktop | 1440–1920px | Enhanced particle density, higher resolution textures |
| Ultra-wide | >1920px | Maximum viewport, expanded 3D field of view |

### Touch Targets
- Navigation pill: full pill area (~200px wide) is tappable
- Category links: generous line-height (1.70) creates adequate touch targets
- Input field: full pill area is tappable
- Safe area insets: supported for notched devices (iOS)

### Collapsing Strategy
- 3D scene: adapts resolution and complexity to device GPU capability
- Navigation: pill maintains position, may scale slightly
- Category nav: repositions but maintains left-aligned stack
- Project cards: fewer visible cards in carousel on smaller viewports
- Particle systems: density scales with device performance
- Text: 3D-rendered text scales with viewport but maintains uppercase/tracking

### Performance Adaptation
- GPU detection determines texture quality and particle count
- Low-end devices: reduced shader complexity, fewer particles
- Mobile: touch-based scroll replaces mouse wheel
- WebGL context loss handling: graceful fallback

## 9. Agent Prompt Guide

### Quick Color Reference
- Background: Void Black (`#000000`)
- Text: Pure White (`#ffffff`)
- Interactive links: Violet (`#b8a0d4`)
- Nav pill background: Frosted Glass (`rgba(255, 255, 255, 0.08)`)
- Nav pill border: `rgba(255, 255, 255, 0.2)`
- Input border: `rgba(180, 160, 210, 0.4)` (violet-tinted)
- Glow accent: Cyan (`#00e5ff`) at low opacity
- Text secondary: `rgba(255, 255, 255, 0.85)`
- Text muted: `rgba(255, 255, 255, 0.5)`

### Example Component Prompts
- "Create a navigation pill: fixed top-right, `rgba(255,255,255,0.08)` background, `backdrop-filter: blur(12px)`, `1px solid rgba(255,255,255,0.2)` border, 40px radius, 12px 32px padding. Two labels 'WORK' and 'CONTACT' in NBArchitektStd 14px Bold, uppercase, 2px letter-spacing, white. Separated by a thin horizontal line at 30% opacity."
- "Design category navigation: left-aligned vertical stack on black background. Each link prefixed with '->' in violet (#b8a0d4), NBArchitektStd 14px Regular, uppercase, 1.5px letter-spacing. Line-height 1.70 for spacing. Categories: WEBSITES, INSTALLATIONS, XR / VR / AI, MULTIPLAYER, GAMES."
- "Build an AI chat input: pill shape (30px radius), `rgba(255,255,255,0.05)` background, `1px solid rgba(180,160,210,0.4)` border. Placeholder 'ASK ME ANYTHING...' in NBArchitektStd 12px Light, uppercase, 1.5px letter-spacing, `rgba(255,255,255,0.4)` color."
- "Create a hero section: pure black background, large heading 'CREATIVE DIGITAL EXPERIENCES' in NBArchitektStd Bold, 96px, uppercase, 8px letter-spacing, white. Below right: body text 'FOUNDED IN 2012' and description in NBArchitektStd Light 13px, uppercase, 1.2px letter-spacing, `rgba(255,255,255,0.85)`."
- "Design a scroll indicator: 'SCROLL DOWN' centered at top, NBArchitektStd 12px Regular, uppercase, 3px letter-spacing, `rgba(255,255,255,0.5)`. Subtle fade-pulse animation."

### Iteration Guide
1. Start with pure black — the void is everything, no grays, no off-blacks
2. All text is uppercase NBArchitektStd with positive letter-spacing — this is non-negotiable
3. Only white and violet for text — white for content, violet (#b8a0d4) for navigation links
4. Frosted glass for all overlay UI — rgba white backgrounds + backdrop-filter blur
5. Pill shapes (30-40px radius) for interactive containers — no sharp corners
6. Minimal HUD layout — position elements at viewport edges, never center-dominant
7. Arrow prefix `->` for category/filter links — terminal aesthetic
8. Opacity-based hierarchy, not size-based — same font size, different opacity levels
9. Zero shadows, zero cards, zero traditional layout — if it looks like a "normal website," it's wrong
10. Think heads-up display, not web page — every element floats over infinite depth
