# Human Attention & Virality Psychology

Why real people stop scrolling, read sentence two, finish a video, trust a publication and send something to a friend. Every section separates peer-reviewed science from practitioner playbooks and translates it into concrete rules.

---

## 1. High-arousal emotion drives sharing (valence alone does not)

- **Source:** Jonah Berger & Katherine L. Milkman (2012), "What Makes Online Content Viral?", *Journal of Marketing Research* (`[peer-reviewed research]`, [PDF](https://jonahberger.com/wp-content/uploads/2013/02/ViralityB.pdf)).
- **What it shows:** Studying every *New York Times* article published over three months plus lab experiments, Berger and Milkman found positive content was slightly more viral overall than negative content, but emotional **arousal** mattered more than positive-vs-negative valence. Activating high-arousal emotions (**awe**, **anger**, **anxiety**) significantly increased sharing even after controlling for surprise, interest, utility and placement. Deactivating emotions like **sadness** reduced sharing.
- **Rule:** Write for activating emotions (awe at a concrete data point, sharp frustration at a broken system, urgent curiosity) rather than flat gloom or lukewarm praise.

## 2. STEPPS: the six social-transmission drivers

- **Source:** Jonah Berger (2013), *Contagious: Why Things Catch On* (`[book]`, [overview](https://jonahberger.com/books/contagious/)).
- **What it shows:** People share things for six recurring reasons:
  1. **Social Currency:** Sharing makes the sender look smart, helpful or in-the-know.
  2. **Triggers:** Everyday cues (Monday morning, tax deadline, hiring season) keep an idea top of mind.
  3. **Emotion:** High-arousal feelings push people to act.
  4. **Public:** Visible, copyable artifacts spread faster.
  5. **Practical Value:** Useful checklists, benchmarks, scripts and deadlines get forwarded.
  6. **Stories:** Ideas wrapped inside a real narrative travel without feeling like an ad.
- **Rule:** Ask before posting: *"What social currency or practical value does someone get for sending this to one friend right now?"*

## 3. Curiosity gaps work only at moderate concreteness

- **Sources:** George Loewenstein (1994), "The Psychology of Curiosity", *Psychological Bulletin* (`[peer-reviewed research]`, [PDF](https://www.cmu.edu/dietrich/sds/docs/loewenstein/PsychofCuriosity.pdf)); Marianne Aubin Le Quéré & J. Nathan Matias (2025), "When curiosity gaps backfire: effects of headline concreteness on information selection decisions", *Scientific Reports* (`[peer-reviewed research]`, [PMC11704130](https://pmc.ncbi.nlm.nih.gov/articles/PMC11704130/)).
- **What it shows:** Loewenstein showed curiosity is an uncomfortable awareness of an information gap, and it only fires when you already have enough context to care about what is missing. Aubin Le Quéré & Matias (2025) analyzed **8,977 randomized Upworthy headline experiments** and found a **curvilinear** curve:
  - Too vague ("You won't believe what happened"): adding concreteness *raises* CTR because the reader finally has something to care about.
  - Too concrete (giving away the entire punchline): adding more concreteness *lowers* CTR because nothing is left to discover.
  - Peak CTR sits at **moderate concreteness**: name the real subject and stakes upfront, and hold back only the *how* or the *twist*.
- **Rule:** Ban blind clickbait and ban spoiler openers. Name the specific subject, actor or number in line 1; hold back the mechanism or outcome for line 2.

## 4. Sticky ideas: SUCCESs and the "Curse of Knowledge"

- **Source:** Chip Heath & Dan Heath (2007), *Made to Stick* (`[book]`, [overview](https://heathbrothers.com/books/made-to-stick/)).
- **What it shows:** Sticky ideas share six traits: **Simple** (one core idea), **Unexpected** (breaks a mental model, then fills the gap), **Concrete** (things you can see, count or touch), **Credible** (testable details or authorities), **Emotional** (care about individuals, not abstractions) and **Stories** (mental simulation). Their core warning is the **Curse of Knowledge**: once you know your domain cold, you slip into insider abstractions.
- **Rule:** Cut abstract nouns ("streamline workflows", "empower stakeholders") and replace them with physical details a stranger can picture.

## 5. Moral-emotional language spreads fast inside partisan bubbles

- **Source:** William J. Brady et al. (2017), "Emotion shapes the diffusion of moralized content in social networks", *PNAS* (`[peer-reviewed research]`, [PubMed 28652356](https://pubmed.ncbi.nlm.nih.gov/28652356/)).
- **What it shows:** Analyzing **563,312 tweets** across polarized topics, each **moral-emotional word** (combining moral judgment and emotion, such as *greed*, *betray*, *destroy*) raised expected retweets by ~19 to 20% (IRR = 1.19 in Study 1). Purely moral or purely emotional words had near-zero effect alone. Diffusion was strongly bounded within ideological groups.
- **Rule:** Use moral framing carefully and only on commentary/editorial brands with verified facts. Keep nonpartisan civic data neutral and keep politics off product/SaaS/agency accounts.

## 6. Negativity bias in headlines is real, measurable and small

- **Source:** Claire E. Robertson et al. (2023), "Negativity drives online news consumption", *Nature Human Behaviour* (`[peer-reviewed research]`, [Nature](https://www.nature.com/articles/s41562-023-01538-4), [PubMed 36928780](https://pubmed.ncbi.nlm.nih.gov/36928780/)).
- **What it shows:** Across **22,743 Upworthy RCTs** (~105,000 headline variants, 370M+ impressions, 5.7M clicks), each additional negative word in an average-length (~15-word) headline raised relative CTR by **2.3%**, while each positive word lowered relative CTR by **1.0%**. The effect was strongest for politics and economy stories. Slightly longer, lower-complexity headlines outperformed cryptic ones.
- **Rule:** Treat negativity as a small, honest dial (name the real cost or failure plainly), never permission for doombait. A 2.3% relative lift is never worth losing reader trust. For utility brands, focus on *friction removal*.

## 7. Pattern interrupts and prediction errors earn the stop

- **Sources:** Heath & Heath (2007) `[book]`; `samber/cc-skills` (`[OSS repo]`); Justin Welsh (`[practitioner playbook]`, [justinwelsh.me](https://www.justinwelsh.me/)).
- **What it shows:** Feeds train readers to skip predictable templates ("In today's fast-paced world...", "5 tips to succeed"). Attention spikes on a **prediction break**: a contrarian claim with a receipt, definition reversal, mid-action scene or unexpected number. On short video, frame 1 plus 6-word on-screen text is processed before the spoken line (`Jakeschincariol/instagram-agent-skill`) `[OSS repo]`.
- **Rule:** Start at the turn or surprising fact, never background context. Cut the first sentence of almost every draft and test if sentence two is a sharper opener.

## 8. Open loops and the Zeigarnik nuance

- **Sources:** Zeigarnik (1927) / Ovsiankina (1928) summaries (`[peer-reviewed research]`); `samber/cc-skills` (`[OSS repo]`).
- **What it shows:** Popular marketing overstates the Zeigarnik effect ("unfinished tasks guarantee recall"). Modern reviews show the memory effect is fragile and context-dependent; what holds reliably (closer to Ovsiankina's resumption effect and Loewenstein's gap) is that **an active unresolved loop pulls attention forward while the reader is engaged**, provided they trust it will close honestly.
- **Rule:** Open a clear loop in line 1, close it quickly with real substance in lines 2 to 6 (or before the midpoint of a short video), and never tease a payoff you do not deliver.

## 9. Specificity, odd numbers and concrete artifacts beat generic tips

- **Sources:** `elvisun/newsjack` (`[OSS repo]`); `Jakeschincariol/youtube-agent-skill` (`[OSS repo]`).
- **What it shows:** Generic advice reliably gets ignored on small accounts. Posts that break out carry **artifacts**: named companies, dollar math, verbatim quotes, screenshots, docket numbers, exact counts. Precise figures (*30,573 claims*, *$18,000 mistake*) read as fact, while round unattributed claims (*"90% of people..."*) read as AI fluff.
- **Rule:** Require at least one concrete noun, number, source or artifact in the first two lines. Ban unattributed percentages.

## 10. Social currency and the "Group-Chat Test"

- **Source:** Berger (2013) `[book]`; X open-source ranker (`copy_link` and `DM share` weights).
- **What it shows:** Both human psychology and platform algorithms reward content people pass privately to one specific person to signal identity, help a friend or spark a debate.
- **Rule:** Before publishing, apply the **Group-Chat Test**: *"Would a real person in my target audience screenshot this or DM it to a friend right now?"*

## 11. Match the hook to Eugene Schwartz's 5 Awareness Stages

- **Sources:** Eugene Schwartz (1966), *Breakthrough Advertising* (`[book]`); `coreyhaines31/marketingskills` `awareness-headlines.md` (`[OSS repo]`).
- **What it shows:** Readers bounce when the hook targets the wrong stage:
  1. **Unaware:** Open with a lived moment, identity or surprising truth. Do not pitch the product.
  2. **Problem-Aware:** Name the friction and quantify its real cost.
  3. **Solution-Aware:** Contrast approaches/mechanisms before naming your brand.
  4. **Product-Aware:** Show proof, clear mechanics and answer an objection.
  5. **Most-Aware:** Direct offer, deadline or clear call to action.
- **Rule:** Lead ~80% of top-of-funnel feed posts at **Unaware** or **Problem-Aware**; save **Product-Aware** proof for demos, carousels and replies where someone asked for a tool.

## 12. Narrative & copy frameworks (AIDA, PAS, BAB, Hormozi, Rule of One)

- **Sources:** `coreyhaines31/marketingskills` (`[OSS repo]`); Alex Hormozi, *$100M Leads* (`[book]` / `[practitioner playbook]`, [acquisition.com/leads](https://www.acquisition.com/leads)); Superdirector (`[practitioner playbook]`, [superdirector.app](https://superdirector.app/how-to/write-scroll-stopping-hooks)).
- **What it shows:**
  - **AIDA** (Attention, Interest, Desire, Action) and **4Ps** (Picture, Promise, Prove, Push) structure full posts and landing pages.
  - **PAS** (Problem, Agitate, Solve) and **BAB** (Before, After, Bridge) are the cleanest 3-beat shapes for short posts.
  - **Rule of One:** One reader, one big idea, one promise, one action.
  - **Hormozi's Hook-Retain-Reward:** Earn the stop, hold via open loops and progress, deliver a dense reward. Practitioners often write 8 to 15 opening lines before picking one.

## 13. Ethics & trust guardrails: when curiosity becomes clickbait

- **Sources:** Joshua M. Scacco & Ashley Muddiman (2016), Center for Media Engagement (`[peer-reviewed research]`, [CME](https://mediaengagement.org/research/clickbait-headlines/)); Scacco & Muddiman (2020), *New Media & Society* (`[peer-reviewed research]`, [SAGE](https://journals.sagepub.com/doi/10.1177/1461444819863408)); Chakraborty et al. (2016) (`[peer-reviewed research]`, [repo](https://github.com/bhargaviparanjape/clickbait)).
- **What it shows:** In controlled experiments (N > 2,000), **question-based news headlines** produced more negative attitudes and lower story expectations, while vague **forward-reference headlines** ("This one senator changed everything") failed to beat traditional headlines on anticipated engagement. Deceptive withholding triggers mutes, reports and abandonment.
- **Rule:** The mystery can be in the *how* or *why*, never in *what the story is about*, and the body must pay off 100% of what the hook promised.

---

# Part 2: Deeper Research

## 14. Outrage and clickbait cost trust and engagement on news

- **Muddiman & Scacco (CME, 2019; N = 1,535):** Outrage-laden articles increased perceptions of "fake news," and outrage headlines decreased intended engagement ([CME](https://mediaengagement.org/research/clickbait-content-may-not-be-click-worthy/)) `[peer-reviewed research]`.
- **Jung et al. (2022, *PLOS ONE*):** Across 4,400+ Facebook posts from 10 news sources, clickbait features had mixed effects; clickbait is not a single lever ([PMC9242456](https://pmc.ncbi.nlm.nih.gov/articles/PMC9242456/)) `[peer-reviewed research]`.
- **Robertson et al. (2023), via Nieman Lab:** Sadness words had a stronger positive click coefficient than angry or scary words ([Nieman Lab](https://www.niemanlab.org/2023/03/negative-words-in-news-headlines-generate-more-clicks-but-sad-words-are-more-effective-than-angry-or-scary-ones/)) `[peer-reviewed research]`.
- **Rule:** Make the true cost or loss vivid, not the anger. Never write outrage-bait.

## 15. Curiosity is a reward signal, and it boosts memory

- **Kidd & Hayden (2015, *Neuron*):** Curiosity acts like an intrinsic drive sharing mechanisms with extrinsic reward seeking ([PMC4635443](https://pmc.ncbi.nlm.nih.gov/articles/PMC4635443/)) `[peer-reviewed research]`.
- **Gruber, Gelman & Ranganath (2014, *Neuron*):** High-curiosity answers were recalled at 70.6% vs. 54.1%, and unrelated faces shown during anticipation were also remembered better ([PMC4252494](https://pmc.ncbi.nlm.nih.gov/articles/PMC4252494/)) `[peer-reviewed research]`.
- **Rule:** Place your core mechanism or proof *inside* an honest open loop rather than tacking it onto the end.

## 16. Packaging sets the ceiling: Paddy Galloway

- From [Colin & Samir, "The New Rules of YouTube"](https://www.colinandsamir.com/resources/the-new-rules-of-youtube-from-paddy-galloway) `[practitioner playbook]`:
  - "The difference between a million views and 28 million views is how you package it."
  - Top creators spend ~30% of their time on ideation and packaging vs. ~5% for smaller creators.
  - **Familiar but unexpected:** Pair a recognizable structure with a fresh twist (e.g., "10 minutes vs. 1 hour vs. 24 hours").
  - Steal proven structures across unrelated niches and iterate winners ("Ride it until they stop you").

## 17. Short-form hooks: Jenny Hoyos

- [YouTube Blog Shorts deep dive (Jan 2025)](https://blog.youtube/creator-and-artist-stories/youtube-shorts-deep-dive/) `[official platform guidance]` + `[practitioner playbook]`; [kdcc interview](https://blog.kdcc.social/make-anything-go-viral-how-to-hook-and-reel-in-your-viewer/) `[practitioner playbook]`:
  - "I really do think you have one second to hook someone, especially on Shorts."
  - Formula: "shock, intrigue, and satisfy."
  - Use a familiar setting plus one unexpected change.
  - Phrase open loops as questions rather than statements; record multiple hooks and test them.
  - Never let the title or thumbnail answer the question itself. Add a small B-storyline to sustain curiosity.

## 18. Novelty and reward prediction error

- **Schultz, Dayan & Montague (1997, *Science*):** Dopamine neurons encode reward prediction error, spiking for unexpected rewards and dipping when expected rewards fail to arrive ([PubMed 9054347](https://pubmed.ncbi.nlm.nih.gov/9054347/)) `[peer-reviewed research]`.
- **Bunzeck & Düzel (2006, *Neuron*):** Substantia nigra/VTA responds to absolute stimulus novelty ([PubMed 16880131](https://pubmed.ncbi.nlm.nih.gov/16880131/)) `[peer-reviewed research]`.
- **Rule:** Prediction breaks work, and bait-and-switch creates a negative prediction error that audiences punish.

## 19. Emotions spread through feeds (with a small effect)

- **Kramer, Guillory & Hancock (2014, *PNAS*, N = 689,003):** Altering feed positivity shifted user posting sentiment slightly in the same direction (with an editorial expression of concern regarding consent) ([PubMed 24889601](https://pubmed.ncbi.nlm.nih.gov/24889601/)) `[peer-reviewed research]`.
- **Rule:** Brand tone shapes community mood over time; never run hidden manipulation experiments.

## 20. Why people share: NYT "Psychology of Sharing" (2011)

- Study of 2,500 medium-to-heavy online sharers ([NYT Co. press release](https://investors.nytco.com/news-and-events/press-releases/news-details/2011/The-New-York-Times-Completes-Research-on-Psychology-of-Sharing/default.aspx)) `[industry data]`:
  - 85% say reading others' responses helps them process information; 73% process information more deeply when sharing it.
  - Five motivations: bring valuable/entertaining content to others, define identity, nourish relationships, self-fulfillment, and support causes/brands.

## 21. Attention depth: Chartbeat data

- **Chartbeat via Slate (Manjoo 2013):** 38% of visitors bounced, most scrolled only about halfway, only ~25% reached pixel 1,600, and scroll depth correlated weakly with sharing ([Slate](https://slate.com/technology/2013/06/how-people-read-online-why-you-wont-finish-this-article.html)) `[industry data]`.
- **Rule:** Put the shareable artifact in the top half of every page or post.

## 22. Shareable news without hurting trust: Reuters Institute DNR 2025

- **Reuters Institute Digital News Report 2025** ([summary](https://reutersinstitute.politics.ox.ac.uk/digital-news-report/2025/dnr-executive-summary)) `[industry data]`:
  - Overall news trust sits at 40%; news avoidance hit a record 40%.
  - Social-video news consumption climbed from 52% (2020) to 65% (2025).
  - All generations value brands with a track record for accuracy.
- **Why people avoid news** ([Robertson, Feb 2025](https://reutersinstitute.politics.ox.ac.uk/news/people-are-turning-away-news-heres-why-it-may-be-happening)) `[industry data]`: Negativity, fatigue, overload and political saturation. Pair critical reporting with practical utility and primary links.

## 23. Upworthy beyond headlines

- **Upworthy Research Archive (Matias et al., 2021, *Scientific Data*):** 32,487 experiments, 150,817 arms, 538M+ participant assignments testing full *packages* (headline + image) ([Nature Sci Data](https://www.nature.com/articles/s41597-021-00934-7); [archive](https://upworthy.natematias.com); [OSF](https://osf.io/jd64p/)) `[peer-reviewed research]`.
- **Rule:** Test full packages (words + visual together) and evaluate by retention/satisfaction, not clicks alone.

## 24. Fluency: simple beats smart-sounding

- **Oppenheimer (2006, *Applied Cognitive Psychology*):** Needlessly complex words made authors appear *less* intelligent ([DOI 10.1002/acp.1178](https://onlinelibrary.wiley.com/doi/10.1002/acp.1178)) `[peer-reviewed research]`.
- **Kahneman, *Thinking, Fast and Slow* (2011):** Cognitive ease increases perceived truth and familiarity; honest anchoring sets a clear reference number `[book]`.
- **Rule:** Plain English, short words, one idea per sentence.

## 25. Cialdini's seven principles, applied ethically

- **Reciprocity, Commitment/Consistency, Social Proof, Authority, Liking, Scarcity, Unity** ([Influence at Work](https://www.influenceatwork.com/7-principles-of-persuasion/)) `[book]`.
- **Ethical use:** Give genuine free value first (Reciprocity); cite real dated counts (Social Proof); quote primary documents/experts verbatim (Authority); state only real constraints (Scarcity); use shared-problem framing ("we read the filing so you don't have to", Unity). Never fake countdowns, testimonials or numbers.

## 26. Classic copy and story structures

- **Sugarman:** "The sole purpose of the first sentence in an advertisement is to get you to read the second sentence" (the slippery slide) ([summary](https://larslofgren.com/joseph-sugarman/)) `[book]`.
- **Ogilvy, *Confessions of an Advertising Man* (1963):** 5x as many people read the headline as the body; specific, news-led headlines outperform clever puns `[book]`.
- **Schwartz, *Breakthrough Advertising* (1966):** Copy channels existing desire; "copy is assembled, not written" from the audience's own language `[book]`.
- **Halbert:** Find the "starving crowd" that already wants what you offer `[book]`.
- **Story Spine (Kenn Adams, 1991):** Once upon a time / Every day / One day / Because of that (x3) / Until finally / Ever since then ([NPR](https://www.npr.org/2026/06/23/nx-s1-5750619/meet-the-creator-of-the-story-spine-an-8-sentence-tool-to-create-and-analyze-stories)) `[book]`.
- **ABT (Randy Olson):** "[context] AND [context], BUT [problem], THEREFORE [consequence]" ([ABT Narrative](https://abtnarrative.com/)) `[book]`.

## 27. What the platforms themselves say about retention

- **YouTube Help ([9314415](https://support.google.com/youtube/answer/9314415)):** Intro metric tracks viewers still watching at 30 s; spikes and dips show what to front-load `[official platform guidance]`.
- **YouTube Help Test & Compare ([16391400](https://support.google.com/youtube/answer/16391400)):** Winner is chosen by **watch time share**, not CTR (not available for Shorts) `[official platform guidance]`.
- **YouTube Blog ([Sep 2025](https://blog.youtube/creator-and-artist-stories/master-these-4-metrics/)):** Browse titles create intrigue; search titles answer the query; high CTR + low retention signals an overpromise `[official platform guidance]`.
- **LinkedIn "see more":** Truncates at roughly ~210 characters on desktop and ~140 on mobile (approx. 3 lines; unconfirmed by LinkedIn, measured by third-party tools) `[anecdotal]`.

## 28. Unverified claims (do not cite as fact)

- **"63% of the highest-CTR TikTok ads deliver the key message in the first 3 seconds":** Circulates only in secondary reposts without a verifiable TikTok primary page. Do not cite as verified fact.
- **LinkedIn "external link penalty" multiplier:** LinkedIn has not published a numeric penalty or "put links in the first comment" rule in official Help/Engineering docs. Make posts self-contained so readers do not bounce immediately before dwelling.
- **Instagram Trial Reels official documentation:** Widely discussed in creator interviews (`[anecdotal]`), though official help-doc specs may vary by rollout.
