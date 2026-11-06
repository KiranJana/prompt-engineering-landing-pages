# Good Prompt A: PREPPED

A conversion spec: an XML-tagged brief for a single-file student landing page with one job.

```
<role>
You are a senior conversion-focused product designer and front-end engineer who has shipped landing pages for DTC food brands (think the clarity of Factor, the personality of a Gen Z snack brand). You write sharp copy, design with intent, and ship clean, accessible, production-quality code.
</role>

<goal>
In ONE response, build a complete, polished, single-file landing page for a local custom meal-prep business for students. The page has ONE job: get a student to **start their first week** (primary CTA: "Build my first week"). The secondary goal is capturing an email for the waitlist/discount if they're not ready.
</goal>

<business_brief>
Edit these values; use them verbatim everywhere. Never invent other facts that contradict them.
- Brand name: PREPPED
- Tagline idea: "Real food. Zero dining-hall regret."
- Location: serves students at [UNIVERSITY NAME] in [CITY]: all on-campus dorms + apartments within 3 miles of campus
- What it is: chef-cooked, macro-labeled meals, customized per student (pick proteins, carbs, spice level, allergies, calorie/protein goal). Cooked fresh locally, never frozen.
- Plans (per week): Starter 5 meals ($11.49/meal), Regular 10 meals ($9.99/meal, MOST POPULAR), Locked-In 15 meals ($8.99/meal)
- Offer: 30% off your first week with a .edu email. Free delivery. Skip, pause or cancel any week, no contract.
- Delivery: Sunday evening + Wednesday evening drops, to your dorm lobby or door, in insulated bags. Meals last 5 days in the fridge, heat in 2-3 minutes.
- Menu: 12 rotating meals each week. Include 6 sample meals with name, calories, protein, carbs, fat, price tags (e.g., Spicy Gochujang Chicken Bowl, Chipotle Steak Burrito Bowl, Lemon Herb Salmon & Rice, Tofu Peanut Noodles (V), Turkey Pesto Pasta, Breakfast Egg & Potato Box).
- Dietary: high-protein, vegetarian, vegan, halal options, gluten-free, dairy-free; top-9 allergens labeled on every meal.
- Audience: 18–24 undergrads/grad students. Pains: dining hall is repetitive and closes early, takeout destroys their budget, no time/skill/kitchen to cook, want to hit gym/protein goals, exam weeks wreck their eating.
- Sample proof (clearly fictional placeholders, first name + major + year only): 3 testimonials with specific results, e.g., "Saved ~$60/week vs DoorDash", "Hit 150g protein daily during midterms".
</business_brief>

<design_direction>
Aesthetic: "fresh editorial". The polish of a 2026 DTC food brand (think Sweetgreen, Huel, Graza): confident, appetizing, generous whitespace, a little playful in the copy, never childish or corporate. Typography and food carry the attention, not decoration.
- Typography: one modern grotesk for headlines and body (e.g., "Geist" or "Instrument Sans" from Google Fonts). Headlines at weight 600 with tight tracking (≈ -0.04em) and line-height ≈ 0.95. Set one or two accent words per key headline in a serif italic (e.g., "Instrument Serif") in the accent color. Headline sizes use clamp() so the hero headline is huge on desktop and still fits on a 360px screen. Use tabular numbers for prices and macros.
- Color: food-first tokens as CSS custom properties: warm white background (#FAF9F6, not beige/cream), pure white surfaces, near-black ink, ONE vivid accent (tomato red-orange that passes AA with white button text), soft food tints for cards and section backgrounds (peach, sage, butter), herb green for dietary tags, and a lime highlight used only for small badges on dark surfaces. Alternate light sections with a few dark ink sections for rhythm. Pass WCAG AA contrast for all text.
- Surfaces: borderless cards with a large radius (24–28px) on white or tinted backgrounds. Separate things with whitespace, tint and 1px hairlines (ink at ≈ 8% opacity), not outlines. Soft, layered, low-opacity shadows only on floating elements (macro card, order summary, sticky bar, dialog). Use a bento-style grid where it sharpens hierarchy.
- Components: solid pill primary button; a quieter secondary (text link with arrow or ghost pill); segmented controls and soft-gray chips with an ink selected state; small uppercase pill badges (e.g., "30% off week 1", "Never frozen") that sit flat in the layout; a scrolling marquee of meal names styled as a quiet typographic band.
- Visuals: do NOT hotlink random stock photos (they break or get hallucinated). Instead build appetizing visuals with inline SVG/CSS in a flat, top-down product-art style: no black outlines, shading through tonal fills and subtle gradients, food sitting on large tinted plates or rounded wells, plus clean macro "nutrition label" cards. It should read as product art, not clip art. Wrap each visual in an element with a data-photo="describe ideal photo" attribute so real photography can be swapped in later.
- Motion: tasteful only. Short fade/slide-up on scroll (≤ 16px) via IntersectionObserver, gentle hover lift with a growing soft shadow, a slow marquee. Respect prefers-reduced-motion (disable all non-essential motion).
</design_direction>

<page_structure>
Build these sections in this exact order. Each has a conversion purpose; honor it.
1. **Announcement bar**: "30% off your first week with your .edu email · Free delivery to [UNIVERSITY NAME] dorms". Dismissible.
2. **Sticky nav**: logo, 3–4 anchor links (Menu, How it works, Pricing, FAQ), primary CTA button. Collapses to a hamburger on mobile.
3. **Hero** (everything above the fold on a 1366×768 laptop AND a 390×844 phone): outcome-driven headline (not "Welcome to…"), one-line subhead stating what/who/where, primary CTA + secondary text link ("See this week's menu"), ONE proof point (e.g., "★ 4.9 from 300+ [UNIVERSITY] students" marked as sample), hero visual of an illustrated meal + floating macro card (e.g., "52g protein · 640 cal").
4. **Marquee strip**: this week's meal names scrolling.
5. **Problem → Solution ("Sound familiar?")**: 3 relatable student pains rendered as short, funny, honest cards, each flipping to how PREPPED fixes it.
6. **How it works**: 3 numbered steps: Customize → We cook fresh → Delivered Sun & Wed. Short and visual.
7. **Interactive meal builder (the centerpiece)**: user picks plan size (5/10/15), protein goal (e.g., Maintain / Lean bulk / Cut), diet filter (All / Vegetarian / Vegan / Halal / Gluten-free), and spice level. Updates live: filtered meal cards, estimated daily protein/calories, weekly price with the 30% first-week discount shown as a strikethrough. CTA under it: "Build my first week".
8. **This week's menu**: 6 meal cards with SVG illustration, name, dietary tags, a mini nutrition label (cal/P/C/F), and allergen icons. Filter chips work (shared state with the builder is a bonus).
9. **Pricing**: 3 plan cards; Regular is visually highlighted as "Most popular". Show per-meal price, weekly total, first-week price, and what's included. Under the cards: "Skip, pause or cancel anytime · no contract". Put one testimonial directly beside/below pricing (proof at the point of hesitation).
10. **Comparison table**: PREPPED vs Dining hall vs Takeout apps vs Cooking yourself on cost/meal, time, protein control, freshness, flexibility. Mobile: stacked cards or horizontally scrollable table with a sticky first column.
11. **Social proof wall**: 3 specific testimonials (name, major, year, a specific result), plus a row of stats marked as sample.
12. **FAQ accordion** (accessible): delivery times/locations, what if I'm not in my dorm, allergies, how long meals last, how to pause/cancel, payment (meal swipes/dining dollars? answer honestly: not accepted, card/Apple Pay yes), group/team orders.
13. **Final CTA block**: bold restated promise + primary CTA + an email capture ("Not ready? Get the menu + 30% off code") with inline validation (must be a valid email; show a friendly .edu nudge) and a success state, without a page reload.
14. **Footer**: delivery area, contact, Instagram/TikTok links (#), small print.
Plus: a **sticky bottom CTA bar on mobile** that appears after scrolling past the hero and hides near the final CTA.
</page_structure>

<copy_rules>
- Voice: a smart upperclassman friend. Direct, warm, a little funny, never cringe slang, no "fam/no cap/slay".
- Lead with outcomes and money/time saved, not features. Every headline should pass the "so what?" test.
- Be specific: numbers, times, prices, grams. No vague claims ("high quality", "best in class", "revolutionary").
- Scannable: headlines ≤ 8 words, paragraphs ≤ 2 short sentences, bullets over prose.
- CTA labels describe the outcome ("Build my first week", "See the menu") and are never "Submit" or "Learn more".
- Never use lorem ipsum. All copy is final and on-brand.
</copy_rules>

<technical_requirements>
- Output: ONE self-contained `index.html` file. Tailwind CSS via the Play CDN (`https://cdn.tailwindcss.com`) with a `tailwind.config` extending your color/font tokens, Google Fonts, and vanilla JavaScript in a single <script> at the end. No frameworks, no build step, no other external dependencies.
- Semantic HTML5 landmarks (header, nav, main, section with aria-labelledby, footer), one <h1>, logical heading order.
- Accessibility: WCAG 2.2 AA. Visible focus rings, full keyboard support (nav, builder controls, accordion, modal/menus), aria-expanded/aria-controls on toggles, labels on all inputs, alt text or aria-hidden on decorative SVGs, tap targets ≥ 44px, a skip-to-content link.
- Responsive and mobile-first: flawless at 360, 390, 768, 1024, 1440px. No horizontal scroll at any width.
- Performance: no images over the network, minimal JS, `font-display: swap`, animations only on transform/opacity.
- SEO basics: <title>, meta description, Open Graph tags, theme-color, an inline SVG favicon, and LocalBusiness JSON-LD using the brief's details.
- Valid HTML: never nest block elements (div, p) inside <button> or <a>; use spans styled as block.
- JS must be clean and commented by section: builder state + pricing math, menu filtering, accordion, mobile nav, sticky CTA logic, email validation, scroll reveals. No console errors.
</technical_requirements>

<restrictions>
Do NOT:
- use the generic "AI look": purple/blue gradients, glassmorphism everywhere, three identical icon+title+text feature cards, centered-everything layouts, or the Inter-only font stack.
- use dated 2021–23 trend styling: neo-brutalist thick black outlines with hard offset shadows, rotated "sticker" badges, dot/grain background textures, hand-drawn squiggle underlines, outlined clip-art illustrations, skeuomorphic receipt edges, or a beige/cream-everything palette.
- add more than ONE primary CTA style. Every primary button says the same action and uses the same accent color; secondary actions are visually quieter.
- invent business facts that aren't in the brief (other prices, locations, guarantees, certifications). If something's missing, choose a sensible neutral phrasing.
- present placeholder stats or testimonials as verified: mark them with a small "sample" note in an HTML comment and a visually subtle footnote.
- hotlink external images, add popups on page load, autoplay audio/video, or use dark patterns (fake countdown timers, fake scarcity).
- leave TODOs, placeholder sections, or half-wired interactions. Every button and control must do something.
- explain the code at length. Output the file first.
</restrictions>

<process>
Work through these phases in order. Do Phases 1–2 silently in your head and output only the final result.
Phase 1, Strategy: Pick the single core promise and the top 3 objections (price, "will I actually like it", commitment). Map which section answers each.
Phase 2, Design system: Define color tokens, type scale (clamp-based), spacing scale, radius, shadow, and the component vocabulary (button, pill badge, card, chip, segmented control, nutrition label) so the page is consistent.
Phase 3, Build: Write the full semantic HTML in the section order above with final copy.
Phase 4, Interactivity: Wire all JS behaviors. Verify the pricing math in integer cents to avoid floating-point drift (weekly = meals × per-meal cents; first week = Math.round(weekly × 70 / 100); display with $ and two decimals). Expected first-week totals: 5 meals $40.22, 10 meals $69.93, 15 meals $94.40.
Phase 5, QA pass: Before outputting, check every item in <definition_of_done> and fix anything that fails.
</process>

<definition_of_done>
- [ ] A visitor understands what, who, where and price within 5 seconds of the hero; primary CTA visible without scrolling on laptop and phone.
- [ ] All 14 sections + mobile sticky CTA are present, in order, with final copy (zero lorem ipsum, zero TODOs).
- [ ] Meal builder updates price, macros and visible meals instantly and correctly for every combination; the 30% discount math is right.
- [ ] Menu filters, accordion, mobile nav, announcement dismiss, email validation + success state all work with mouse, touch and keyboard.
- [ ] No horizontal scroll at 360px; type and spacing feel intentional at every breakpoint.
- [ ] AA contrast, visible focus states, reduced-motion respected, one <h1>, labeled inputs.
- [ ] The page looks like a distinct brand someone designed, not a template.
</definition_of_done>

<output_format>
Return the complete `index.html` in a single code block, ready to save and open in a browser. After the code block, add at most 5 bullets: key design decisions + exactly which brief values to edit (brand, university, city, prices).
</output_format>
```
