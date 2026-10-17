# Liquid Gold — standalone extraction

Open `liquid-gold-standalone.html` directly in a modern browser. No installation, server, or internet connection is needed. WebGL2 with floating-point framebuffer support is needed for animation; a static preview is shown otherwise.

The original liquid solver, gold background shader, typography/refraction layers, idle pouring, and tile-flip transition were extracted from https://getplate.pages.dev/home/js/liquid.js and https://getplate.pages.dev/home/js/wow.js on 2026-10-16. Original effect: Plate / Ohad Krispin. Source comments and attribution are preserved. The editor and standalone host are new.

## Change the text

Use the brand and headline fields, then **Apply text**. The description is directly editable below the headline. Open **Appearance** for four color grades. The original “Tell your agent / Make it mine” button turns a brand name into a balanced headline, selects a different color grade, and triggers the original tile-flip wave. The headline is vertically centered and left aligned; the category and lower-right dial have been removed. Put each headline line on a separate row (up to four). Changes stay in memory for the current session.

You can also call this JavaScript API after the page finishes loading:

```js
window.liquidGold.setText({
  brand: 'Your Brand',
  headline: ['Ideas that', 'keep moving.'],
  lede: 'Your description here.\nMove the pointer to pour.',
  grade: 'gold' // gold, glass, sage, warm
});
window.liquidGold.pour();
```

To change the defaults permanently, edit the `cur` initialization and form field defaults in the HTML. All scripts, shaders, and three WOFF2 fonts are embedded in the file. There are no external runtime dependencies or analytics. Fonts are Geist, Archivo, and Bodoni Moda, distributed under the SIL Open Font License.

Verified in Chrome: WebGL rendering, animated text replacement, embedded fonts, and no console warnings or errors. Reduced-motion preferences suppress idle motion and tile flipping. Pause/Resume stops and restarts the simulation.

## 5SENSE

Open `5sense.html` directly in a modern browser. All fonts and scripts are embedded; there are no runtime network dependencies.

The five sections retain the reference's lighting, gold palette, typography, glass frame, and WebGL2 fluid engine:

- Eyes: localized magnification and thermal shimmer.
- Ears: expanding wavefronts refract the surface and text. No audio is played.
- Memory: floating particles use the same drift, magnetic attraction, and speed-driven flares as Instinct. Twelve brighter neuron bases carry short branching connections and smaller satellite particles. Local pulses travel along the branches, and faint brain-wave oscillations gently pass through the gold.
- Instinct: magnetic glowing sparks and speed-driven flares.
- Taste: liquid silk. Hundreds of fine luminous particles advect through a continuous curved flow field, leaving persistent glowing threads over the original gold surface. The pointer attracts and bends the current; pressing creates a stronger swirling bloom. Small glints travel through the stream, and the text receives a restrained liquid shimmer. The flow uses the section's selected color and pauses with scrolling, reduced motion, visibility changes, and the page's motion button.

Text editors are always visible. Each section has a **Color** button with 12 choices: Liquid gold, Cool glass, Sage, Warm silver, Rose quartz, Copper, Amethyst, Arctic blue, Pearl, Deep teal, Emerald, and Graphite. Colors apply immediately; **Apply text** saves the headline and description. Text and color choices save independently per section in localStorage when available. **Reset** restores that section's text and original gold color. **Pour again** restarts its surface pattern.

Use the top navigation to move between sections. Move or drag over a canvas to interact. On touch screens, horizontal gestures interact while vertical swipes scroll the page, including when the swipe begins on the canvas. Keyboard users can focus a canvas and press Enter. **Pause motion** stops the animation across the page. Offscreen sections do not animate, reduced-motion preferences suppress continuous idle animation, and unavailable WebGL2 falls back to a still preview in the selected color. Canvases flow normally with the page rather than sticking inside each section, and textareas grow to fit their contents instead of introducing inner scroll areas. GPU animation pauses during scrolling; new renderers initialize after scrolling settles so they do not interrupt native page scrolling.

### Mobile source

The live mobile DOM and running `#wow-gl` renderer at https://getplate.pages.dev/ were inspected on 2026-10-16 with an iPhone-sized, touch-enabled browser. The source uses the same shader engine on desktop and mobile; `coarse` selects 60% coverage, 62% radius reach, a 128 simulation grid, a 320 dye grid, and 16 pressure iterations. `5sense.html` uses that phone baseline on every device, with separate motion profiles for each sense.

Source references: https://getplate.pages.dev/home/js/wow.js and https://getplate.pages.dev/home/js/liquid.js. Original engine by Plate / Ohad Krispin; standalone sensory variations, color controls, and optional softer glass composite are adaptations in `5sense.html`.
