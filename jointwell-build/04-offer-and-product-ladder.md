# 04. Offer and product ladder

## Final offer stack (homepage buy box and product page)

| In the box | Worth | You pay |
|---|---|---|
| Jointwell heated joint wrap | £62.45 | £49.96 |
| Extension strap (shoulder and elbow) | £9 | Free |
| USB-C charging cable | £6 | Free |
| Mugwort warming sachet | £4 | Free |
| Tracked UK delivery | £4.95 | Free |
| 90-day trial, return postage paid | | Free |
| 2-year warranty, UK support | | Included |
| **Total value** | **£86.40** | **£49.96** |

"Worth" figures are what each item sells for on its own on UK marketplaces (strap and cable) or what we will charge for it as a separate SKU (sachet, see below). Keep them defensible: if the refill 6-pack sells at £8.95, one sachet is worth £1.49 at most and the "£4" line should become "£1.50". The rule for every line is that a customer could check it.

Bonus to add within 90 days (report 5.5): one physical extra that costs under £3 and reads as £10 to £15. Chosen: a printed A5 card, "The morning half hour", with the routine on one side and the heat-level guide on the other, laminated. Add it as a stack line "Morning routine card, £3, Free" once it exists.

Tiers, unchanged: One wrap £49.96 (was £62.45). Two wraps £71.96 (was £89.95), preselected, "Most chosen". Four wraps £99 (was £179.90), "Best value". The Four wraps variant does not exist in this store yet; create it so the third tier shows.

## Guarantee wording (90 days)

Short form, under every button: **90-day trial, we pay return postage**

Full form, guarantee section and product page:

> **The 90-day worst-joint trial.** If it doesn't help, we don't keep your money. Use Jointwell every morning for up to three months, on your own knee or shoulder, in your own kitchen. If you can't feel the difference, send it back within 90 days of delivery for a full refund and we pay the return postage. Every wrap carries a 2-year warranty as well, with UK support. Worst case, you post it back and you are where you started.

Policy page wording (Settings > Policies > Refund policy), replace the existing 30-day text with:

> You have 90 days from the day your order is delivered to return any Jointwell wrap for a full refund of what you paid, for any reason, used or unused. Email us at [support email] with your order number. We will send you a UK returns address and a prepaid postage label. Once it arrives back we refund you in full to the way you paid, usually within 5 working days. Refills, straps and liners can be returned unused within 30 days. If anything arrives damaged or faulty at any time in the two-year warranty, tell us and we will replace it or refund you, your choice, postage on us.

## The product ladder

The wrap is one sale. Everything below is a reason to email the list and a second reason to come back. Launch order and timing are set so each product exists before the email that sells it goes out.

### 1. Second wrap (exists today)

- What: the Two wraps tier, and a partner-price offer to single-wrap buyers.
- Price: £24.96 for a second wrap when bought within 30 days of the first (£49.96 + £24.96 = £74.92, slightly above the £71.96 pair price so the pair stays the better deal on day one).
- Launch: day 1. Set up as a Shopify automatic discount "Second wrap" that applies to a second unit of the wrap for customers with one previous order, or as a discount code SECONDWRAP sent only in the email.
- Sold by: email 4 (day 20, "One for the other knee"), and the November gift email.
- Product page copy: none needed; it is the same product.

### 2. Strap and liner pack, £9.95

- What: one replacement extension strap plus two washable inner liners that sit between the wrap and the skin. Low margin, high frequency. Keeps people opening emails.
- Product title: Jointwell strap and liner pack
- Handle: `jointwell-strap-and-liner-pack`
- Price: £9.95, free delivery over £20, otherwise £2.95 tracked.
- Launch: week 6 (needs sourcing; see 10-launch-plan).
- Sold by: email 6 (day 45) as a cross-sell line, the monthly Advice digest, and the product page of the wrap ("Often bought with").
- Product page copy:

  > **A fresh liner and a spare strap.** The inner liner is the part that touches your skin, so it is the part that wants washing now and then. This pack has two washable liners and a spare extension strap, the one that takes the wrap round a shoulder or up to an elbow, in case yours has gone the way of the odd sock. Fits every Jointwell wrap. £9.95, and the same 2-year warranty as the wrap.

  Stack lines for `product.jw` template: Extension strap £9 / Two washable liners £6 / Total £15, you pay £9.95.

### 3. Mugwort sachet refills, 6-pack £8.95

- What: the consumable. Six mugwort warming sachets that slip into the pocket of the wrap.
- Product title: Jointwell mugwort warming sachets, pack of 6
- Handle: `jointwell-mugwort-sachets-6`
- Price: £8.95, free delivery over £20, otherwise £2.95 tracked. A 12-pack at £15.95 once the 6-pack has sold.
- Launch: week 6, same supplier order as the liners.
- Sold by: email 6 (day 45, the main refill email), then every 45 days to anyone who has not bought refills, and the monthly digest.
- Product page copy:

  > **The warm herbal note in the pocket.** Every wrap ships with one mugwort sachet in the front pocket. It is a traditional warming herb, and people tell us they miss the smell when it fades. This is six more. Slip one in, switch the wrap on, and the heat brings it out. Each sachet lasts around a month of daily use. Nothing medicinal is claimed for it; it is there because the morning half hour is nicer with it.

  Stack lines: Six sachets £12 (at £2 each bought singly) / Total £12, you pay £8.95.

  Compliance note: no claim that mugwort does anything for joints. "Traditional warming herb" and "people tell us they miss the smell" are the limit.

### 4. Neck and shoulder wrap

- What: a U-shaped heated wrap for the neck and both shoulders. Same supplier category, new ad angle, new email.
- Product title: Jointwell neck and shoulder wrap
- Handle: `jointwell-neck-and-shoulder-wrap`
- Price: £54.96, compare at £69.95. Bundle with the knee wrap at £89.96.
- Launch: week 10, once the knee wrap has 50 reviews and the refills are live. Needs its own CE/EMC test document before listing.
- Sold by: a dedicated launch email to the whole list, then a "neck" doorway article and ad angle.
- Product page copy (first paragraph; rest follows the wrap's structure):

  > **For the stiff neck that arrived with the reading glasses.** The same held warmth and gentle massage as the knee wrap, shaped to sit round the neck and across both shoulders while you sit. Five heat levels, three massage strengths, cordless, and it switches itself off at thirty minutes. Same 90-day trial, same 2-year warranty.

### 5. Lower back wrap

- What: a wide belt-style heated wrap for the lower back.
- Product title: Jointwell lower back wrap
- Handle: `jointwell-lower-back-wrap`
- Price: £59.96, compare at £74.95.
- Launch: week 12 or later, after the neck wrap. Needs CE/EMC document.
- Sold by: launch email, a "gardener's back" doorway article, and the winter ad set.
- Product page copy, first paragraph:

  > **For the back that decides whether you garden today.** A wide heated belt that straps round the lower back and stays there while you move about the kitchen. Held warmth from 45°C to 65°C, massage if you want it, cordless, and off by itself at thirty minutes. Try it for 90 days on us.

### 6. November gift bundle

- What: two wraps in a gift box with a card, for women who buy for sisters, husbands and their own mothers.
- Product title: Jointwell gift pair
- Handle: `jointwell-gift-pair`
- Price: £74.96 (the pair price plus £3 for the box and card, which cost under £2).
- Launch: 1 November, on sale until 18 December (last posting dates permitting). Real dates, stated plainly; no countdown.
- Sold by: email 9 ("Two under the tree"), a Facebook Group post, and one ad angle in November only.
- Product page copy:

  > **One for her, one for you.** Two Jointwell wraps in a box that does not need wrapping, with a card you can write in. The 90-day trial runs from the day it is opened, not the day it is bought, so a present opened on the 25th has until the end of March. Tell us the delivery date you want and we will hold it.

  Trial-start-from-opening is a promise; put it in the refund policy for gift orders.

## What this does to customer value

| | Today | With the ladder |
|---|---|---|
| Average first order | £50 to £60 (mostly single wraps) | £65 to £72 (two-wrap preselect plus stack) |
| Second purchase within 90 days | none | 20 to 30% take a second wrap, refills or the strap pack |
| Average customer value at 6 months | £55 | £75 to £90 |

At £75 to £90 a customer, a cost per purchase of £25 on Facebook is profitable. At £55 it is not. The ladder is what makes the ads work, which is why refills and the second-wrap email come before any scaling in 10-launch-plan.

## Theme files

- `templates/product.jw.json`: Dawn's main product section (vendor and share removed), then JW Product offer stack, What to expect, What real buyers say, We are the sellers, Guarantee, Questions. Assign it to the wrap in the product's Theme template dropdown. The refill and strap products use the same template with their own stack lines edited in the theme editor.
- `sections/jw-product-stack.liquid`: the itemised stack with an editable list, the product's live price in the total row, and the trust strip.
