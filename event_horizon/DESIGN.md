# Design System Specification: The Kinetic Observatory

## 1. Overview & Creative North Star

**Creative North Star: The Kinetic Observatory**
This design system is built to evoke the vastness of deep space and the cold precision of advanced robotics. We are moving away from the "flat web" and into an atmospheric, multi-layered digital environment. The goal is to make the user feel like they are operating a high-end orbital interface—where data is weightless, and every interaction feels like a calculated pulse of energy.

To achieve an editorial, high-end feel, this design system rejects standard "container-and-border" layouts. Instead, we utilize **Intentional Asymmetry** and **Tonal Depth**. By placing high-contrast technical labels against vast, dark voids, we create a sense of scale. Elements should feel like they are floating in a vacuum, held together by gravitational hierarchy rather than rigid boxes.

---

## 2. Colors: The Engine Glow & The Void

The palette is anchored in the "Infinite Void" (`surface-container-lowest`: #000000) and punctuated by high-energy "Engine Glow" accents.

*   **The "No-Line" Rule:** To maintain a premium, cinematic feel, 1px solid borders for sectioning are strictly prohibited. Boundaries must be defined solely through background color shifts. Use `surface-container-low` for large content blocks sitting on a `surface` background. The eye should perceive the edge through the shift in value, not a structural line.
*   **Surface Hierarchy & Nesting:** Treat the UI as a series of physical layers. 
    *   **Base:** `surface` (#0e0e10)
    *   **Elevated Sections:** `surface-container-low` (#131315)
    *   **Interactive Cards:** `surface-container` (#19191c)
    *   **Floating Elements:** `surface-container-highest` (#262528)
*   **The "Glass & Gradient" Rule:** For primary actions and hero moments, use a "Glow Gradient" transitioning from `primary` (#8ff5ff) to `primary_container` (#00eefc). For floating modal overlays, apply `surface_bright` at 40% opacity with a `backdrop-blur` of 20px to simulate frosted lens glass.
*   **Accent Roles:** 
    *   `primary` (Cyan) is for "System Active" states and primary navigation.
    *   `secondary` (Orange) is for "Kinetic Energy" and high-priority warnings/alerts.
    *   `tertiary` (Violet) is for "AI Processing" and deep data visualization.

---

## 3. Typography: Technical Elegance

This design system uses a dual-font strategy to balance robotic precision with human-centric AI intelligence.

*   **The Technical Edge (Space Grotesk):** Used for all `display`, `headline`, and `label` roles. Its geometric nature reflects the structural integrity of hardware. 
    *   *Editorial Tip:* Use `label-sm` in all-caps with 0.1em letter-spacing for technical metadata to mimic blueprint annotations.
*   **The Intelligent Core (Manrope):** Used for `title` and `body` scales. Manrope provides the necessary legibility for complex documentation and AI-generated insights.
*   **Hierarchy as Identity:** Create a dramatic scale contrast. Pair a `display-lg` headline with a `label-md` metadata tag positioned asymmetrically to create a "Technical Poster" aesthetic.

---

## 4. Elevation & Depth: Tonal Layering

Traditional drop shadows are too "software-standard." We achieve depth through atmospheric physics.

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-high` card on a `surface-container-lowest` background. The difference in luminance creates a "natural lift."
*   **Ambient Shadows:** If a floating element (like a dropdown) requires a shadow, it must be an "Atmospheric Glow." Use the `primary` color at 5% opacity with a 40px blur, making the element appear as if it is backlit by the system's own energy.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use the "Ghost Border" method: the `outline-variant` token at 15% opacity. This provides a faint glimmer of an edge without closing off the layout.
*   **Glassmorphism:** For interactive floating panels, use a combination of `surface_variant` at 30% opacity, a 16px `backdrop-blur`, and a top-edge inner stroke (0.5px) of `primary` at 20% opacity to simulate a light-catching glass edge.

---

## 5. Components: Precision Primitives

### Buttons
*   **Primary:** Solid `primary` background with `on_primary` text. Use `rounded-sm` (0.125rem) for a sharp, machined look.
*   **Secondary (Engine Glow):** No background. `primary` text with a "Ghost Border." On hover, add a subtle `primary_container` outer glow.
*   **Tertiary:** `label-md` typography with no container, using an icon suffix for direction.

### Input Fields
*   **Style:** Minimalist. Only a bottom border using `outline` (at 30% opacity). When focused, the border transitions to `primary` and a subtle `primary_dim` glow appears beneath the text.
*   **Labels:** Always use `label-sm` in `primary` color, positioned above the input to look like telemetry data.

### Cards & Lists
*   **Constraint:** No divider lines. Use `8` (2rem) or `10` (2.5rem) vertical spacing from the scale to separate list items.
*   **Interaction:** On hover, a card should shift from `surface-container` to `surface-container-high`.

### Specialized: Telemetry Chips
*   Used for AI status or robot vitals. Small, `rounded-none` containers with `surface-container-highest` background and `label-sm` mono text. Include a small blinking dot using the `secondary` color for "Live" states.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use extreme white space. Allow the `background` (#0e0e10) to breathe to emphasize the "Deep Space" theme.
*   **Do** align text to a technical grid but allow images or 3D robot renders to break that grid and overlap containers.
*   **Do** use `secondary` (Orange) sparingly. It is a "Heat Source"—too much of it breaks the cold, futuristic aesthetic.

### Don't:
*   **Don't** use standard `9999px` pill shapes for buttons. Keep corners sharp (`sm` or `md`) to maintain a "machined hardware" feel.
*   **Don't** use pure grey shadows. Always tint shadows with the `surface_tint` or `primary` color to maintain atmospheric depth.
*   **Don't** use 100% opaque borders. They act as "visual cages" and kill the expansive feeling of this design system.