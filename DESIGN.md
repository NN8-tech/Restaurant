# Design System Document: High-End Editorial

## 1. Overview & Creative North Star: "The Digital Maître D’"
The Creative North Star for this design system is **"The Digital Maître D’."** Just as a fine dining experience is defined by what is unsaid—the effortless flow of service, the tactile quality of the linen, and the intentional use of space—this digital experience must feel curated rather than constructed.

We are breaking away from the "template" look of standard restaurant sites. We achieve this through **Intentional Asymmetry** (e.g., a high-resolution dish partially overlapping a beige surface container) and **Negative Space as Luxury**. White space is not "empty"; it is a premium material. This system rejects rigid grids in favor of a fluid, editorial layout that feels like a high-end coffee table book.

## 2. Colors: Tonal Depth & Metallic Accents
Our palette is rooted in organic neutrals and punctuated by the glow of gold. 

*   **Primary (#735c00) & Primary-Container (#D4AF37):** These are our "Gilded Touches." Use them sparingly for key calls-to-action (CTAs) or as subtle highlights.
*   **Surface Hierarchy:** Our "Beige" is not one color, but a series of layers. Use `surface` (#fcf9f8) for the main canvas.
*   **The "No-Line" Rule:** Explicitly prohibit 1px solid borders for sectioning. Boundaries must be defined solely through background color shifts. To separate the hero from the story section, transition from `surface` to `surface-container-low` (#f6f3f2).
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers of fine paper. A reservation card should be `surface-container-lowest` (#ffffff) sitting atop a `surface-container` (#f0eded) section.
*   **The "Glass & Gradient" Rule:** For floating navigation or wine lists, use Glassmorphism. Apply `surface` at 80% opacity with a `backdrop-filter: blur(12px)`. 
*   **Signature Textures:** For primary buttons, apply a subtle linear gradient from `primary` to `primary-container` at a 45-degree angle to mimic the sheen of brushed brass.

## 3. Typography: The Editorial Voice
Typography is the primary vehicle for our "Upscale" brand. We pair the authoritative weight of a serif with the invisible efficiency of a sans-serif.

*   **Display & Headline (Noto Serif):** Used for titles that need to "breathe." Always use high-contrast scales. `display-lg` (3.5rem) should be used for the restaurant’s name or philosophy, often with increased letter-spacing for a "stately" feel.
*   **Title & Body (Manrope):** Our modern sans-serif. Use `title-md` for menu categories. The `body-lg` (1rem) is designed for readability in storytelling sections, utilizing a generous line-height (1.6 - 1.8) to maintain the feeling of openness.
*   **Label (Manrope):** Used for micro-copy like "Est. 1994" or "Scroll to Explore." These should often be in all-caps with 0.1rem letter-spacing to denote prestige.

## 4. Elevation & Depth: Atmospheric Layering
We do not use shadows to create "pop"; we use them to create "atmosphere."

*   **The Layering Principle:** Depth is achieved by stacking surface-container tiers. For a menu item detail, place a `surface-container-highest` card on a `surface-container-low` background. 
*   **Ambient Shadows:** If a floating element (like a "Book a Table" FAB) is required, use a shadow with a 40px blur, 0% spread, and 6% opacity of the `on-surface` color. It should feel like a soft glow, not a drop shadow.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility on form inputs, use the `outline-variant` (#d0c5af) at 20% opacity. 100% opaque borders are forbidden.
*   **Glassmorphism:** Use semi-transparent `surface` colors for the navigation bar to allow high-quality food photography to bleed through as the user scrolls, creating an integrated, immersive experience.

## 5. Components: Refined Interaction

*   **Buttons:** 
    *   **Primary:** Rectangular, 0px radius. Background: `primary-container`. Text: `on-primary-container`. 
    *   **Tertiary:** No background. Underlined with a 1px `primary` line that sits 4px below the text.
*   **Cards (Menu/Events):** Forbid the use of divider lines. Separate items using `surface-container-low` backgrounds and ample padding (min 32px). Images should bleed to the edges of the card.
*   **Input Fields:** Ghost-style inputs only. Use a bottom-only `outline-variant` (20% opacity). Labels use `label-md` and float above the input.
*   **Menu Lists:** Instead of dots (Price........$40), use wide horizontal spacing. The price should sit in `label-md` typography, slightly offset from the dish name to create an asymmetric, modern look.
*   **The "Signature Detail" Component:** Use a "Gold Serif Flourish"—a small, `primary` color decorative element or a single gold vertical line (`primary-fixed`) to lead the eye between sections.

## 6. Do’s and Don’ts

### Do:
*   **Do** use 0px border-radius for everything. Sharp corners convey architectural precision and modern chic.
*   **Do** use "Overlapping Elements." Let a high-res image of a cocktail overlap a text block by 20-30px to break the grid.
*   **Do** prioritize "Big Photography." One stunning image is better than four small ones.

### Don't:
*   **Don't** use pure black (#000000). Use `on-background` (#1c1b1b) for a softer, more expensive feel.
*   **Don't** use standard "Hover" states. Instead of a color change, use a subtle "Scale" (1.02x) or a soft fade in opacity.
*   **Don't** use dividers or lines to separate content. Use the `surface` color steps and vertical white space (at least 80px - 120px between sections).