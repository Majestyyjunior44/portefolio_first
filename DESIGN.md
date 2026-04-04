```markdown
# Design System Document: The Terminal Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Architect"**
This design system moves beyond the standard "developer portfolio" by treated code as art and whitespace as a luxury. It avoids the cluttered, "noisy" aesthetic of typical tech sites in favor of a high-end, editorial layout. We break the template look through **Intentional Asymmetry**—where content is weighted to one side to create a sense of forward motion—and **Monolithic Typography**, using massive scale shifts to guide the eye. The goal is a "Fintech-Premium" feel: stable and professional, yet pulsing with the energy of a neon-lit IDE.

## 2. Colors: The Depth of the Machine
The palette is rooted in a "Deep Space" navy, using high-saturation neon accents to highlight technical precision.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit 1px solid borders for sectioning. Structural boundaries must be defined solely through background color shifts or tonal transitions. Use `surface_container_low` against a `surface` background to denote a change in context. Lines are for code; space is for design.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. We use "Tonal Stepping" to create depth:
*   **Base Level:** `surface` (#010e24) - The infinite background.
*   **Section Level:** `surface_container_low` (#02132b) - Large content blocks.
*   **Component Level:** `surface_container` (#061934) - Cards and interactive zones.
*   **Elevation Level:** `surface_container_high` (#0b203d) - Floating menus or active states.

### The "Glass & Gradient" Rule
To escape a "flat" feel, use Glassmorphism for floating elements (like Navbars or Tooltips). Use `surface_bright` at 60% opacity with a `20px` backdrop-blur. 
*   **Signature Texture:** Main CTAs should utilize a subtle linear gradient from `primary` (#58f5d1) to `primary_container` (#1cd0ad) at a 135-degree angle. This provides a "glow" that flat colors cannot replicate.

## 3. Typography: Editorial Authority
The type system relies on the tension between the humanist clarity of **Inter** and the technical rigidity of **Space Grotesk** (Monospace).

*   **Display (Inter):** Use `display-lg` (3.5rem) with a `-0.04em` letter-spacing. This is your "Statement" type—it should feel heavy, authoritative, and cinematic.
*   **The Technical Label (Space Grotesk):** All metadata, chips, and "kicker" headlines must use `label-md` or `label-sm`. This creates the "Developer" signature.
*   **Hierarchy via Contrast:** Never pair two sizes that are adjacent in the scale. Jump from a `display-md` headline directly to a `body-md` description to create a sophisticated, high-contrast editorial rhythm.

## 4. Elevation & Depth: Tonal Layering
We do not use drop shadows to mimic light; we use tonal shifts to mimic density.

*   **The Layering Principle:** Place a `surface_container_lowest` (#000000) card onto a `surface_container` (#061934) background to create a "recessed" or "inset" look. This feels more "Fintech" and stable than traditional floating shadows.
*   **Ambient Shadows:** If an element must float (e.g., a modal), use a shadow color tinted with `surface_tint` (#58f5d1) at 4% opacity. Blur: `40px`, Spread: `0px`. It should feel like a soft neon glow, not a gray shadow.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline_variant` at 15% opacity. It should be barely perceptible, acting as a "whisper" of a container.

## 5. Components: Precision Engineered

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary_container`), `on_primary` text, `md` (0.375rem) roundedness. No border.
*   **Secondary:** "Ghost" style. `outline` color for text, no fill. On hover, transition to a 10% `primary` background opacity.
*   **Tertiary:** Monospace font (`label-md`), all caps, with a `primary` color. Used for "View Project" or "Read More" links.

### Cards & Project Items
*   **Rule:** Forbid divider lines. Separate content using the `spacing-8` (2.75rem) value.
*   **Interactions:** On hover, a card should shift from `surface_container` to `surface_container_high`. No "lift" (Y-axis movement)—only a color shift.

### Inputs & Fields
*   **Style:** Minimalist. Only a bottom border using `outline_variant`.
*   **Focus State:** The bottom border transforms into a 2px `primary` solid line. Label moves from `body-md` to `label-sm` (Monospace) above the field.

### Signature Component: The "Terminal Trace"
A vertical decorative line (using `primary` at 20% opacity) that connects section headers. It mimics the look of a code indentation guide, reinforcing the developer aesthetic.

## 6. Do's and Don'ts

### Do
*   **Use Massive Whitespace:** If you think there is enough space, double it. Use `spacing-20` (7rem) between major sections.
*   **Align to a Grid, then Break it:** Place your text on a strict grid, but let images or "code snippets" bleed off the edge of the screen.
*   **Mix Case:** Use Sentence case for headlines and ALL CAPS (Monospace) for technical labels.

### Don't
*   **Don't use 100% White:** Use `on_surface` (#dbe6ff). Pure white (#ffffff) is too harsh against the deep navy and cheapens the premium feel.
*   **Don't use Rounded Corners on Everything:** Keep `roundedness.md` (0.375rem) as your maximum for cards. Avoid "bubbly" or fully rounded shapes unless it's a pill-tag.
*   **Don't use Center Alignment:** High-end editorial design is almost always left-aligned or intentionally staggered. Center alignment feels like a template.

### Accessibility Note
Ensure all `primary` (#58f5d1) text on `surface` (#010e24) maintains a 4.5:1 contrast ratio. If using the accent for small labels, ensure the font-weight is at least Medium (500).```