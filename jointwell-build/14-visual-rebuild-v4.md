# 14. The visual rebuild (branch `jointwell-v4`), 6 September 2026

The v3 page had the right arguments in the right order and read like a report: fifteen sections of grey cards with paragraphs in them, 26px headings, 16px body, thumbnails inside boxes. Set beside a page like Primal Queen's it looked like information, not a brand. This pass keeps the arguments and changes how they land: one idea per screen, headlines big enough to sell on their own, one photo per idea, a third of the words, and the same button and trust line under every section so the page reads as a system.

`jointwell-v3` is live. This branch does not touch it. Connect `jointwell-v4` to a new unpublished theme, look at it on a phone, and publish it from the theme list when you are happy.

## What changed

- **Identity.** Warm cream page, terracotta as a colour rather than an accent, one dark clay band for the guarantee. Pill buttons with a shadow, 56px tall. Headlines 40px on a phone and 60px on a desktop; body 19 to 20px. All in `assets/jw4.css`, loaded after the old stylesheet, so the v3 sections that stay pick up the new scale too.
- **Sale bar** (`jw4-sale-bar`) under the header: the autumn price with its real end date, free delivery, the trial. No countdown. The owner changes the product price on that date, or the line stops being true.
- **Hero** (`jw4-hero`): one photo with a real customer's line pinned to it, the headline "Stop planning your day around one knee.", three ticks, the price, one button, the dispatch clock. The tier picker moved to the offer block, so the page asks "how many" once.
- **Enemy and belief** (`jw4-enemy`): four cupboard items as big statements, then the belief in one line: the ten minutes was the problem, not the heat.
- **Mechanism** (`jw4-mechanism`): three alternating photo rows, one sentence each, then the one claim we make.
- **Reviews wall** (`jw4-reviews`): the five real buyers, photo first, big quote, "Verified buyer" tag. Cards hide until a quote is present. Add each Judge.me link so the tag can be checked.
- **Founder story** (`jw4-founder`): the grandson's story in five short paragraphs beside one large photo. The wrap still gets no credit for him walking again and the illness is still not named.
- **Routine ladder** (`jw4-routine`): Day 1, Day 3, Week 2, Week 4, Day 90 as five columns.
- **Guarantee band** (`jw4-guarantee`): the four terms as big numbers on the dark band.
- Kept from v3 with the new styling: heat chart, authority quotes (the dense evidence card is hidden on the homepage), doorway tabs, offer block, FAQ, final call. Dropped from the homepage: proof strip (folded into the hero trust line), comparison table (the enemy section does its job), lead magnet, the old "why" section.

## Urgency, kept honest and visible

Sale bar with a real end date, dispatch cut-off clock, sticky bar. No countdown to nothing, no stock warnings, no invented purchase counts. That is the DMCC line for a UK seller and this audience checks.

## Rules that must hold for any new section

Header content 50 characters or fewer. Section and block names 25 or fewer. Never `"default": ""` on a text or textarea setting. Shopify's GitHub sync drops a file that breaks these without telling you, and then drops every template that uses it, which is how v3 went 404.
