# Cowork brief: Jointwell (velagoods.co.uk) full marketing build, v2

Give this to Claude Cowork with `primal-queen-to-jointwell-report.md`. Read the report first; it contains the analysis and the decisions. This brief says what to produce, in what order, and what the constraints are. Cowork will write theme code directly to the Shopify theme repository on GitHub.

---

## 1. Who I am and what this is

I run Jointwell, a cordless heated joint wrap with vibration massage for knees, shoulders and elbows, sold on Shopify at velagoods.co.uk. One SKU, three tiers (1 wrap £49.96, 2 wraps £71.96, 4 wraps £99), free UK delivery, 30-day guarantee with return postage paid (moving to 90 days), 2-year warranty, CE tested (EMC). Judge.me collects verified reviews. Three real testimonials are on the page (Maggie 64, Sue 68, Janet 70).

**Customer:** UK women aged 55 to 65+, knees or a shoulder that have worsened over years, GP says "wear and tear", wheat bag / creams / physio have half worked. On Facebook daily. Distrust adverts. Trust other women their age.

**Model being borrowed from:** primalqueen.com. The report explains which of their mechanics to take (feeling-first headline, named enemy, customer identity, origin story, repeated CTA and guarantee, itemised offer stack, expectation timeline, condition doorways, product ladder) and which to leave (fake scarcity, hype language, hidden specs).

---

## 2. Hard constraints. Do not break these.

1. **No medical claims.** Never "clinically proven", "treats arthritis", "relieves pain", "cures", as a claim about this device. Use borrowed authority ("Heat and massage are what the NHS and orthopaedic surgeons recommend for stiff joints") and customer reports ("people tell us"). The product is a comfort device, not a medical device. Keep the existing disclaimer footer.
2. **No fake urgency or scarcity.** The DMCC Act bans it in the UK. Deadlines only if real. No "selling out", no fake countdowns.
3. **No invented reviews, names, quotes or photos.** Use only the three existing testimonials and any I add. Where you need placeholders, mark them `[PLACEHOLDER: real customer quote]`.
4. **British English throughout.** Plain words. No "unleash", "unlock", "empower", "journey", "game-changer".
5. **Write for a 62-year-old reading on a phone without her glasses.** Short sentences. One idea per section. No horizontal scrolling. Body text 18px minimum, buttons 48px minimum, dark text on light backgrounds.
6. **No em dashes in any copy.**
7. **No photo, name (beyond first name) or personal details of the owner on the site.** The origin story is about my grandfather, written in first person, signed with a first name. See section 3.1, item 9.
8. **The origin story must never imply the wrap got my grandfather walking.** Physio and medical treatment did. The wrap is for the cold hour in the morning. Any sentence that could be read as "heat wrap reversed a bedridden condition" is a medical claim and is out. The word "cancer" does not appear anywhere on the site, in emails or in ads.
9. **Everything must be buildable and maintainable by one person with no developer.** Where a section needs custom Liquid, JSON or CSS, write it, test it, and commit it (see section 5).

---

## 3. Deliverables, in this order

Write planning and copy files to `jointwell-build/` at the repo root (git-ignored from the theme; see section 5). Write theme code into the theme directories. Finish one deliverable before starting the next. Ask me questions only where the report and this brief leave something undecided; otherwise decide and record it in `jointwell-build/00-decisions.md`.

### 3.1 Homepage: `jointwell-build/01-homepage-spec.md` plus theme code

For every section, in page order, give in the spec: purpose (one line), final copy ready to use, layout on desktop and mobile, image description and aspect ratio, button text and link, style tokens, and the theme file(s) that implement it.

Then implement it: a Liquid section per block under `sections/jw-*.liquid` with a schema so I can edit copy in the theme editor, CSS in `assets/jw-home.css`, and the homepage template `templates/index.json` wired to those sections in this order:

1. Announcement bar (real offer only)
2. Header: logo, nav renamed ("How it works", "Advice", "Reviews", "Track my order", "Contact"), live Judge.me count and average
3. Hero: feeling-first H1, sub-line, one large image, price, one CTA, three-line trust strip, one testimonial card (Maggie) beside the price
4. Tier picker with two-wrap preselected, itemised offer stack with a £ value on every free line
5. "That's not on you" problem section (moved up from below the buy box)
6. Borrowed authority: NHS first, two surgeons, done
7. Heat-decay chart vs wheat bag (inline SVG, responsive)
8. Comparison: three columns (Jointwell / wheat bag / physio), stacked cards on mobile, no swipe
9. **"Why Jointwell exists"** (replaces the founder section). First person, signed "[FIRST NAME], grandson". Structure: grandad stopped walking; physio and doctors got him back on his feet, stated plainly; the untreated hour before the physio arrived, cold joints, wheat bag round the microwave; I went looking for something for that hour; what it is and is not; the guarantee. Use the draft in Appendix A as the starting text. Image slot for one photo of my grandfather at his kitchen table wearing the wrap if he agrees, otherwise hands and a mug, otherwise the wrap on the table. No photo of me.
10. Expectation timeline: Day 1, Day 3, Week 2, Week 4, Month 3
11. Condition doorways strip: knee arthritis / stiff shoulder / tennis elbow / after a knee replacement / morning stiffness / kneeling and gardening / cold weather aches, each with one line and a link to its Journal article
12. Real-home photo grid (women only; specify four shots to reshoot if needed)
13. "What real buyers say": the three existing cards, linked to their Judge.me reviews, "photo supplied by customer" caption, full Judge.me widget below
14. "We are the ones selling it" trust section (keep existing copy verbatim)
15. Guarantee block, 90 days: "The 90-day worst-joint trial"
16. FAQ (existing questions plus three new ones you propose), full-width tap targets, native `<details>` elements
17. Final CTA: "Get down on the floor with the grandchildren. And get back up again."
18. Footer with UK address placeholder, disclaimer, "Jointwell by Vela Goods"

After every section from 3 onwards, a reusable snippet `snippets/jw-cta-strip.liquid` renders the CTA plus trust strip (90-day trial, we pay return postage · 2-year UK warranty · Free tracked delivery).

Also produce text wireframes of the full page for desktop and mobile in the spec.

### 3.2 `jointwell-build/02-style-guide.md` plus `assets/jw-tokens.css`

Colour palette as CSS custom properties (hex, contrast ratios checked against WCAG AA at 18px), two fonts maximum from Shopify's font library with sizes for H1/H2/H3/body/caption/button on mobile and desktop, button and card styles, icon set, photography rules (real homes, women 55 to 70, daylight, no models under 50, no studio white), and a do/don't list. Update `config/settings_data.json` only for the font choices; put everything else in the tokens file.

### 3.3 `jointwell-build/03-doorway-pages.md` plus Journal articles

For each of the seven condition doorways: a 600 to 900 word Journal article in plain English, H1, meta title and description, the internal link to the buy button, one testimonial to feature (or a placeholder), the SEO keyword it targets, and the Facebook ad it pairs with. Articles cannot be committed as theme files; write them as ready-to-paste markdown plus a `templates/article.jw-doorway.json` template with a persistent CTA block so each article ends on the buy button.

### 3.4 `jointwell-build/04-offer-and-product-ladder.md`

Final offer stack table with values. Guarantee wording (90 days). Second-purchase plan: second-wrap upsell, strap and liner pack £9.95, mugwort sachet refills £8.95, neck/shoulder and lower-back versions, November gift bundle. For each: product page copy, price, launch timing, which email sells it. Produce `templates/product.jw.json` and `sections/jw-product-stack.liquid` for the itemised stack on product pages.

### 3.5 `jointwell-build/05-email-flows.md`

Every email written in full, subject line and body: welcome (the grandad story, shortened), day 3 getting the most out of it, day 10 review request, day 20 second wrap for a partner, day 25 "before your trial ends", day 45 sachet refills, abandoned basket (2), monthly Advice digest template, review-reply templates (positive, mixed, negative). Trigger and timing for Klaviyo or Shopify Email on each.

### 3.6 `jointwell-build/06-facebook-ads.md`

Campaign structure for Meta (one campaign, women 55 to 70, UK, broad, Facebook feed and Reels, £30 to £50/day for testing). For each of the ten angles in the report:

**Image ads:** headline overlay, primary text, description, CTA button, image description (frame, who, where, lighting), 1:1 and 4:5. Three variants per angle.

**Video ads:** script with shot list (shot / duration / on screen / subtitle text / voiceover), 15s and 30s versions, phone-filmed in a real home, large subtitles, slow cuts. One per angle.

The grandad angle replaces the "founder story" angle: a to-camera or voiceover version of Appendix A, with constraint 8 applied to every line. Plus the review-carousel ad (Maggie, Sue, Janet), a testing plan (first four angles, kill rule at £30 cost per purchase after 20 purchases, scaling rule) and a UTM/naming convention.

### 3.7 `jointwell-build/07-social-media.md`

Facebook Page and Group ("the morning half hour" or better): description, rules, first 10 seed posts, 12-week posting rhythm with every post written (text plus image/video description), and how to turn group replies into on-page testimonials with permission. Instagram-lite version. Note that YouTube Shorts and TikTok are secondary.

### 3.8 `jointwell-build/08-content-shot-list.md`

Everything to photograph or film in one day: shot, setting, who, clothing, props (tea, wrap, jigsaw, garden, crossword, dog), angle, and which section or ad it feeds. Include the heat-test video (hot water bottle vs Jointwell at 0/15/30 minutes with a kitchen thermometer), and the grandad shots if he agrees (kitchen table, wrap on, mug, no direction to look happy; let him be himself). No shots of me.

### 3.9 `jointwell-build/09-compliance-checklist.md`

Every claim on the site, in emails and in ads, with: substantiation, CAP Code / ASA pass or fail, DMCC Act (urgency, reviews), MHRA (device claims). The grandad section gets its own line-by-line check against constraint 8. Flag anything to change before launch.

### 3.10 `jointwell-build/10-launch-plan.md`

The 90-day sequence from the report as a week-by-week checklist with owner (me), tool and time estimate. Metrics: landing page conversion (2.5 to 4%), cost per purchase (under £25), average order value (£70), verified reviews (50 by day 60), refund rate (under 5%).

---

## 4. How to work

- Read the report fully before writing anything.
- Write final copy, not descriptions of copy.
- Where you need something from me (grandad's consent and photo, UK address, real Judge.me count, product photos), put it in `jointwell-build/00-decisions.md` under "Needed from owner" and carry on with a placeholder.
- When all ten are done, write `jointwell-build/00-README.md` listing every file with a one-line summary and the order to implement them in.

Start with the homepage.

---

## 5. Repository and deployment rules

The theme repo is connected to Shopify through the GitHub integration. Shopify pulls whatever branch is connected to a theme, and if that theme is the live one, a push goes straight to customers. So:

1. **Never commit to `main` or to whichever branch is connected to the published theme.** Create `jointwell-rebuild` from `main` and do all work there. Confirm in `00-decisions.md` which branch is live before the first commit.
2. **I will connect `jointwell-rebuild` to an unpublished theme in Shopify** (Online Store > Themes > Add theme > Connect from GitHub). That gives a preview URL. Do not publish a theme yourself and do not touch theme settings in the Shopify admin.
3. **Authentication is handled by the git credential helper on this machine.** The personal access token is not in this brief, not in any file you write, not in any commit message, and not to be echoed to the terminal. If a push fails on auth, stop and tell me; do not ask for or attempt to reconstruct the token.
4. **Commit small and often**, one section per commit, message format `home: hero section` / `home: offer stack` / `email: day 10 review request`. Push after each deliverable.
5. **Do not delete or rewrite existing theme files.** New sections are additive (`sections/jw-*.liquid`, `snippets/jw-*.liquid`, `assets/jw-*.css`). The only existing files you edit are `templates/index.json`, `layout/theme.liquid` (to include the two CSS files) and `config/settings_data.json` (fonts only). Keep a copy of each original as `*.orig` in `jointwell-build/originals/` before editing.
6. **Validate before pushing.** Run `shopify theme check` if the CLI is available; otherwise lint Liquid for unclosed tags and confirm every section has a valid schema block. A broken `index.json` blanks the homepage.
7. **Add `jointwell-build/` to `.gitignore` for theme purposes** is not possible since Shopify ignores unknown top-level folders anyway; commit it, but keep no secrets, customer data or review exports in it.
8. **Judge.me** is installed as an app; reference its widgets via the app block or the documented `<div class="jdgm-widget jdgm-review-widget">` markup rather than copying script tags.
9. Write a `jointwell-build/DEPLOY.md` that tells me, step by step, how to preview the branch theme, what to check on a phone, and how to publish it when I am satisfied.

---

## Appendix A: "Why Jointwell exists" starting text

A few years ago my grandad stopped walking. His joints had got so bad that he was in bed most of the day and the stairs might as well have been a mountain.

He got back on his feet. That was the physios and the doctors, months of it, and I want to be clear about that, because a heated wrap did not do it and I am not going to pretend it did.

What I saw during those months was the hour before the physio arrived. First thing, joints cold, everything stiff, and a wheat bag going round the microwave for the third time. That was the bit nobody was treating, and it was the bit that decided whether the rest of the day went well.

So I went looking for something for that hour. Warmth that stayed warm, that he could strap on at the table and forget about, with a bit of massage, and that he could not leave running by accident. Jointwell is what I found and had tested.

It is for the mornings. It is not a cure and it will not replace your physio. If it does for your knee what it did for his hour before breakfast, keep it. If it does not, post it back and we will pay the postage.

[FIRST NAME], grandson
