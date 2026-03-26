# Design System Strategy: The Cinematic Vanguard

## 1. Overview & Creative North Star
**Creative North Star: The Cinematic Vanguard**

This design system is not a collection of components; it is a filmic experience. In the high-end real estate marketing world, we aren't selling floor plans—we are selling a lifestyle of power, elegance, and exclusivity. 

To achieve this, we move away from "Standard Web" patterns. We embrace **The Cinematic Vanguard**, a style defined by aggressive editorial typography, deep tonal depth, and a rejection of traditional containment. We break the "template" look through intentional asymmetry, where elements overlap like frames in a film reel, and high-contrast color shifts create a sense of drama. Every layout should feel like a premium coffee-table book or a high-fashion editorial.

---

## 2. Colors & Tonal Depth

Our palette is anchored in deep blacks and "Golden Hour" accents. We use color to direct the eye, not to box content in.

### The Color Palette
- **Core Blacks:** `surface` (#131313) and `surface_container_lowest` (#0e0e0e).
- **The Signature Gold:** `primary_fixed` (#ffe170) and `primary_container` (#ffdd55). Use these sparingly for high-impact CTAs and key highlights.
- **Muted Earth:** `secondary` (#d0c4c2) and `on_surface_variant` (#cfc6af). These provide the "silver" and "stone" undertones that ground the luxury feel.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders to define sections. Traditional borders feel "cheap" and structural. Instead:
- **Define through Contrast:** Separate a Hero section from a Content section by shifting from `surface` (#131313) to `surface_container_low` (#1b1b1b).
- **The Edge of Light:** Use subtle 1px gradients that fade in and out to suggest a boundary without drawing a hard line.

### Surface Hierarchy & Nesting
Treat the UI as a physical set. Use the `surface-container` tiers to create "nested" depth:
1. **Base Layer:** `surface_container_lowest` (#0e0e0e) for the deep background.
2. **Interactive Layer:** `surface_container` (#1f1f1f) for cards or secondary modules.
3. **Elevated Layer:** `surface_container_high` (#2a2a2a) for modals or floating navigation.

### The "Glass & Gradient" Rule
To add visual "soul," use **Glassmorphism**. Floating elements (like navigation bars or property overlays) should use `surface_variant` at 60% opacity with a `backdrop-blur` of 20px. Apply a subtle linear gradient from `primary` to `primary_container` on main CTAs to mimic the sheen of polished metal.

---

## 3. Typography: Editorial Authority

We use a high-contrast typographic scale to create a sense of hierarchy and prestige.

*   **The Hero (Champion Gothic):** Used for `display-lg` through `headline-sm`. This is our "Voice of Authority." It should be used for bold, short statements. Letter spacing should be tightened (-2% to -4%) for a dense, cinematic look.
*   **The Narrative (Instrument Sans):** Used for `title` and `body` styles. This font brings modern clarity. It feels premium and architectural.
*   **The Meta-Data (Space Grotesk):** Used for `label-md` and `label-sm`. Use these for technical details (e.g., "SQ FT," "LOCATION") in uppercase with wide letter spacing (+10% to +15%) to evoke a technical, high-end blueprint aesthetic.

---

## 4. Elevation & Depth: Tonal Layering

We do not use shadows to create "pop." We use light and layering.

*   **The Layering Principle:** Stacking tiers is mandatory. A `surface-container-high` card sitting on a `surface` background creates a soft, natural lift that feels integrated into the environment.
*   **Ambient Shadows:** If an element must float (e.g., a "Request a Tour" fab), use an extra-diffused shadow. 
    *   *Value:* Blur 40px, Spread -10px, Opacity 8%.
    *   *Color:* Use a tinted version of `on_surface` rather than pure black.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.
*   **Motion & Depth:** When users hover over an image, use a slight "Zoom-in" transition (1.05 scale) combined with a shift in background color from `surface` to `surface_container_highest`.

---

## 5. Components

### Buttons
*   **Primary:** Background: `primary_container` (#ffdd55), Text: `on_primary` (#3a3000). Sharp corners (`rounding-sm`: 0.125rem) to maintain an aggressive, modern edge.
*   **Tertiary (Ghost):** No background. Text: `primary_fixed`. Underline: 1px `primary_fixed` that expands on hover.

### Input Fields
*   **Styling:** Never use a four-sided box. Use a "Bottom Stroke Only" approach using the `outline_variant` at 40% opacity. 
*   **Focus State:** The bottom stroke transitions to `primary_fixed` (#ffe170) with a subtle glow.

### Cards & Lists
*   **The "No-Divider" Rule:** Forbid divider lines. Separate list items using `spacing-6` (2rem) of vertical white space or a subtle background toggle between `surface` and `surface_container_low`.
*   **Imagery:** Images are the hero. Every card should feature high-quality photography with a dark overlay (20% black) to ensure typography remains legible.

### Signature Component: The "Cinematic Scroller"
A full-width horizontal carousel where the center image is slightly larger (`surface_container_highest`) and side images are desaturated and slightly blurred, creating a "Lens Focus" effect.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical layouts. Place a headline on the left and the body text shifted 3 columns to the right.
*   **Do** use "Bleed" imagery. Let photos run off the edge of the screen to suggest a world larger than the viewport.
*   **Do** prioritize whitespace. Luxury is defined by the space you *don't* fill.

### Don't:
*   **Don't** use standard 1px borders. It breaks the cinematic immersion.
*   **Don't** use bright, saturated colors other than the Gold/Silver accents. 
*   **Don't** use "Soft/Round" corners. Keep the `rounding` scale strictly to `sm` (0.125rem) or `none`. Rounded bubbles are for consumer apps; sharp edges are for luxury brands.
*   **Don't** use standard "Drop Shadows." Use tonal layering or ambient blurs.

---
*Director's Final Note: Every pixel must feel intentional. If an element doesn't serve the story of luxury and motion, remove it. We are building an icon, not a website.*