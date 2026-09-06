# 13. The optimal pass (branch `jointwell-v3`), 5 September 2026

Two versions existed: the first build (report structure, honest copy, CTA after every section, itemised value stack) and the live rebuild on `jointwell-rebuild` (product-first hero with tiers, proof strip, authority with faces and evidence, five-column comparison, photo reviews, routine timeline, box list, checks-plus-guarantee panel, lead magnet, sticky bar, anchor nav, dispatch clock, quiz, video slot). This pass keeps what each did best and re-orders the page to the five jobs a cold-traffic sales page has to do in sequence: name the pain, install the belief, show the mechanism only we have, stack the offer, remove the reasons to wait.

`jointwell-rebuild` is live. Nothing here touches it. Connect `jointwell-v3` to a new unpublished theme, check it on a phone, then publish it from the theme list when you are happy (DEPLOY.md).

## What was kept from the live version

Hero with the tier picker, ticks, proof line, mini review card, dispatch clock, reassurance icons, quiz button and video slot. Proof strip of checkable items. Authority with headshots and the evidence card. Five-column comparison. Photo reviews with "uses it on" tags. The Morning Half Hour timeline written as a protocol. Checks-plus-guarantee panel with the four plain terms. Lead magnet. Sticky bar. Anchor-only nav on the homepage. Footer with company and cancellation lines. The velagoods colour scheme.

## What was brought back from the first build

- **The enemy and the belief shift**, now the heaviest section on the page and placed second: everything in the cupboard gave warmth that faded; none of it failed because her joints are too far gone; a stiff joint wants warmth that stays; the ten minutes was the problem, not the heat. It ends with the three-step mechanism (the old "How it works" tiles, merged in) and one line stating the only claim we make. File: `sections/jw-belief.liquid`.
- **CTA and trust strip after every section.** The rebuild had switched most of them off. They are back, and every one below the hero jumps to the offer block, not back up to the hero.
- **The itemised value stack**, with a value on every line the owner can evidence (the wrap at its £65 full price, strap and cable at what they sell for, the sachet at the refill price, the routine card at print cost, delivery at Royal Mail's tracked rate) and a "Bought separately, £89. You pay £49" line. Values that cannot be evidenced (warranty, trial) carry no figure.

## What is new

- **A second buy box near the bottom**, `sections/jw-offer-block.liquid`, id `#jw-offer`: box photo, the value stack, the specifics toggle, the tier picker (same variants as the hero, kept in sync by one script), the button with the live price, the four guarantee terms, payment icons. This is the block every CTA on the page points at, so the reader is only ever asked one question: how many.
- **Doorways as tabs that open in place**, `sections/jw-doorways.liquid`, no JavaScript: seven situations, each with a photo, the situation in one line, how it goes on, when, one thing worth knowing, the buy button and a link to the long article. A woman who arrived from a shoulder ad taps "Stiff shoulder" and sees her morning without leaving the page.
- **Sticky bar watches both buy boxes** and hides when either is on screen.
- **Mobile overflow fixed**: the block button was 19px wider than the screen on the live version. `box-sizing: border-box` is now on every button.
- **Two wraps preselected** in both pickers (average order value target £70).

## The order, and why

1. Hero: pain headline, ticks, proof, price, tiers, button, reassurance. She can buy in the first screen if she arrived warm.
2. Proof strip: four checkable things before a word of pitch.
3. Why it works (enemy, belief, mechanism). The longest section, as it should be.
4. Heat chart: the mechanism made visible.
5. Authority: the NHS and two surgeons agree with the belief.
6. Reviews: women like her, with photos, saying it in their words.
7. Why Jointwell exists: the grandson, mirroring her mornings.
8. Doorways: her exact situation, in place.
9. Comparison: the alternatives she has already tried, priced.
10. The Morning Half Hour: what to expect, so refunds drop.
11. Checks and guarantee: the last reasons to wait, removed.
12. Offer block: how many, and everything she gets.
13. FAQ: objections as support.
14. Lead magnet: the not-yet reader leaves an email.
15. Final call.

## Urgency, kept honest

Dispatch clock (real), the autumn price with its real end date, a sticky bar, a marquee-free page. No countdown to nothing, no stock warnings. That is the DMCC line and it stays.

## Compliance flags carried forward

1. **Reviews.** The five review cards (Sarah, Margaret, Linda, Brenda, Susan) are real buyers, confirmed by the owner on 6 September. They stay. Add each one's Judge.me link in the review card settings so the "Verified buyer" tick can be checked by anyone who wants to.
2. The "sold in Australia" line that an earlier pass added was not true and has been removed from the hero, the reviews note and every schema default. The owner confirmed there was never an Australian run. Do not add it back.
3. The sub-line "so the first steps of the day aren't the worst" is an outcome phrase. It is mild, but "so the first steps of the day start warm" is safer.
4. Source URLs on the authority quotes and evidence lines are still blank in places.
5. The product page (`templates/product.json`) was not touched in this pass.

## Files changed in this pass

`sections/jw-belief.liquid` (new), `sections/jw-doorways.liquid` (rebuilt), `sections/jw-offer-block.liquid` (new), `snippets/jw-cta-strip.liquid`, `snippets/jw-product-card.liquid`, `snippets/jw-sticky-bar.liquid`, `sections/jw-authority.liquid`, `sections/jw-why.liquid`, `sections/jw-timeline.liquid`, `sections/jw-heat-chart.liquid`, `sections/jw-word-guarantee.liquid`, `sections/jw-header.liquid` (anchor defaults), `assets/jw-home.css`, `templates/index.json`. `jw-how-it-works` and `jw-box` stay in the theme but are no longer on the homepage.

## 6 September fix: why the homepage showed 404

Shopify's GitHub sync silently drops any file that fails its schema validation, and then drops every template that references a dropped section. Three sections failed: `jw-hero` and `jw-reviews` had a settings header longer than 50 characters, and `jw-offer-block` (with the same pattern in hero, reviews and proof strip) had text settings with `"default": ""`. Shopify rejects both. Without those three sections, `templates/index.json`, `product.json`, `product.jw.json` and `page.jw-landing.json` were rejected too, so the homepage had no template and returned 404.

Fixed by shortening the headers and removing the blank defaults (a text setting with no default is simply blank). Each schema was checked against Shopify's own validator on an unpublished theme before this commit. Rules to keep for any new section: header content 50 characters or fewer, section and block names 25 or fewer, never `"default": ""` on a text or textarea setting.

`jointwell-v3` is now the branch connected to the LIVE theme. Anything pushed to it goes to customers. Start the next pass on a new branch.
