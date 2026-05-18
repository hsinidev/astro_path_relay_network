---
name: Deep Space Telemetry
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#393939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#20201f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353535'
  on-surface: '#e5e2e1'
  on-surface-variant: '#b9ccb2'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#84967e'
  outline-variant: '#3b4b37'
  surface-tint: '#00e639'
  primary: '#ebffe2'
  on-primary: '#003907'
  primary-container: '#00ff41'
  on-primary-container: '#007117'
  inverse-primary: '#006e16'
  secondary: '#c6c6c6'
  on-secondary: '#2f3131'
  secondary-container: '#484949'
  on-secondary-container: '#b8b8b8'
  tertiary: '#fcf8f8'
  on-tertiary: '#313030'
  tertiary-container: '#dfdcdb'
  on-tertiary-container: '#626060'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#72ff70'
  primary-fixed-dim: '#00e639'
  on-primary-fixed: '#002203'
  on-primary-fixed-variant: '#00530e'
  secondary-fixed: '#e3e2e2'
  secondary-fixed-dim: '#c6c6c6'
  on-secondary-fixed: '#1a1c1c'
  on-secondary-fixed-variant: '#464747'
  tertiary-fixed: '#e5e2e1'
  tertiary-fixed-dim: '#c9c6c5'
  on-tertiary-fixed: '#1c1b1b'
  on-tertiary-fixed-variant: '#474646'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353535'
typography:
  display-lg:
    fontFamily: JetBrains Mono
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.05em
  headline-md:
    fontFamily: JetBrains Mono
    fontSize: 20px
    fontWeight: '600'
    lineHeight: '1.4'
    letterSpacing: 0.02em
  body-base:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.6'
    letterSpacing: 0em
  data-mono:
    fontFamily: JetBrains Mono
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1'
    letterSpacing: 0.05em
  label-caps:
    fontFamily: JetBrains Mono
    fontSize: 10px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.15em
spacing:
  base-unit: 4px
  gutter: 16px
  margin-mobile: 12px
  grid-overlay-size: 32px
  stack-sm: 8px
  stack-md: 24px
---

## Brand & Style
The design system is engineered for mission-critical reliability, evoking the precision of a high-altitude ground station. It prioritizes data density and immediate legibility over decorative elements, adopting a **Technical-Minimalist** aesthetic. 

The brand personality is authoritative, cold, and calculated. It targets engineers and orbital mechanics who require rapid cognitive processing of complex datasets. The visual language utilizes a "HUD" (Heads-Up Display) metaphor, employing mathematical grid overlays and thin vector strokes to create an environment that feels like a real-time window into deep space.

## Colors
The palette is anchored in a high-contrast dark mode to reduce eye strain during long-duration monitoring. 

- **Deep Space Black (#050505):** The absolute foundation, used to represent the vacuum of space and provide a pure canvas for light-emitting elements.
- **Laser Green (#00FF41):** Used exclusively for active data, successful telemetry connections, and primary calls to action. It should feel like a phosphorus glow on a cathode-ray tube.
- **Silver (#C0C0C0):** Reserved for structural scaffolding, including borders, grid lines, and secondary labels.
- **Functional Accents:** While restricted, subtle shifts into Amber and Red are permitted only for systemic warnings and critical signal loss.

## Typography
This design system utilizes **JetBrains Mono** across all hierarchy levels to maintain a rigid, "NASA-grade" technical feel. The monospaced nature ensures that fluctuating numerical data remains vertically aligned, which is critical for scanning telemetry tables.

- **Headlines:** Use tight letter spacing to feel like a stamped serial number.
- **Data Points:** Use the `data-mono` style for all real-time coordinates and timestamps.
- **Labels:** Always displayed in uppercase with generous letter spacing to differentiate metadata from actual values.

## Layout & Spacing
The layout follows a **Fixed-Density Grid** philosophy. Every screen is overlaid with a subtle 32px mathematical grid that acts as the alignment guide for all modules.

- **Mobile-First Alerts:** Alerts occupy the top 15% of the viewport, utilizing a "sticky" behavior to ensure critical signal status is never occluded.
- **Module Boxing:** Content is partitioned into 1px bordered containers. Spacing inside these containers is tight (8px-12px) to maximize information density.
- **Safe Zones:** A 12px margin is maintained on mobile devices to prevent interaction interference with hardware bezels.

## Elevation & Depth
Depth is not communicated through shadows, but through **Tonal Layering** and **Luminance**. In the vacuum of this UI, light source equals proximity.

1.  **Floor:** Deep Space Black (#050505) is the furthest plane.
2.  **The Grid:** Silver lines at 10% opacity sit just above the floor.
3.  **Surfaces:** Containers use a slightly lighter neutral (#1A1A1A) with 1px Silver outlines.
4.  **Active Elements:** Elements with the Laser Green glow (`box-shadow: 0 0 10px rgba(0, 255, 65, 0.4)`) are perceived as "projected" closest to the user.
5.  **Scrims:** When modals appear, they use a high-density blur (20px) rather than a simple black overlay to maintain the "glass" aesthetic.

## Shapes
The shape language is strictly **Rectilinear**. All corners are set to 0px (Sharp). This reinforces the mathematical, "built-for-purpose" nature of the design system. 

Circles are only permitted when representing actual spherical data (e.g., planetoids, radar pings, or orbital paths). All UI containers, buttons, and input fields must maintain 90-degree angles to ensure they align perfectly with the background grid overlay.

## Components
Consistent component styling ensures the interface remains predictable during high-stress operations.

- **Buttons:** Ghost-style by default with a 1px Silver border. Upon interaction or "Active" state, the background fills with Laser Green and the text knocks out to Deep Space Black.
- **Data Chips:** Small, rectangular tags with a background of #1A1A1A and a left-side 2px accent bar in Green or Silver to denote category.
- **Input Fields:** Bottom-border only (1px Silver). The cursor should be a solid Green block that blinks at a 1Hz frequency.
- **Status Indicators:** Use a "Pulsing Dot" icon for live connections. The pulse should have a soft Laser Green glow to simulate a physical LED.
- **Mathematical Overlays:** Decorative but functional crosshair vectors should appear in the corners of primary data containers to "frame" the telemetry.
- **Alert Banners:** Full-width, high-contrast blocks. Critical alerts use a solid Red background; status updates use a solid Green background. Text in these banners is always Deep Space Black for maximum contrast.