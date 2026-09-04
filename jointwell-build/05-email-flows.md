# 05. Email flows

Every email in full. Plain text with one button; no banners, no columns, no stock photos. Sender name "Jointwell" with the owner's first name in the signature. 18px body in whatever template the tool provides. British English, no em dashes, no medical claims, no urgency that is not real.

Triggers are written for Klaviyo; Shopify Email equivalents are noted where they differ. `[FIRST NAME]` is the owner. `{first_name}` is the customer, with a fallback of "there" (as in "Hello there").

Placeholders you must fill before switching a flow on: `[SUPPORT EMAIL]`, `[RETURNS ADDRESS]`, `[REVIEW LINK]` (the Judge.me review request link), `[GROUP LINK]` (the Facebook Group), `[STRAP PACK LINK]`, `[REFILLS LINK]`.

---

## Flow A: Welcome (new subscriber or first order)

**Trigger.** Klaviyo: Subscribed to list, or Placed Order with no prior orders, whichever first; send once. Shopify Email: Welcome automation. **Timing:** 10 minutes after the trigger.

**Subject:** Why Jointwell exists (the short version)
**Preview:** It started with the hour before the physio arrived.

Hello {first_name},

I want to tell you why this wrap exists, because it is not a story about a product.

A few years ago my grandad stopped walking. His joints had got so bad that he was in bed most of the day. He got back on his feet, and I want to be clear that it was the physios and the doctors who did that, over months. A heated wrap did not, and I am not going to pretend it did.

What I saw in those months was the hour before the physio arrived. First thing, joints cold, everything stiff, a wheat bag going round the microwave for the third time. Nobody was looking after that hour, and it decided how the rest of the day went.

So I went looking for something for it. Warmth that stayed warm, that he could strap on at the table with a bit of massage, and that switched itself off. Jointwell is what I found and had safety-tested.

It is for the mornings. It is not a cure and it will not replace your physio. If it does for your knee what it did for his hour before breakfast, keep it. If it does not, post it back and we pay the postage. You have ninety days.

[FIRST NAME], grandson

Button: **See how it works** → homepage

P.S. If you have already ordered, your dispatch email is on its way separately. Most orders leave within 1 to 3 working days.

---

## Flow B: Day 3, getting the most out of it

**Trigger.** Placed Order (the wrap). **Timing:** 3 days after the order is marked delivered (Klaviyo: Fulfilled Order plus the carrier's delivered event if you have it; otherwise 9 days after the order). Shopify Email: not available as a delivered trigger; use 9 days after order.

**Subject:** Kettle on, wrap on
**Preview:** Three things people wish they had known on day one.

Hello {first_name},

Your wrap should be with you now. Three things people tell us they wish they had known on day one:

**1. Charge it fully before the first go.** The cable is USB-C, the same as most phones. The panel shows the battery level.

**2. Start at level 3.** The five levels run from 45°C to 65°C. Most people settle at 3 or 4. Go up if you want it warmer; there is no prize for level 5.

**3. Give it the whole half hour.** It switches itself off at thirty minutes. The people who get on with it best make it a fixed part of the morning: kettle on, wrap on, and it clicks off around the second cup. Habit is the whole trick.

For a shoulder or an elbow, the extension strap is in the box. Loop it through the wrap, over the shoulder and under the arm, or up the forearm to the elbow.

If anything is not right with it, reply to this email. It comes to a person.

[FIRST NAME]

Button: **Read the questions people ask** → homepage FAQ

---

## Flow C: Day 10, review request

**Trigger.** 10 days after delivered (or 16 days after order). Skip if a review already exists (Klaviyo: Judge.me integration, "Submitted review" event). **Timing:** 9am local.

**Subject:** Would you tell the next person?
**Preview:** Honest, verified, two minutes. Good or bad.

Hello {first_name},

You have had the wrap about ten days now, which is long enough to have an opinion.

Would you write it down for the next person? The reviews on our site are collected by Judge.me from real orders, which means we cannot write them, edit them or delete the bad ones. That is the point. A woman deciding whether to trust a heat wrap she saw on Facebook needs to hear from someone who actually bought one, not from us.

Good, bad or "not sure yet" are all useful. Two minutes, and a photo if you have one of it on your knee in your own kitchen. We will not use your surname.

Button: **Write your review** → [REVIEW LINK]

Thank you either way.

[FIRST NAME]

Note on incentives: if you ever offer anything for a review (a £5 code, a free sachet pack), it goes to everyone who reviews, good or bad, and the email must say so. Never for positive reviews only. That is a DMCC Act line.

---

## Flow D: Day 20, one for the other knee

**Trigger.** 20 days after delivered, customer bought exactly one wrap. **Timing:** 9am.

**Subject:** One for the other knee, or for someone else's
**Preview:** A second wrap at half price, for the next 10 days.

Hello {first_name},

A lot of people who buy one wrap come back for a second, and it is usually for one of three reasons: the other knee, a husband who keeps borrowing it, or a sister who saw it on the kitchen table.

So here is the offer we make once, to people who already have one: a second wrap for £24.96, half the usual price, with the code SECONDWRAP. Same 90-day trial, same 2-year warranty. The code works until [DATE, 10 days from send] and then it does not, because that is the date, not a trick.

Button: **Add a second wrap** → product page with code applied

If one is enough, that is fine too. Nothing else changes.

[FIRST NAME]

Note: the end date must be printed and must be real. Klaviyo can insert a date 10 days from send; Shopify Email needs the date typed per batch.

---

## Flow E: Day 25, before your trial ends

**Trigger.** 25 days after delivered. Skip if a review exists. **Timing:** 9am.

**Subject:** Before your trial ends, tell us honestly
**Preview:** No sales pitch. Two questions.

Hello {first_name},

You have had the wrap nearly a month. Your trial runs for ninety days, so there is no clock on this, but a month is usually when people know.

Two questions, and you can reply to this email with one word each:

1. Is it earning its place by the kettle, or not?
2. Is there anything about it that annoys you?

If the answer to the first is "not", say so and we will send the returns label straight away; you do not have to wait for the ninety days to run out. If the answer is "yes", would you put it in a review so the next person hears it from you rather than from us?

Button: **Leave a review** → [REVIEW LINK]

Either way, thank you for trying it properly.

[FIRST NAME]

---

## Flow F: Day 45, sachet refills

**Trigger.** 45 days after delivered, has not bought refills. **Timing:** 9am. Repeat every 45 days while that stays true, up to three times.

**Subject:** The sachet in the pocket
**Preview:** Six more, £8.95, and a spare strap if yours has wandered.

Hello {first_name},

There is a mugwort sachet in the front pocket of your wrap. It is a traditional warming herb, and people tell us they miss the smell once it fades, usually around a month in. This is not a medical thing; it just makes the half hour nicer.

Six more sachets are £8.95, and each one lasts about a month of daily use.

Button: **Refill the pocket** → [REFILLS LINK]

While you are there: a strap and liner pack (a spare extension strap and two washable inner liners) is £9.95. The liner is the part that touches your skin, so it is the part that wants a wash now and then.

[STRAP PACK LINK]

Free delivery when the two go together.

[FIRST NAME]

---

## Flow G: Abandoned basket (two emails)

**Trigger.** Started Checkout, no order within 1 hour. Klaviyo flow; Shopify Email: Abandoned checkout automation. Stop the flow if an order is placed.

### G1, 1 hour after

**Subject:** You left a wrap in your basket
**Preview:** No rush. Here is the bit people usually want to check first.

Hello {first_name},

You had a Jointwell wrap in your basket and did not finish. That is fine; it is a strange thing to buy from a website, and most people want to check something first.

The thing they usually want to check is the returns. So, plainly: you have ninety days from delivery to send it back for a full refund, for any reason, and we pay the return postage. There is a UK returns address and a 2-year warranty. Our reviews are collected by Judge.me from real orders, so we cannot write them or delete the bad ones.

Button: **Back to your basket** → checkout link

If you have a question the site did not answer, reply to this email. It comes to a person.

[FIRST NAME]

### G2, 24 hours after (only if still no order)

**Subject:** The question most people ask before they buy
**Preview:** "How do I know this isn't another Facebook gadget?"

Hello {first_name},

The question most people ask before they buy is the one we put in the FAQ: how do I know this isn't another Facebook gadget?

Fair question, because this market is full of them. Here is the honest answer. We dispatch most orders within 1 to 3 working days and track every one. There is a UK returns address, UK support, a 2-year warranty and a 90-day trial where we pay the postage back. Junk sellers cannot afford that guarantee, and they will not hand control of their reviews to a third party the way we have with Judge.me.

If it does not help your knee, you post it back and you are where you started.

Button: **Back to your basket** → checkout link

[FIRST NAME]

No discount in either email. A discount here teaches people to abandon baskets.

---

## Flow H: Monthly Advice digest (template)

**Trigger.** Manual campaign, first Tuesday of the month, 9am, to everyone on the list.

**Subject:** [Month]: [article title, e.g. "The gardener's version of tennis elbow"]
**Preview:** One thing worth reading, one thing from the Group, one thing we changed.

Hello {first_name},

**Worth reading this month**
[Two sentences on the article and why now. Link.]
Button: **Read it** → article

**From the morning half hour**
[One reply from the Facebook Group, with the member's permission, first name only. For example: "Sue put hers on before the school run with the grandchildren and says the car park steps were easier." Link to the Group.]

**Something we changed**
[One honest line about the business: a new liner supplier, a returns label change, a mistake we fixed. People trust a company that says what it got wrong.]

**If you need anything**
Refills are £8.95 for six. A spare strap and liners are £9.95. And the ninety days stand.

[FIRST NAME]

---

## Review reply templates (Judge.me)

Reply to every review within two working days, in the owner's voice, first name only. Never argue. Never ask for a change to a rating.

**Positive (4 or 5 stars)**

> Thank you, {first_name}. "[Quote four to eight words from the review]" is exactly what we hoped it would be for. If the sachet in the pocket fades, reply to any of our emails and we will sort you out. [FIRST NAME]

**Mixed (3 stars, or a good review with a real complaint)**

> Thank you for being straight with us, {first_name}. You are right about [the complaint, in their words]. [One sentence on what we are doing about it, or an honest "we do not have a fix for that yet".] If it has not earned its place by the kettle by the end of your ninety days, the returns label is yours for the asking, and no hard feelings. [FIRST NAME]

**Negative (1 or 2 stars)**

> I am sorry, {first_name}. That is not what we wanted for you. I have emailed you separately with a returns label; you do not have to wait or explain. Your review stays up as it is, because the next person deserves to see it. If there is anything I have got wrong in the description, tell me and I will change it. [FIRST NAME]

Then actually send the label, the same day.

---

## Timing summary

| Flow | Trigger | Delay | Skip if |
|---|---|---|---|
| A Welcome | subscribe or first order | 10 min | already received |
| B Day 3 | delivered | 3 days (9 after order if no delivered event) | |
| C Review | delivered | 10 days | review exists |
| D Second wrap | delivered, 1 wrap bought | 20 days | bought 2 or more |
| E Before trial ends | delivered | 25 days | review exists |
| F Refills | delivered | 45 days, repeat x3 | bought refills |
| G1 Basket | checkout started | 1 hour | ordered |
| G2 Basket | checkout started | 24 hours | ordered |
| H Digest | manual | first Tuesday monthly | |
