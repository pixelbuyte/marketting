# Humanoid Robotics Marketing Operating System
### From zero followers to a company launch, told through the build itself

*Prepared September 2026. Research grounded in what's currently working for Figure, Unitree, 1X, Boston Dynamics, Tesla Optimus and Apptronik as of mid-2026 (see Sources at bottom).*

---

## 0. What's actually working right now (2026), and why

Before prescribing tactics, here's the pattern underneath every robotics moment that has spread in the last 18 months:

- **Unitree** wins distribution not because of polish, but because of *price + accessibility + real units in real hands*. Their G1 dancing at China's CCTV Spring Gala and later on Nasdaq's opening bell worked because it was a **real, physical, unscripted-feeling demo in a high-trust context** (state TV, a stock exchange bell), not a rendered concept video. Cost of entry to the meme (buy/rent a G1, film it doing something absurd) is low, so the internet remixes it endlessly — "Unitree vs Boston Dynamics" is now a TikTok genre other people make *for* them.
- **Boston Dynamics'** Spot/Atlas virality (e.g. the AGT synchronized dance) works on **spectacle + emotional projection** — robots doing something physically implausible, filmed cleanly, with no explanation needed. Zero seconds of context required to feel something.
- **Figure AI** built its narrative almost entirely on **partnership + capability milestones** (OpenAI integration, BMW factory pilots) covered by tech press, not organic social virality. Their weakness — no-revenue, no organic audience — is exactly the trap you must avoid: they depend on press cycles and funding headlines, which dry up between raises.
- **1X** and **Apptronik** lean into **founder-led, workshop-style video**: unscripted lab footage, visible failure, a person narrating why a mechanism exists. This is the closest model to what you should run, because it's replicable without a PR budget.
- **Tesla Optimus** shows the downside case: heavy skepticism accumulates when demos are suspected of teleoperation or staging without disclosure. Every "was that real?" comment thread is a credibility tax. **Radical labeling discipline (render vs. sim vs. teleop vs. autonomous) is now a competitive advantage**, not just an ethics checkbox — audiences in 2026 are trained to distrust robot demos by default, and the accounts that over-disclose earn outsized trust.

**The underlying mechanism for why robotics content spreads:** it's one of the only content categories left where a single unedited 5–15 second clip creates an *instant, cross-cultural, no-context-needed emotional reaction* (surprise, delight, uncanny valley, or "wait, is that real?"). That reaction is what algorithms reward with completion rate and rewatches. Everything else — captions, brand, story — rides on top of that reaction. Your entire content system should be built to manufacture that reaction honestly and repeatedly from real engineering work.

---

## 1. Positioning: what to say you're building, right now

You are not yet a company. Say that. Position as:

> **"An independent R&D lab building a general-purpose humanoid robot in public, one mechanism at a time."**

Working line for bios/website: *"We're building a general-purpose humanoid — in the open. Follow the build from first sketch to first steps."*

Do NOT claim: a company name as a brand yet (unless you already have one you're committed to), a timeline to "AGI-for-bodies," or comparisons ("better than Optimus"). Comparisons invite scrutiny you can't yet survive.

Every public asset (video caption, CAD render, post) should be labeled with one of these four tags, visibly, every time:
- 🎨 **CONCEPT** — render/vision, not built
- 🧪 **SIMULATION** — running in sim only
- 🔧 **PROTOTYPE** — physical, partially working
- ✅ **DEMONSTRATED** — physical, repeatable, real (state if teleop-assisted or autonomous)

This labeling system *is* your brand's credibility engine. Make it a recognizable visual tag (a small corner badge) so people start trusting your feed specifically because you're the lab that always discloses.

---

## 2. Target audiences, ranked

1. **Engineers/roboticists/hardware builders** — your highest-value early audience. They amplify credible technical content, become hires, and are immune to hype (so winning them signals quality to everyone else).
2. **AI/ML and "build in public" tech Twitter (X)** — high-leverage amplifiers, connect you to press and investors.
3. **Robotics-adjacent creators (5K–500K)** — the ladder that gets you infrastructure-level reach before you have your own.
4. **General tech-curious public (via short-form video, algorithmic reach)** — your volume/awareness layer; converts a small % to email but mostly builds ambient brand recognition.
5. **University robotics labs / student communities** — talent pipeline + credible amplification (they share things that make their field look good).
6. **Journalists/press** — reactive audience; earn them with real milestones, not pitches.
7. **Investors** — should feel like they're *discovering* you via the above channels, not being pitched directly this early.

---

## 3. Platform strategy — what to use first, what to skip

**Use, in this order:**
1. **X (Twitter)** — the default home for build-in-public, AI/robotics discourse, and where journalists + investors actually watch. Post here first, always.
2. **YouTube Shorts + a long-form YouTube channel** — Shorts for algorithmic discovery, long-form for the devlog archive that becomes your "scroll back and watch it being born" asset. This is the single most important platform for the founder's specific goal (watchable history).
3. **TikTok** — same short clips as Shorts, reformatted; this is your highest-ceiling discovery engine for the general public, cross-post everything.
4. **Reddit** (r/robotics, r/mechatronics, r/artificial, r/singularity, r/hardware, local maker subreddits) — huge for engineer audience and technical credibility; comment/engage before ever "promoting."
5. **Instagram Reels** — same short-form asset, third-tier priority, mostly a repost target.
6. **A devlog blog / changelog page on your own site** — the "spine" all social content links back to; this is what makes your history scrollable and SEO-durable.
7. **Discord** — once you have ~1,000 real followers, for the community pillar (voting, challenges).
8. **Hacker News** — situational: only for genuinely technical writeups or milestones (a "Show HN" for something people can inspect), not routine updates. One good HN front-page hit can outperform months of social posting for the engineer/investor audience.
9. **LinkedIn** — low priority now; use later for hiring, partnerships, and enterprise/customer narrative once you have Gen 1.
10. **Newsletters/podcasts** — as a guest, once you have 2–3 real milestones to talk about; don't pitch yourself as "visionary," pitch a specific engineering story.

**Skip / don't waste time on:** paid ads (zero use pre-audience — you have nothing to retarget yet), Facebook, Pinterest, Snapchat, generic "AI influencer" engagement pods, and buying followers/engagement (destroys the exact credibility this strategy depends on).

---

## 4. Zero → 100,000: literally what to do

### 0 → 10 followers
This is a personal-network + seeding problem, not a platform problem.
- Founder posts from their **personal, already-existing account** (do not start a brand-new zero-history account first — algorithms and humans both distrust brand-new accounts with no signal). The company account is created and cross-linked, but the founder's personal credibility carries the first weeks.
- Post the first real artifact: a sketch, a CAD screenshot, or "why I'm building this" — one authentic paragraph, one image.
- Manually DM/tell 20–30 people who would *actually* find this interesting (former colleagues, robotics Discords, university contacts). Ask them to follow, not to share — asking for shares this early reads as needy and gets ignored; genuine follows compound.
- Join 5–10 relevant Discords/subreddits as a real participant for two weeks *before* posting your own project there.

### 10 → 100
- Publish devlog #1 on your own site + a thread on X summarizing it with 1 photo/video. Cross-post the same clip to Shorts/TikTok/Reels natively (not a repost link — upload directly to each platform).
- Answer/engage in 5 robotics/AI threads per day on X with genuinely useful comments (not "check out my project" — just be a real, sharp voice; profile link does the work).
- Submit your best technical post to one relevant subreddit, framed as "here's how I solved X problem," not "here's my project."
- Goal artifact for this stage: **first physical part fabricated**, filmed.

### 100 → 1,000
- Ship one short-form video every 2–3 days minimum (the algorithm rewards frequency + consistency far more than any single production value at this size).
- Start the "Day X of building a humanoid" numbered series — numbering creates a binge/return incentive ("what's Day 40 look like").
- Do your first small-creator outreach (5K–50K tier, see §18) offering an exclusive early look.
- Launch the waitlist page (see §16) once you have your first "wow" clip to point at — a waitlist with nothing to show yet converts poorly.
- Goal artifact: **first joint/actuator moving under its own control**, filmed from 3 angles, both a 9s vertical cut and a 3-minute explainer.

### 1,000 → 10,000
- This is where a specific video should try to break out: pick your strongest visual milestone (first grasp, first stand, first step) and produce it as a proper "hero" piece — hook in first 1.5s, then the fuller story, cross-posted everywhere same day.
- Begin the recurring series structure (§14) so the account has multiple hooks, not just one.
- Start creator ladder tier 2 (50K–250K) outreach using proof from tier 1 collabs.
- Pitch your first specific-milestone story to 3–5 relevant journalists/newsletters (see §19).
- Goal artifact: **first autonomous (non-teleop) micro-task**, clearly labeled as such.

### 10,000 → 100,000
- You now have enough historical archive that new viewers can "scroll back and watch it being born" — start explicitly promoting that ("new here? start from Day 1" pinned post/thread).
- Run your first real challenge involving the community (vote on a design choice, submit a task idea) — this is when the Community pillar actually works, not before, because you need enough people for a vote to feel meaningful.
- Approach tier 3 creators (250K–1M) and consider your first funded collab.
- This is your **Launch 1 (Gen 1 design reveal)** window — see §23.

---

## 5. First 30 days (day-by-day where useful)

- **Day 1–3:** Set up devlog site + waitlist page (skeleton is fine). Founder personal-account post #1: why this project exists. Create brand accounts on X, YouTube, TikTok, Instagram (claim handles even if quiet at first).
- **Day 4–7:** Film/publish first "state of the project" piece — sketches, CAD, whatever exists today, honestly labeled 🎨/🧪. This is devlog #1.
- **Day 8–10:** Join and genuinely participate in 5+ relevant communities (Reddit, Discord, X circles).
- **Day 11–14:** First physical milestone content (even a single motor test counts) — this is your first short-form clip.
- **Day 15–17:** Publish devlog #2. Submit a technical post to one subreddit.
- **Day 18–21:** Second short-form clip. Start numbered "Day X" series publicly (retroactively number days 1–21 if useful).
- **Day 22–24:** First outreach to 3–5 small creators (5K–50K tier).
- **Day 25–27:** Devlog #3. Waitlist page goes live with a real CTA tied to your best clip so far.
- **Day 28–30:** Review: which single piece of content performed best? Do a "why this worked" retro and double down on that format for month 2.

## 6. First 90 days (weekly milestones)

- **Weeks 1–4:** Foundation — accounts, devlog cadence (weekly), first physical build content, community participation, waitlist live. Target: first 100–300 followers across platforms combined.
- **Weeks 5–8:** Cadence increase to 2–3 short videos/week + weekly devlog. First creator collabs (tier 1). First subreddit/HN technical post that performs. Target: 1,000–3,000 followers, 50–150 waitlist signups.
- **Weeks 9–12:** First "hero" milestone video (first grasp/stand/step). First press pitch sent. Community challenge #1 (if audience size supports it). Target: 5,000–15,000 followers, 300–800 waitlist signups.

---

## 7. Content calendar (frequency per platform)

| Platform | Frequency | Format |
|---|---|---|
| X | 5–7 posts/week (mix of clips, engineering notes, replies) | Native video + text threads |
| YouTube Shorts / TikTok / Reels | 3–5 short clips/week, same asset cross-posted | 9–60s vertical |
| YouTube long-form | 1 devlog/week (5–12 min) | Horizontal |
| Reddit | 1–2 genuinely useful posts/month per relevant subreddit | Text + image/video |
| Own devlog/blog | 1 post/week minimum | Long-form written + media |
| Instagram feed/carousel | 1–2/week (design, CAD, behind-the-scenes stills) | Carousel |
| Discord | Daily light presence once launched (~1K followers) | Community |
| Newsletter (owned, to waitlist) | 1/week or biweekly | Recap + exclusive bit not posted publicly |

---

## 8. 30 actual post ideas (not generic categories)

1. "We tried to make our robot pick up an egg without crushing it. Attempt 1." (fail, cut to redesign, attempt 2 succeeds)
2. "This $40 gripper couldn't hold a phone. Here's what we built instead." (part comparison)
3. CAD-to-real split screen: the exact same joint, simulation on left, physical part on right, synced motion.
4. "Our robot's knee doesn't look human. Here's the engineering reason why." (explainer)
5. "What happens when we unplug a sensor mid-task" (failure/robustness demo)
6. "Day 12: first time this arm moved on its own"
7. Time-lapse: raw aluminum stock → machined part → assembled joint (60s)
8. "We spent 3 weeks on a hand that still can't do this." (honest failure post)
9. Side-by-side: our actuator vs. a $400 commercial actuator, same load test
10. "Sketch to CAD to sim in 40 seconds" (idea-to-simulation speedrun edit)
11. Founder voiceover: "Why I'm building a humanoid instead of a startup that's easier to fund"
12. "First time it balanced on one leg. It fell 14 times before this." (failure supercut → success)
13. "Ask the robot to do something it's never seen." (novel task attempt, labeled honestly re: autonomy level)
14. Behind-the-scenes: whiteboard session where a design decision gets made (unscripted)
15. "Here's what $10,000 of humanoid hardware actually looks like laid out on a table"
16. Teardown-style: "Why we chose this motor over 4 alternatives" (engineering comparison)
17. "This sensor died mid-demo. Here's the raw, unedited footage." (radical transparency piece)
18. Community poll result reveal: "You voted for the red hand. Here it is."
19. "Gen 1 arm vs Gen 2 arm: same task, one year apart"
20. Quick myth-check: "Is this teleoperated or autonomous? Here's exactly which parts of this clip are which."
21. "What breaks first when a robot falls" (slow-motion failure analysis, oddly satisfying)
22. Guest cut: a small creator's reaction filming your lab for the first time
23. "The ugliest but most important part of the robot" (spotlight an unglamorous but critical component)
24. "We let the community suggest a challenge. Here's us attempting it live/on camera."
25. 3-generation part evolution montage (if/when you have it): v1 → v2 → v3 of the same mechanism
26. "How many failed prototypes did it take to get a working finger?" (count them on screen)
27. Founder Q&A clip answering the most-asked comment question of the week
28. "Inside our sim environment" — screen capture of a training/testing run with plain-language narration
29. Milestone recap thread: "This is everything that happened in the last 90 days" (retention/onboarding content for new followers)
30. "We're hiring/looking for X" — framed as a build update, not a job ad (only once real)

---

## 9. 20 short-video hooks (first 1.5 seconds)

1. "It failed 30 times before this happened."
2. "This part broke on camera. We kept it in."
3. "Nobody told this robot how to do this."
4. "$40 part vs. our part. Same test."
5. "We didn't expect this to work."
6. "This is not CGI." (only use when 100% true and clearly demonstrable)
7. "Watch its hand at 0:04."
8. "This took one year to go from this... to this."
9. "We asked it to do something new."
10. "This is what happens when a sensor dies."
11. "You voted. We built it."
12. "This joint moves like a human wrist. Here's why."
13. "Day 1 vs. today."
14. "We almost didn't show you this failure."
15. "This is real. Here's the unedited version."
16. "One year of humanoid progress in 45 seconds."
17. "It's never seen this object before."
18. "This part cost us three redesigns."
19. "This is the ugly part nobody shows you."
20. "Watch what happens when we remove the safety stop." (only if genuinely safe/controlled — high engagement but must be handled responsibly)

---

## 10. 10 robotics demonstrations designed for social media

1. Pick-up-a-fragile-object challenge (egg, chip, glass) — instant stakes, instant readability.
2. Balance recovery test — push/nudge the robot, show it recover (or fail and explain why).
3. Novel-object grasp — hand it something it's never encountered on camera.
4. Human-handoff — robot receives and passes an object to a person naturally.
5. Stairs/uneven terrain attempt — mobility is visually legible to anyone.
6. "Copy this human movement" — side-by-side with a person doing the same motion.
7. Blindfolded/occluded-sensor task — shows perception dependency clearly.
8. Speed challenge — same task timed across two hardware generations.
9. Tool-use attempt — screwdriver, pouring water, etc. — universally understood difficulty.
10. "Live, unedited, one take" challenge video — leans directly into the credibility gap competitors have created.

---

## 11. Five recurring video series

1. **"Day X"** — numbered build log, the connective spine of the whole channel.
2. **"Fail Reel"** — weekly/biweekly compilation of failures with brief engineering notes (turns failure into a beloved, trust-building format).
3. **"Part of the Week"** — deep-dive engineering explainer on one component.
4. **"Ask the Lab"** — founder/engineer answering top audience questions.
5. **"Gen vs. Gen"** — comparative capability demos as new hardware generations ship.

---

## 12. Founder build-in-public strategy

- The founder is the face and voice for at least the first 12 months — audiences bond with people, not logos, at zero-trust stage.
- Post in first person, share real uncertainty ("we don't know if this will work") — manufactured confidence reads as fake in this category now.
- Weekly or biweekly short personal-note video/post separate from engineering content — humanizes the account and is disproportionately shared.
- Never claim sole credit if there's a team — name and show collaborators; it reads as more credible and attracts more talent.

---

## 13. Waitlist strategy

Positioning: **"FOLLOW THE BUILD"** as the primary CTA — it fits your actual funnel (attention → curiosity → trust) far better than "GET EARLY ACCESS" (implies a product exists) or "JOIN THE ROBOTICS LAB" (fine as a secondary/community framing once you have Discord, but weaker as the top-of-funnel CTA before there's a "lab" to join).

Capture:
- Email (required)
- Interest: developer / customer / investor / enthusiast / researcher / creator (single-select)
- Optional: profession/background (free text, optional)
- Referral source (auto-captured via UTM/referral code, not asked)

Referral mechanism: **"Invite 2 people → get the next devlog 48 hours early + a numbered spot on the founding waitlist."** Keep it modest and true — no fake scarcity, no fake countdown timers, no "only 500 spots" unless that's a real constraint.

---

## 14. Landing page structure

1. **Hero:** one real photo/video of the robot (or its most credible current state, honestly labeled) + one sentence positioning + email capture CTA ("Follow the Build").
2. **What we're building:** 2–3 sentences, no hype adjectives, one labeled image (concept/sim/prototype).
3. **The build log:** embedded feed or link to 3 most recent devlog entries — proof of momentum.
4. **Credibility disclosure block:** short explicit statement of your labeling system (concept/sim/prototype/demonstrated) — this becomes a trust signal, not boilerplate.
5. **Founder note:** short, personal, why this project exists.
6. **Waitlist form:** email + interest dropdown + referral code field.
7. **Follow links:** X/YouTube/TikTok/Instagram, framed as "watch it happen in real time."

---

## 15. Creator outreach strategy

Ladder, never top-down:
- **Tier 1 (5K–50K, robotics/engineering/maker niches):** message personally, offer an exclusive first look/lab visit (virtual or in-person), no payment expected. Ask: "Would you want to be the first to show your audience X before we post it publicly?"
- **Tier 2 (50K–250K):** once you have 2–3 tier-1 collabs as proof, pitch with those examples attached. Offer either an exclusive access moment or co-created content (they film a segment with you).
- **Tier 3 (250K–1M):** pitch a specific milestone moment (e.g. Gen 1 reveal), not a generic partnership — creators say yes to *events*, not *relationships*, at this stage.
- **Major creators:** only approach once you have a real reveal-scale moment (Launch 2 or later) and ideally an inbound signal (they've already mentioned humanoid robots).

**Sample outreach message (tier 1):**
> Hi [name] — I'm building a general-purpose humanoid robot from scratch, fully in public (zero followers a few months ago, now documenting every part of the build). We just [specific real milestone]. I think your audience would find [specific technical detail] genuinely interesting, and I'd love to give you first access to film/cover it before we post publicly — no strings, just credit. Here's what exists so far: [link to devlog/best clip].

---

## 16. PR strategy

Only pitch around real, specific, newsworthy events — never "we are building the future." Trigger events:
- A capability demonstrated for the first time (labeled appropriately)
- A significant technical benchmark/result
- A funding round or partnership
- Gen 1/Gen 2 reveal
- First customer or research collaboration

**Pitch structure:** one-line news hook + one real proof asset (video/data) + one line of context on why it matters + offer of an exclusive/first-look to one outlet before wider distribution. Build a target list of 10–15 reporters who already cover robotics/embodied AI (from bylines on Unitree/Figure/1X coverage) rather than generic tech desks.

---

## 17. Community strategy

- Don't open Discord until ~1,000 engaged followers — an empty community reads as failure.
- First community mechanics: non-critical design votes (color, name of a part, a challenge to attempt next), submitted challenge ideas, AMA sessions.
- Recognize contributors publicly (shoutouts in devlogs) — cheap and highly retentive.

---

## 18. Referral loop

Invite 2 → early access to next devlog + founding waitlist number. Invite 5 → name/handle featured in a devlog credits reel. Keep thresholds low and genuinely deliverable — a referral program that overpromises and underdelivers burns exactly the trust this whole strategy is built on.

---

## 19. Launch-video concept

A 60–90s video structured as: **cold open on the single best physical demo you have → hard cut to black, one line of text ("X months ago, this didn't exist") → rapid built-in-public montage (sketches → CAD → first parts → failures → progress) scored to rising music → return to the opening demo, now with context → close on "Follow the build" CTA.** This format works because it retroactively reframes the opening hook once the audience understands the timeline — the "reveal" is the speed of progress, not just the robot.

---

## 20. Gen 1 reveal campaign

- **T-14 days:** start teasing via close-up detail shots (no full reveal) across all channels.
- **T-7 days:** publish a "what to expect" devlog framing what Gen 1 does and doesn't do yet (manage expectations explicitly).
- **Reveal day:** launch video (above) + full devlog writeup + press pitch to your target list, all coordinated same-day + AMA that evening.
- **T+3 days:** "reactions" content — creator collab reactions, community Q&A responses.
- **T+14 days:** retrospective post: "what Gen 1 taught us," sets up next arc.

---

## 21. Budget scenarios

**$0/month:** Founder-shot/edited content on a phone; free tools (CapCut/DaVinci Resolve free tier) for editing; organic-only outreach; own time for community management. Fully viable — most of this plan assumes $0.

**$500/month:** A basic ring light/mic kit (one-time), a modest budget for boosting 1–2 best-performing posts per month, small thank-you gifts for tier-1 creator collaborators, a simple email tool (e.g. a free-tier ESP upgraded to paid).

**$2,000/month:** Part-time editor (5–10 hrs/week) to increase cross-platform output consistency, a proper camera/audio kit, sponsored inclusion in one relevant newsletter/podcast per quarter, modest paid boost on top-performing organic content only (never cold ads to strangers with no context).

**$10,000/month:** Dedicated part-time content producer, professional footage for milestone/reveal moments (Gen 1 reveal, etc.), paid creator collaborations at tier 2, PR/comms support for press cycles around major milestones, budget for a real developer/community platform as the audience scales.

At every tier: spend on **making real progress more visible**, never on manufacturing an appearance of progress that doesn't exist.

---

## 22. Metrics dashboard

Track weekly, per platform and in aggregate:
- Views, watch time, completion rate (leading indicators of hook/format quality)
- Shares, saves (indicate resonance beyond passive viewing)
- Profile visits → follower conversion rate (indicates whether content is converting curiosity into commitment)
- Website visits from social (traffic quality, not just volume)
- Waitlist conversion rate from site visits (funnel health)
- Referral rate (% of new signups from existing waitlist members)
- Email open/click rate (owned-audience engagement, most durable metric)
- Creator collab ROI (followers/waitlist signups attributable per collab, tracked via unique links)

Build this as a simple weekly spreadsheet or lightweight dashboard; the specific tool matters far less than the discipline of reviewing it every week and asking "what earned the reaction, and can we do more of that honestly."

---

## 23. Weekly experiments to run

Rotate one variable at a time so you can attribute results:
- Hook wording/structure (test 2–3 hook styles per week)
- Video length (15s vs 30s vs 60s cut of the same footage)
- Posting time-of-day
- Caption style (question vs. statement vs. none)
- Thumbnail/cover frame choice
- CTA placement and wording (in-video vs. caption vs. bio only)
- Cross-post timing (same day vs. staggered across platforms)

---

## 24. What NOT to do (credibility killers in robotics specifically)

- Never present teleoperated or heavily edited footage as autonomous without disclosure — this is the single fastest way to permanently lose trust in this category in 2026.
- Never fabricate scarcity ("only 100 spots") or fake countdown urgency.
- Never compare yourselves directly and unfavorably-for-competitors ("better than Optimus") before you can back it with a real head-to-head demo.
- Never buy followers/engagement/comments.
- Never publish content that reveals proprietary manufacturing detail, full CAD, control source code, or safety-bypass mechanisms in the name of "transparency."
- Never let a funding announcement stand in for a capability milestone — press and audiences increasingly discount money-only news in this sector.
- Never go silent for long stretches then reappear with a big reveal — the "build in public" trust asset decays without consistent cadence; a slower, honest cadence beats a sporadic, hype-driven one.
- Never claim a timeline ("shipping in 2027") you're not confident you'll hit — missed public timelines in robotics get remembered and mocked.

---

## Sources

- [Top 5 Viral Humanoid Moments That Made 2025 The Year Of Robotics – KraneShares](https://kraneshares.com/top-5-viral-humanoid-moments-that-made-2025-the-year-of-robotics/)
- [Unitree's Strategy to Make Humanoid Robots Work – Bismarck Analysis](https://brief.bismarckanalysis.com/p/unitrees-strategy-to-make-humanoid)
- [China's Unitree Robotics Is Leading the Humanoid Revolution – TIME](https://time.com/article/2026/07/23/unitree-china-human-robotics/)
- [Unitree Reclaims the Spotlight with 18,000 Cumulative Bipedal Humanoids Produced – Humanoids Daily](https://www.humanoidsdaily.com/news/unitree-reclaims-the-spotlight-with-18-000-cumulative-bipedal-humanoids-produced)
- [A Complete Guide To Unitree Robotics' 2026 IPO – KraneShares](https://kraneshares.com/a-complete-guide-to-unitree-robotics-2026-ipo-why-it-matters-for-star-market-etf-kstr-humanoid-robotics-etf-koid/)
- [Unitree IPO Subscription Opens: Profitable Robot Maker vs. $39B No-Revenue Figure AI – Tech Times](https://www.techtimes.com/articles/322574/20260731/unitree-ipo-subscription-opens-profitable-robot-maker-vs-39b-no-revenue-figure-ai.htm)
