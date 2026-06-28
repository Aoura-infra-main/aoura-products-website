# Aoura Products Website Documentation

This documentation serves as a comprehensive guide for AI agents and developers to understand the company context, design aesthetics, and technical patterns used across the Aoura Products website. When creating or modifying pages, this guide should be referenced to ensure consistency without requiring explicit prompting.

## 1. Company Overview
- **Name:** Aoura Products (A Division of Aoura Group)
- **Nature of Business:** B2B wholesale supplier of complete office supplies (writing instruments, filing, paper, printers, ink, cleaning equipment, pantry).
- **Key Value Propositions:** 100+ products across 8 categories, a single account and invoice, competitive direct pricing, same-day dispatch in Dubai, UAE-wide delivery, and buffer stock across multiple warehouses (Deira, Sajjah).
- **Target Audience:** UAE-based businesses seeking a streamlined, premium, and reliable B2B purchasing experience.

## 2. Global Design Style & Aesthetics
- **Core Aesthetic:** Modern, premium, clean, and highly readable. The design exudes a sleek corporate elegance through minimalist layouts and generous whitespace.
- **Color Palette:**
  - **Backgrounds:** White (`#fafafa`), Light Grey (`#f4f4f4`, `#e8e8e8`), and Deep Black (`#0a0a0a`).
  - **Text:** Black (`#0a0a0a`) for high contrast on light backgrounds, Dark Grey (`#555555`, `#9a9a9a`) for secondary body text. White (`#fafafa`) or slightly transparent white on dark sections.
  - **Accents:** Subtle pops of color used sparingly (e.g., `#1a6bff` for specific tech-product accents, `#25d366` for WhatsApp, `#4ade80` for free shipping tags).
- **Typography:**
  - **Headings & Display:** `Cormorant Garamond`, Georgia, serif. Used for all `h1`-`h4` tags to provide a premium, editorial feel. Italics (`<em>`) are often used to emphasize specific words elegantly.
  - **Body Text:** `DM Sans`, sans-serif. Used for paragraphs, buttons, and navigation. Highly readable and modern.
- **Shape Language:**
  - Buttons and tags use pill shapes (`border-radius: 999px`).
  - Cards, images, and containers use soft rounded corners (`border-radius: 14px` to `18px`).
- **Interactive Elements:**
  - Smooth hover transitions on buttons (opacity shifts, subtle `transform: translateY(-1px)`).
  - Scroll-triggered reveal animations (`.reveal` class fading up elements on intersection).

## 3. Header Design
- **Structure:** A floating, sticky navbar positioned slightly below the top of the viewport (`top: 16px`), centered horizontally.
- **Styling:** Employs glassmorphism. Background is translucent (`rgba(255,255,255,0.78)` for light themes, `rgba(10,10,10,0.72)` for dark themes) with a blur effect (`backdrop-filter: blur(18px)`). Contains a subtle border and soft drop shadow.
- **Desktop View:**
  - Brand Logo/Text on the far left.
  - Navigation links in the center with subtle background hover states.
  - A primary Call-to-Action (CTA) button on the far right (e.g., "Order Now").
- **Mobile View:** Links are hidden, replaced by a 3-line hamburger menu that toggles a floating glassmorphic dropdown drawer below the navbar.

## 4. Footer Design
- **Theme:** Always dark (Deep Black background with white/grey text) to firmly ground the bottom of the page.
- **Grid Layout:** Typically a 4 to 5 column CSS Grid on desktop containing:
  1. Brand summary and tagline.
  2. Internal company links (About Us, Shop, FAQ).
  3. Contact Information (WhatsApp, Email, Website).
  4. Marketplace Links (Custom buttons with SVG logos for Amazon and Noon).
  5. Social Media Links (Instagram, LinkedIn, X using styled SVG icons).
- **Payment Strip:** A distinct horizontal strip featuring "Secured by Stripe", SSL Encryption, and SVG icons of accepted payment methods (Visa, Mastercard, Amex, Apple Pay, Google Pay).
- **Bottom Bar:** Copyright information, address summary, and legal policy links.

## 5. Page Layout & Component Guidelines
- **Sections (`<section>`):** Pages are divided into full-width sections. Backgrounds typically alternate between white, light-grey, and black.
- **Spacing:** Generous padding is applied to sections (e.g., `--section-pad: 80px` or `90px` on desktop).
- **Eyebrows:** Section titles are consistently introduced by an "eyebrow" text element—small, uppercase, heavily letter-spaced (`letter-spacing: 0.2em`), and usually grey or faded white.
- **Grids:** CSS Grid is heavily utilized for product categories, features, and delivery tables. Grids are responsive by default.
- **Dividers:** Short horizontal lines (`width: 40px; height: 1px; background: var(--black)`) often placed under section titles to anchor the text.
- **Marquees:** CSS-animated infinite scrolling text bands used to highlight product categories or key benefits dynamically.

## 6. Mobile Responsiveness & Adaptation
- **Breakpoints:**
  - `@media (max-width: 900px)`: Tablets and small laptops. Grid columns usually drop to 2, or complex 2-column layouts stack to 1.
  - `@media (max-width: 768px)`: Standard mobile breakpoint. Navbar switches to hamburger.
  - `@media (max-width: 480px)`: Small mobile breakpoint.
- **Spacing Adjustments:** Section padding automatically reduces (e.g., from `80px` to `60px` or `48px`) to maximize screen real estate on small devices.
- **Typography:** Uses CSS `clamp()` functions (e.g., `font-size: clamp(2rem, 3.5vw, 3rem)`) ensuring headings scale down fluidly without media query snapping.
- **Stacking:** Grids fluidly collapse (e.g., a 4-column product grid goes to 2-columns on tablet, and 1-column on mobile).
- **Touch Targets:** Buttons and interactive elements are enlarged on mobile (minimum touch heights applied via padding) to ensure accessibility.
- **Floating Action Button:** A floating WhatsApp button (`.wa-float`) is styled prominently at the bottom right corner, easily reachable by the thumb.
