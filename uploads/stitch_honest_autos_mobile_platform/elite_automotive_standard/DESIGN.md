---
name: Elite Automotive Standard
colors:
  surface: '#f9f9f9'
  surface-dim: '#dadada'
  surface-bright: '#f9f9f9'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f3f3f4'
  surface-container: '#eeeeee'
  surface-container-high: '#e8e8e8'
  surface-container-highest: '#e2e2e2'
  on-surface: '#1a1c1c'
  on-surface-variant: '#444748'
  inverse-surface: '#2f3131'
  inverse-on-surface: '#f0f1f1'
  outline: '#747878'
  outline-variant: '#c4c7c7'
  surface-tint: '#5f5e5e'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#1c1b1b'
  on-primary-container: '#858383'
  inverse-primary: '#c8c6c5'
  secondary: '#115cb9'
  on-secondary: '#ffffff'
  secondary-container: '#659dfe'
  on-secondary-container: '#003370'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#191c1f'
  on-tertiary-container: '#818488'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#e5e2e1'
  primary-fixed-dim: '#c8c6c5'
  on-primary-fixed: '#1c1b1b'
  on-primary-fixed-variant: '#474746'
  secondary-fixed: '#d7e2ff'
  secondary-fixed-dim: '#acc7ff'
  on-secondary-fixed: '#001a40'
  on-secondary-fixed-variant: '#004491'
  tertiary-fixed: '#e0e2e6'
  tertiary-fixed-dim: '#c4c7ca'
  on-tertiary-fixed: '#191c1f'
  on-tertiary-fixed-variant: '#44474a'
  background: '#f9f9f9'
  on-background: '#1a1c1c'
  surface-variant: '#e2e2e2'
typography:
  display-lg:
    fontFamily: Oswald
    fontSize: 48px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: 0.02em
  headline-lg:
    fontFamily: Oswald
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: 0.01em
  headline-lg-mobile:
    fontFamily: Oswald
    fontSize: 28px
    fontWeight: '600'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Oswald
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Roboto Flex
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Roboto Flex
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  label-sm:
    fontFamily: Roboto Flex
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1'
    letterSpacing: 0.05em
spacing:
  base: 8px
  container-max: 1280px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 48px
---

## Brand & Style

This design system is engineered for a premium automotive detailing service that prioritizes precision, transparency, and high-end results. The brand personality is authoritative yet approachable, reflecting the "honest" craftsmanship of a local Orewa business while maintaining the polish of a luxury showroom.

The visual direction follows a **Modern Minimalism** approach with a **High-Contrast** edge. It utilizes expansive whitespace, rigorous grid alignment, and a sophisticated monochromatic base. The aesthetic avoids unnecessary decoration, focusing instead on sharp lines and technical clarity to evoke a sense of mechanical perfection and showroom-quality finishes.

## Colors

The palette is anchored in **Deep Charcoal (#1A1A1A)**, providing a grounding, premium weight that mirrors the sleekness of high-performance vehicles. This is contrasted against a sterile **Pure White (#FFFFFF)** background to ensure maximum legibility and a clean "just-detailed" feel.

The accent color is a **Professional Deep Blue (#0056B3)**, chosen to convey trust and reliability. This accent should be used sparingly for primary actions, subtle indicators, and links. A **Metallic Silver (#94A3B8)** is used for secondary borders and dividers to add a subtle technical texture to the interface.

## Typography

The typography strategy leverages the verticality and strength of **Oswald** for all display and heading roles. All headers should be treated with uppercase styling to reinforce the bold, professional nature of the automotive industry.

**Roboto Flex** serves as the primary engine for communication. Its neutral, highly-legible character ensures that service descriptions and pricing are easy to digest. Use `body-lg` for introductory paragraphs and `label-sm` for technical specifications or metadata.

## Layout & Spacing

The layout utilizes a **Fixed Grid** model on desktop (12 columns) and a **Fluid Grid** on mobile (4 columns). The rhythm is based on a strict 8px baseline to ensure mathematical precision in element alignment.

- **Desktop:** 1280px maximum content width with 48px outer margins.
- **Tablet:** Fluid width with 32px margins.
- **Mobile:** Fluid width with 16px margins.

Section vertical spacing should be generous (80px - 120px) to allow the "minimalist" aesthetic to breathe, emphasizing the quality of imagery and content over density.

## Elevation & Depth

This design system uses **Tonal Layers** and **Low-Contrast Outlines** rather than heavy shadows to maintain a flat, professional look. 

- **Level 0 (Surface):** Pure White (#FFFFFF).
- **Level 1 (Card/Container):** Off-white (#F9FAFB) with a 1px border (#E5E7EB).
- **Interactive State:** A very subtle, extra-diffused shadow (0px 4px 20px rgba(0,0,0,0.05)) may be used on hover to indicate interactivity without breaking the flat aesthetic.

Backgrounds for immersive sections should use the Primary Deep Charcoal with white text to create "impact zones" within the scroll experience.

## Shapes

The shape language is **Sharp (0)**. To reflect the precision of automotive engineering and the "Honest" brand name, the UI avoids rounded corners entirely. 

Hard 90-degree angles communicate stability, technical accuracy, and a no-nonsense professional attitude. This applies to buttons, input fields, cards, and image containers.

## Components

### Buttons
Primary buttons use the Deep Charcoal background with white uppercase Oswald text. Secondary buttons use a 2px charcoal border with a transparent background. Hover states for primary buttons should shift to the Professional Blue accent.

### Input Fields
Fields are defined by a 1px bottom border only (#94A3B8) in their default state, shifting to a 2px Deep Charcoal border on focus. This creates a clean, architectural look suitable for high-end service bookings.

### Cards
Cards for services (e.g., "Full Ceramic Coating") should be stark white with a thin silver border. They should use high-resolution automotive imagery that fills the top half of the card, with typography left-aligned below.

### Chips/Tags
Used for service features (e.g., "UV Protection"). These are small, uppercase labels in Roboto Flex with a light gray background (#F3F4F6) and dark text.

### Progress Indicators
For detailing packages that involve multiple steps, use a thin, technical line-based stepper component in the Professional Blue accent to guide the user through the process.