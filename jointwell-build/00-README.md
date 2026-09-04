# Jointwell build: file index

Read in this order. Implement in this order.

| File | What it is |
|---|---|
| `00-decisions.md` | Every open question, decided, plus the list of things needed from the owner. |
| `DEPLOY.md` | How to preview the branch theme, what to check on a phone, how to publish. |
| `01-homepage-spec.md` | Section-by-section copy, layout, images and file map for the homepage, with desktop and mobile text wireframes. Implemented in `sections/jw-*.liquid`, `snippets/jw-cta-strip.liquid`, `assets/jw-home.css`, `templates/index.json`. |
| `02-style-guide.md` | Colours, type, buttons, cards, icons, photography rules, do/don't. Implemented in `assets/jw-tokens.css` and the font lines in `config/settings_data.json`. |
| `03-doorway-pages.md` | Seven Advice articles, ready to paste, with meta, keyword, testimonial slot and paired ad. Template `templates/article.jw-doorway.json`. |
| `04-offer-and-product-ladder.md` | Final offer stack, 90-day guarantee wording, second-purchase plan and product page copy. Template `templates/product.jw.json`, section `sections/jw-product-stack.liquid`. |
| `05-email-flows.md` | Every email in full, with triggers and timing. |
| `06-facebook-ads.md` | Campaign structure, ten angles with image and video ads, testing plan, naming. |
| `07-social-media.md` | Facebook Page and Group, seed posts, 12-week rhythm, permission process. |
| `08-content-shot-list.md` | One-day shoot: every photo and video, who, where, props, which section it feeds. |
| `09-compliance-checklist.md` | Every claim, with substantiation and CAP / DMCC / MHRA pass or fail. |
| `10-launch-plan.md` | The 90-day sequence as a week-by-week checklist with metrics. |
| `originals/` | Untouched copies of the three Dawn files this build edits. |

All ten deliverables are present. Theme files added by them beyond the homepage: `templates/article.jw-doorway.json`, `sections/jw-article-cta.liquid`, `templates/product.jw.json`, `sections/jw-product-stack.liquid`.

Order to implement: 00-decisions (read), DEPLOY steps 1 to 3, 01 and 02 (already built, check on a phone), 04 (policy and product setup), 09 (owner fixes), then 03, 05, 07, 08, 06, and 10 as the week-by-week checklist that sequences all of it.
