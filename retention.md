# Retention: What Happens After the Hook

The hook gets you a stop. The body has to earn every next second, scroll or swipe. This guide covers body structure: open loops, re-hooks, payoff pacing and abrupt endings across formats. Sources are tagged `[peer-reviewed research]`, `[official platform guidance]`, `[industry data]`, `[book]`, `[practitioner playbook]`, `[OSS repo]` or `[anecdotal]`.

## 1. Why the body matters more than people think

- **Platforms rank on retention.**
  - YouTube's Test & Compare picks the winning title/thumbnail by **watch time share, not CTR** ([YouTube Help 16391400](https://support.google.com/youtube/answer/16391400)) `[official platform guidance]`.
  - YouTube calls a package that gets clicks but loses viewers a broken promise: "high CTR with low retention means the thumbnail promises something the video doesn't deliver" ([YouTube Blog, Sep 3 2025](https://blog.youtube/creator-and-artist-stories/master-these-4-metrics/)) `[official platform guidance]`.
  - X's open-sourced ranker (`xai-org/x-algorithm`) weights replies, dwell, quotes, DM shares and copy-link shares far above likes.
- **Retention multiplies views.** In the leaked 2024 MrBeast production guide (unconfirmed by his company), two videos of nearly the same length got 120M and 45M views; the difference was 1 minute 38 seconds of extra average watch time (pp. 27-28) `[anecdotal]`.
- **Readers rarely finish, and finishing is not why they share.** Chartbeat data reported by Slate:
  - 38% of visitors bounced without engaging.
  - Most scrolled only about halfway.
  - Scroll depth had only a very weak relationship with sharing ([Slate / Chartbeat, Manjoo 2013](https://slate.com/technology/2013/06/how-people-read-online-why-you-wont-finish-this-article.html)) `[industry data]`.
  - **Rule:** Put the shareable fact high, and treat everything below it as a reward for the most engaged readers.
- **Curiosity improves memory for what comes next.** In Gruber et al. (2014), participants recalled high-curiosity trivia answers better (70.6% vs. 54.1%) and even remembered unrelated faces shown during the anticipation window better ([Neuron, PMC4252494](https://pmc.ncbi.nlm.nih.gov/articles/PMC4252494/)) `[peer-reviewed research]`. An honest open loop holds attention and improves recall of the content inside it.

## 2. The six retention tools

| Tool | What it is | Source |
|---|---|---|
| **Open loop** | A question the body promises to answer later. Phrase it as a question, not a statement ("Can we fix this in 10 minutes?"). | Jenny Hoyos ([kdcc](https://blog.kdcc.social/make-anything-go-viral-how-to-hook-and-reel-in-your-viewer/)) `[practitioner playbook]`; Loewenstein 1994 `[peer-reviewed research]` |
| **Confirm the promise** | The first beat after the hook proves the reader or viewer is in the right place. On YouTube, the intro metric tracks the % still watching at 30 s. | [YouTube Help 9314415](https://support.google.com/youtube/answer/9314415) `[official platform guidance]`; MrBeast guide pp. 5-7 `[anecdotal]` |
| **Hype to execution** | Stop telling and start showing: put the first receipt right after the hook and compress early setup ("crazy progression"). | MrBeast guide p. 7 `[anecdotal]` |
| **Re-hook** | A new, bigger reveal at the exact point where attention sags (roughly 1/3 to 1/2 through, or at 3 and 6 minutes in longer video). | MrBeast guide pp. 7-8 `[anecdotal]`; `sergebulaev/youtube-skills` retention-beats `[OSS repo]` |
| **Stair-step payoff** | Escalate stakes item by item, putting the biggest item last ($1 -> $10 -> ... -> record). | MrBeast guide p. 29 `[anecdotal]` |
| **Abrupt ending** | Stop the moment the payoff lands. Never signal the end ("to wrap up") except to build hype for the payoff itself. | MrBeast guide pp. 8, 29, 35 `[anecdotal]` |

Supporting narrative tools:
- **B-storyline:** A small secondary thread running under the main arc (e.g., a personal constraint or side-bet), giving viewers a second reason to stay (Jenny Hoyos, kdcc) `[practitioner playbook]`.
- **Pattern interrupt:** A cut, location change or on-screen callout at a section break (`sergebulaev/youtube-skills` retention-beats) `[OSS repo]`.
- **The slippery slide:** Every sentence exists solely to get the next sentence read. Use a short first sentence, short paragraphs and "seeds of curiosity" at paragraph ends (Joseph Sugarman, *Adweek Copywriting Handbook*) `[book]`.
- **And, But, Therefore (ABT):** Replace "and, and, and" lists with tension ("but") and consequence ("therefore") (Randy Olson, *Houston, We Have a Narrative*, 2015) `[book]`.
- **Story Spine:** "Once upon a time... Every day... One day... Because of that... Because of that... Until finally... Ever since then..." (Kenn Adams, 1991) `[book]`.

## 3. Format playbooks

### X single post (one screen)
1. **Line 1:** The hook (from `hooks.md`).
2. **Line 2:** The payoff of line 1 or the first receipt. Never more setup.
3. **Lines 3 to 5:** One fact per line, escalating slightly (stair-step).
4. **Last line:** The single most surprising true detail, a genuine question you want answered, or the source link (in a reply if needed). Stop there.

### X thread
| Post | Job |
|---|---|
| **1** | Claim, exact count of items coming, and the order (ranked or escalating). |
| **2** | First receipt immediately. Zero context dump. |
| **3 to 4** | **Re-hook:** the item that makes readers stop scrolling again (a bigger number, a twist or "the one we didn't expect"). |
| **Middle** | One idea per post. Each post should still work if screenshotted alone (screenshots travel). |
| **Second to last** | The biggest stake (stair-step). |
| **Last** | The payoff plus one action (a link or a real question). No recap, no "follow for more." |

Source: `blacktwist/social-media-skills` thread-writer (5 thread formats: listicle, story arc, framework, breakdown, contrarian) `[OSS repo]`; MrBeast guide pp. 7-8, 29, 35 `[anecdotal]`.

### Carousel (Instagram / LinkedIn)
- Slide 1 is the hook and must stand alone. Slide 2 starts delivering immediately with no intro slide.
- Put a re-hook on slide 3 or 4 ("this next one is the part most people miss").
- One idea per slide, big type readable on a phone.
- Second-to-last slide is the strongest item. Last slide is the receipt or source plus one clear action.
- The count on slide 1 must match what you actually deliver.

Source: `Jakeschincariol/instagram-agent-skill` ig-carousel `[OSS repo]`; `coreyhaines31/marketingskills` carousel-frameworks `[OSS repo]`.

### Reel / TikTok / YouTube Short (15 to 60 s)
| Time | Beat |
|---|---|
| **0 to 1 s** | Frame-one hook: motion or the receipt, with an on-screen line (<=6 words) readable with sound off. |
| **1 to 3 s** | Confirm the stakes: one spoken line (<=2 s) that makes the viewer need the resolution. |
| **3 to 10 s** | Hype to execution: show the thing. |
| **Midpoint** | Re-hook: a new number, twist or visual cut that resets attention. |
| **Last 2 to 3 s** | Payoff, then cut immediately. Ideally the last line flows back into the first so it loops seamlessly. |

Source: `sergebulaev/youtube-skills` retention-beats `[OSS repo]`; `coreyhaines31/marketingskills` hook-system (visual + spoken + caption) `[OSS repo]`; Jenny Hoyos (record two hooks, trial them) `[practitioner playbook]`. Note: YouTube Test & Compare is not available for Shorts ([YouTube Help 16391400](https://support.google.com/youtube/answer/16391400)).

### Long-form YouTube (first 30 s)
`0:00 to 0:03` cold line or peak clip -> by `0:10` restate the title's promise -> by `0:18` open a loop or raise the stakes -> by `0:28` a "by the end you'll..." contract -> hard cut into the body. Re-hook at each section break (`sergebulaev/youtube-skills`). In the back half, viewers are in a "lull," which is where longer explanations can live (MrBeast guide p. 8).

### LinkedIn post
- The first two lines live above "see more" (roughly ~210 characters on desktop, ~140 on mobile, `[anecdotal]`). Line 2 should end on an open beat.
- After the fold, use short paragraphs, one idea each, and a turn roughly two-thirds of the way down ("Then we checked the numbers.").
- End on the lesson or one specific question. No hashtag wall.

Source: `Jakeschincariol/linkedin-agent-skill` li-post `[OSS repo]`.

### News articles and data explainers
- **Top 50% of the page:** Headline, dek with the key fact, first paragraph with the primary-source receipt, and the shareable number. Most readers never scroll further (Chartbeat).
- **Below that:** Context, the strongest opposing argument, methodology and primary links. This is where long-term trust is earned (Reuters Institute DNR 2025: all generations favor brands with a track record for accuracy) `[industry data]`.
- **News avoidance is at a record 40% (DNR 2025).** Drivers include negativity, overload and political fatigue ([Reuters Institute 2025](https://reutersinstitute.politics.ox.ac.uk/digital-news-report/2025/dnr-executive-summary)). Pair critical reporting with practical "what it means for you" clarity rather than pure outrage.

## 4. Seven retention killers

1. **Body-hook mismatch** (winning a tap with a promise the body fails to deliver). Fastest way to lose viewers and trigger negative platform signals.
2. **Setup before the receipt** ("Before we get into it, some context...").
3. **Signaling the end** ("To wrap up...", "In conclusion...").
4. **Separate sponsor/pitch blocks** dropped awkwardly in the middle instead of integrating the product naturally into the useful story.
5. **Running the exact same format back to back** (triggers viewer fatigue and author-diversity decay).
6. **Dull middles:** every post, slide or beat must add a new fact or turn the story.
7. **Fake intensity or fabricated facts:** destroys audience trust permanently.

## 5. Quick retention check

- [ ] Does the first beat after the hook confirm the promise?
- [ ] Is there a re-hook around the one-third to one-half mark?
- [ ] Do the items escalate, with the biggest stake last?
- [ ] Does it end the moment the payoff lands, without a recap or "follow for more"?
