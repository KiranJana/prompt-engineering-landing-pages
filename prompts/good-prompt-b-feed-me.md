# Good Prompt B: Feed Me

A creative brief for an award-level, 10-page Next.js brand site with a mascot and a 3D hero.

```
You are a world-class creative web developer and motion designer. Build a high-end, award-winning (Awwwards-level) website for a custom meal prep brand called **"Feed Me – Ind Wes Custom Meals"**. The site should feel playful, energetic, and appetizing, like a food brand with real personality, not a generic template.

## Brand and vibe
- Brand name: Feed Me – Ind Wes Custom Meals. The "Feed Me" voice is cheeky and hungry ("Feed me, Seymour" energy, but friendly). Use it in headlines, buttons, and microcopy (e.g. "Feed Me Now," "Feed Me Monday," "Still hungry?").
- Color theme: **red and white only**.
  - Primary: bold, appetizing red (e.g. #E4002B / tomato red) plus a deep red (#9E0A1F) for depth.
  - Base: clean white (#FFFFFF) and warm off-white (#FFF6F3).
  - Use near-black (#1A1A1A) for body text only, and soft pink-red tints for backgrounds and highlights.
  - Food photography supplies the other colors; the UI stays red and white.
- Style: oversized expressive typography, chunky rounded shapes, hand-drawn doodles, sticker-style badges, red/white checkered and diner-style patterns, and mouth-watering food photography with subtle grain.
- Mascot: an original, friendly character, a hungry smiling red meal-prep container with a big mouth that says "Feed Me!". It reacts to scrolling, hovering, and clicks (opens its lid, licks its lips, does a happy dance when you add a meal).
- Avoid: stock-template layouts, centered-everything sections, generic gradients, and boring card grids.

## Tech stack
- Next.js (App Router) + TypeScript + Tailwind CSS
- GSAP (ScrollTrigger, SplitText, Flip) for scroll storytelling
- Framer Motion for UI and page transitions
- Lenis for smooth scrolling
- Three.js / React Three Fiber for one hero 3D moment (a floating red meal box with ingredients orbiting it)
- Lottie or Rive for micro-animations
- Fully responsive, mobile-first, 60fps

## Pages
1. **Landing page**
   - Hero: giant "FEED ME." headline with a split-text reveal, the 3D or parallax meal box, and floating ingredients that follow the cursor. Main CTA: "Build My Box."
   - Sticky scroll story, "From Our Kitchen to Your Fork": 4 pinned steps (Choose, Customize, We Cook, You Devour) with morphing illustrations.
   - Red and white marquee strips of rotating food words ("FRESH • CUSTOM • HOT • YOURS").
   - Interactive Build-a-Bowl teaser: drag and drop ingredients, with live calories and macros animating as you add them.
   - Meal showcase carousel with tilt-on-hover cards that flip to show nutrition.
   - "Your Week, Sorted" calendar that fills up on scroll.
   - Testimonials as a physics-based pile of sticker notes you can toss around.
   - Animated stats counters, an FAQ with bouncy accordions, and a big playful footer with the mascot saying goodbye.
2. **Menu / Meals**: filterable grid (high-protein, vegan, keto, family, low-carb) with animated filter transitions, quick-view modals, and allergen icons.
3. **Custom Meal Builder (hero feature)**: a step-by-step wizard covering goal, diet, allergies, portions, meals per week, and delivery days. It has a live-updating price and macro summary, red and white confetti on completion, and a mascot that reacts at each step.
4. **How It Works**: scroll-driven timeline with a red progress path that draws itself.
5. **Pricing / Plans**: weekly and monthly toggle with morphing numbers, plus a wiggling "Most Popular" badge.
6. **About / Our Story (Ind Wes)**: kinetic typography, a chef/team section with hover-reveal fun facts, and sourcing counters.
7. **Recipes / Blog**: magazine-style layout with a reading progress bar and a "Surprise Me" random recipe button.
8. **Contact / Delivery Zone Checker**: ZIP code input with an animated map result and a funny success or fail message.
9. **Cart / Checkout**: slide-in cart drawer, a free-delivery progress bar, and a celebratory "You've been fed!" confirmation page.
10. **Custom 404**: "This page got burnt" with a playful animation or mini-game.

## Animation and interaction requirements (go big)
- Custom cursor that changes to a fork, spoon, or "FEED" label depending on context, with magnetic buttons.
- Page transitions that wipe like a lunch-box lid opening and closing.
- Scroll-triggered reveals, parallax layers, pinned sections, and horizontal scroll galleries.
- Text effects: split-letter reveals, scramble text, and wavy underlines.
- Hover micro-interactions on every interactive element (squish, wiggle, bounce, ingredient pop-outs).
- Easter eggs: a Konami code that rains food emojis, clicking the mascot 5 times for a surprise, and a hidden catch-the-falling-veggies mini-game that rewards a discount code.
- Gamified loading screen with a plate or container filling up, then "Dinner is served."
- Sound toggle (off by default) with subtle sizzle, pop, and click sounds.
- Respect `prefers-reduced-motion` with graceful fallbacks.

## Quality bar
- Lighthouse 90+ on performance, accessibility, and SEO. Lazy-load heavy assets, use AVIF/WebP, and keep animations GPU-friendly (transform and opacity).
- WCAG AA contrast, especially red-on-white and white-on-red text, plus keyboard navigation, focus states, and semantic HTML.
- Clean, modular component architecture with reusable animation hooks.
- Realistic placeholder content (meal names, macros, prices, reviews). No lorem ipsum.
- Include SEO metadata, Open Graph tags, and a favicon in the brand red.

## Deliverables
1. A short design-system summary (red/white palette, type scale, spacing, motion principles).
2. The full working codebase, with file structure and setup instructions.
3. Build in stages: first the design system and landing page, then the remaining pages, then polish animations. Show me the landing page first so I can approve before you continue.

Push the creativity as far as you can. When in doubt, choose the more surprising, more delightful option.
```
