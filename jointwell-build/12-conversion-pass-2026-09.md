# 12. Conversion pass, 5 September 2026

Worked from the seven-point critique against Frownies, NeuroMD, Mendi and Primal Queen. Everything below stays inside the CAP lines in 09.

## What changed in the theme

| Critique point | Where | What |
|---|---|---|
| 1. Under-proofed hero, no video | `jw-hero` | Proof line ("Rated 4.8 by 312 verified customers") renders only when `proof_count` is set. Video slot in the photo column with a play poster (defaults to the live CDN demo poster); paste the MP4 or YouTube link in `video_url`. "Sold in Australia for two years" line under the headline. |
| 2. Borrow authority | `jw-authority`, now second on the page | Headshots (from the live CDN), full names and credentials. New "What the evidence says" card with three sourced lines. NHS logo deliberately not used: the NHS identity is not licensed for third-party commercial use, so it is text only. |
| 2. "Independently tested" | `jw-proof` (trust row) | Now says CE, EMC Directive 2014/30/EU, independent lab, 21 Nov 2024, links the certificate, and says what the test does not cover. |
| 3. Reason to buy today | `jw-hero`, `jw-box` | Honest dispatch clock ("Order in the next 2 hr 14 min and it leaves us today"), UK time, weekdays, cut-off in settings. Box items can carry evidenced values and a total line that only shows when every item has one. No fake sale, no countdown to nothing. |
| 4. Traffic leaks | `jw-header`, `jw-doorways` | Landing mode: on the homepage the nav is four anchors (How it works, Reviews, Guarantee, FAQ). Track my order and Contact stay in the footer. Doorway tiles open a panel in place (photo, four lines, how it goes on, buy button); the long article is an optional secondary link. |
| 5. Built for the reader | `jw-box`, `templates/index.json` | "The specifics" merged into "What's in the box" behind a large-type toggle; standalone specs section removed. Comparison cut from six columns to five (creams dropped; the £25 Amazon pad stays because it is objection 14). `jw-why` renders nothing while the story field is empty rather than a blank band. |
| 5. Sticky bar | `snippets/jw-sticky-bar.liquid` | Shows on every screen size once the buy box scrolls off, hides when it is back on screen. Price follows the tier picked in the hero. |
| 6. Wider proof | `jw-reviews` | Total line and average (hidden until a real count exists), an outcome stat with its methodology (hidden until all three fields are filled), a "uses it on" tag per review. The five Yorkshire placeholder reviews and their generated headshots are gone; the four verified Australian buyers from the research file are in, with the Australia explanation moved above them as the brief recommends. |
| 7. Small wins | `jw-hero`, `jw-magnet`, `jw-word-guarantee` | Quiz is a full-width secondary button with a line under it. New mid-page lead-magnet section after the reviews. Guarantee box lists four plain terms, the first being "You pay to send it back: nothing." |

New assets: `jw-photo-bed/van/breakfast/kettle/crossword-elbow/garden-window.jpg` (lifestyle, two men) and the five feature tiles `jw-feature-heat/massage/timer/joints/weight.jpg`.

## Owner to-do before this goes live

1. **Proof count.** Fill `proof_count` and `proof_rating` in the hero, and `count`/`rating` in reviews, from Judge.me. Until then those lines stay hidden on purpose.
2. **Video.** Film the 30-second clip (strap on, panel lights, timer clicks off, stand up) and paste the link into the hero. The poster currently points at the old theme's CDN file: re-upload `th-video-demo-poster.jpg` and the four expert headshots to Content > Files and swap the URLs before the old theme is deleted.
3. **Sources.** The authority quotes and evidence lines have blank `source_url` fields. Put the live URL on every one before publishing, or delete the line. A quote with no link is a claim you have to defend.
4. **Reviews.** Geoff's line mentions pain being "more manageable". The research file recommends it; a solicitor may not. Decide.
5. **Box values.** Only fill `value` on box items with a price you can evidence. Otherwise leave them blank and the total line stays hidden.
6. **The live site.** velagoods.co.uk currently says "Clinically proven to ease pain, stiffness and improve blood flow", lists conditions under "Made for", and shows strike-through prices and reviews that name osteoarthritis. All four are the exposures in the offer brief, Section 17.1. This branch fixes none of that on the live theme; publishing this theme replaces it.
7. **Doorway articles.** Homepage tiles now use situation language. If you publish the seven Advice articles from 03, rename their H1s to match, or the tile and the article will disagree.
