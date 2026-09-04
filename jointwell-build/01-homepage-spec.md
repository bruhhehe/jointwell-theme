# 01. Homepage spec (velagoods.co.uk / Jointwell)

Built on Shopify Dawn 16.0.0. Every section is a Liquid section under `sections/jw-*.liquid` with a schema, so all copy below can be edited in the theme editor without touching code. Styles live in `assets/jw-tokens.css` (tokens) and `assets/jw-home.css` (layout). `templates/index.json` wires the sections in the order below. The reusable CTA plus trust strip is `snippets/jw-cta-strip.liquid`.

Global rules applied throughout: body text 18px minimum, buttons 48px minimum tall, dark text on light backgrounds, no horizontal scrolling, British English, no em dashes, no medical claims, no fake urgency. Verified locally by rendering every section at 390px and 1366px: scroll width equals viewport width on both.

Theme editor settings that are not code (do these once in Shopify admin): Dawn's own announcement bar text (Online Store > Themes > Customize > Header group) either matches the JW announcement or is removed; the main menu (Online Store > Navigation) is renamed to How it works / Advice / Reviews / Track my order / Contact; the Judge.me app embed is switched on in the theme editor.

---

## Page order and file map

| # | Section | File | Background |
|---|---|---|---|
| 1 | Announcement bar | `sections/jw-announcement.liquid` | accent |
| 2 | Header trust line (under Dawn header) | `sections/jw-header-trust.liquid` | page |
| 3 | Hero | `sections/jw-hero.liquid` | page |
| 4 | Buy box and offer stack | `sections/jw-offer.liquid` | page |
| 5 | That's not on you | `sections/jw-problem.liquid` | band |
| 6 | Borrowed authority | `sections/jw-authority.liquid` | page |
| 7 | Heat chart and feature tiles | `sections/jw-heat-chart.liquid` | band |
| 8 | Comparison | `sections/jw-comparison.liquid` | page |
| 9 | Why Jointwell exists | `sections/jw-why.liquid` | band |
| 10 | What to expect | `sections/jw-timeline.liquid` | page |
| 11 | Condition doorways | `sections/jw-doorways.liquid` | band |
| 12 | Real-home photos | `sections/jw-photo-grid.liquid` | page |
| 13 | What real buyers say | `sections/jw-reviews.liquid` | band |
| 14 | We are the ones selling it | `sections/jw-trust.liquid` | page |
| 15 | Guarantee | `sections/jw-guarantee.liquid` | band |
| 16 | Questions | `sections/jw-faq.liquid` | page |
| 17 | Final call | `sections/jw-final-cta.liquid` | band |
| 18 | Footer note (above Dawn footer) | `sections/jw-footer-note.liquid` | band |

Every section from 3 onwards ends with `{% render 'jw-cta-strip' %}`: a primary button (default "Try it for 90 days", links to `#jw-buy`) and the three-line trust strip "90-day trial, we pay return postage · 2-year UK warranty · Free tracked delivery". The strip appears 14 times on the page (every section from the hero onwards, plus the buy box's own trust lines).

---

## 1. Announcement bar

Purpose: one true offer line, nothing else.

Copy: **Free tracked UK delivery on every order. 90-day trial, we pay the return postage.**

Layout: full width, centred, 18px white on accent terracotta, one line on desktop, wraps to two on mobile. No countdown, no stock count. If the launch price has a real end date, the line can say "Launch price £49.96 until 8 September" as long as the date is true.

Style tokens: `--jw-accent` background, white text.

## 2. Header trust line

Purpose: put the brand, the country and a checkable review count in the first 60px so the visitor knows who she is dealing with.

Copy, left: **Jointwell by Vela Goods, UK**. Right: five stars, then the live Judge.me "all reviews" text widget (`jdgm-all-reviews-text`), with a written fallback beneath it that is hidden as soon as Judge.me renders. Default fallback: **Verified reviews collected by Judge.me**. Replace with the real figure (for example "4.8 from 41 verified reviews") once you have it. Never write a number you cannot show.

Layout: single 48px row, brand left, reviews right, wraps to two rows under 500px. Links to `#jw-reviews`.

## 3. Hero

Purpose: feeling first, product name fourth. A woman her age beside the price before the tier picker.

Copy:
- Eyebrow: For knees, shoulders and elbows that have got worse over the years
- H1: **Get down on the floor with the grandchildren. And get back up again.**
- Sub-line: A cordless heated wrap with massage for knees, shoulders and elbows. Made for knees, shoulders and elbows that have got worse over the years. Try it for 90 days on your worst joint. If it does not help, we pay the postage back.
- Product name line: Jointwell heated joint wrap
- Price: ~~£62.45~~ **£49.96**, note "One payment. Free tracked UK delivery." (pulled from the product when one is chosen in the editor)
- Button: Try it for 90 days → `#jw-buy`
- Review card: Maggie, 64, five stars, Verified buyer, quote `[PLACEHOLDER: real customer quote]`, link "Read the verified review" → her Judge.me review. "Photo supplied by customer" caption appears only when a real customer photo is set.

Layout, desktop: two columns, copy 52% left, photo 48% right, review card overlapping the photo's bottom-left corner. Mobile: copy, button and trust strip first, then photo, then review card.

Image: `assets/jw-hero.jpg` by default (woman in her sixties at the kitchen table, wrap on knee, coral jumper, garden behind). Square, 1024px. Replace through the editor with a 4:5 photo when reshot; see 08-content-shot-list.

Style: H1 44px desktop / 32px mobile, weight 700; price 34px; eyebrow accent colour.

## 4. Buy box and offer stack

Purpose: choose a tier with two wraps preselected, then see every free thing priced so £49.96 looks small against £86.40.

Copy:
- H2: Choose your wrap
- Intro: One for each knee, or one for you and one for your sister. Every tier carries the same trial and warranty.
- Tier picker title: How many?
- Tiers: One wrap / Your worst joint / ~~£62.45~~ £49.96. **Two wraps** (badge Most chosen, preselected) / One for each knee / ~~£89.95~~ £71.96 / Save £27.96 against two at £49.96. Four wraps (badge Best value) / One for you, one for your sister, two for the family / ~~£179.90~~ £99 / Save £100.84 against four at £49.96.
- Button: Add to basket
- Stack title: What you get for £49.96

| In the box | Worth | You pay |
|---|---|---|
| Jointwell heated joint wrap | £62.45 | £49.96 |
| Extension strap (shoulder and elbow) | £9 | Free |
| USB-C charging cable | £6 | Free |
| Mugwort warming sachet | £4 | Free |
| Tracked UK delivery | £4.95 | Free |
| 90-day trial, return postage paid | | Free |
| 2-year warranty, UK support | | Included |
| **Total** | **£86.40** | **£49.96** |

Note under the stack: Values are what each item costs bought separately. Nothing here is a limited-time trick.

Mechanics: the tiers are radio inputs named `id` inside a `/cart/add` form, so the button adds the chosen variant without JavaScript. Choose the product in the section settings; tiers map to variants in order (1st tier = 1st variant) or a variant ID can be typed on each tier. If the product has fewer variants than tiers (today the product has Single and Pair), the extra tier is hidden automatically and the preselected tier is clamped. With no product chosen, the button links to the product page instead.

Layout, desktop: tiers left, stack card right with the "in the box" photo (`assets/jw-box.jpg`) on top. Mobile: stacked, tiers first.

## 5. That's not on you

Purpose: name the enemy (the wheat bag, the pills, the physio bill) and forgive the reader before she reaches the mechanism.

Copy:
- H2: You have tried everything. That's not on you.
- The wheat bag helps for ten minutes. Then it goes cold and you are back at the microwave for the fourth time tonight.
- The pills work until they wear off.
- The physio helps for a few days. Then the stiffness comes back, £50 a visit, next appointment three weeks off.
- Turn (bold): None of them failed because your joints are too far gone. They gave you a moment of ease and then took it back.
- Body: What you were missing was warmth that stays at the level you choose for a full half hour, with massage alongside it, on a wrap that stays put while you drink your tea. That is the whole idea.

Layout: single column, 760px max, each item a white card with an accent left rule. Band background.

## 6. Borrowed authority

Purpose: the NHS and two orthopaedic surgeons say heat and massage help stiff joints. Statements about heat in general, not about this device. This section replaces "clinically proven".

Copy:
- H2: Heat and massage are what the NHS and orthopaedic surgeons recommend for stiff joints
- Intro: Jointwell puts both in one wrap you strap on at the kitchen table. Here is what the people who are not selling anything say about heat and massage.
- NHS: "Heat applied to the affected area can be very effective in reducing pain."
- Brandon Kambach, MD, orthopaedic surgeon: "Heat therapy is an easy, inexpensive, and medication-free way to relieve some types of arthritis stiffness and pain."
- Hayden N. Box, MD, orthopaedic surgeon: "Using heat on sore or stiff joints can bring significant relief, especially when dealing with chronic arthritis pain."
- Footnote: These are statements about heat and massage in general. Jointwell is a comfort device. It is not a medical treatment and does not cure, treat or prevent any condition.

Each quote block has a "Source" link field: add the URL of the NHS page and the two articles before launch (see 09-compliance-checklist).

Layout: three cards, NHS wider on desktop; stacked on mobile.

## 7. Heat chart and feature tiles

Purpose: the one visual that makes the whole case, then four tiles with the specifics (specifics are the trust).

Copy:
- H2: Your wheat bag lasts ten minutes. Your knee hurts all day.
- Intro: Anything you heat in a microwave is hottest the moment you pick it up and cooler every minute after. Jointwell holds the level you choose, from 45°C to 65°C, for a full thirty minutes, then switches itself off.
- Chart: inline SVG, responsive, y axis 35 to 65°C, x axis 0 to 30 minutes. Solid accent line held flat; dashed ochre wheat-bag curve falling from 65°C to lukewarm by 15 minutes. Legend top, axis labels 18px, accessible title and description.
- Caption: The wheat bag line is a typical curve, not a lab result. Boil your own hot water bottle and put a hand on it at twenty minutes. You will not need us to tell you what you find.
- Body: Five heat levels. Three massage strengths. 360 g, so it does not drag on the knee. Charged over USB-C with the same cable as your phone. A 30-minute timer, so it cannot be left running.
- Tiles (image, title, one line): Five heat levels, held / 45°C to 65°C. Pick a level and it stays there for the full 30 minutes. · Three massage strengths / Gentle, comfortable or strong. Chosen on a lit panel you can read without glasses. · Switches itself off at 30 minutes / Every time. Start at 45°C and work up. · Knee, shoulder or elbow / One wrap, one size. The extension strap in the box takes it round a shoulder.

Images: `assets/jw-feature-heat.jpg`, `jw-feature-massage.jpg`, `jw-feature-timer.jpg`, `jw-feature-joints.jpg` (existing site tiles, cropped to 16:10 from the top so the baked-in text does not repeat the title).

Layout: chart 760px centred; tiles 4 across desktop, 2 across tablet, 1 on mobile.

## 8. Comparison

Purpose: Jointwell vs wheat bag vs physio, fair, with running costs. Three cards, stacked on mobile, no swipe.

Copy:
- H2: What the physio does with her hands for £50 a visit, in your armchair for £49.96 once
- Intro: A fair comparison. The physio is worth every penny for the things only a physio can do. This is about the other 29 days of the month.

| | Jointwell (highlighted) | Wheat bag | Physio |
|---|---|---|---|
| Heat | 45 to 65°C, held for 30 minutes | Hottest at the start, then fading | Sometimes, for a few minutes |
| Massage | Three strengths | None | Hands-on, the best there is |
| Stays put | Strapped on, any chair in the house | Slides off | Not applicable |
| Effort | Half an hour with your morning tea | Back to the microwave, again | Travel, waiting room, weeks between visits |
| Cost | £49.96 once | £8 to £15 once | £40 to £70 every visit |

## 9. Why Jointwell exists

Purpose: replaces the founder section. Who are you? A grandson who watched the cold hour before the physio arrived.

Copy: Appendix A of the brief, verbatim, signed "[FIRST NAME], grandson". The text states plainly that physios and doctors got grandad walking and that the wrap did not. Checked line by line in 09-compliance-checklist. The illness named in constraint 8 of the brief is not mentioned anywhere in the theme.

Image: `assets/jw-wrap-mug.jpg` (the wrap on a table beside a mug) as the honest default until a photo of grandad exists. The editor field takes his photo at the kitchen table if he agrees, otherwise his hands and a mug. Never a photo of the owner.

Layout, desktop: photo 40% left (sticky), story 60% right. Mobile: photo then story.

## 10. What to expect, and when

Purpose: set expectations so early refunds drop, phrased as usage and habit, never as outcome.

Copy:
- H2: What to expect, and when
- Intro: Nobody can promise what a wrap will do for your joint. Here is what using it looks like, so you know what you are trying.
- Day 1: Warmth you set, not warmth you wait for. Charge it, strap it on, pick a level. Most people go straight to level 3.
- Day 3: The morning half hour becomes a habit. Kettle on, wrap on. It switches itself off when the tea is finished.
- Week 2: This is when people tell us the first-thing-in-the-morning stiffness is easier to walk off. Your joint gets the deciding vote, not our copy.
- Week 4: A month in. You will know by now whether it has earned its place by the kettle.
- Month 3: Your 90 days are up. Keep it, or post it back and we pay the postage. The warranty runs for two years either way.
- Button: Start the 90 days

Layout: vertical timeline, accent dots on a rule, 760px.

## 11. Condition doorways

Purpose: one wrap, seven ways in, each matching an ad angle and an Advice article.

Copy: H2 Which joint runs your day? Intro: Same wrap, different mornings. Pick the one that sounds like yours. Seven cards: Knee arthritis · Stiff shoulder · Tennis elbow · After a knee replacement · Morning stiffness · Kneeling and gardening · Cold weather aches, each with the one line in the section and a "Read more" link. Links point to `#jw-buy` until the Advice articles in 03-doorway-pages are published; then set each card's link to its article.

Layout: 4 across desktop, 2 across tablet, 1 on mobile, whole card is the tap target.

## 12. Real-home photos

Purpose: women 55 to 70 in real rooms. No men on the homepage.

Copy: H2 In real kitchens, on real knees. Four photos with captions: at the kettle (Walk to the kettle wearing it. 360 g, about the weight of a mug of tea.), armchair reading (Any chair in the house. No wire to the wall.), on the floor with a jigsaw (Down on the floor for the jigsaw. And back up again.), elbow (The extension strap takes it up the arm to the elbow.).

Images: `assets/jw-photo-kettle.jpg`, `jw-photo-armchair.jpg`, `jw-photo-floor.jpg`, `jw-photo-elbow.jpg`. Four more built-in options are selectable per block (garden, bed, radiator, both knees). Shots to reshoot with real customers are in 08-content-shot-list.

## 13. What real buyers say

Purpose: the three verified reviews, each linked to Judge.me, then the full widget.

Copy: H2 What real buyers say. Intro: Collected by Judge.me from verified orders. We cannot write them, edit them or delete the bad ones. Each card links to the review it came from. Cards: Maggie, 64 · Sue, 68 · Janet, 70, quotes `[PLACEHOLDER: real customer quote]` until pasted from Judge.me, "Read the verified review" link, "Photo supplied by customer" caption only when a customer photo is set. Below: the Judge.me review widget (`jdgm-review-widget`) for the chosen product.

## 14. We are the ones selling it

Copy kept verbatim from the current site with two changes: "thirty days" became "ninety days", and each checkable item now carries a link (CE certificate image in the theme, the refund policy page, the reviews section). Do not rewrite.

## 15. Guarantee

Copy:
- Eyebrow: The 90-day worst-joint trial
- H2: If it doesn't help, we don't keep your money.
- Lead: Use Jointwell every morning for up to three months, on your own knee or shoulder, in your own kitchen.
- Body: If you can't feel the difference, send it back within 90 days of delivery for a full refund and **we pay the return postage**. Every wrap carries a 2-year warranty as well, with UK support.
- Worst case, you post it back and you are where you started.
- Button: Start the 90 days

Layout: one bordered card, 760px, band background. The refund policy page in Shopify must be updated to 90 days before this goes live (09-compliance-checklist).

## 16. Questions

Native `<details>` elements, full-width 56px tap targets, plus/minus icon, no JavaScript. The six existing questions (trial length updated to 90 days) plus three new ones: Can I use it after a knee replacement? · How do I charge it, and how long does a charge last? (contains a placeholder for the charge time from the manual) · What happens if I send it back? The "Will it fit me?" answer shows the size diagram `assets/jw-dimensions.jpg`.

## 17. Final call

Copy: H2 Get down on the floor with the grandchildren. And get back up again. Text: Half an hour a morning, so the day stops being planned around one joint. Try it for 90 days. If your knee is not convinced, we pay the postage back. Button and trust strip. Image `assets/jw-photo-floor.jpg` right on desktop, below on mobile.

## 18. Footer note

Brand line Jointwell by Vela Goods, UK. UK address `[PLACEHOLDER]`. Disclaimer, verbatim from the current footer plus the GP line: Jointwell is a heat and massage device for the comfort and relaxation of stiff, tired knees, shoulders and elbows. It is not a medical treatment and does not cure, treat or prevent any disease or condition, including arthritis. If you have diabetes, circulation problems or reduced skin sensation, check with your GP before using any heat product. Support line: UK support by email, 2-year warranty on every wrap, 90-day trial with return postage paid.

---

## Text wireframe, desktop (1366px)

```
[Dawn announcement (set in editor)]
[Dawn header: logo | How it works  Advice  Reviews  Track my order  Contact | basket]
[JW announcement: Free tracked UK delivery on every order. 90-day trial, we pay the return postage.]
[Jointwell by Vela Goods, UK ............................ ★★★★★ 4.8 from 41 verified reviews]

| eyebrow                                   |                                  |
| H1 Get down on the floor...               |        HERO PHOTO (square)       |
| sub-line                                  |                                  |
| Jointwell heated joint wrap               |  [Maggie, 64 ★★★★★ Verified]     |
| £62.45  £49.96  One payment. Free...      |  ["quote" Read the verified rev] |
| [ Try it for 90 days ]  ✓ ✓ ✓             |                                  |

| Choose your wrap                                                               |
| How many?                                 |  [box photo]                     |
| ( ) One wrap ............ £49.96          |  What you get for £49.96         |
| (•) Most chosen Two wraps £71.96          |  table: item | worth | you pay   |
| ( ) Best value Four wraps £99             |  Total £86.40 | £49.96           |
| [ Add to basket ]  ✓ ✓ ✓                  |                                  |

[band] You have tried everything. That's not on you. | 3 cards | turn | body | CTA
Heat and massage are what the NHS... | NHS card | surgeon | surgeon | footnote
[band] Your wheat bag lasts ten minutes... | CHART | caption | body | 4 tiles | CTA
What the physio does... | Jointwell (hi) | Wheat bag | Physio | CTA
[band] [photo 40%] | Why Jointwell exists, story, signature, CTA
What to expect, and when | timeline 5 steps | CTA
[band] Which joint runs your day? | 4 + 3 doorway cards
In real kitchens, on real knees | 4 photos
[band] What real buyers say | Maggie | Sue | Janet | Judge.me widget | CTA
We are the ones selling it... | 4 checks with links | closing | CTA
[band] [ The 90-day worst-joint trial card ] CTA
Questions people ask before they buy | 9 details rows | CTA
[band] Get down on the floor... text + CTA | [floor photo]
[band] Jointwell by Vela Goods, UK | address | disclaimer | support line
[Dawn footer]
```

## Text wireframe, mobile (390px)

```
[Dawn header: ☰ logo basket]
[JW announcement, 2 lines]
[Jointwell by Vela Goods, UK]
[★★★★★ 4.8 from 41 verified reviews]
eyebrow
H1 (32px, 3 lines)
sub-line
product name
£62.45 £49.96
[ Try it for 90 days  (full width) ]
✓ 90-day trial... ✓ 2-year... ✓ Free tracked...
[ HERO PHOTO full width ]
[ Maggie, 64 review card ]
Choose your wrap / intro
( ) One wrap £49.96
(•) Most chosen Two wraps £71.96
( ) Best value Four wraps £99
[ Add to basket (full width) ]
[ box photo ] What you get for £49.96 / table / total
[band] That's not on you: 3 cards, turn, body, CTA
Authority: 3 cards stacked
[band] Chart (full width), caption, body, 4 tiles stacked, CTA
Comparison: 3 cards stacked (no swipe)
[band] photo, Why Jointwell exists, story, CTA
Timeline 5 steps, CTA
[band] 7 doorway cards stacked
Photos 2 x 2
[band] Reviews 3 cards stacked, widget, CTA
Trust checks, closing, CTA
[band] Guarantee card, CTA
FAQ rows (56px each), CTA
[band] Final call text, CTA, floor photo
[band] Footer note
[Dawn footer]
```
