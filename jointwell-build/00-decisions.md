# 00. Decisions

Recorded as they were made. Anything the brief and report left open is decided here so the build never stalls.

## Repository and deployment

- 2026-09-04: Repo seeded with clean Shopify Dawn 16.0.0 on `main`. The store's published theme (`store/main` on cjyz7c-cf.myshopify.com, currently the Bunny Perch store) is not connected to this repository, so nothing here can reach customers until the owner connects a branch and publishes.
- Work branch: `jointwell-rebuild`, created from `main`. All Jointwell code is additive: `sections/jw-*`, `snippets/jw-*`, `assets/jw-*`. The only existing files edited are `templates/index.json`, `layout/theme.liquid` (two stylesheet lines) and `config/settings_data.json` (fonts only). Originals are in `jointwell-build/originals/`.
- Pushes are made from the owner's computer via `jw-push.cmd` (commits with the owner's identity and pushes `jointwell-rebuild`). The script, its log and the commit-message file are git-ignored.
- An unpublished theme named "jointwell-rebuild PREVIEW (do not publish)" was created in the store from the public Dawn 16.0.0 zip as a scratch target. It contains no Jointwell files. It can be deleted or ignored; the branch-connected theme is the real preview.
- A Harvard Medical School shield (`logo-mark.svg` in the assets folder) was not used. It is a third party's trademark and would imply endorsement.

## Product and store

- The store today has one product (Bunny Perch). The Jointwell product on velagoods.co.uk has two variants (Single, Pair). The buy box hides any tier without a matching variant, so with two variants the Four wraps tier is hidden until a third variant exists. Decision: create the Four wraps variant (£99, compare at £179.90) when the product is set up in this store.
- Price and compare-at price on the hero come from the product when one is chosen; typed fallbacks (£49.96 / £62.45) are used until then.
- Guarantee moved from 30 to 90 days everywhere on the page, per the brief. The refund policy page must be changed to match before publishing (DEPLOY.md step 4).

## Copy

- "Clinically proven" removed. Authority section uses the NHS quote and two orthopaedic surgeons, phrased as statements about heat and massage in general.
- The trust section ("We are the ones selling it") is kept verbatim apart from "thirty days" becoming "ninety days".
- Timeline is written as habit and usage. "People tell us" is used once, in Week 2, as a report rather than a claim.
- No em dashes anywhere in theme copy. Checked with a search across `sections/jw-*` and `jointwell-build/`.
- The illness named in constraint 8 of the brief is not mentioned anywhere in the theme or the build folder.
- FAQ: the charge-time answer contains a placeholder rather than an invented figure. The battery capacity (3000 mAh) is from the existing product page.

## Images

- Built-in photos are taken from the owner's existing site assets (`knee masager` folder) and resized to 1200px max, JPEG quality 82. Only photos of women are used on the homepage. Photos of men (greenhouse, newspaper, hi-vis, crossword man) are not used.
- The "Why Jointwell exists" default image is the wrap beside a mug, not a stock older man, because a stranger's photo presented as grandad would be dishonest. The editor field takes the real photo when it exists.
- Review cards carry no photo by default. "Photo supplied by customer" appears only when a customer photo is set, so the caption is never attached to a stock image.
- The existing site photos appear to be AI-generated. They are acceptable as placeholders and for the feature tiles, but the report's warning stands: reshoot with real customers before scaling ads. Shot list in 08.

## Needed from owner

- Grandad's consent and a photo at his kitchen table (or hands and a mug), and his first name for the signature.
- UK address for the footer note.
- The three real review quotes (Maggie, Sue, Janet) and their Judge.me review links; customer photos if they will share them.
- Real Judge.me count and average for the header fallback line, once there are enough reviews.
- The Jointwell product created in this store with three variants, and chosen in the three sections that ask for it.
- Charge time and sessions per charge from the manual, for the FAQ.
- Source URLs for the NHS quote and the two surgeon quotes (the existing site cites them; paste the links into each quote block).
- The CE certificate as a PDF if preferred to the image already in `assets/jw-ce-certificate.jpg`.
