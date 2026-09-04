# 02. Style guide

Everything here is implemented in `assets/jw-tokens.css` as CSS custom properties. Fonts are set in `config/settings_data.json` (the only change made to that file). Nothing else in Dawn's settings was touched.

## Colour

| Token | Hex | Use | Contrast |
|---|---|---|---|
| `--jw-bg` | #FBF7F1 | page ground, warm off-white | text on it 15.6:1 |
| `--jw-bg-alt` | #F2EBE1 | alternating section bands | text on it 14.2:1 |
| `--jw-card` | #FFFFFF | cards, tier rows, tables | text on it 17.4:1 |
| `--jw-border` | #E3D9CB | hairlines and card borders | decorative |
| `--jw-text` | #1F1B16 | all body and heading text | see above |
| `--jw-muted` | #5A5249 | captions, secondary lines | 6.6:1 on bg, 7.4:1 on white |
| `--jw-accent` | #9A3F1C | buttons, eyebrows, chart line | white on it 7.0:1 |
| `--jw-accent-dark` | #7D3114 | hover, links | white on it 9.4:1, on bg 8.1:1 |
| `--jw-accent-soft` | #F6E4DA | selected tier, highlighted card | text on it 13.9:1 |
| `--jw-good` | #2E6B4A | ticks, "Free", "Verified buyer" | 6.3:1 on white |
| `--jw-warn` | #8A6A00 | wheat-bag line in the chart | 5.4:1 on white |
| `--jw-star` | #D99A1E | stars only, never text | decorative |
| `--jw-focus` | #1D4ED8 | keyboard focus ring | 3px, offset 3px |

All text/background pairs pass WCAG AA at 18px (4.5:1) with margin; every pair used for body text is above 6:1.

## Type

Two weights of one family from Shopify's font library: **Nunito Sans** 700 for headings (`nunito_sans_n7`), **Nunito Sans** 400 for body (`nunito_sans_n4`). Fallback stack: "Segoe UI", Arial, sans-serif. Chosen for open letterforms, a tall x-height and clear 1/l/I at small sizes on a phone.

| Role | Mobile | Desktop | Weight | Line height |
|---|---|---|---|---|
| H1 | 32px | 44px | 700 | 1.15 |
| H2 | 26px | 34px | 700 | 1.2 |
| H3 | 20px | 22px | 700 | 1.3 |
| Lead paragraph | 20px | 20px | 400 | 1.5 |
| Body | 18px | 18px | 400 | 1.55 |
| Caption | 16px | 16px | 400 | 1.5 (captions and trust strip only, never body) |
| Button | 18px | 18px | 700 | 1.2 |

Sentence case everywhere. No all-caps. No italics for emphasis; bold only.

## Buttons

Primary: accent background, white text, 48px minimum height, 12px 24px padding, 8px radius, 2px border in the same colour, darkens on hover and focus. Full width on mobile, minimum 280px on desktop. One primary button per section; there are no secondary buttons on the homepage. Text links are accent-dark, underlined, 3px underline offset.

## Cards

White, 1px border, 12px radius, 20px padding, soft two-layer shadow. Highlighted cards (the selected tier, the Jointwell comparison column, the guarantee) use a 2px accent border and the accent-soft background.

## Icons

Text characters only, so nothing has to load: ✓ (U+2713) for trust lines and verified badges, ★ for stars, a CSS-drawn plus/minus circle for the FAQ. No icon font, no SVG icon set.

## Spacing and shape

Section padding 48px mobile / 72px desktop. Content max width 1100px; reading-width sections 760px. Grid gap 16px. Tap targets 48px minimum, FAQ rows 56px.

## Photography rules

- Real homes: kitchen table, armchair, bed, carpet, back door, garden. Never a studio white background, never a lifestyle set.
- Women aged 55 to 70. No models under 50 on the homepage. Men only in a "she buys for him" context on other pages, if at all.
- Daylight from a window. No flash, no colour grading, no filters.
- The wrap on the joint in use, not held up to camera.
- Props: mug of tea, crossword, jigsaw, newspaper, wellies, dog. No phones.
- Customer photos: use the customer's own phone photo, caption "Photo supplied by customer", link to the review. A slightly soft photo beats a perfect one.
- Squares (1:1) for grids and the hero; 4:5 for single portraits.

Note on the current built-in photos: they were generated for the existing site and are used as placeholders so the page is never empty. Replace them with the shots in 08-content-shot-list before spending on ads; the report is explicit that this audience checks.

## Do and don't

Do: short sentences, one idea per section, specifics (45 to 65°C, 360 g, 46 cm), "people tell us", "the NHS says", plain British words (post it back, kettle on).

Don't: "clinically proven", "relieves pain", "treats arthritis", "unleash", "unlock", "empower", "journey", "game-changer", countdowns, "selling out", stock counters, invented names or quotes, em dashes, text under 16px, light grey text, centred body copy longer than two lines, carousels that need a swipe.
