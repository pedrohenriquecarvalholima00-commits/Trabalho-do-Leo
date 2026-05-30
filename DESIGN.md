---
name: Kubernetes Management System
colors:
  surface: '#0b1326'
  surface-dim: '#0b1326'
  surface-bright: '#31394d'
  surface-container-lowest: '#060e20'
  surface-container-low: '#131b2e'
  surface-container: '#171f33'
  surface-container-high: '#222a3d'
  surface-container-highest: '#2d3449'
  on-surface: '#dae2fd'
  on-surface-variant: '#bcc9cd'
  inverse-surface: '#dae2fd'
  inverse-on-surface: '#283044'
  outline: '#869397'
  outline-variant: '#3d494c'
  surface-tint: '#4cd7f6'
  primary: '#4cd7f6'
  on-primary: '#003640'
  primary-container: '#06b6d4'
  on-primary-container: '#00424f'
  inverse-primary: '#00687a'
  secondary: '#4edea3'
  on-secondary: '#003824'
  secondary-container: '#00a572'
  on-secondary-container: '#00311f'
  tertiary: '#ffb2b7'
  on-tertiary: '#67001b'
  tertiary-container: '#ff7f8b'
  on-tertiary-container: '#7d0023'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#acedff'
  primary-fixed-dim: '#4cd7f6'
  on-primary-fixed: '#001f26'
  on-primary-fixed-variant: '#004e5c'
  secondary-fixed: '#6ffbbe'
  secondary-fixed-dim: '#4edea3'
  on-secondary-fixed: '#002113'
  on-secondary-fixed-variant: '#005236'
  tertiary-fixed: '#ffdadb'
  tertiary-fixed-dim: '#ffb2b7'
  on-tertiary-fixed: '#40000d'
  on-tertiary-fixed-variant: '#92002a'
  background: '#0b1326'
  on-background: '#dae2fd'
  surface-variant: '#2d3449'
typography:
  headline-lg:
    fontFamily: Inter
    fontSize: 30px
    fontWeight: '700'
    lineHeight: 38px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Inter
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  body-lg:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 18px
  code-md:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 16px
  sidebar-width: 260px
---

## Brand & Style

This design system is engineered for high-stakes infrastructure management. The brand personality is **Reliable, Technical, Powerful, and Organized**. It prioritizes clarity over decoration, ensuring that DevOps engineers and SREs can diagnose complex cluster states at a glance.

The visual style is **Corporate / Modern** with a lean toward **Technical Minimalism**. It utilizes a structured, information-dense layout that balances data richness with enough breathing room to prevent cognitive overload. The aesthetic emphasizes "Observability First," where every visual element—from a tiny status dot to a full-screen log view—serves a functional purpose.

## Colors

The palette is optimized for long-duration monitoring in a dark environment. 

- **Primary (Cyan):** Used for primary actions, focus states, and active resource selection.
- **Secondary (Emerald):** Reserved exclusively for "Healthy," "Running," and "Success" states.
- **Tertiary (Coral):** Reserved for "Error," "Failed," and "Critical" alerts.
- **Warning (Amber):** Used for "Pending," "Warning," or "Throttling" states.
- **Neutrals:** A range of deep Slates and Navys provide the structural foundation, creating a clear hierarchy between the canvas, sidebar, and content cards.

## Typography

The typography system uses **Inter** for its exceptional legibility in UI contexts and **JetBrains Mono** for technical data, logs, and resource names.

- **Headlines:** Use tight letter spacing and bold weights to anchor page sections.
- **Body:** Scaled for density; `body-md` (14px) is the workhorse for general interface text.
- **Technical Data:** Use `code-md` for Pod names, IP addresses, and YAML manifests. This distinguishes "data" from "interface."
- **Labels:** Use `label-caps` for small metadata tags and table headers to provide a structural secondary layer of information.

## Layout & Spacing

The design system employs a **Fixed-Fluid Hybrid Grid**. The navigation sidebar is fixed at 260px, while the main content area utilizes a fluid 12-column grid.

- **Density:** We use a 4px baseline grid. Compact spacing (`sm` and `md`) is preferred to maximize the amount of information visible without scrolling.
- **Breakpoints:**
  - **Desktop (1440px+):** Full 12-column visibility.
  - **Tablet (768px - 1439px):** Sidebar collapses to icons; 8-column grid for content cards.
  - **Mobile (<768px):** Single column flow; horizontal scrolling for data tables.
- **Margins:** Main containers use `lg` (24px) padding, while internal card elements use `md` (16px) to maintain a tight, technical feel.

## Elevation & Depth

Depth is used sparingly to maintain the "enterprise-grade" feel. Visual hierarchy is established through **Tonal Layers** rather than heavy shadows.

- **Level 0 (Canvas):** The deepest background (`background_canvas`), used for the main application backdrop.
- **Level 1 (Sidebar/Cards):** Elements sitting on the canvas use `background_surface`. They feature a 1px solid border (`#334155`) to define boundaries.
- **Level 2 (Modals/Popovers):** Elements requiring focus use `background_container` with a soft, 15% opacity black shadow (12px blur) to lift them off the base layers.
- **Active States:** Subtle inner-glows in the primary cyan color are used for focused inputs or active navigation items.

## Shapes

The shape language is **Soft**. This keeps the interface looking modern and approachable while maintaining the structural rigidity expected of a professional tool.

- **Standard Elements:** Buttons, Inputs, and Cards use a 4px (`0.25rem`) radius.
- **Containers:** Large dashboard widgets use a 8px (`0.5rem`) radius.
- **Status Indicators:** Use circular (fully rounded) dots for health indicators to distinguish them from interactive UI elements.

## Components

### Buttons
- **Primary:** Solid Cyan with white/dark-navy text. High contrast for main actions (e.g., "Deploy").
- **Secondary/Ghost:** Slate borders with transparent backgrounds. Used for secondary actions (e.g., "Refresh," "Logs").

### Status Chips
- Small, pill-shaped indicators.
- **Running:** Emerald text on 10% Emerald background.
- **Error:** Coral text on 10% Coral background.
- **Pending:** Amber text on 10% Amber background.

### Data Tables
- High-density rows (40px height).
- Intermittent zebra striping for readability.
- Hover states using `background_container` to highlight the current row.

### Resource Cards
- Used in cluster overviews.
- Include a small sparkline (linear graph) to show CPU/Memory trends.
- Use `headline-sm` for the resource title and `code-md` for the resource name.

### Input Fields
- Dark-filled backgrounds with a subtle bottom border.
- On focus, the border transitions to Primary Cyan.
- Use monospaced fonts for fields requiring technical input (e.g., Image Tags, Selectors).

### Monitoring Graphs
- Use vibrant primary/secondary colors for the line strokes.
- Use semi-transparent area fills beneath the lines to show volume.
- Grid lines should be low-contrast (Slate 800) to keep the focus on the data.