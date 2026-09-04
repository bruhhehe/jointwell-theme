# 11. Post-purchase emails (paste into Shopify Email > Automations)

Both trigger on "Order placed" for the Jointwell heated joint wrap, with a delay. Shopify Email cannot be set up through the API, so create each automation in admin and paste the copy below. Plain text, one column, 18px or larger, dark text, one button.

## Email A. Day 21: one for the other knee

**Trigger:** Order placed, wait 21 days. Exclude anyone who ordered Two wraps or Four wraps.
**Discount:** create a fixed-amount discount code SECONDWRAP, £25 off, limited to the One wrap variant, one use per customer, valid 14 days from send. That makes a second wrap £24, so £49 + £24 = £73, still above the £69 pair so the pair stays the better deal for new buyers.
**Subject:** One for the other knee, Sarah?
**Preview:** Three weeks in. A second wrap is £24 until [date].

Hello [first name],

You've had your Jointwell about three weeks now. By this point most people have a routine: kettle on, wrap on, half an hour, then the day.

The thing we hear most often at three weeks is "I wish I'd got two." One for each knee. Or one for you and one for the shoulder that plays up in the evening. Or one for the person in the other armchair, who has been borrowing yours.

So, for the next fourteen days, a second wrap is £24 instead of £49. Same wrap, same 90-day trial, same 2-year warranty, free tracked delivery. Use the code SECONDWRAP at checkout.

[Button: Get a second wrap for £24]

If yours has not earned its place by the kettle, you don't need this email. You need the returns page, and we pay the postage: [link to /pages/returns-policy].

Stan
Jointwell by Vela Goods, UK

## Email B. Day 30: the sachet refill

**Trigger:** Order placed, wait 30 days. Only send once the sachet 6-pack is published (product exists as a draft: jointwell-mugwort-sachets-6).
**Subject:** The smell will be fading about now
**Preview:** Six more mugwort sachets, £8.95.

Hello [first name],

The mugwort sachet in the front pocket of your wrap lasts about a month of daily use, so around now the warm herbal smell will be going. Some people don't notice. Quite a few tell us they miss it.

If you're one of them, this is six more. Slip one in, switch the wrap on, and the heat brings it out. £8.95 for the six, which is about a month each.

[Button: Six more sachets, £8.95]

Nothing medicinal is claimed for it. It's there because the morning half hour is nicer with it. If you'd rather go without, lift the sachet out and the wrap works exactly the same.

Stan
Jointwell by Vela Goods, UK

## Lead magnet delivery

Anyone who fills in the footer form is tagged `routine-pdf`. Create a Shopify Email automation: trigger "Customer tagged routine-pdf", no delay, subject "Your 7-morning stiffness routine", body one line plus the PDF link. Upload `jointwell-build/jointwell-7-morning-routine.pdf` under Content > Files and paste its URL as the button link.
