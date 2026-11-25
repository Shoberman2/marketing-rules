# Spencer's Marketing Rules

The master playbook for hooks, human attention, retention and ethical social distribution. Grounded in open-sourced ranking code, peer-reviewed psychology and journalism research, official platform documentation, classic copywriting, and top open-source marketing agent skills.

Every finding is tagged by evidence tier: `[official / source-code]`, `[peer-reviewed research]`, `[industry data]`, `[book]`, `[practitioner playbook]`, `[OSS repo]` or `[anecdotal]`.

---

## 1. Core Philosophy

Platform ranking algorithms and human psychology agree on the same thing: **attention is earned in the first moment and kept by delivering real substance.**

- Platforms punish empty clicks and engagement bait. They reward replies, private shares (DM sends, link copies), saves, watch time and dwell.
- Humans scroll past vague teases and predictable templates. They stop for specific artifacts, calibrated curiosity gaps, genuine prediction breaks and practical value they would send to a friend.
- **Zero fluff, zero em dashes, zero fabricated claims.**

---

## 2. Platform Algorithm Signals

### 2.1 X (Source Code: `xai-org/x-algorithm`) `[official / source-code]`

From `xai-org/x-algorithm` (`home-mixer/params/param.rs`, Apache-2.0, Nov 2026): Phoenix predicts the probability (or continuous dwell) of each user action and ranks via `Final Score = sum(weight_i * P(action_i))`.

*Important technical note written into the source:* weights multiply **predicted probabilities**, not raw action counts. Negative weights are large because reports and blocks are rare events.

| Action | Default Weight | Practical Takeaway |
|---|---:|---|
| Share via copy link | `20.0` | Write save-worthy, share-worthy artifacts (never ask people to copy the link). |
| Reply (mutual follow on original post) | `5.0` (+`15.0` = `20.0`) | Spark real conversation, especially among followers who interact back. |
| Reply (general) | `5.0` | End with a sharp observation or genuine question people want to answer. |
| Quote | `5.0` | Publish clear takes and receipts others want to react to. |
| Share via DM | `5.0` | Pass the "Group-Chat Test" (Section 3.10). |
| Follow author | `4.0` | Consistent niche value turns one post into a follower. |
| Share (generic) | `2.118` | Useful takeaways travel. |
| Repost | `1.0` | Useful, not the top lever. |
| Like (favorite) | `0.708` | Weakest active signal. Never optimize for raw likes. |
| Click dwell time / Click | `0.385` / `0.274` | Reward clicks inside the post. |
| Open link | `0.2` | Make the post self-contained; links alone carry little weight. |
| Not dwelled | `-0.02` | Weak hooks that get scrolled past hurt. |
| Block author | `-31.2` | Avoid rage-bait and spam. |
| Not interested | `-53.07` | Stay relevant to your niche. |
| Mute author | `-58.8` | Do not flood feeds with near-duplicates. |
| Report | `-234.0` | Never deceive, harass or post fake claims. |

Additional ranking mechanics in the repo:
- **First 2 hours & 48-hour window:** `ColdStartMaxPostAgeSecs = 7200` (2 hours) with Thompson sampling; posts older than 48 hours drop out of For You.
- **Out-of-network discount:** Default `OonWeightFactor = 0.75` (`vm-ranker/params.rs`). Posts must earn strong early engagement to break out beyond followers.
- **Author diversity decay:** Repeated posts from the same author in one batch are decayed. Space originals hours apart and rotate formats.
- **Built-in enforcement labels:** Code includes `llm_slop_user` enforcement plus `PROMOTES_REPLIES`, `PROMOTES_SHARES`, `PROMOTES_CLICKS` and `CopyLinkBaitEmbeddingGrokDistilled`. Never write engagement bait or AI slop.

*Note: Treat the 2023 `twitter/the-algorithm` repo (AGPL-3.0) as historical background only.*

### 2.2 Instagram & Reels `[official platform guidance]`

From Instagram official blogs (2023 to 2025), Adam Mosseri's creator guidance (Feb 2025) and Meta's Reels Chaining transparency docs (Nov 2025):
- **Three core reach metrics (Mosseri, Feb 13, 2025):** Average watch time (for Reels), likes per reach, and **sends per reach** (DM shares).
- **3-second hook rule:** Watch your **3-second view rate** (share of viewers still watching past second 3).
- **Stand-alone test:** New Reels are tested with a small audience (including non-followers), then widened. Follower count is not the primary ticket into recommendations.
- **Originality enforcement:** Instagram labels unoriginal reposts, boosts the original creator, and can strip repeat aggregators from recommendations. Watermarked, low-res, muted, bordered, engagement-baited or majority-static-text Reels are downranked.

### 2.3 TikTok `[official platform guidance]`

From TikTok Safety & Newsroom recommendation docs:
- **Core signals:** Likelihood of watch completion (especially finishing a longer video), shares, comments, likes and skips.
- **Follower count and past viral videos are not direct ranking factors.**
- **90-day pool & no volume penalty:** For You draws mostly from the last 90 days; leave underperforming videos up, and focus on retention rather than trying to game upload counts.

### 2.4 LinkedIn `[official platform guidance]`

From LinkedIn Help and LinkedIn Engineering blogs (2020 dwell-time paper, Mar 2026 generative recommender post):
- **Core signals:** Dwell time (on feed and after click), `P(skip)` on ultra-short dwells, meaningful comments, reactions and reshares, evaluated across the viewer's full interaction sequence.
- **What to avoid (explicitly listed as ineligible for broader reach):** Pure promo with no insight, off-topic promotional comments, engagement pods, engagement bait ("Like if you agree", tagging for reach, irrelevant hashtags), unoriginal copies, and humor/news memes lacking professional context.
- **The "external link penalty" myth:** LinkedIn's Help and Engineering posts do **not** publish a numeric link penalty or instruct putting links in the first comment. What *is* documented is dwell/skip modeling: if a post is just a bare link that sends people away before they read, low dwell hurts reach. Write posts that deliver full value on-feed.

### 2.5 YouTube & YouTube Shorts `[official platform guidance]`

From YouTube Help (`9314415`, `16391400`, `11914225`, `16559650`) and YouTube Blog (Sep 2025):
- **Long-form:** Watch time share wins Test & Compare experiments, **not CTR**. High CTR with low retention signals a broken promise ("overpromising"). Monitor the **30-second intro retention** rate. Browse titles build intrigue; search titles answer the query directly.
- **Shorts:** Ranked by view vs. swipe-away rate, average view duration, average percentage viewed, likes and post-watch satisfaction surveys.

### 2.6 Cadence & Reply Effects `[industry data]`

From Buffer's 2026 study (52M+ posts; observational associations, not proven causation):
- **Replying to comments correlates with higher engagement:** Threads +42%, LinkedIn +30%, Instagram +21%, Facebook +9.5%, X +8%. Always stay active in the first 1 to 2 hours after posting to answer real comments, and leave 3 to 5 thoughtful, concrete niche replies per day on other accounts.
- **No-post penalty vs. diminishing returns:** Posting 1 to 2 times per week strongly beats zero-post weeks, while excessive low-quality volume reduces reach per post. Consistency and quality win over spraying filler.
- **Starting posting windows (audience local time, test against your own analytics):** X 8 to 11 a.m. weekdays; Instagram 9 a.m. or 6 p.m. weekdays; LinkedIn 3 to 6 p.m. Wed to Sun; TikTok 6 to 11 p.m. daily + weekend mornings. Breaking news goes live immediately while fresh.

---

## 3. The Psychology of Attention, Sharing & Trust

1. **Arousal beats valence (Berger & Milkman 2012, *JMR*):** `[peer-reviewed research]` Studying 3 months of *New York Times* articles plus lab studies, high-arousal activating emotions (**awe**, **anger**, **anxiety**) drove sharing significantly more than low-arousal **sadness**, even though positive articles slightly outperformed negative ones overall.
2. **STEPPS (Berger 2013, *Contagious*):** `[book]` People share for **Social Currency** (makes them look smart/in-the-know), **Triggers** (daily cues), **Emotion**, **Public** visibility, **Practical Value** (checklists, math, deadlines) and **Stories**.
3. **Curiosity peaks at moderate concreteness (Loewenstein 1994; Aubin Le Quéré & Matias 2025, *Scientific Reports*, 8,977 Upworthy RCTs):** `[peer-reviewed research]` Vague clickbait ("You won't believe...") fails because the reader lacks context to care. Total spoilers fail because nothing is left to learn. **Peak CTR occurs at moderate concreteness:** name the subject and stakes clearly, and hold back only the *how* or *twist* for line 2.
4. **Curiosity boosts memory (Kidd & Hayden 2015; Gruber et al. 2014, *Neuron*):** `[peer-reviewed research]` High-curiosity answers are recalled at 70.6% vs. 54.1%, and unrelated details shown during the anticipation window are remembered better too. Place your key fact *inside* an honest open loop.
5. **Novelty & prediction error (Schultz et al. 1997, *Science*; Bunzeck & Düzel 2006, *Neuron*):** `[peer-reviewed research]` Dopamine neurons fire for unexpected reward and drop when an expected reward fails to appear. Honest pattern interrupts hook attention; bait-and-switch creates negative prediction error that audiences punish.
6. **Sticky ideas & Curse of Knowledge (Heath & Heath 2007, *Made to Stick*):** `[book]` Great ideas are **Simple, Unexpected, Concrete, Credible, Emotional, Stories (SUCCESs)**. Replace abstract buzzwords ("streamline workflows") with physical details a stranger can picture.
7. **Moral-emotional contagion (Brady et al. 2017, *PNAS*, 563,312 tweets):** `[peer-reviewed research]` Each moral-emotional word raised retweets ~19 to 20% (IRR = 1.19), but diffusion stayed heavily inside ideological bubbles. Keep moralized politics off utility/product brands and keep civic data nonpartisan.
8. **Negativity bias is real and small (Robertson et al. 2023, *Nature Human Behaviour*, 22,743 Upworthy RCTs):** `[peer-reviewed research]` Each negative word raised relative CTR by **2.3%** while each positive word lowered it by **1.0%** (strongest in politics/economy). Never trade credibility for a 2.3% lift.
9. **Outrage & question-headline costs (Scacco & Muddiman 2016, 2019, CME, N > 2,000 / 1,535):** `[peer-reviewed research]` Hollow question headlines ("Did X betray voters?") and outrage framing lowered story expectations, reduced intended engagement and made readers perceive articles as "fake news."
10. **The Group-Chat Test & NYT Sharing Study (2011, N = 2,500):** `[industry data]` People share to bring value, define identity and nourish relationships; 73% process ideas deeper by sharing. Ask before posting: *"Would one specific person in my audience screenshot this or DM it to a friend right now?"*
11. **Halfway reading depth & news avoidance (Chartbeat 2013; Reuters Institute DNR 2025):** `[industry data]` 38% of article visitors bounce, most stop halfway, and scroll depth barely predicts sharing. News trust sits at 40% while news avoidance hit 40% (driven by negativity and fatigue). Put shareable receipts in the top half, and pair critical stories with practical utility and primary links.
12. **Processing fluency & anchoring (Oppenheimer 2006; Kahneman 2011):** `[peer-reviewed research]` / `[book]` Needlessly complex prose makes writers look *less* intelligent. Plain English feels truer; honest, sourced reference numbers anchor perception fairly.
13. **Schwartz's 5 Awareness Stages (1966, *Breakthrough Advertising*):** `[book]` Match the opener to where the reader is: **Unaware** (lived moment), **Problem-Aware** (friction + cost), **Solution-Aware** (mechanism contrast), **Product-Aware** (proof + objection handling), **Most-Aware** (offer + price). Lead ~80% of cold feed posts at Unaware or Problem-Aware.
14. **Ethical Cialdini (7 principles):** `[book]` Give real value upfront (Reciprocity), cite dated counts (Social Proof), quote primary records (Authority), state real limits only (Scarcity), use shared-problem framing (Unity). Zero fake timers or invented numbers.
15. **Classic copy & narrative arcs:** `[book]`
    - **Sugarman's slippery slide:** Sentence 1 exists solely to get sentence 2 read.
    - **Ogilvy:** 5x more people read the headline than the body; specific news beats clever puns.
    - **Halbert:** Speak directly to the "starving crowd" already feeling the pain.
    - **Rule of One:** One reader, one big idea, one promise, one action.
    - **ABT (Randy Olson):** `[Context] AND [Context], BUT [Problem], THEREFORE [Consequence]`.
    - **Story Spine (Kenn Adams):** Once upon a time / Every day / One day / Because of that / Until finally / Ever since then.
16. **Unverified folklore to stop repeating:** Do not cite "63% of top TikTok ads put the key message in the first 3 seconds" (no primary TikTok source found), do not assume a fixed LinkedIn external-link multiplier, and note that Zeigarnik memory effects are fragile in modern replication (use open loops to pull attention *forward*, not as magic recall tricks).

---

## 4. Hook Craft & Top Formulas by Format

### The 10 Psychological Levers
`GAP` (Calibrated curiosity gap) · `FLIP` (Prediction break / contrarian) · `NUM` (Specificity / hard number) · `SCENE` (In medias res / scene) · `CALL` (Identity callout) · `STAKES` (Loss / hidden cost) · `PROOF` (Receipt / primary source) · `USE` (Practical value) · `TIME` (Timeliness / novelty) · `VS` (Comparison / choice). Strong hooks stack two levers (e.g., `GAP+NUM` or `FLIP+PROOF`).

### Hook Scoring Rubric (`social-media-skills/skills`, MIT)
Write **5 to 10 candidate hooks** per post and score each `0` to `2` across 6 dimensions (**Truth** and **Pull** are pass/fail gates):
1. **Gap:** Does it open an unresolved tension without being vague?
2. **Specificity:** Does it carry a named noun, number or physical detail?
3. **Truth (Pass/Fail):** Is every implied claim 100% verifiable and deliverable?
4. **Fit:** Does it match the reader's awareness stage and platform native style?
5. **Voice:** Does it sound like a real human in your brand voice (zero AI slop)?
6. **Pull (Pass/Fail):** Would the target reader genuinely stop scrolling to read line 2?

### Top Formulas by Format (see [`hooks.md`](hooks.md) for all 202)

- **X Single Post:**
  - *The Withheld Noun (`GAP+NUM`):* "The [specific thing] behind [specific outcome]."
  - *Common Belief, Then Receipt (`FLIP+PROOF`):* "Most [audience] think [belief]. [Primary source] says [opposite]."
  - *The Cost Math (`NUM+STAKES`):* "[Process] costs [$X] before [outcome]. The math:"
  - *PAS Opener (`USE+STAKES`):* "Problem in one line. Agitate in one line. Solution next."
- **X Thread Post 1:**
  - *Counted List With Ranked Surprise (`GAP+NUM`):* "[N] [items] from [source], ranked. Number [N] is the one nobody expected."
  - *Breakdown Thread (`NUM+PROOF`):* "We reviewed [N] [artifacts]. Three patterns:"
  - *Thread Story Arc (`SCENE+GAP`):* Inciting moment in post 1; resolution held until the final post.
- **Reel / TikTok / YouTube Short (First 3 Seconds):**
  - *Three-Track Video Rule:* Write **Visual Action (0 to 3 s)**, **Spoken Line (<=2 s)** and **On-Screen Text (<=6 words)** separately. Record both a question version and a statement version (Jenny Hoyos).
  - *Question On Screen, Answer Off Screen (`GAP`):* "Overlay: Can [task] finish in [constraint]?"
  - *Wrong-Then-Right Demo (`FLIP+SCENE`):* 1 s showing the common mistake, hard cut to the right method.
  - *Split-Screen Proof (`PROOF+VS`):* Left: the claim. Right: the primary document, visible from frame 1.
- **Carousel Slide 1:**
  - *Problem Slide 1, Solution Slide 2 (`USE+GAP`):* Pain sharply stated on slide 1; fix starts immediately on slide 2 (no filler intro slide).
  - *Single-Stat Cover (`NUM`):* One big number, one line of context, one visible source line.
  - *Myth vs. Fact Cover (`FLIP`):* Big "MYTH:" on slide 1; verified "FACT:" on slide 2.
- **LinkedIn (First ~140 mobile / ~210 desktop chars):**
  - *See-More Cliff (`GAP+CALL`):* Line 1 states a sharp claim; line 2 breaks cleanly before the fold.
  - *Mistake Confession (`SCENE+STAKES`):* "We used to [specific mistake] for [duration]. Here is what it cost."
  - *Insider Secret (`PROOF+GAP`):* "Something [industry] rarely says out loud: [specific truth]."
- **Headline / Article Title:**
  - *Upworthy Calibrated (`GAP+NUM`):* "[Named subject] + [specific stake] + one withheld mechanism."
  - *Primary Source Beat (`PROOF+FLIP`):* "[Outlet/Official] said [claim]. Page [N] of [document] says [detail]."
- **YouTube Title + Thumbnail:**
  - *Thumbnail-Title Split (`GAP+SCENE`):* Thumbnail shows the object/contrast; title adds the stake without repeating the thumbnail's words or giving away the answer.

---

## 5. Retention Architecture: After the Hook

Getting the tap is half the job; platforms rank on watch time, dwell and satisfaction. Full format playbooks live in [`retention.md`](retention.md).

### The Six Retention Tools
1. **Open loop:** Pose an answerable question early that the body resolves.
2. **Confirm the promise:** Beat 2 immediately proves the opener was honest (never bait-and-switch).
3. **Hype to execution:** Skip "some background first" and show the first receipt immediately.
4. **Re-hook:** Place a sharper reveal, bigger number or twist around the 1/3 to 1/2 mark where attention sags.
5. **Stair-step payoff:** Order multi-item posts from smallest to largest stake so tension climbs.
6. **Abrupt ending:** Stop the moment the payoff lands. Never signal the end ("To wrap up...", "Follow for more").

### Seven Retention Killers
1. Body-hook mismatch.
2. Context dumps before the first receipt.
3. Signaling the end or adding recap fluff.
4. Separate ad/pitch blocks dropped cold (integrate product utility inside the story).
5. Repeating the exact same format back to back.
6. Dull middles where a slide/post adds no new fact.
7. Fake intensity or unverified claims.

---

## 6. Lessons from the Leaked MrBeast Production Guide

*Disclosure & Evidence Tier:* In September 2024, a 36-page internal onboarding PDF titled "How to Succeed in MrBeast Production" circulated online. MrBeast's company has neither confirmed nor denied its authenticity. Treat all insights below as `[anecdotal]` / `[practitioner playbook]`. Even the document warns on page 2: *"This is not a rulebook... I will apply everything I read with a grain of salt."*

Core principles translated for short-form video and text:

- **Optimize for platform retention, not vanity polish (pp. 3, 5, 27-28):** The goal is performance on the platform, measured via CTR, AVD and AVP. Comparing two similar-length videos (120M vs. 45M views), the winner held viewers *"a minute and 38 seconds longer."* For text and short video, optimize for watch time, swipe-through and dwell, not raw likes.
- **Package sets expectations and must be true (pp. 5-6, 14):** Pick ideas for visual/conceptual intrigue (*"I Survived"* beats *"I Spent"*), but never break the package's promise. A mismatch between thumbnail/hook and early content makes viewers feel *"lied to and click off."* Guardrail: make true facts vivid; never exaggerate beyond the record.
- **The opening decides everything (pp. 6-7):** Even a 60M-view video lost 21M viewers in the first minute. Confirm the hook immediately, keep visuals sharp and front-load the strongest beat.
- **Hype to execution & "crazy progression" (p. 7):** *"Stop telling people what they will be watching and start showing them."* Compress early setup so momentum starts on line 2 / second 3.
- **Planned re-engagements (pp. 7-8):** Place major turns where viewers naturally sag (approx. 3 and 6 minutes in long-form; post 3-4 in a thread; slide 3-4 in a carousel; midpoint of a 30s Reel).
- **The "wow factor" (pp. 9-10):** Include something competitors cannot easily replicate: proprietary data, primary documents, live demos or real before/afters.
- **Stair-stepping & abrupt endings (pp. 29, 34-35):** Escalate stakes item by item, rotate formats so audiences never go stale, and *"video endings must always be abrupt to protect retention."*
- **Honesty & filtering (pp. 34-35):** *"We don't fake things."* If an idea feels 50/50, throw it out and write a better one.
- **Integrate brand mentions (pp. 32-33):** Separate pitch blocks create retention craters; weave product mechanics directly into the useful tutorial or story.

---

## 7. Takeaways from `marketingskills` & Open-Source Agent Skills

Synthesized from `coreyhaines31/marketingskills` (62k+ stars, MIT) and sibling MIT skills:
- **Three-channel video hook (`ad-creative/hook-system.md`):** Every video opener has three simultaneous channels: visual motion, spoken line and on-screen caption. Every hook move has a known failure mode (curiosity gaps without payoff poison trust; bold claims need on-screen proof; confessions read fake without lived detail).
- **Diagnostic funnel:** High thumbstop + immediate drop-off means your hook attracted the wrong audience, not that your topic is bad.
- **Fidelity laddering:** Test an angle cheaply (text post or simple screen-on-text clip) before investing heavy production time.
- **One variable per test:** Change only the opener, format or timing in a weekly experiment.
- **Copywriting + Copy-editing split:** Draft first for voice, specificity and awareness fit (`copywriting`), then run a ruthless line-by-line cut for plain English and zero AI tells (`copy-editing`).

---

## 8. Mandatory 12-Item Pre-Post Checklist

Every original post, thread opener, short-video script, carousel cover, LinkedIn post and headline must pass **12/12 on Hard Guardrails (10 to 12)** and at least **7/9 on Attention & Craft (1 to 9)** (standalone file: [`checklist.md`](checklist.md)).

### Attention & Craft (Pass >= 7/9)
1. **First-moment stop:** Line 1 (or 0 to 3 s / Slide 1) opens with a calibrated gap, prediction break or concrete scene. Wrote 5+ hook candidates; cut background throat-clearing.
2. **Moderate concreteness:** Names the real subject and stakes upfront while holding back the *how* or *twist* for line 2.
3. **Rule of One:** One reader, one core idea, one payoff.
4. **Artifact or hard number:** At least one verifiable noun, dollar figure, document/docket number, quote or screenshot.
5. **Group-Chat / Save Test:** Would a real person in your audience bookmark this or DM it to one friend?
6. **Awareness match:** Matches where the reader sits (usually Unaware or Problem-Aware in a feed).
7. **Two-lever video check (video only):** Spoken hook (<=2 s) and on-screen text (<=6 words, <=1 s) written separately, visual motion at 0:00, payoff before halfway.
8. **AI-tell & slop purge:** Zero banned LLM tells or em dashes.
9. **Body holds, ending is abrupt:** Beat 2 confirms the promise; re-hook around 1/3 to 1/2 mark if longer than one screen; stops immediately when payoff lands.

### Hard Guardrails (Must Pass 3/3)
10. **100% payoff & honest framing:** Body fully delivers what the hook promised; zero fake deadlines or hollow question clickbait.
11. **Verified facts & primary sources:** All product numbers, prices, dated counts and news/data claims are verified from primary sources.
12. **Right account, right autonomy:** Matches brand voice, approval rules (draft-only vs. auto-publish) and channel boundaries.

---

## 9. Ethics, Trust Guardrails & Anti-Patterns

### Delete on Sight (AI Tells & Dead Openers)
From `miqdadbadjuber/anti-slop`, `coreyhaines31/marketingskills` (`ai-tells.md`) and `samber/cc-skills`:
1. **"Not X. Y." / "It's not just X, it's Y."** State Y directly with proof.
2. **Throat-clearing:** "In today's fast-paced world...", "Let's dive in", "Here's the thing:", "Buckle up", "Hot take:".
3. **Simulated scenes:** "Have you ever wondered...?", "Picture this:", "Imagine a world where...".
4. **Rhetorical question + self-answer:** "The catch? There isn't one."
5. **Colon reveals:** "The secret: consistency."
6. **Reflexive tricolons:** "Fast, secure, and scalable."
7. **Unattributed percentages:** "90% of teams..." (cite primary source + date, or cut).
8. **Em dashes (`-`).** Zero anywhere. Use periods, colons or commas.
9. **Describing the obvious asset:** "Here is a photo of..."
10. **Engagement bait:** "Like if you agree", "Reply YES", "Comment for the link", "Tag 3 friends." Officially penalized across platforms.
11. **Hollow question headlines & outrage-bait on news:** State the verified tension plainly. Never harass, defame or pass off AI-generated images as real photographs.
12. **Vague teases or spoiler openers:** Never hide what the story is about, and never close the curiosity loop inside the hook itself.
13. **Overpromising:** Winning a tap with a claim the body cannot prove.
14. **Copied content:** Never repost watermarked video or pass off someone else's work as yours; add original analysis and credit the source.

---

## 10. Weekly Learn-and-Adapt Loop

1. **Log metrics daily:** Track platform-native signals that matter (replies, DM sends, bookmarks/saves, 3-second view rate, average watch time, profile clicks) rather than chasing raw likes.
2. **Maintain a weekly swipe file (5 to 10 posts):** Keep 2 to 3 of your own top performers above median plus 3 to 7 standout in-niche posts. Record date, exact hook, format, key metric and one testable hypothesis. Never copy text verbatim; extract the mechanism.
3. **Run one single-variable experiment per week:** Test only one change at a time (opener style, format or posting window) against your recent median, then keep, drop or iterate.

---

## 11. Open-Source Repos & Datasets Index

Metadata verified via GitHub API on Nov 24 to 25, 2026.

### MIT-Licensed Agent Skills & Tools
| Repo | Stars | License | What It Provides |
|---|---:|---|---|
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | 62,498 | MIT | 23 marketing skills: copywriting, copy-editing, social, ad-creative hook system, marketing-psychology, advisor council. |
| [miqdadbadjuber/anti-slop](https://github.com/miqdadbadjuber/anti-slop) | 10,078 | MIT | Structural and lexical AI-slop filter (`antislop-copywriting`). |
| [Jakeschincariol/instagram-agent-skill](https://github.com/Jakeschincariol/instagram-agent-skill) | 9,056 | MIT | Reel hooks (`hooks.json`), regex `hookscore.py`, `ig-carousel`, `ig-viral`, `ig-human`, `slop.json`. |
| [ScrapeCreators/social-media-research-skills](https://github.com/ScrapeCreators/social-media-research-skills) | 7,861 | MIT | Outlier finding and competitor teardowns (requires paid ScrapeCreators API key). |
| [Jakeschincariol/youtube-agent-skill](https://github.com/Jakeschincariol/youtube-agent-skill) | 7,332 | MIT | Opening-15s video hooks, `retention.py`, `title.py`, `yt-shorts`, `yt-package`. |
| [Jakeschincariol/linkedin-agent-skill](https://github.com/Jakeschincariol/linkedin-agent-skill) | 3,956 | MIT | 21 LinkedIn hook formulas with failure modes (`hooks.json`), `li-post`, `li-carousel`. |
| [zubair-trabzada/ai-marketing-claude](https://github.com/zubair-trabzada/ai-marketing-claude) | 2,950 | MIT | 15 Claude marketing skills covering copy and social. |
| [elvisun/newsjack](https://github.com/elvisun/newsjack) | 1,711 | MIT | Journalism headline generator, angle generator and fact-check skills. |
| [blacktwist/social-media-skills](https://github.com/blacktwist/social-media-skills) | 680 | MIT | Thread architecture (listicle, story arc, framework, breakdown, contrarian), carousel and post writers. |
| [Yuzzyuk/marketing-os](https://github.com/Yuzzyuk/marketing-os) | 582 | MIT | 18-tactic hook engine and scored content audits. |
| [bestofmarketing/awesome-marketing](https://github.com/bestofmarketing/awesome-marketing) | 512 | MIT | Curated directory of marketing tools and reading lists. |
| [social-media-skills/skills](https://github.com/social-media-skills/skills) | 411 | MIT | 11 hook mechanisms, 3-channel video rule, 6-dimension 0-2 scoring rubric. |
| [pietervanheijningen/clickbait-remover-for-youtube](https://github.com/pietervanheijningen/clickbait-remover-for-youtube) | 405 | MIT | Reminder that heavy audiences actively filter out clickbait. |
| [bradautomates/head-of-content](https://github.com/bradautomates/head-of-content) | 336 | MIT | Cross-platform outlier content research skills. |
| [samber/cc-skills](https://github.com/samber/cc-skills) | 253 | MIT | 5-lever hook model, calibrated curiosity, 30 formulas, 14 dead openers. |
| [rediumvex/viral-hooks-skill](https://github.com/rediumvex/viral-hooks-skill) | 147 | MIT | 100 categorized fill-in-the-blank hooks across 10 triggers. |
| [alchaincyf/mrbeast-skill](https://github.com/alchaincyf/mrbeast-skill) | 125 | MIT | MrBeast methodology skill (Chinese) with title/retention scripts. |
| [aaaaqwq/agi-super-team](https://github.com/aaaaqwq/agi-super-team) | 121 | MIT | Viral title patterns for YouTube, X threads and LinkedIn. |
| [sergebulaev/youtube-skills](https://github.com/sergebulaev/youtube-skills) | 106 | MIT | Beat-by-beat retention timelines (0:00 to 0:30 long-form, 0 to 3s Shorts), thumbnail principles. |
| [bhargaviparanjape/clickbait](https://github.com/bhargaviparanjape/clickbait) | 72 | MIT | 16,000-headline dataset + classifier (Chakraborty et al. 2016) for negative clickbait calibration. |
| [coleschaffer/dtc-copywriting-skills](https://github.com/coleschaffer/dtc-copywriting-skills) | 31 | MIT | 30+ direct-response skills (`hook-battery`, `copy-rewrite`). |
| [nagisanzenin/idiolect](https://github.com/nagisanzenin/idiolect) | 26 | MIT | Literature-reviewed theory of human prose and corrections to marketing folklore. |
| [krishna-build/marketing-prompts](https://github.com/krishna-build/marketing-prompts) | 21 | MIT | X and LinkedIn hook prompt ideas. |
| [GuilhermeAlbert/awesome-copywriting](https://github.com/GuilhermeAlbert/awesome-copywriting) | 3 | MIT | Structured overview of AIDA, PAS, BAB, 4Ps, Schwartz and Hormozi. |
| [maubinle/sentence_concreteness](https://github.com/maubinle/sentence_concreteness) | 2 | MIT | Python package to score headline concreteness (Aubin Le Quéré & Matias 2025). |
| [mmaguero/clickbait-detector-en](https://github.com/mmaguero/clickbait-detector-en) | 1 | MIT | English tweet clickbait detector trained on Webis-Clickbait-17. |

### Algorithm & Research Reference Repos (Non-MIT)
| Repo | Stars | License | Notes |
|---|---:|---|---|
| [xai-org/x-algorithm](https://github.com/xai-org/x-algorithm) | 34,414 | Apache-2.0 | Live X For You ranking architecture and default action weights. |
| [twitter/the-algorithm](https://github.com/twitter/the-algorithm) | 74,117 | AGPL-3.0 | Historical 2023 X recommendation code (background only). |
| [MKLab-ITI/news-popularity-prediction](https://github.com/MKLab-ITI/news-popularity-prediction) | 33 | Apache-2.0 | Predicts news popularity from comment-tree features. |
| [kaustubh0201/Clickbait-Classification](https://github.com/kaustubh0201/Clickbait-Classification) | 3 | GPL-3.0 | BERT classification of YouTube clickbait titles. |
| [mflorczak/x-algorithm-weights-history](https://github.com/mflorczak/x-algorithm-weights-history) | 0 | CC-BY-4.0 | Tracks mirrored default-weight changes in `xai-org/x-algorithm`. |

### Public Academic Datasets
- **Upworthy Research Archive:** 32,487 headline/image A/B experiments (538M+ assignments): [upworthy.natematias.com](https://upworthy.natematias.com) · [OSF](https://osf.io/jd64p/) · [*Scientific Data* (2021)](https://www.nature.com/articles/s41597-021-00934-7) `[peer-reviewed research]`
- **Webis-Clickbait-17:** Crowd-rated publisher tweets: [webis.de](https://webis.de/data/webis-clickbait-17.html) `[peer-reviewed research]`
- **Jung et al. (2022) Facebook Clickbait Set:** 4,400+ posts from 10 news outlets: [*PLOS ONE* (PMC9242456)](https://pmc.ncbi.nlm.nih.gov/articles/PMC9242456/) `[peer-reviewed research]`
- **Stop Clickbait (Chakraborty et al. 2016):** 16,000 labeled headlines: [bhargaviparanjape/clickbait](https://github.com/bhargaviparanjape/clickbait) `[peer-reviewed research]`
- **YouTube Thumbnails (`l3afai/youtube-thumbnails`):** Thumbnail and title pairs on [Hugging Face](https://huggingface.co/datasets/l3afai/youtube-thumbnails).
