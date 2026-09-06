# Skintel — Zero-to-Customers Acquisition System

**Written:** 6 September 2026
**Constraints this plan is built for:** never launched, ~0 audience, **$0 budget**, **faceless content only** (no face, no voice), domain stays `www.skinstel.com`.

Everything below is designed to work inside those four constraints. Where a constraint is actively costing you money, I say so and price the fix — but no line item in the 30-day plan requires spending anything.

---

## 1. Current marketing diagnosis

**The product is built. The distribution is at zero. That gap is the entire problem.**

What's actually true right now:

| Reality | Evidence |
|---|---|
| Product is live in production | Stripe live keys, Supabase auth, full app (Scanner, Journal, Compare, Culprits, Recommend, Routine) |
| Pricing exists and works | Pro $9/mo, $79/yr; founding tier lists $49.99 → $20 via code |
| Guest checkout, no signup wall | `api/stripe-checkout.ts` — this is a real conversion asset, most competitors don't have it |
| A video render pipeline exists | `marketing/video/` — hero, shelf, routine, versus, progress, ads cuts already built |
| The August launch never ran | Confirmed. So there is no proven channel, no CPA data, no list |
| Nobody can find you | See below — this is the acute problem |

**The four things actively bleeding:**

1. **Branded search is dead and you've chosen to live with it.** You say "Skintel," people type `skintel.com` and land on a competitor. `skintel.app` and `skintel.io` are both live skincare products with near-identical pitches. **Consequence you must design around: your brand name can never be the call-to-action.** Every single piece of content must show `skinstel.com` as readable text on screen, and the name must never be spoken as the only pointer. This is a permanent tax on every view you earn. (The $11/yr fix — `tryskintel.com` — remains available if you change your mind; it is the single highest-ROI dollar available to this project.)

2. **The site is a client-rendered SPA.** Google sees an empty div. Your `index.html` meta tags mean link previews work fine, but **organic search ranking is effectively unavailable** until content is server-rendered or pre-rendered. Don't budget any hope on SEO in the next 90 days. Do fix it in the background (see §21).

3. **Your positioning in the repo is excellent and nowhere in your marketing.** `index.html` says: *"Your skin isn't broken — your routine is fighting itself."* That is a genuinely strong, specific, emotionally-true hook. Meanwhile the category you're drifting toward — "AI skin analysis from a selfie" — is crowded, commoditized, and where your two name-twins already sit. **Do not compete on skin scoring. Compete on ingredient correlation.**

4. **There is no free entry point.** `TryItDemo.tsx` exists but the product's real magic — *"here is the one ingredient in all six of your products"* — is behind the app. For a $0 strategy, the free tool IS the acquisition channel. See §13.

**Honest expectation setting:** faceless + $0 + no audience + no branded search means the first 30 days are about *finding one repeatable format*, not about revenue. A realistic 30-day outcome is **300–800 landing sessions and 40–120 email signups**. Anyone promising you more than that on this budget is selling something.

---

## 2. Positioning

**Say this:**

> **Skintel finds the ingredient that's breaking you out — by cross-referencing every product you own against your own breakout history.**

**One-liner for bios and video end-cards:**
> Your skin isn't broken. Your routine is fighting itself. → skinstel.com

**The wedge, stated plainly.** Yuka, Onskin, Cosmily and Sezia all answer *"is this ingredient bad?"* — a generic, context-free, often fear-based verdict. Users have started publicly criticizing exactly that. Skintel answers a different and much better question: ***"which ingredient is bad for me?"*** — derived from correlation across the products you actually own and the breakouts you actually logged.

That distinction is:
- **True** (it's what the product does)
- **Defensible** (requires your journal + correlation model; a static ingredient database can't replicate it)
- **Demonstrable in 8 seconds on screen** (which is the whole ballgame for faceless content)

**Never say:** "AI-powered skincare platform," "revolutionary," "your personal skin intelligence." The last one is literally `skintel.app`'s headline. Stay off their turf.

---

## 3. Target customer

**Primary — "the frustrated stacker."** 18–34, uses 5–12 products, has been breaking out for 3+ months, has already tried eliminating things at random and failed. She does not want a skin score. She wants a *culprit*. She is actively searching TikTok for "skincare ingredient checker" **right now**. This is your entire early market.

**Secondary — "the reactive-skin sufferer."** Rosacea, eczema, perioral dermatitis, fungal acne (malassezia). This group is *intensely* motivated, already ingredient-literate, and clusters in dense, searchable communities (r/SkincareAddiction, r/Fungalacne, r/tretinoin). They convert far better than the general market and they evangelize. **Highest value per user by a wide margin.**

**Tertiary — "the shelf auditor."** Buys a lot, wants to know what to throw away. Lower intent, high volume, good for reach content.

**Explicitly not your customer yet:** men's grooming, anti-aging 45+, and "clean beauty" ideologues (that last group will fight you about ingredient safety in comments and burn your time).

---

## 4. Best acquisition channels, ranked by ROI for *this* product

| # | Channel | Why it ranks here | Effort |
|---|---|---|---|
| **1** | **TikTok search interception** | Proven existing demand — dedicated discovery pages exist for "skincare ingredient checker," "app to check skincare ingredients." Faceless-native. Free. | High, daily |
| **2** | **The free public tool (§13)** | Converts strangers without a follow. Works while you sleep. The only true compounding asset on a $0 budget. | One-time build |
| **3** | **Reddit (niche subs)** | Your secondary audience lives here at high density and high intent. Text-based = perfectly faceless. | Medium, daily |
| **4** | **YouTube Shorts** | Same asset as TikTok, second-best faceless discovery, and Shorts search is under-exploited in this niche | Free repost |
| **5** | **Instagram Reels** | Third repost target. Skincare audience is native here. Carousels also work well faceless. | Free repost |
| **6** | **X** | Low direct conversion for consumer skincare, but the best place to build-in-public for future investor/press/creator inbound | Low, cheap |
| **7** | **Discord / Facebook groups** | Dense, high-intent, but slow and manual. Good for beta recruitment specifically. | Medium |
| **8** | **Product Hunt** | Save it. One shot, best used at a real relaunch moment with an existing base to mobilize. Firing it now with zero audience wastes it. | Later |
| **9** | **SEO** | Blocked by the SPA issue. Real long-term value, zero 90-day value. | Background |

**Ignore entirely, for now:** paid ads (nothing to retarget, no proven CVR — you'd be buying learning at $12–54 CPA against a $20 product), LinkedIn, Pinterest, podcasts, press/PR (you have no news), and paid influencers (no budget, and unpaid outreach works better at your stage anyway — see §11).

---

## 5. Zero → 100 signups

This phase is won by **interception, not creation.** You are not trying to be discovered. You are trying to show up where someone is already typing your problem into a search bar.

**Days 1–3 — build the trap before driving traffic.**
- ~~Ship the free public tool (§13, option A)~~ — **done**, live at `/shelf-audit`. No signup to use it; email gated *after* the result is delivered.
- Fix the CTA (§7). Put `skinstel.com` in readable text on every video template in `marketing/video/`.
- Create accounts: TikTok, YouTube, Instagram. Handle: use something searchable, not just the brand — e.g. `skintel.app.official` is taken by a competitor, so go descriptive: **`ingredientculprit`** or **`skinteldotcom`**. Bio line: *"Find the ingredient breaking you out → skinstel.com"*.

**Days 4–14 — search-intercept content, 2 posts/day.**
Title and caption every video with the exact phrases people already search:
- "skincare ingredient checker"
- "how to find what's breaking me out"
- "check my skincare ingredients"
- "is this ingredient comedogenic"
- "fungal acne safe checker"

Format: screen recording of the scan → the reveal. No face needed. 12–22 seconds. The product does the talking.

**Days 7+ — the mechanic that makes this work: "Send me your shelf."**
Post: *"Comment 3 products you use. I'll run them through and tell you what they have in common."* Then screen-record each result as its own video.

This single loop is the core of the whole strategy because it:
- is 100% faceless and costs $0
- turns your product into infinite content
- generates comment volume (the strongest early algorithm signal)
- produces personalized videos that get **saved and shared**, not just watched
- gives you dozens of real user routines — which is free product research

**Reddit, in parallel (days 5+).** Answer 3 questions/day in r/SkincareAddiction, r/AsianBeauty, r/Fungalacne, r/tretinoin, r/30PlusSkinCare — with genuinely useful ingredient analysis and **no link**. After ~2 weeks of real contribution, your post history does the selling. See §12.

**Target: 100 signups by day 21.** Source will be roughly 60% TikTok/Shorts, 25% Reddit, 15% free tool direct.

---

## 6. Zero → 1,000 signups

Getting to 1,000 is about **finding the one format that worked and industrialising it.**

1. **Identify the winner.** By day 30 you'll have ~50 posts. One or two will have meaningfully outperformed. Do not celebrate it — dissect it (§21 feedback loop).
2. **Make 5 variations of the winner, not 5 new ideas.** Same structure, different product/ingredient/problem. This is the single highest-leverage move available to a $0 account.
3. **Turn the "send me your shelf" loop into a series** with a fixed visual template so it becomes recognizable. Number them ("Shelf #47") — numbering drives return viewing.
4. **Add the second format: the callout.** "This ingredient is in 8 of the 10 best-selling moisturizers" — screen-recorded, data-driven, faceless, and inherently shareable because it's useful independent of your app.
5. **Recruit unpaid creators** with free lifetime Pro (§11) — at 1,000 signups you finally have enough proof to make the ask credible.
6. **Turn on the referral loop** (§14) once you're past ~300 signups; earlier than that, a referral program has nobody to refer to.

**Realistic timeline to 1,000 on $0 + faceless: 90–120 days**, and it depends almost entirely on whether one format breaks out. Plan for the median, stay ready for the tail.

---

## 7. Landing page improvements

Your page must answer five questions before a stranger scrolls past. Right now it's optimized for people who already know what Skintel is — nobody does.

**Fix these, in priority order:**

1. **Kill the brand-first hero.** Lead with the *problem*, not the name. Replace the top of `Landing.tsx` with the line you already wrote and buried: **"Your skin isn't broken — your routine is fighting itself."** Subhead: *"Scan every product you own. Skintel finds the one ingredient hiding in all of them."*

2. **The CTA should not be "Join Waitlist."** You have a live product — a waitlist would be a lie. The strongest option here, given the product actually delivers an answer:
   > ### **"Find my culprit ingredient →"**
   It's specific, it's a benefit, it implies a result, and it matches exactly what the visitor came to do. Runner-up: *"Scan my shelf — free."* Avoid "Get Early Access" (implies not-live) and "Try It Free" (generic, tells them nothing).

3. **Put the demo above the fold.** `TryItDemo.tsx` should be the hero, not a section. A visitor should be able to paste one ingredient list and get a real answer *without scrolling and without an account*. Every step between landing and value costs you roughly half your traffic.

4. **Show the output, not the interface.** Screenshots of a dashboard mean nothing. Show a *result*: "Found in 6 of your 8 products: **Cetearyl Alcohol**." That single image is your best marketing asset and it currently isn't on the page.

5. **Add the honest differentiator block.** One short section: *"Other apps rate ingredients. Skintel correlates them against your breakouts."* Directly addresses the documented complaint about Yuka-style generic ratings.

6. **Domain reinforcement.** Since branded search is lost, the page title and OG image must carry `skinstel.com` visibly — anyone screenshotting your content should be re-transmitting the correct URL.

7. **Cut the seat counter unless it's true.** `useFoundingCount.ts` is honest now (good — the phantom +138 was removed). Keep it honest. A counter that reads 12/500 is better than a fake one that gets caught; but if the number is embarrassingly low, hide the counter and use the price step for urgency instead.

---

## 8. Pre-launch offer

You don't need a waitlist — you need a reason to act *today*. Since the product is live, the offer should trade **access + price** for **feedback**.

**The offer: "Founding 100."**
> First 100 people get Pro for **$20 once — 3 months, no auto-renew** — plus direct line to the founder and their requested feature considered first.

Why this works: it's real (you built it), it's cheap enough to be impulsive, no-auto-renew removes the subscription objection that kills consumer conversion, and "no auto-renew" is a genuine trust differentiator worth saying out loud.

**Free tier stays free and generous.** On a $0 acquisition budget, your free tier *is* your marketing. Let people scan 3 products free, forever, no account. The paywall belongs at the *correlation* step — the part only you can do.

**No fake scarcity.** If 100 seats sell, say so and open the next batch. Don't run a countdown timer that resets.

---

## 9. Waitlist strategy

Since there's a live product, reframe: **you're collecting emails, not waitlist positions.**

Capture at three points:
1. **After the free tool delivers value** — "Want your full trigger map? Enter your email." (highest converting moment; they've just seen it work)
2. **Exit intent on the landing page** — "Send me the 12 ingredients most likely to be breaking you out" (a lead magnet, not a signup)
3. **In-app**, when a free user hits the 3-product limit

Fields: email only. Every additional field costs you conversions. Capture source via UTM automatically. Ask about skin type *in the first email*, not on the form.

---

## 10. Content strategy

**Governing rule:** the viewer must get something useful even if they never download anything. Content that only makes sense if you already care about Skintel will die at 200 views.

| Platform | Frequency | Format | Purpose |
|---|---|---|---|
| **TikTok** | 2/day | 12–22s screen recording, text on screen, trending audio low | Discovery + search interception |
| **YouTube Shorts** | 2/day (same asset) | Same, re-uploaded natively | Second discovery engine, better search longevity |
| **Instagram Reels** | 1–2/day (same asset) | Same | Third surface, skincare-native audience |
| **Instagram carousels** | 3/week | 6–8 slide ingredient explainers | Saves + shares, strong faceless format |
| **Reddit** | 3 helpful comments/day, 1 post/week | Text, no links initially | High-intent, high-conversion |
| **X** | 1/day | Build-in-public + ingredient findings | Long-game inbound |
| **Email** | 1/week | Value first, product second | Owned audience |

**On the no-voice constraint:** research is consistent that voiceover meaningfully lifts average view duration versus silent text-on-screen, and Cal.ai's screen-recording-plus-VO format drove $1.5M MRR in 34 days. You've said text/music only, so that's the default here — but **test it**: free-tier TTS on 5 videos in week 3 against 5 silent ones. If watch time lifts, that's a free upgrade and you never have to show your face or use your own voice. I'd put real money on it winning.

---

## 11. Creator strategy ($0 version)

With no budget, you cannot buy distribution — but you can trade **access and analysis**, which nano-creators genuinely want.

**Selection criteria (in order):** audience match over size, every time. A 4,000-follower fungal-acne creator will outperform a 400,000-follower general beauty creator for this product, by a lot.

- 1,000–15,000 followers (nano) — will reply to DMs, often have no brand deals yet
- Posts about *problems*, not hauls (acne journeys, "what broke me out," routine eliminations)
- Comments section full of "what products do you use?" — that's a distribution engine you can plug into

**The ask (free, and genuinely valuable to them):**
> Hi [name] — I built a tool that cross-references every product in a routine and finds the ingredient they have in common. I ran your routine from your [specific video] through it and found something I think you'd want to see — [one real, specific finding]. Happy to send the full breakdown, free, no strings. If it's useful, share it. If not, no worries at all.

**Why this converts:** you led with a free, personalized, genuinely interesting result about *them*. You didn't ask for anything. Do 5/day, expect 1–2 replies. That's 30–60 warm creator conversations in a month for $0.

**Compensation ladder, for when you do have budget:** free lifetime Pro → affiliate (30% recurring) → $50–150 flat per UGC asset → paid posts. **Pay for UGC rather than influence** when you need ad creative you can reuse; pay for influence when you need reach. At $0, do neither — do the free analysis play above.

---

## 12. Community strategy

**The rule: contribute for two weeks before you ever mention the product.** A new account dropping a link in r/SkincareAddiction gets banned and you lose the channel permanently. That risk is not worth any short-term gain.

**Targets:** r/SkincareAddiction, r/AsianBeauty, r/Fungalacne, r/tretinoin, r/30PlusSkinCare, r/Rosacea, r/eczema, plus 3–5 skincare Discords.

**The playbook:**
1. **Listen (days 1–5).** Log every recurring question. "What's breaking me out?" appears constantly — that's your product's exact job.
2. **Answer (days 5–20).** 3 substantive comments/day doing manual ingredient analysis. Actually help. No link, no mention.
3. **Introduce (day 20+).** Only where genuinely relevant, and always as disclosure: *"I built a tool that does this — happy to just run it for you and paste the result if that's easier."* Offering to do it *for* them converts far better than a link, and it's within the rules of most subs.

**Value-first post that creates curiosity without spam:**
> **"I analyzed the ingredient lists of the 40 most-recommended moisturizers on this sub. 27 of them share one ingredient."**
> [Full findings in the post — genuinely complete, no gate.] Comments will ask how you did it. *That's* where the tool comes up, naturally, when asked.

---

## 13. Free-value growth loop

**This is your single most important build.** On $0, a free tool is worth more than any content strategy, because it converts strangers without requiring them to follow you.

**Option A — "The Shelf Audit" — is shipped.** Live at `skinstel.com/shelf-audit` ([`pixelbuyte/Skintel#18`](https://github.com/pixelbuyte/Skintel/pull/18)). Paste 2–6 real ingredient lists → instantly see **the ingredients they share**, computed live, no account required. Email is asked only after the result, pitched as unlocking correlation against your own breakouts. The hero's "Find my culprit — free" CTA now points there instead of the scripted demo, so the free-tier promise is literal.

**Not yet built, real gap:** the auto-generated shareable result card (branded, `skinstel.com` readable on it) — every share would re-transmit the domain, which partially solves the branded-search problem for free. Right now a user can screenshot the page, but there's no purpose-built share asset. Worth building once the tool has any traffic to learn from.

**Four more, in priority order:**
- **B. Fungal-acne (malassezia) safe checker** — narrow, intensely searched, tiny competitive set, and the community *will* spread it themselves
- **C. "Is my routine fighting itself?"** — conflict detector (retinol + AHA, niacinamide + low-pH vitamin C). Highly shareable, very screenshot-friendly
- **D. Comedogenic score for a full routine** — intercepts one of the highest-volume existing searches
- **E. Dupe finder** — "same actives, cheaper" — enormous organic share potential, though further from your core

**The loop:** stranger searches problem → finds your tool via TikTok/search → gets a real answer free → sees the shared-ingredient result → screenshots or shares it → domain travels → wants correlation against their own breakouts → enters email → gets sequence → becomes Founding 100.

---

## 14. Referral strategy

Turn this on **after ~300 signups**, not before.

Since the product is live, reward with **product**, not queue position:

| Referrals | Reward |
|---|---|
| 1 | +5 free product scans |
| 3 | 1 month Pro free |
| 5 | 3 months Pro free |
| 10 | Lifetime Pro |

Lifetime at 10 is defensible: someone who brings 10 real users is worth more as an evangelist than as $79/yr. **Deliver every reward instantly and automatically** — a referral program that pays late destroys more trust than it earns.

---

## 15. Email sequence

Weekly. Value first. The product shows up as the answer to a problem you've already made them feel.

| # | Timing | Subject | Job |
|---|---|---|---|
| 1 | Instant | "Here's what your products have in common" | Deliver their actual result immediately. No pitch. |
| 2 | Day 2 | "The 12 ingredients most likely to be breaking you out" | Pure value. Genuinely useful even if they never return. |
| 3 | Day 5 | "Why 'non-comedogenic' means nothing" | Educational + positions against generic-rating competitors. |
| 4 | Day 9 | "What did your scan actually say?" | Ask a question. Replies are gold — this is your beta recruitment pool. |
| 5 | Day 14 | "Founding 100 — $20, three months, no auto-renew" | The offer, once, clearly. |
| 6 | Day 21+ | Weekly: one ingredient finding + one product update | Sustain. Keeps the list warm without begging. |

Never send a "just checking in" email. Every send must carry one genuinely useful thing.

---

## 16. Beta recruitment plan

You need **20–30 people you actually talk to**, not thousands of silent signups.

**Where:** email-3 repliers, Reddit commenters you've helped, "send me your shelf" commenters, Discord regulars. All free.

**The ask:** *"Can I give you 3 months of Pro free if you'll do a 15-minute call and tell me where it's confusing?"* Nearly everyone says yes.

**What to actually learn** (write these down verbatim, they become your marketing copy):
- What did you *think* it would do before you used it?
- Where did you get stuck or confused?
- What made you almost close the tab?
- What would you have paid for?
- How would you describe this to a friend? ← **this one is your headline; steal their exact words**

The last question routinely produces better copy than anything a marketer writes.

---

## 17. 30-day execution calendar

### Week 1 — Build the trap
| Day | Do | Metric |
|---|---|---|
| 1 | ~~Ship free Shelf Audit tool (no-signup). Rewrite hero + CTA to "Find my culprit ingredient"~~ — done | Tool live |
| 2 | Add `skinstel.com` as readable text to all `marketing/video/` templates. Build shareable result card | Templates updated |
| 3 | Create TikTok/YT/IG accounts w/ searchable handles + domain in bio. Set up UTMs + analytics | Accounts live |
| 4 | Produce 10 videos in one batch (screen recordings of real scans) | 10 in bank |
| 5 | Post 2. Join 7 subreddits + 3 Discords. Read only | 2 posted |
| 6 | Post 2. Log 20 recurring community questions | Question log |
| 7 | Post 2. Write email 1 + 2. Review: any video above 1,000 views? | Baseline set |

### Week 2 — Content testing + community
| Day | Do | Metric |
|---|---|---|
| 8–14 | 2 posts/day, testing 5 distinct hook types. 3 Reddit comments/day (no links). Launch "Send me your shelf." DM 5 nano-creators/day with free personalized analysis | **Watch time + comment volume** |
| 14 | **Checkpoint:** which hook type won? Which platform delivered clicks, not just views? | Winner identified |

### Week 3 — Double down + recruit
| Day | Do | Metric |
|---|---|---|
| 15–21 | 5 variations of the winning format. First value-first Reddit post. Run TTS-vs-silent test (5 v 5). Recruit first 10 beta users | Signups/day trending up |
| 21 | Target: **100 signups** | 100 emails |

### Week 4 — Scale winners + convert
| Day | Do | Metric |
|---|---|---|
| 22–28 | Triple down on the winning format only. Ship free tool #2 (fungal-acne checker). Open Founding 100. Run 10 beta calls | **First paying customers** |
| 29–30 | Retro: cost per signup by channel, which content converted vs. which just got views. Plan month 2 | Repeatable channel identified |

---

## 18. 90-day strategy

**Days 1–30 — Validation.** Find one format that reliably produces landing sessions. Success = 100+ emails and a known winning hook. Revenue is not the goal.

**Days 31–60 — Repeatability.** Industrialize the winner. Ship free tools 2 and 3. Turn on referrals at 300 signups. Convert beta feedback into landing page copy. First unpaid creator collabs go live. Target: **500 signups, 25–50 paying**.

**Days 61–90 — Compounding + relaunch.** By now you have social proof (real testimonials), a proven format, and a small list. This is when Product Hunt is worth firing — with an audience to mobilize behind it. Fix the SPA/SEO issue so the free tools can start ranking. Target: **1,000–1,500 signups, 100+ paying, one repeatable acquisition channel you'd spend money on.**

The 90-day exit condition that matters: **you know what a signup costs you in effort, and you know which single action produces more of them.** That's what makes budget worth raising.

---

## 19. Budget allocation

**$0 (your current reality)** — 100% sweat. Content batching, Reddit, free tools, unpaid creator outreach. Everything in the 30-day plan runs at zero. *The one exception worth breaking $0 for: $11.25 for `tryskintel.com`. It is the highest-ROI money available to this project and it's less than a sandwich.*

**$100** — $11 domain · $89 into 1–2 nano-creator UGC assets you can reuse forever.

**$250** — $11 domain · $150 UGC (3 assets) · $89 testing your best organic video as a paid post to a cold audience *purely to learn CTR*.

**$500** — $11 domain · $250 UGC/creators · $150 paid amplification of a **proven** organic winner · $89 landing page A/B tooling. Never boost an untested video.

**$1,000** — $400 creators/UGC · $400 paid on proven winners · $200 tooling + landing tests.

**$5,000** — $2,000 creator programme (5–8 micro-creators) · $1,500 paid social on validated creative · $750 production · $500 retargeting · $250 tooling. **Only spend at this level once cost-per-signup is known.** Scaling an unknown CPA is how you lose $5,000 and learn nothing.

---

## 20. Metrics dashboard

**Vanity metrics to explicitly ignore:** follower count, total views, likes.

**Landing:** unique visitors · CTA click rate · **signup conversion %** · source (UTM) · % who complete a free scan

**Content (per post):** 3-second retention · avg watch time · completion % · **shares + saves** (the real signal — likes are noise) · profile clicks · **link clicks**

**The one metric that matters most in month 1: link clicks per 1,000 views.** A video with 200k views and 30 clicks told you the hook worked and the offer didn't. A video with 8k views and 200 clicks is the one to make five variations of.

**Waitlist/email:** signups by source · referral rate · open/click rate · free-tool → email conversion %

**Creators:** cost (time or $) · views · clicks · signups · **cost per signup** · eventual paid conversion

**Paid (when applicable):** CPM · CTR · CPC · landing CVR · **cost per activated user** (not per signup — activation is someone who completed a scan)

---

## 21. Experiments to run this week

Change one variable at a time or you'll learn nothing.

1. **Hook type (biggest lever).** 5 videos × 5 hook styles: problem-first / result-first / callout / question / POV. Measure 3-second retention only.
2. **Silent vs. TTS voiceover.** 5 v 5, identical content. Measure average watch time. *(Research strongly suggests VO wins; this is a free upgrade that keeps you faceless.)*
3. **CTA wording.** "Find my culprit ingredient" vs. "Scan my shelf — free." Measure landing CVR.
4. **Demo above vs. below fold.** Measure % completing a free scan.
5. **Video length.** 12s vs. 22s, same content. Measure completion rate.
6. **Reddit:** offering to run the scan *for* someone vs. linking the tool. Measure replies.

**Background, non-experiment:** start fixing the SPA pre-rendering. It unlocks SEO for the free tools, which is the only channel that compounds without ongoing effort.

**The scale loop, for when something hits.** If a video does 120k views, do not celebrate — interrogate:
> Why did the hook work? → Who watched (demo/geo)? → Did they click? → Did they sign up? → Make 5 variations → Does the landing page match the video's exact promise? → Can it become an ad? → Can a creator remake it?

**CREATE → DISTRIBUTE → MEASURE → LEARN → ITERATE → SCALE.** A 120k-view video that sent 11 people to a landing page that promised something different is a *failure with good-looking numbers*. Treat it as one.

---

## 22. Content deliverables

### 30 short-form video ideas (all faceless, all screen-recorded)
1. Scan 5 best-selling moisturizers → reveal the shared ingredient
2. "I scanned my entire shelf. 6 of 8 products had the same thing."
3. Run a famous 10-step routine through the conflict checker
4. "This $12 product and this $120 product have identical actives"
5. Fungal-acne check on 5 "gentle" cleansers
6. Comment-request shelf audit (**the core repeatable series**)
7. "Non-comedogenic" label vs. actual comedogenic ingredients in the same product
8. Retinol + AHA conflict, visualized on screen
9. Scan the top 5 products from a viral TikTok routine
10. Before/after: routine with the culprit vs. routine without
11. "Three products, one ingredient, three months of breakouts"
12. Drugstore vs. luxury: same ingredient list, 10× the price
13. Ingredient that appears in 27 of 40 sub-recommended moisturizers
14. "Your sunscreen might be the problem" — scan 5 popular SPFs
15. Scan a "clean beauty" product → show what's actually in it
16. Fragrance/parfum hidden across a full routine
17. "I ran 100 products through this. Here's the most common irritant."
18. Alcohol denat. across toners
19. Essence vs. serum: ingredient lists side by side
20. Scan viewer-submitted routine #1 (numbered series)
21. What changes when you remove one product — correlation view
22. "This ingredient is in every product that broke me out"
23. Scan the 5 most-recommended acne products
24. Silicone-free claim vs. actual ingredient list
25. Two products people always layer that shouldn't be layered
26. The cheapest routine that passes every check
27. Scan products sorted by price — does more expensive mean better formulated?
28. "Rate my shelf" — full audit, scored on screen
29. One ingredient, 12 different INCI names (why you keep missing it)
30. Build-in-public: "I built this because 6 products broke me out and I couldn't tell which"

### 20 opening hooks
1. "Six of your eight products have the same ingredient."
2. "You're not allergic to the product. You're allergic to one ingredient in it."
3. "'Non-comedogenic' is not a regulated term."
4. "I scanned 40 moisturizers. 27 shared this."
5. "Your skin isn't broken. Your routine is fighting itself."
6. "This ingredient has 12 different names."
7. "Stop guessing which product broke you out."
8. "These two products cancel each other out."
9. "Paste your ingredients. Watch this."
10. "The $12 one and the $120 one are the same formula."
11. "Comment 3 products. I'll find what they share."
12. "Your sunscreen might be the problem."
13. "You eliminated the wrong product."
14. "Everyone recommends this. Here's what's in it."
15. "This is why your skin got worse after you 'simplified.'"
16. "One ingredient. Three products. Three months."
17. "'Clean beauty' — let's actually read the label."
18. "Watch what happens when I scan this."
19. "I checked the top 5 acne products. One of them is comedogenic."
20. "It's not the retinol. It's what you're layering it with."

### 10 carousel ideas
1. 12 ingredients most likely to be breaking you out
2. Ingredient conflicts you're probably making right now
3. 12 INCI names for the same ingredient
4. What "non-comedogenic," "hypoallergenic," and "dermatologist-tested" legally mean (nothing)
5. How to read an INCI list in 30 seconds
6. Fungal-acne trigger list, ranked
7. Correct layering order + why
8. 5 signs it's an ingredient issue, not a barrier issue
9. Same actives, ⅓ the price — 6 dupe pairs
10. What to eliminate first when you're breaking out (a decision tree)

### 10 Reddit post ideas
1. "I analyzed the 40 most-recommended moisturizers on this sub. 27 share one ingredient." (full data, no gate)
2. "Mapped every INCI alias for the top 20 irritants — here's the list"
3. "Comedogenic ratings are mostly based on 1970s rabbit-ear studies. Here's what the research actually says."
4. "I cross-referenced 100 'fungal acne safe' products. 14 aren't."
5. "Post your routine, I'll do a free manual ingredient conflict check" (comment thread — enormous goodwill)
6. "The layering conflicts that come up most often here, with the chemistry"
7. "Price vs. formulation: I compared 30 drugstore/luxury pairs"
8. "Why elimination diets for skincare usually fail (you're removing products, not ingredients)"
9. "What I learned reading 500 ingredient lists"
10. "I built a free tool that finds shared ingredients across your routine — no signup, feedback welcome" (**only after 3+ weeks of genuine contribution, and only where sub rules allow**)

### 10 X posts/threads
1. Thread: "I read 500 skincare ingredient lists. 9 things I learned."
2. "'Non-comedogenic' is not regulated. Here's what it actually means." 🧵
3. Build-in-public: what I'm shipping this week
4. Screenshot of a real correlation result + the story
5. Thread: 12 INCI aliases for one ingredient
6. "Most skincare apps rate ingredients. That's the wrong question."
7. Weekly metrics transparency post (build-in-public compounds here)
8. "The hardest technical problem in this app was matching INCI names across brands" 🧵
9. Poll: "Do you know which product broke you out last time?"
10. "We found the same ingredient in 27 of 40 top moisturizers" + data

### 10 creator concepts (all $0 / free-access offers)
1. Free personalized shelf audit sent as a ready-to-post video
2. "Analyze my routine" — you produce, they post, they keep it
3. Creator's audience submits routines, you analyze, creator posts results
4. Free lifetime Pro for an honest review (positive or negative)
5. Co-branded "acne-safe" list in their niche
6. React-ready asset: you send the analysis, they film reacting
7. Before/after correlation story with a creator who has a documented acne journey
8. Fungal-acne creator collab — audit 20 products the community argues about
9. "I ran [creator]'s viral routine through the checker" (with permission — gives them content too)
10. Free tool built for their specific niche, credited to them

### 5 UGC ad concepts (for when budget exists)
1. Silent screen recording: paste ingredients → reveal → "that's the one." Text-only.
2. Shelf-to-result: phone films products, cuts to scan result
3. Problem-agitate: "3 months, 4 eliminations, wrong every time" → tool → answer
4. Comparison: generic rating app vs. Skintel correlation, side by side
5. Testimonial-over-screen-recording: real beta user's words, screen recording visuals (stays faceless)

### 5 viral/share loops
1. **Shareable result card** — branded, screenshot-friendly, `skinstel.com` readable on it
2. **"Send me your shelf"** — comments → content → more comments
3. **Free niche tool** the community spreads for you (fungal-acne checker is the strongest candidate)
4. **Referral rewards** in product credit (§14)
5. **"Tag someone whose routine needs this"** — native to skincare comment culture

### 5 free-tool ideas
Covered in §13 — ranked: **A. Shelf Audit — shipped, live at `/shelf-audit`** · B. Fungal-acne safe checker (build next) · C. Routine conflict detector · D. Full-routine comedogenic score · E. Dupe finder.

### 5 landing page experiments
1. Hero: problem-first vs. product-first
2. CTA: "Find my culprit ingredient" vs. "Scan my shelf — free"
3. Demo above fold vs. below
4. Result-screenshot hero image vs. app-interface screenshot
5. Founding 100 offer visible immediately vs. after the free scan

---

---

## 23. Decision record: AI actors, hiring, and multi-platform

Three questions came up after the plan was written. Recording the answers so they don't get relitigated.

### Do not use AI-actor UGC tools (Arcads and similar) — decided, not a budget call

**1. It's a paid-ads tool.** Arcads is built for paid ads; reviewers recommend it for advertisers already spending **$500+/month**. Entry pricing is ~$110/month for 10 videos. For organic short-form, cheaper editors give more variety per dollar. Our budget is $0, so this would be the entire budget buying the wrong category of asset.

**2. Synthetic testimonials are disqualifying in this category.** An AI-generated person saying "this found what was breaking me out" is a fabricated endorsement for a health-adjacent product — an FTC endorsement problem, and directly corrosive to our only real wedge. Our positioning is *"other apps give generic, fear-based ratings; we correlate honestly against your own data."* That argument cannot be delivered by a synthetic person who never used the product. One commenter spotting it takes the positioning down with it.

**3. Platform enforcement removes the option of hiding it.** TikTok's 2026 policy detects synthetic media via C2PA Content Credentials, invisible watermarking, and computer-vision classifiers rather than self-disclosure. Penalties ladder warning → 7-day posting restriction → 30-day suspension → permanent ban. A "reduce AI content" control in Manage Topics also lets users opt out of AI content entirely, so part of the target audience never sees it.

**The deciding fact: the product doesn't need a person on screen.** Skintel's winning shot is an ingredient list and a reveal. An AI actor adds cost, legal exposure and reach risk to a format that has no human in frame to begin with.

**Where AI video is fine:** b-roll, motion graphics, and the existing `marketing/video/` render pipeline. **The line is synthetic humans making product claims.** Don't cross it.

### Hiring sequence — editor before marketer

Hiring someone to find a winning format before one exists is paying for guesses.

| Stage | Hire | Rate |
|---|---|---|
| Now ($0, no proven format) | **Nobody.** Founder posts screen recordings — nothing personal appears in them | $0 |
| Once one format performs | **Clipper/editor** — turns 1 recording into 5 posts. Volume is the bottleneck, not ideas | ~$5–15/hr |
| Once there's budget for faces | **Real UGC creators** with proper `#ad` disclosure — legal, credible, and no synthetic-testimonial exposure | $50–150/video |

**Hard exception: never outsource Reddit.** It's the highest-intent channel and communities detect astroturfing quickly; a ban is permanent. Reddit requires a genuine account with real ingredient knowledge — which requires nothing of the founder's face or voice.

### Budget is $150/month — and no, not a MacBook Pro

The real constraint hiding in the laptop question: the iOS app is Capacitor and pre-launch, and building/signing/submitting to the App Store requires macOS. The founder's daily machine is Windows. So a Mac genuinely sits in the critical path of shipping what the waitlist promises — but **owning one is not required.**

**Ship iOS for $0:** Codemagic's free tier provides 500 macOS M2 build minutes/month and builds, signs, and publishes Capacitor iOS apps to App Store Connect from the cloud. The `ios:build` script becomes a `codemagic.yaml`. At $150/month, a $1,600–2,500 MacBook Pro is 11–17 months of saving with nothing spent on growth — a decision not to market for a year.

**The one mandatory purchase: Apple Developer Program, $99/year.** Without it there is no App Store listing, and the landing page is currently showing App Store badges for something that cannot ship.

| When | Spend | Condition |
|---|---|---|
| Month 1 | $99 Apple Developer Program; bank the remaining $51 | Unblocks iOS. Content is founder-made screen recordings — no spend needed while a format is still being found |
| Month 2+ | $60–80 clipper/editor · $50–70 one real nano-creator with `#ad` disclosure · ~$20 reserve | **Only once a format shows signal.** If nothing is working yet, spend $0 and bank it |

**When a Mac does earn its cost:** debugging native iOS issues (simulator, Capacitor plugins) through cloud CI is slow — each iteration burns minutes and takes 10–15 minutes round-trip. At that point the answer is a **Mac mini M4 at $599 base (regularly $479–549 on sale)** — three to four months of budget, not fifteen, and fully sufficient for Xcode. The Windows machine stays the daily driver.

### Multi-platform is redistribution, not three strategies

One screen recording → TikTok + YouTube Shorts + Instagram Reels, uploaded natively to each. That is free and takes minutes. Running three *different* content strategies at zero audience spreads effort thin and slows down format discovery. **One asset, three surfaces, one format under test at a time.**

---

## Sources

- [Skintel — Personal skin intelligence (skintel.app, name-collision competitor)](https://www.skintel.app/)
- [Skintel: AI Skin Care App — App Store](https://apps.apple.com/us/app/skintel-ai-skin-care-app/id6755764884)
- [Skintel: AI Skin Analysis — Google Play](https://play.google.com/store/apps/details?id=ch.skintel.app)
- [Skin Care Ingredient Checker — TikTok discovery page](https://www.tiktok.com/discover/skin-care-ingredient-checker?lang=en)
- [App to Check Skincare Ingredients — TikTok discovery page](https://www.tiktok.com/discover/app-to-check-skincare-ingredients)
- [Ingredient Rater App Skincare — TikTok discovery page](https://www.tiktok.com/discover/ingredient-rater-app-skincare)
- [How to Grow TikTok Without Showing Your Face in 2026 — Kineclip](https://kineclip.com/blog/grow-tiktok-without-showing-face/)
- [Top 20 Faceless TikTok Ideas That Actually Go Viral (2026) — InReels](https://www.inreels.ai/blog/faceless-tiktok-ideas)
- [TikTok for Creators: Complete Growth & Earning Guide (2026) — Flowshorts](https://flowshorts.app/blog/tiktok-guide)
- [Arcads AI pricing in 2026: plans, credits, and the real cost — eesel AI](https://www.eesel.ai/blog/arcads-ai-pricing)
- [Arcads Review: Who Should Use It for AI UGC Ads in 2026 — MaxAEO](https://maxaeo.ai/blog/arcads-review/)
- [TikTok's AI-Generated Content Policy in 2026: Labels, Ads, and What Gets Removed — Cinerads](https://www.cinerads.com/blog/tiktok-ai-content-policy)
- [TikTok AI Content Policy 2026: 4-Tier Labels & Penalties — AuditSocials](https://www.auditsocials.com/blog/tiktok-ai-content-disclosure-rules-2026)
- [AI Content Disclosure Rules 2026 (TikTok, IG, YouTube) — SocialScale Hub](https://www.socialscalehub.com/academy/ai-content-disclosure-rules-2026-tiktok-instagram-youtube)
