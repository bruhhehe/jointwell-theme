# 09. Compliance checklist

Every claim on the site, in the emails and in the ads, with what backs it up and whether it passes. Three tests:

- **CAP / ASA**: the UK Advertising Codes. Objective claims need evidence held before publication; health claims about a product need evidence about that product, not about heat in general; comparative claims must be fair and verifiable.
- **DMCC**: the Digital Markets, Competition and Consumers Act 2024, consumer protection provisions in force from April 2025. Bans fake reviews, hiding negative reviews, fake urgency and scarcity, drip pricing, and misleading omissions. Fines up to 10% of turnover.
- **MHRA**: a product that claims to treat, prevent or relieve a disease or condition is a medical device and needs UKCA/CE medical marking. This wrap has an EMC/electrical safety certificate only, so it must be sold as a comfort device with no medical purpose claimed.

Status: **Pass**, **Fix before launch**, or **Pass with condition**.

## Site: homepage

| Claim (where) | Substantiation | CAP/ASA | DMCC | MHRA | Status |
|---|---|---|---|---|---|
| "Free tracked UK delivery on every order" (announcement, stack, strip) | Shipping settings: free UK shipping, tracked service | Pass if true for every UK order including Highlands and Islands | Pass, no drip pricing | n/a | Pass with condition: confirm shipping zones cover all UK postcodes |
| "90-day trial, we pay the return postage" (everywhere) | Refund policy page must say 90 days and prepaid label | Pass once policy matches | Pass, and it is a genuine consumer benefit beyond the 14-day statutory right | n/a | **Fix before launch**: update the refund policy from 30 to 90 days |
| "2-year UK warranty" | Written warranty terms on the policy page; UK support address | Pass with terms published | Pass | n/a | Pass with condition: publish the warranty terms |
| "Jointwell by Vela Goods, UK" plus a UK address (header line, footer) | Companies House or sole-trader trading address | Pass | Pass; a trading address is required for distance selling | n/a | **Fix before launch**: fill the address placeholder |
| Live Judge.me count and average (header) | Judge.me widget; the written fallback must match | Pass | Pass: real, unedited count | n/a | Pass with condition: never type a number the widget does not show |
| H1 "Get down on the floor with the grandchildren. And get back up again." | Aspirational, no claim of efficacy | Pass: puffery, not an objective claim | Pass | Pass: no condition named | Pass |
| Sub-line "Made for arthritis, worn joints and long-term stiffness" | Describes the intended user, not an effect | Borderline: "made for arthritis" names a condition | Pass | Risk: naming a disease as the purpose can read as a medical intended purpose | **Fix before launch**: change to "Made for knees, shoulders and elbows that have got worse over the years" (the eyebrow already says this; remove "arthritis" from the sub-line and keep it out of product-purpose sentences) |
| Price £49.96, was £62.45 (hero, tiers) | Compare-at price must be a price the wrap was actually sold at for a meaningful period | Pass only if £62.45 was a real prior selling price | Pass under the same condition; a never-charged "was" price is misleading | n/a | Pass with condition: keep dated proof the wrap sold at £62.45 (the current product page shows £62.45 as the base price, which is enough if orders were taken at it) |
| Tier savings "Save £27.96 on two singles", "Save £100.84 on four singles" | Arithmetic against 2 x £62.45 and 4 x £62.45 | Pass, arithmetic checks (2 x 62.45 = 124.90 minus 71.96 = 52.94; 4 x 62.45 = 249.80 minus 99 = 150.80) | | | **Fix before launch**: the savings lines on the current site compare to something else. Against £62.45 singles the savings are £52.94 and £150.80; against £49.96 singles they are £27.96 and £100.84. Use the £49.96 comparison and say "on two at the launch price" or recompute. Decision: change the lines to "Save £27.96 against two at £49.96" and "Save £100.84 against four at £49.96" |
| Offer stack "Worth" values (£9 strap, £6 cable, £4 sachet, £4.95 delivery) | Marketplace prices for equivalent items, and our own refill price | Pass if each figure is what the item sells for separately | Pass; presenting free items with a value is allowed when the value is real | n/a | Pass with condition: keep a screenshot of the comparable prices; change the sachet line to £1.50 once the 6-pack is £8.95 |
| "Total value £86.40" | Sum of the lines | Pass, arithmetic checks (62.45 + 9 + 6 + 4 + 4.95 = 86.40) | | | Pass |
| "That's not on you" section | Opinion and description of the reader's experience | Pass | Pass | Pass | Pass |
| NHS quote "Heat applied to the affected area can be very effective in reducing pain" | NHS page URL, held | Pass with the source held and quoted accurately | Pass | Pass: attributed statement about heat in general | Pass with condition: paste the URL into the source field and check the wording still matches the live NHS page |
| Surgeon quotes (Kambach, Box) | Source articles, held | Same as above; must be verbatim and in context | Pass | Pass, with the footnote that these are about heat in general | Pass with condition: source URLs |
| Authority footnote "It is not a medical treatment and does not cure, treat or prevent any condition" | | Pass | Pass | Pass: this is the sentence that keeps it a comfort device | Pass |
| Heat chart: wheat bag curve | Illustrative, labelled "a typical curve, not a lab result", reader invited to test | Pass as an illustration that is clearly labelled as such | Pass | n/a | Pass; upgrade to "our own kitchen test, [date]" once the thermometer video exists |
| "Holds the level you choose, 45°C to 65°C, for 30 minutes" | Product specification and the thermometer test | Pass with the test held | Pass | n/a | Pass with condition: run the test in 08 and keep the readings |
| "360 g", "46 cm across", "55 cm strap span", "3000 mAh", "USB-C", "30-minute auto shut-off", "five levels", "three strengths" | Manufacturer spec sheet and a check with kitchen scales and a tape | Pass | Pass | n/a | Pass with condition: weigh and measure one unit and keep the note |
| Comparison table: physio "£40 to £70 every visit", wheat bag "£8 to £15" | Published UK private physio prices; retail wheat bag prices | Pass if representative and the basis is clear | Pass | n/a | Pass with condition: keep three price screenshots for each |
| Comparison "Massage: hands-on, the best there is" (physio column) | Opinion, favourable to the competitor | Pass | Pass | n/a | Pass |
| "Why Jointwell exists" | See separate line-by-line below | | | | See below |
| Timeline "This is when people tell us the first-thing-in-the-morning stiffness is easier to walk off" | Customer reports (emails, reviews) held | Pass if there are genuine reports on file; "people tell us" is a report, not an efficacy claim | Pass | Borderline: "stiffness easier" is a symptom outcome | Pass with condition: keep the customer messages on file; if none exist yet, change to "This is when the morning half hour has become a habit" until they do |
| Timeline "Keep it, or post it back and we pay the postage" | Policy | Pass | Pass | n/a | Pass |
| Doorway card lines (e.g. "Wear and tear, the GP says") | Descriptive | Pass | Pass | Pass: no claim the wrap does anything for the condition | Pass |
| Doorway "After a knee replacement: Once your surgeon and physio say heat is fine" | Advisory, defers to clinicians | Pass | Pass | Pass | Pass |
| Review cards: names, ages, quotes, "Verified buyer" | Judge.me verified reviews, linked | Pass only with real reviews | **DMCC: fake or unverifiable reviews are banned outright** | n/a | **Fix before launch**: replace the three placeholders with real verified quotes and links, or remove the cards. Never launch with placeholders visible |
| "Photo supplied by customer" | Customer's own photo with written permission | Pass | Pass | n/a | Pass with condition: permission on file per photo |
| "Collected by Judge.me from verified orders. We cannot write them, edit them or delete the bad ones." | Judge.me settings: verified-only, no moderation of negatives | Pass | Pass, and it is the DMCC-compliant position | n/a | Pass with condition: do not use Judge.me's "hide review" on negative reviews; replies only |
| "We are the ones selling it" section | Statements about our own conduct | Pass | Pass | n/a | Pass |
| "Our CE test document ... covers electrical safety. It does not say this is a medical device" | The certificate (EMC Directive 2014/30/EU) | Pass | Pass | Pass: correctly limits what the certificate means | Pass; note the certificate shown is EMC only; if electrical safety (LVD) is not on it, change "electrical safety" to "electromagnetic compliance" |
| Guarantee section | Policy | Pass | Pass | n/a | Fix the policy page (above) |
| FAQ "It isn't a cure and we won't pretend otherwise" | | Pass | Pass | Pass | Pass |
| FAQ "Is it safe? Will it burn me?" answer | Spec: 45 to 65°C, 30-minute cut-off; GP warning | Pass | Pass | Pass with the warning present | Pass; keep the diabetes/circulation/sensation line, and add "Do not use while asleep" to the manual and the answer |
| FAQ "When will it arrive?" 1 to 3 working days dispatch, 4 to 8 days delivery | Order records | Pass if typical | DMCC: delivery times must be accurate | n/a | Pass with condition: review against actual order data monthly |
| FAQ charge time | Placeholder | | | | **Fix before launch**: fill from the manual |
| FAQ "Can I use it after a knee replacement?" | Advisory, defers to surgeon | Pass | Pass | Pass | Pass |
| Footer disclaimer | | Pass | Pass | Pass: required | Pass |
| No countdown, no "selling out", no stock counter anywhere | Checked across all sections | | DMCC fake urgency ban | | Pass |
| Announcement "Launch price until 8 September" (if used) | The price genuinely changes on that date | Pass | Pass only if the price really goes up on 8 September; if it does not, this becomes fake urgency | n/a | Pass with condition: if the price is not going up on 8 September, remove the date |

## "Why Jointwell exists": line by line against constraint 8

| Line | Could it be read as "the wrap got him walking" or as a medical claim? | Status |
|---|---|---|
| "A few years ago my grandad stopped walking. His joints had got so bad that he was in bed most of the day and the stairs might as well have been a mountain." | Describes the situation. No product mentioned. | Pass |
| "He got back on his feet. That was the physios and the doctors, months of it, and I want to be clear about that, because a heated wrap did not do it and I am not going to pretend it did." | States the opposite of the banned implication, explicitly. | Pass; this is the sentence that carries the section |
| "What I saw during those months was the hour before the physio arrived. First thing, joints cold, everything stiff, and a wheat bag going round the microwave for the third time." | Describes a cold hour and a wheat bag. | Pass |
| "That was the bit nobody was treating, and it was the bit that decided whether the rest of the day went well." | "Nobody was treating" could imply the wrap treats it. Risk is low because the next paragraph frames it as warmth, and the section ends with "not a cure". | Pass with condition: keep the "not a cure" sentence; consider "nobody was looking after" instead of "treating" |
| "So I went looking for something for that hour. Warmth that stayed warm, that he could strap on at the table and forget about, with a bit of massage, and that he could not leave running by accident. Jointwell is what I found and had tested." | Describes features. "Had tested" refers to the CE/EMC test; do not let it read as clinical testing. | Pass with condition: keep "had tested" or change to "had safety-tested" for clarity |
| "It is for the mornings. It is not a cure and it will not replace your physio." | Explicit disclaimer. | Pass |
| "If it does for your knee what it did for his hour before breakfast, keep it. If it does not, post it back and we will pay the postage." | "What it did for his hour" is about the hour (warmth), not the joint. | Pass |
| Signature "[FIRST NAME], grandson" | First name only, no surname, no photo of the owner. | Pass once the name is filled |
| The illness in constraint 8 | Searched: not present in any theme file, build document, email or ad. | Pass |

Decision applied: "nobody was treating" changed to "nobody was looking after" and "had tested" changed to "had safety-tested" in the section default text. (Applied in `sections/jw-why.liquid`.)

## Emails

| Claim | Where | Status |
|---|---|---|
| The grandad story | Welcome | Same text as the site with the same explicit sentence; Pass |
| "Most people settle at 3 or 4" | Day 3 | Pass with condition: based on customer replies; if no data yet, say "many people" |
| Review request wording, no incentive | Day 10 | Pass under DMCC (no incentive; if one is added it must be for all reviews and stated) |
| SECONDWRAP code with a printed end date | Day 20 | Pass only if the date is real and the code stops working on it; otherwise fake urgency. Fix the date per send |
| "Almost everyone who buys one wrap comes back for a second" | Day 20 | **Fix**: unsubstantiated until there is data. Changed to "A lot of people who buy one wrap come back for a second" and keep the reorder figures on file; if the real rate is under a third, change to "Some people" |
| Sachet "traditional warming herb", "people tell us they miss the smell" | Day 45 | Pass: no medicinal claim |
| "Each sachet lasts about a month" | Day 45 | Pass with condition: test one for a month |
| Abandoned basket: no discount, factual returns statements | G1, G2 | Pass |
| Review reply templates never ask for a rating change or offer anything to change a review | | Pass under DMCC |

## Ads

| Claim | Angle | Status |
|---|---|---|
| Thermometer readings | 3 | Pass only with the real readings from the filmed test; never typed in advance |
| "The NHS lists heat as one of the simple things that helps stiff joints" | 9a, 9e | Pass with the NHS source held; keep it about heat in general |
| "Every physio says warm the joint before you move it" | 7 v2 | **Fix**: "every" is unsubstantiable. Changed to "Physios usually say warm the joint before you move it" |
| "What the physio does with her hands for £50" | 7 | Pass as a price comparison with sources held; the ad also says "not a replacement for your physio" |
| "Not a cure" in the grandad ads | 2 | Pass; required |
| Review carousel | 8 | Pass only with real, verified, linked reviews; do not run before |
| "Junk sellers cannot afford that" | 5 | Opinion, general, no competitor named; Pass |
| "Almost everyone comes back for a second" | not used in ads | n/a |
| All ads: no "relieves pain", no "treats", no condition-outcome claims about the device | all | Pass; checked line by line |
| Meta's own health policy: no "before and after", no implying a personal health condition of the viewer ("your arthritis") | all | Pass; copy addresses joints and mornings, not the viewer's diagnosis. 9a "If your GP has said wear and tear" is a hypothetical; acceptable, but if Meta rejects it, change to "When the GP says wear and tear" |

## Fixes applied in this build

1. Sub-line "Made for arthritis..." changed in `sections/jw-hero.liquid` to "Made for knees, shoulders and elbows that have got worse over the years."
2. Tier savings lines changed in `sections/jw-offer.liquid` presets and `templates/index.json` to "Save £27.96 against two at £49.96" and "Save £100.84 against four at £49.96".
3. "Why Jointwell exists": "nobody was treating" to "nobody was looking after"; "had tested" to "had safety-tested". Same change in the welcome email and the ad scripts.
4. Day 20 email: "Almost everyone" to "A lot of people".
5. Ad 7 v2: "Every physio" to "Physios usually".
6. FAQ safety answer: "Do not use it while asleep" added.

## Fixes the owner must make before launch

1. Refund policy page: 90 days, prepaid label, warranty terms.
2. UK address in the footer note.
3. Real review quotes and links, or remove the cards.
4. Charge time in the FAQ.
5. Source URLs on the three authority quotes.
6. Weigh and measure one unit; keep the note.
7. Run the thermometer test and keep the readings.
8. Confirm the compare-at price history for £62.45.
9. Remove the 8 September date from any announcement if the price is not actually changing that day.
