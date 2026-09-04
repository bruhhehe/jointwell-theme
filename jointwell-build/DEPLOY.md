# DEPLOY: preview, check, publish

Repo: github.com/bruhhehe/jointwell-theme. `main` is untouched Dawn 16.0.0. All Jointwell work is on `jointwell-rebuild`. Nothing here is live until you publish a theme in Shopify yourself.

## 1. Connect the branch to an unpublished theme

1. Shopify admin > Online Store > Themes.
2. Add theme > Connect from GitHub. Choose the `bruhhehe` account, the `jointwell-theme` repository, branch `jointwell-rebuild`.
3. Shopify creates an unpublished theme named after the branch. Every push to the branch updates it within about a minute. Leave "Publish" alone.

You can also connect `main` as a second unpublished theme if you want a clean Dawn to compare against.

## 2. Set the things that are settings, not code

Open the unpublished theme with Customize.

- Header group: set Dawn's own announcement bar text to match the JW one, or remove that block. Set the logo.
- Online Store > Navigation: rename the main menu items to How it works, Advice, Reviews, Track my order, Contact, and point them at `/#jw-buy`, the Advice blog, `/#jw-reviews`, the tracking page and the contact page.
- App embeds (bottom of the editor's left panel): switch Judge.me on so the review count and widget render.
- Product page: on the Jointwell product, set Theme template to `jw` so it gets the offer stack, timeline, reviews, trust, guarantee and FAQ under Dawn's product section. On each Advice article, set Theme template to `jw-doorway`.
- Homepage sections: choose the Jointwell product in JW Hero, JW Buy box and stack, and JW What real buyers say. Paste the three real quotes and their Judge.me links into the review cards. Fill the UK address in JW Footer note. Fill the charge time in the FAQ.
- Save. Saving in the editor writes to the theme, not to GitHub; that is expected. Do not edit `templates/index.json` in the code editor while the branch is connected.

## 3. Check on a phone

Use the preview link (Actions > Preview on the theme card) and open it on your own phone, not the desktop's mobile view.

- Nothing scrolls sideways. Try every section, especially the comparison cards, the offer stack table and the chart.
- Every button is easy to hit with a thumb and reads without glasses.
- Hero: headline, price and "Try it for 90 days" are visible without scrolling on a normal phone.
- Buy box: two wraps is preselected; Add to basket adds the right variant; the basket shows the right price.
- Judge.me count shows in the header line and the widget shows under the review cards. If not, the app embed is off.
- FAQ rows open and close by tapping the whole row.
- Links: CE certificate opens, returns policy opens, doorway cards go somewhere sensible.
- Read every line once for anything that sounds like a medical claim or urgency. There should be none.
- Search the page for "PLACEHOLDER". There must be none left.

Then the same on a laptop, and once with Windows high-contrast or a screen reader if you can.

## 4. Publish

1. Update the refund policy (Settings > Policies) to 90 days with return postage paid, so the site and the policy agree.
2. Online Store > Themes > the `jointwell-rebuild` theme card > Actions > Publish. Shopify keeps the old live theme in the list so you can publish it back in one click if anything is wrong.
3. Straight after publishing, open the live site on your phone and repeat the checks in section 3 in two minutes: hero, add to basket, reviews, FAQ.

## 5. After publishing

- Keep `jointwell-rebuild` connected. Future pushes go live immediately, so from then on treat that branch as production and do new work on a fresh branch connected to a fresh unpublished theme.
- The push script `jw-push.cmd` in the repo folder commits everything and pushes `jointwell-rebuild`. Once that branch is live, do not run it without checking what it will push.
