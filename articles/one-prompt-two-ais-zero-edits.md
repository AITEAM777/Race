# PART 1: THE COMPLETE ENGLISH ARTICLE

# One Prompt, Two AIs, Zero Edits: What Claude and ChatGPT Produce When You Stop Helping Them and Let the Work Speak for Itself

*Draft status: research current as of October 9, 2026. The comparison framework, pricing, model lineups and third-party evidence below are complete. The author's own Zero-Edits test runs are designed and documented here but not yet executed, and no result is reported for them.*

---

## How to read the evidence in this article

Every claim in this piece carries one of five labels, because the difference between "Anthropic says", "a blogger saw" and "we measured" is the whole point of an honest comparison.

| Label | What it means |
|---|---|
| **[DOCUMENTED]** | Stated in official Anthropic or OpenAI material, or in coverage directly quoting it |
| **[THIRD-PARTY]** | A public test or demo by someone else, usually a single run, not replicated by us |
| **[ON X]** | A public post on X found during research; must be opened and checked before embedding |
| **[PLANNED]** | Part of our own Zero-Edits protocol; designed, not yet run, no outcome claimed |
| **[ANALYSIS]** | The author's interpretation or hypothesis, clearly marked as such |

---

## Introduction: Stop Helping

Most AI comparisons are quietly rigged, and not by the companies. They are rigged by us.

We type a prompt, glance at the answer, and then start helping. "Make it shorter." "No, the other kind of chart." "You forgot the mobile layout." Ten turns later we have something good, and we credit the model for a result that was really a collaboration. The model that looks best in those comparisons is often just the one that responds best to coaching.

That is a legitimate thing to measure. It is just not the thing most people actually experience on a busy Tuesday, when they paste one request into a chat box, hope for the best, and either use what comes back or give up.

So this article asks a narrower, harsher question: **what do Claude and ChatGPT produce when you give them one prompt, accept the first answer, and change nothing?** One prompt. Two AIs. Zero edits.

The timing could hardly be better. In the span of five weeks, both companies reshuffled their entire lineups. Anthropic shipped Claude Fable 5.1 on September 1 and Claude Opus 5.5 on September 22, 2026. OpenAI unveiled GPT-6 Astra on September 3, released GPT-6 Sol and GPT-6 Luna on September 22, roughly ninety minutes after Anthropic's announcement according to one tester's timeline, and began rolling GPT-6 into ChatGPT for everyone on October 7. Anyone who formed an opinion about "Claude vs ChatGPT" in the summer is now comparing two products that no longer exist.

What follows is part field guide and part lab notebook. It brings together what the companies officially document, what independent testers have already shown with identical prompts, and a transparent protocol for the head-to-head tests this publication will run next. Where the evidence picks a winner, you will see it. Where it does not, you will see why.

[MEDIA TO ADD: Opening hero graphic. Split-screen of a single prompt box in the center with two output panels, one labeled "Claude", one labeled "ChatGPT", and a small "0 edits" counter beneath each.]

---

## 1. Meet the Contenders

### Claude, October 2026

**[DOCUMENTED]** Anthropic's current lineup, per its developer documentation, has four tiers:

- **Claude Fable 5.1**, described as the model "for demanding reasoning and long-horizon agentic work." It is the slowest and most expensive of the four.
- **Claude Opus 5.5**, "for long-running agentic coding and knowledge work," and the model Anthropic tells developers to start with for most workloads.
- **Claude Sonnet 5.5**, "the best combination of speed and intelligence."
- **Claude Haiku 5.5**, built for high-volume, latency-sensitive tasks such as classification and routing.

All four share a 1-million-token context window, up to 128K tokens of output on the standard API, image input, tool use, and a reliable knowledge cutoff of June 2026. Thinking is "adaptive": the model decides how much to reason, steered by an effort setting, and on Fable 5.1 and Opus 5.5 it is always on.

The headline of the autumn is Opus 5.5. Coverage of the launch consistently reports Anthropic's positioning that it delivers Fable 5.1-level results on most tasks at roughly 40 percent lower running cost than its predecessor, Opus 5. Its API price fell 20 percent, from $5/$25 to $4/$20 per million input/output tokens.

**[THIRD-PARTY]** One detail matters enormously for a zero-edits test: the writing changed. BleepingComputer, citing analysis from the benchmarking platform Arena, reported that Opus 5.5 uses dramatically fewer em dashes than Opus 5 (0.8 per 1,000 words, down from 15.2) and far fewer semicolons, but that its average answer grew longer, from 453 to 481 words. Anthropic itself says the model puts the most important information first and follows the writing rules you give it. If that is true, it should show up in a test where you are not allowed to say "please stop doing that."

On the consumer side, Claude comes with Artifacts (live documents, apps and visualizations inside the chat), Claude Code for software work, Claude Design, Slides and Docs, web search, file creation and code execution, plus Claude in Chrome on paid plans.

### ChatGPT, October 2026

**[DOCUMENTED, via coverage of OpenAI announcements]** OpenAI's lineup reorganized itself around three GPT-6 models:

- **GPT-6 Astra**, announced September 3 and described by OpenAI as "the most intelligent and aligned model in the world." Its rollout was staged, starting with a limited group of organizations in a cybersecurity access program. In ChatGPT it appears as GPT-6 Pro on higher tiers.
- **GPT-6 Sol**, released September 22, the everyday frontier model for paid users, followed on September 29 by **GPT-6.1 Sol**, aimed at coding, computer use and professional work in ChatGPT Work and Codex.
- **GPT-6 Luna**, the lighter, cheaper model that Free and Go users receive.

On October 7, OpenAI began rolling GPT-6 into the main ChatGPT experience: paid tiers got GPT-6 Sol first, with Free and Go users receiving GPT-6 Luna from October 8. The headline feature is **Intelligent UI**, which lets answers include charts, graphics, buttons, forms and small interactive tools generated on the spot. OpenAI's help documentation notes that Intelligent UI is not available with Pro effort, which still runs on GPT-6 Astra, and that the older desktop apps do not support it.

Around those models sits the broadest product surface in consumer AI: ChatGPT Images 2.5 (released September 8 with a sketch-to-image feature), voice, Codex for software work, ChatGPT Work for longer agentic sessions, custom GPTs and a large third-party ecosystem.

**[ANALYSIS]** The two companies have converged on the same shape: a very expensive "thinking" flagship (Fable, Astra), a workhorse frontier model (Opus 5.5, Sol), and a cheap fast tier (Haiku, Luna). That symmetry is what makes a fair fight possible. It also creates the first trap of any comparison: **pitting one company's flagship against the other's workhorse.** A surprising number of viral tests do exactly that.

[MEDIA TO ADD: Infographic "The Two Ladders". Two vertical ladders side by side: Claude (Haiku 5.5, Sonnet 5.5, Opus 5.5, Fable 5.1) and OpenAI (GPT-6 Luna, GPT-6 Sol / 6.1 Sol, GPT-6 Astra), with horizontal dotted lines pairing comparable tiers.]

---

## 2. Where They Actually Differ on Real Work

Benchmarks tell you which model wins on average across thousands of tasks. You do not do thousands of tasks. You do yours. So instead of a leaderboard, here is how the available evidence breaks down by the kind of work people actually bring to these tools.

### Code, games and 3D scenes

This is where the zero-edits question has the most public evidence, because "build me X in a single HTML file" is the internet's favorite AI stress test.

**[THIRD-PARTY]** The most carefully described single test comes from Gekkode, which gave both models the same brief, a fishing boat caught in a night storm rendered in 3D on a single web page. Each model ran alone in an empty folder at its "xhigh" effort setting, Opus 5.5 in Claude Code and GPT-6 Sol in Codex, and neither could see its own scene before handing it over. That is about as close to zero edits as a public test gets. The result was not a knockout:

- Opus 5.5 delivered the scene the author judged most faithful to the brief, but took almost 39 minutes and cost about $6.96 at API rates.
- GPT-6 Sol met all thirteen checkpoints of the brief in about 5 minutes for about $0.29, with a clearer, calmer, less stormy scene.

Read that again: roughly the same checklist compliance, a quality edge for Claude, and a **24x cost gap and 8x speed gap** for OpenAI. The author called it a trade-off, not a win.

Other single-run tests point in a similar direction, with varying emphasis:

- **MindStudio**, building a product landing page, judged Opus 5.5's page stronger, with smoother scroll animation and more convincing product imagery, at about $18.32 versus roughly $5.89 for GPT-6 Sol.
- **Stork**, rebuilding a scene in Blender, called Opus 5.5 the clear winner on polish and detail and reported that GPT-6 Sol's result had disconnected parts and a reversed logo. Opus cost $27.86 and took about an hour; Sol cost $4.50 and took 48 minutes.
- **Moe Lueker**, generating two games from one prompt, found Opus 5.5 built the better game in both rounds, while the cost ranking flipped between rounds.
- **DataCamp**, in a Tetris-clone test, gave GPT-6 Sol the edge on visual polish, a useful reminder that the pattern is a tendency, not a law.

**[ANALYSIS]** Across these tests, a consistent signature emerges. Claude tends to over-deliver: richer environments, more details nobody asked for, longer runs and higher bills. GPT-6 Sol tends to deliver exactly the brief, quickly and cheaply, with less ambition. In a zero-edits world, which one "wins" depends on whether unrequested richness is a gift or a liability for your task.

### Writing

**[THIRD-PARTY]** Tom's Guide ran ChatGPT-6 and Claude Opus 5.5 through the same five everyday prompts. In the rewrite test, which demanded no em dashes, no clichés and a banned-word list, Claude won "by a hair," with the reviewer describing ChatGPT's version as clean and scannable but ultimately the loser on that prompt. The reviewer also described ChatGPT as consistently the less "fluffy" of the two, with answers that sometimes did not go as deep. A secondary write-up reports the overall tally as four to one in Claude's favor; we could not confirm that tally on the Tom's Guide page itself, so treat it as unverified. Note the timing too: at least one source points out that GPT-6 Sol was not yet available in the main ChatGPT chat when that test ran in late September, so "ChatGPT-6" may not match today's default model.

**[ANALYSIS]** Constraint-heavy writing is the ideal zero-edits test, because a single violated rule (one em dash, one banned word) is objectively countable. Anthropic has publicly claimed improved rule-following for Opus 5.5, and OpenAI has claimed clearer communication and slightly shorter answers for GPT-6. Both claims are testable without any judgment calls.

### Research and current events

**[DOCUMENTED]** Both assistants can search the web on every plan, including free tiers. OpenAI claims GPT-6 Instant shows live web search answers 44 percent faster on average than GPT-5.6 Instant. Anthropic documents a June 2026 reliable knowledge cutoff for all current Claude models.

**[ANALYSIS]** Neither company publishes a citation-accuracy number that would let us declare a research winner, and we found no rigorous identical-prompt research test from the past month. This category is genuinely **inconclusive** until it is tested.

### Long documents

**[DOCUMENTED]** All four current Claude models accept up to 1 million tokens of context. Third-party trackers report the GPT-6 API models at about 1.05 million tokens with a surcharge for requests over 272K input tokens; we could not confirm those figures on OpenAI's own pages. Consumer apps may expose less than the API maximum on either side.

**[ANALYSIS]** On paper, both can swallow a book. Whether either can find the one contradictory clause on page 214 without being pointed at it is precisely the kind of question a zero-edits test answers and a spec sheet does not.

### Visuals, images and interactive answers

**[DOCUMENTED]** This is the clearest structural difference. ChatGPT generates images natively (ChatGPT Images 2.5) and, since October 7, can answer with Intelligent UI elements. Claude does not offer native photographic image generation in the way ChatGPT does; it builds visuals as code, through Artifacts, SVG, HTML and its Design and Slides tools.

**[ANALYSIS]** For "make me a poster," ChatGPT plays on home turf. For "make me an interactive dashboard I can keep," the comparison becomes Intelligent UI versus Artifacts, and that matchup is too new for any public test we found.

[MEDIA TO ADD: Side-by-side screen recording showing Claude (Artifacts) and ChatGPT (Intelligent UI) answering the identical prompt "Show me how compound interest changes if I invest $200 a month for 30 years at 4%, 6% and 8%," with no follow-up messages.]

---

## 3. The Zero-Edits Protocol: How We Test

Third-party demos are valuable, but each one uses different prompts, effort settings and tools. To make our own comparison meaningful, every test in this series follows the same rules.

### The rules

1. **One prompt, written in advance.** Prompts are drafted, frozen and published before either model sees them. No rewording after the fact.
2. **Zero edits, zero follow-ups.** The first complete response is the result. We do not reply, regenerate selectively, or fix anything by hand. If a model asks a clarifying question instead of answering, that counts as its answer.
3. **Matched tiers.** Workhorse versus workhorse (Opus 5.5 versus GPT-6 Sol or 6.1 Sol), flagship versus flagship (Fable 5.1 versus GPT-6 Astra / GPT-6 Pro), cheap versus cheap (Haiku 5.5 or Sonnet 5.5 versus GPT-6 Luna). Each matchup is labeled.
4. **Two tracks.** A **consumer track** uses the default chat apps on the $20 plans with default settings, because that is what most readers use. A **builder track** uses the API or the coding agents (Claude Code, Codex) at matched effort, because that is what developers pay for.
5. **Three runs per prompt.** Models are non-deterministic. Each prompt runs three times per model in fresh sessions with memory and custom instructions disabled; we report the median score and show the best and worst outputs.
6. **Blind judging.** Outputs are stripped of model names and styling cues where possible and scored by at least two judges who did not run the prompts.
7. **Everything logged.** Exact prompt, model name as displayed, date, plan, effort level, wall-clock time, and (on the builder track) token cost from the provider's own usage dashboard.

### The planned test battery

**[PLANNED]** None of these has been run yet. Each is described by what it is designed to measure.

| # | Test | What it measures | Why it suits zero edits |
|---|---|---|---|
| 1 | Single-file 3D scene (Three.js) | Brief fidelity, visual ambition, working code on first load | It either runs or it does not |
| 2 | Playable browser game | Game logic, controls, polish, bugs on first play | Bugs are observable without interpretation |
| 3 | Landing page for a fictional product | Design taste, responsiveness, copy quality | Mobile breakage is objective |
| 4 | Constraint-heavy rewrite | Rule-following (banned words, length, no em dashes) | Violations can be counted |
| 5 | 100-page document audit | Long-context recall, finding planted contradictions | Planted errors give a ground truth |
| 6 | Messy CSV to chart and insight | Data cleaning, arithmetic accuracy, visualization | Numbers can be checked |
| 7 | Current-events research brief | Freshness, citation accuracy, hallucinated sources | Every link can be clicked |
| 8 | Visual explainer | Native images (ChatGPT) versus code-built visuals (Claude) | Shows the structural difference honestly |

The exact prompts are published in the production section at the end of this article so anyone can replicate them.

[MEDIA TO ADD: Process diagram "The Zero-Edits Pipeline": Frozen prompt → Fresh session (x3) → First response captured → Anonymized → Blind scoring → Median reported.]

---

## 4. What the Evidence Looks Like

Words about visual output are a poor substitute for seeing it. This section collects the strongest existing visual evidence and marks where our own captures will go.

### Existing third-party demonstrations

**[THIRD-PARTY]** The storm-at-sea test from Gekkode is the best candidate for a featured visual, because its setup is documented: same brief, empty folders, matched "xhigh" effort, no peeking. If the article embeds one external example, it should be this one, captioned with the time and cost figures, so readers see the trade-off rather than just the prettier picture.

**[ON X]** OpenDesign posted a comparison of GPT-6 Sol and Claude Opus 5.5 building an ancient Chinese city in 3D from the same prompt, saying both "nailed the rendering and details, with very different styles," and promising full prompts and a benchmark later. It is a useful illustration of the "different design sensibilities" point, but the promised methodology had not been located at the time of writing.

### Our own captures

[MEDIA TO ADD: Side-by-side video, 60 to 90 seconds, of Claude Opus 5.5 (Claude Code) and GPT-6 Sol (Codex) completing Test 1, the single-file 3D scene, with a visible timer and cost counter, ending on both scenes rendering live.]

[MEDIA TO ADD: Screenshot pair of Test 4, the constraint-heavy rewrite, with every rule violation highlighted in red on each output.]

[MEDIA TO ADD: Screenshot pair of Test 3, the landing page, captured at 390px phone width, since mobile layout is where first-attempt pages most often break.]

[MEDIA TO ADD: Short GIF of each model's Test 2 game being played for 10 seconds, uncut.]

---

## 5. How We Score: An Objective Rubric

"Which one is better?" is not a measurement. This rubric turns it into one. Every output is scored out of 100.

| Criterion | Weight | What judges check |
|---|---|---|
| **Brief fidelity** | 30 | Each requirement in the prompt is listed in advance as a checkbox. Score is the share met. |
| **Correctness** | 25 | Does the code run? Are the numbers right? Are the cited sources real and supporting the claim? |
| **Craft** | 20 | Design quality, writing quality, structure. Scored blind by two judges on a 1 to 5 scale, averaged. |
| **Zero-edit usability** | 15 | Could a reader use this exactly as delivered? 15 = yes, 8 = one small fix needed, 0 = unusable. |
| **Efficiency** | 10 | Time to complete and, on the builder track, dollar cost. Faster/cheaper model gets 10; the other is scaled proportionally. |

Three design decisions are worth defending.

**Fidelity outweighs craft.** A beautiful answer to a different question is a failure in a zero-edits world, because you are not allowed to say "that's not what I asked."

**Efficiency is included but capped.** The third-party evidence above shows cost gaps of up to roughly 24x on a single task. Ignoring that would flatter Claude; letting it dominate would flatter OpenAI. Ten points is a deliberate middle ground, and the raw time and cost are always published alongside so readers can reweight.

**Ties are allowed.** If medians differ by fewer than five points, the test is reported as a tie. Three runs per model is not enough data to make smaller gaps meaningful, and we will not pretend otherwise.

---

## 6. Pricing, Subscriptions and Access

### Consumer plans side by side

| Tier | Claude | ChatGPT |
|---|---|---|
| Free | $0: Sonnet and Haiku, web search, Artifacts, file creation, memory | $0, ad-supported: GPT-6 Luna, limited usage |
| Budget | No equivalent | Go, $8/month (ad-supported in the US): GPT-6 Luna, more usage |
| Standard | Pro, $20/month or $17/month billed annually: Opus, Sonnet, Haiku; Fable via usage credits; Claude Code; Claude in Chrome | Plus, $20/month: GPT-6 Sol in chat; Codex access |
| Power | Max, from $100/month: 5x or 20x Pro usage; Fable at 50% of weekly limits | Pro, $100, $200 or $500/month: GPT-6 Pro (Astra) and higher limits; the $500 tier adds Astra Ultrafast |
| Teams | Team: $25 standard seat, $125 premium seat per month ($20 / $100 annually) | Business: about $25 standard seat per month ($20 annually), with a premium seat reported |
| Enterprise | $20/seat/month annually plus usage at API rates | Custom pricing |

**[DOCUMENTED]** Claude figures come from Anthropic's pricing page. **[THIRD-PARTY]** ChatGPT figures come from multiple October 2026 pricing guides that cite OpenAI's own pages; we could not load OpenAI's pricing page directly during research, and several guides note that the Pro $200 allowance changed for new subscribers in late September. Check openai.com before buying.

### API pricing (per million tokens, input / output)

| Tier | Claude | OpenAI |
|---|---|---|
| Flagship | Fable 5.1: $10 / $50 | GPT-6 Astra: $10 / $50 (reported) |
| Workhorse | Opus 5.5: $4 / $20 | GPT-6 Sol: $2 / $10 (reported); 6.1 Sol: $2 / $10 (reported) |
| Fast | Sonnet 5.5: $2 / $10 | (no separate tier) |
| Cheapest | Haiku 5.5: from $0.10 / $0.50 | GPT-6 Luna: $0.10 / $0.50 (reported) |

**[ANALYSIS]** The flagship and budget tiers are priced identically. The interesting gap is in the middle: GPT-6 Sol costs half as much per token as Opus 5.5, and Sonnet 5.5 matches Sol's price exactly. That makes **Sonnet 5.5 versus GPT-6 Sol** the most commercially relevant matchup nobody seems to be testing, and it is on our list.

Per-token price is also not per-task price. In the Gekkode test, the cost gap was about 24x, far wider than the 2x token-price gap, because Opus worked much longer. Claude's thoroughness is a feature you pay for by the minute.

---

## 7. Which One Should You Use?

These recommendations rest on documented features and the third-party evidence above. They will be revised once our own Zero-Edits results are in.

**If you write for a living.** Start with Claude. Third-party writing tests and Anthropic's documented focus on rule-following and plain style both point the same way, and the Tom's Guide rewrite test went Claude's way, narrowly. Keep ChatGPT for headline brainstorming and anything that needs an image attached.

**If you build software or prototypes.** Use both, deliberately. Evidence suggests Claude (Opus 5.5 in Claude Code) produces richer, more polished first attempts, while GPT-6 Sol in Codex delivers to spec much faster and cheaper. A practical pattern: Sol for quick scaffolds and throwaway prototypes, Opus for the version someone will actually look at.

**If you need images, voice or an all-in-one assistant.** ChatGPT. Native image generation, voice and Intelligent UI make it the broader everyday product, and the $8 Go tier has no Claude equivalent.

**If you work with very long documents.** Either can technically ingest a book-length file. Claude's 1M-token window is officially documented on every current model, which makes it the safer default today, but our Test 5 exists because "can ingest" and "can reliably find" are different claims.

**If you are budget-constrained.** On the free tier, both are capable; ChatGPT Free is ad-supported, Claude Free has tighter usage limits during busy periods. On the API, Luna and Haiku 5.5 are priced identically at the bottom, and Sol and Sonnet 5.5 are priced identically in the middle.

**If you are a power user deciding where to put $100 or more.** Claude Max and ChatGPT Pro both start at $100. Choose based on where your work lives: coding agents and long documents favor Claude Max; multimedia, voice and access to Astra favor ChatGPT Pro.

[MEDIA TO ADD: Decision flowchart "Which AI for which job?" with five entry points (Writing, Coding, Images, Long documents, Budget) leading to Claude, ChatGPT, or "Use both."]

---

## 8. The AI Battle on X

X has become the unofficial arena for one-prompt showdowns. The posts below were found during research. **We were unable to open x.com directly from our research environment, so the descriptions come from search-index text; every post must be opened and checked before it is embedded.** None of them is a controlled experiment.

**OpenDesign: ancient Chinese city in 3D (GPT-6 Sol vs Opus 5.5).** [ON X] Same prompt, both models, very different visual styles. Best placed in Section 4 as an illustration that "better" in 3D often means "different taste." Link: https://x.com/OpenDesignHQ/status/2102700049885245874

**Izzy: launch-video prompt (Opus 5.5 vs "ChatGPT-6 Sol").** [ON X] The poster says Claude's output was clearly better; replies reportedly questioned whether assets were provided. Useful as a cautionary example of how setup details decide the outcome. Best placed in Section 3 next to the protocol rules. Link: https://x.com/israelfemiojo/status/2102642002613481939

**Julian Goldie: "ChatGPT Ultrafast Mode: Is It Worth $500 a Month?"** [ON X, X Article] Reportedly finds Ultrafast much faster but says Opus 5.5 and Sonnet 5.5 produced better-looking builds from the same prompts. Best placed in Section 6 beside the Pro 500 tier. Link: https://x.com/JulianGoldieSEO/article/2106221272376221809

**UxUi Tega: Claude vs ChatGPT vs Figma Make.** [ON X] A design-focused "same prompt, pick your winner" post. Model versions are not stated in the indexed text, so confirm before using. Best placed in Section 2 under visuals. Link: https://x.com/Tegadesigns/status/2091215120475004968

**Chase Dimond: same email prompt to Grok, ChatGPT and Claude.** [ON X] Reported takeaway: ChatGPT most polished and ready to use, Claude most editorial and concept-driven. A good writing-section example; confirm date and model versions. Link: https://x.com/ecomchasedimond/status/2048975571640852989

**[ANALYSIS]** Notice what these posts share. The setup is rarely disclosed in full, model names drift ("ChatGPT-6", "GPT-6 Sol", "Astra"), and almost every one is a single run. They are excellent at revealing personality differences and almost useless for picking a winner. That is exactly the gap a frozen-prompt, three-run, blind-judged protocol is designed to close.

[MEDIA TO ADD: Embedded X post from OpenDesign (after verification), placed directly after the Gekkode storm-scene discussion in Section 4.]

---

## 9. The Scoreboard

### What the evidence currently supports

| Category | Current evidence | Leaning | Confidence |
|---|---|---|---|
| 3D scenes and games, quality | Several single-run third-party tests | Claude (Opus 5.5) | Moderate: consistent direction, small samples, one counterexample |
| 3D scenes and games, speed and cost | Same tests, with logged time and cost | ChatGPT (GPT-6 Sol) | Moderate to high: gaps are large and consistent |
| Constraint-heavy writing | One magazine test, vendor claims | Claude, narrowly | Low: single source, model naming unclear |
| Concise everyday answers | One magazine test | ChatGPT | Low |
| Native image generation | Documented feature difference | ChatGPT | High: Claude does not offer the equivalent |
| Interactive answers | Artifacts vs Intelligent UI, both documented | Inconclusive | Untested head to head |
| Research and citations | No rigorous recent test found | Inconclusive | None |
| Long-document accuracy | Specs only | Inconclusive | None |
| API value per token | Documented and reported prices | ChatGPT in the middle tier; tie at top and bottom | High on price, low on value per task |

### Our Zero-Edits results

| Test | Claude | ChatGPT | Result |
|---|---|---|---|
| 1. 3D scene | Pending | Pending | Not yet run |
| 2. Browser game | Pending | Pending | Not yet run |
| 3. Landing page | Pending | Pending | Not yet run |
| 4. Constrained rewrite | Pending | Pending | Not yet run |
| 5. Document audit | Pending | Pending | Not yet run |
| 6. CSV to insight | Pending | Pending | Not yet run |
| 7. Research brief | Pending | Pending | Not yet run |
| 8. Visual explainer | Pending | Pending | Not yet run |

### Conclusions so far

**[ANALYSIS]** Three conclusions survive the evidence.

First, **the two companies have built different personalities, not just different models.** Claude's current workhorse behaves like a perfectionist contractor: it reads the brief, imagines what you probably wanted, and builds that, at length and at cost. GPT-6 Sol behaves like an efficient one: it ticks every box, ships fast and leaves the extras to you. In a zero-edits world, the perfectionist wins when the brief is underspecified and you wanted ambition, and the efficient one wins when the brief is precise and you wanted it done.

Second, **cost per task, not cost per token, is the number that matters.** A 2x token-price difference became a roughly 24x task-cost difference in the best-documented test, because one model simply worked longer.

Third, **there is no overall winner yet, and anyone claiming one is overreaching.** The strongest public evidence is a handful of single runs with inconsistent model naming. It shows tendencies. It does not settle anything.

---

## 10. What Comes Next

This article is the first edition of a living comparison. Here is the update plan.

**Round 1: The eight Zero-Edits tests.** All eight prompts from Section 3, consumer and builder tracks, three runs each, blind-scored. Results will replace every "Pending" in the scoreboard, with raw outputs published.

**Round 2: The forgotten matchup.** Claude Sonnet 5.5 against GPT-6 Sol. Identical API prices, very different reputations, and almost no head-to-head testing in public.

**Round 3: Interactive answers.** Claude Artifacts against ChatGPT Intelligent UI, using prompts where the ideal answer is a small tool rather than a paragraph.

**Round 4: The flagships.** Claude Fable 5.1 against GPT-6 Astra on the hardest tasks in the battery, with full cost disclosure, since both list at $10 / $50 per million tokens.

**Watch list.** A rumored "Claude Fable 5.5" circulated on X in early October; as of October 5, Anthropic had made no announcement, and its model catalog still lists Fable 5.1 as the newest Fable. OpenAI's GPT-6 rollout to Free and Go users began October 8 and is still settling. Any official release will trigger a re-run of the affected tests.

[MEDIA TO ADD: "Coming next" banner graphic listing Rounds 1 to 4 with a simple progress bar for each.]

---

## Conclusion: Let the Work Speak

The most useful thing a zero-edits test does is take you out of the result. Remove the coaching and the follow-ups, and what remains is each model's default judgment about what you meant. That is the thing you are really choosing when you pick an assistant.

On today's evidence, that judgment differs in a consistent and useful way. **Claude tends to give you more than you asked for.** That makes it the better first draft for writing, design and builds where polish matters and the brief is loose, and the more expensive one when you are paying by the token. **ChatGPT tends to give you exactly what you asked for, quickly,** wrapped in the widest set of tools in the industry: images, voice, interactive answers and an $8 entry tier. That makes it the better everyday generalist and the more economical builder when the spec is tight.

So the honest answer to "which should I use?" is a question back: **when you send one prompt and walk away, do you want ambition or precision?** If you want ambition, start with Claude. If you want precision, breadth and lower cost, start with ChatGPT. If your work spans both, and most serious work does, the $20 you spend on the second subscription is probably the best value in this entire comparison.

And if you want to know which one wins on your kind of task, do what this series is about to do: write the prompt once, run it on both, change nothing, and let the work speak.

*The Zero-Edits results will be published as an update to this article. Prompts are below for anyone who wants to run them first.*

---
---

# PART 2: REFERENCES AND VERIFICATION NOTES

**Research date for all sources: October 9, 2026.**

### Official sources (opened directly)

- Anthropic, Models overview (lineup, API prices, context, cutoffs, retirement dates): https://platform.claude.com/docs/en/about-claude/models/overview
- Anthropic / Claude, Plans and pricing (Free, Pro, Max, Team, Enterprise): https://claude.com/pricing

### Official sources (identified via search, not opened: openai.com, help.openai.com and anthropic.com/news were unreachable from the research environment)

- OpenAI, "GPT-6 and Intelligent UI for everyone": https://openai.com/index/gpt-6-for-everyone/
- OpenAI Help Center, "GPT-6 and other models in ChatGPT": https://help.openai.com/en/articles/20001354-gpt-56-and-gpt-6-pro-in-chatgpt
- OpenAI, ChatGPT release notes: https://help.openai.com/en/articles/6825453-chatgpt-release-notes
- Anthropic, Claude Fable page: https://www.anthropic.com/claude/fable
- Anthropic, Claude Fable 5 and Claude Mythos 5: https://www.anthropic.com/news/claude-fable-5-mythos-5
- Anthropic, Introducing Claude Opus 5: https://www.anthropic.com/news/claude-opus-5

### News coverage

- CNBC, GPT-6 Astra rollout (Sept 3, 2026): https://www.cnbc.com/2026/09/03/open-ai-astra-gpt-6-cyber.html
- Al Jazeera, GPT-6 Astra (Sept 4, 2026): https://www.aljazeera.com/economy/2026/9/4/openai-unveils-gpt-6-astra-amid-rising-scrutiny-and-safety
- gHacks, GPT-6 for all ChatGPT users (Oct 8, 2026): https://www.ghacks.net/2026/10/08/openai-brings-gpt-6-to-all-chatgpt-users-adding-intelligent-ui-with-interactive-answers/
- Engadget, GPT-6 Astra rollout schedule: https://www.engadget.com/2252859/how-to-use-gpt-6-astra-rollout-schedule/
- VentureBeat, Claude Opus 5.5 release: https://venturebeat.com/technology/anthropic-releases-claude-opus-5-5-beating-fable-5-1-on-key-agentic-benchmarks-at-60-cheaper-api-price
- The Decoder, Opus 5.5 and writing style: https://the-decoder.com/claude-opus-5-5-matches-fable-5-1-at-40-percent-lower-cost-as-anthropic-promises-to-fix-claudish-writing/
- DeepLearning.AI The Batch, Opus 5.5: https://www.deeplearning.ai/the-batch/claude-opus-5-5-leaps-forward
- BleepingComputer, Opus 5.5 em-dash and length analysis: https://www.bleepingcomputer.com/news/artificial-intelligence/claude-opus-55-uses-95-percent-fewer-em-dashes-but-its-answers-are-getting-longer/amp/

### Third-party tests cited

- Gekkode, same 3D scene test: https://www.gekkode.com/en/intelligence-artificielle/claude-opus-5-5-vs-gpt-6-sol-3d-test/
- MindStudio, Opus 5.5 vs GPT-6 Sol: https://www.mindstudio.ai/blog/opus-5-5-vs-gpt-6-sol
- Stork, Blender 3D test: https://www.stork.ai/blog/opus-55s-shocking-3d-power
- Moe Lueker, same prompt, two games: https://moelueker.com/blog/claude-opus-5-5-vs-gpt-6-astra
- DataCamp, GPT-6 Sol vs Opus 5.5: https://www.datacamp.com/blog/gpt-6-sol-vs-claude-opus-5-5
- Tom's Guide, five everyday prompts: https://www.tomsguide.com/ai/i-tested-chatgpt-6-vs-claude-opus-5-5-with-5-everyday-prompts-it-wasnt-even-close

### Pricing trackers (ChatGPT plans and OpenAI API)

- Lindy, ChatGPT pricing: https://www.lindy.ai/blog/chatgpt-pricing
- AI Toolbox, ChatGPT pricing October 2026: https://www.ai-toolbox.co/chatgpt-models/chatgpt-pricing
- FinOps LLM, GPT-6 pricing: https://finopsllm.com/research/gpt-6-pricing
- OpenRouter, GPT-6 Astra: https://openrouter.ai/openai/gpt-6-astra

### Evidence gaps and caveats

1. **Third-party test details came through search summaries.** The Gekkode, MindStudio, Stork, Moe Lueker, DataCamp and Tom's Guide pages could not be opened directly; figures were taken from search-index extracts. Before publication, open each page and confirm the times, costs and verdicts quoted.
2. **OpenAI figures are secondary.** ChatGPT plan prices, GPT-6 API prices and context windows come from trackers and news coverage that cite OpenAI, not from OpenAI's pages directly. The GPT-6.1 Sol cached-input price differs between sources.
3. **Model naming is inconsistent in the wild.** "ChatGPT-6", "GPT-6", "GPT-6 Sol" and "GPT-6 Pro/Astra" are used loosely. Each test cited may have used a different variant.
4. **Benchmarks were deliberately not used to declare winners.** Reported figures such as an 89.9% SWE-bench Pro score for Opus 5.5 and an Artificial Analysis index of 58 vs 48 (Opus 5.5 vs GPT-6 Sol) are vendor-reported or aggregator-reported and were not verified against primary sources, so they were left out of the article body.
5. **The Tom's Guide 4-to-1 tally** is from a secondary write-up and is not confirmed.
6. **X posts were not opened.** x.com was unreachable; post text comes from search snippets. All five must be checked for existence, date, wording and model versions before embedding.
7. **No original experiments have been run.** All Zero-Edits results are pending; nothing in the article claims otherwise.

---
---

# PART 3: VISUAL AND VIDEO PRODUCTION PLAN

*(Інструкції для вас написані українською. Усі промпти для генерації та тестів залишені англійською, щоб їх можна було копіювати без змін.)*

## 3.1 Зображення для кожного розділу

| Розділ | Що потрібно | Де розмістити |
|---|---|---|
| Вступ | Hero-графіка «один промпт, дві відповіді» | Одразу під заголовком, перед вступом |
| 1. Учасники | Інфографіка «Дві драбини моделей» | Наприкінці розділу 1 |
| 2. Реальні задачі | Відео Artifacts vs Intelligent UI | Наприкінці підрозділу «Visuals, images and interactive answers» |
| 3. Методологія | Схема «Zero-Edits Pipeline» | Після таблиці тестів |
| 4. Докази | Відео тесту 1, скріншоти тестів 3 і 4, GIF тесту 2 | На місцях маркерів [MEDIA TO ADD] |
| 5. Оцінювання | Візуальна картка рубрики (5 критеріїв і ваги) | Замість або поруч із таблицею рубрики |
| 6. Ціни | Графіка порівняння тарифів | Над таблицею тарифів |
| 7. Рекомендації | Блок-схема «Який AI для якої задачі» | Наприкінці розділу 7 |
| 8. X | Вбудовані пости після перевірки | Як описано в розділі 8 |
| 10. Далі | Банер «Coming next» | Наприкінці розділу 10 |

## 3.2 Готові промпти для генерації зображень (англійською)

**Hero image:**
> Editorial tech illustration, a single glowing prompt input box at the center of a dark charcoal background, two thin light beams splitting from it to the left and right, each ending in a floating translucent screen showing abstract code and layout blocks. Left screen tinted warm terracotta, right screen tinted cool teal. Small minimalist counter under each screen reading "0 edits". Clean, premium, magazine cover style, no logos, no brand marks, no text other than "0 edits", 16:9.

**"The Two Ladders" infographic:**
> Minimal flat infographic on an off-white background, two vertical ladders side by side. Left ladder labeled "Claude" with rungs from bottom to top: "Haiku 5.5", "Sonnet 5.5", "Opus 5.5", "Fable 5.1". Right ladder labeled "OpenAI" with rungs: "GPT-6 Luna", "GPT-6 Sol", "GPT-6 Astra". Dotted horizontal lines connect Haiku 5.5 to GPT-6 Luna, Opus 5.5 to GPT-6 Sol, Fable 5.1 to GPT-6 Astra. Sans-serif typography, muted colors, no logos, 4:5.

**Zero-Edits Pipeline diagram:**
> Clean horizontal flow diagram with six rounded boxes connected by arrows: "Frozen prompt", "Fresh session x3", "First response captured", "Anonymized", "Blind scoring", "Median reported". Monochrome navy on white with one accent color, generous spacing, editorial style, 16:9.

**Scoring rubric card:**
> Minimal data card showing five horizontal bars proportional to weights: "Brief fidelity 30", "Correctness 25", "Craft 20", "Zero-edit usability 15", "Efficiency 10". Off-white background, single accent color, sans-serif, editorial magazine style, 1:1.

**Decision flowchart:**
> Simple decision flowchart, five starting boxes on the left: "Writing", "Coding", "Images", "Long documents", "Budget". Arrows lead to three endpoint boxes on the right: "Start with Claude", "Start with ChatGPT", "Use both". Flat vector style, clean lines, neutral palette, no logos, 16:9.

**"Coming next" banner:**
> Wide editorial banner with four stacked rows labeled "Round 1: Zero-Edits battery", "Round 2: Sonnet 5.5 vs GPT-6 Sol", "Round 3: Artifacts vs Intelligent UI", "Round 4: Fable 5.1 vs GPT-6 Astra", each with an empty thin progress bar. Dark background, light text, minimal, 3:1.

## 3.3 Рекомендовані відео

1. **Головне відео (тест 1, 3D-сцена).** Запишіть екран обох агентів одночасно (Claude Code з Opus 5.5 та Codex з GPT-6 Sol або 6.1 Sol), з видимим таймером. Змонтуйте 60 до 90 секунд: старт, прискорене виконання, фінальний рендер обох сцен. Вкажіть у титрах час і вартість з дашбордів провайдерів.
2. **Artifacts vs Intelligent UI.** Запис чату в браузері, один промпт про складні відсотки, без жодних уточнень.
3. **GIF гри (тест 2).** 10 секунд реальної гри в кожну версію, без монтажу.

## 3.4 Ідентичні промпти для експериментів (англійською, копіювати без змін)

Правила: нова сесія, пам'ять і custom instructions вимкнені, одна відповідь, жодних уточнень, три прогони на модель.

**Test 1: 3D scene**
> Create a single self-contained HTML file that renders a 3D scene of a small fishing boat caught in a storm at night using Three.js loaded from a CDN. Requirements: animated waves that move the boat realistically; rain; periodic lightning that briefly lights the whole scene; a lighthouse on a distant cliff with a rotating beam; the camera can be orbited with the mouse; it must run at a smooth frame rate on a mid-range laptop and work on mobile. Output only the complete HTML file.

**Test 2: Browser game**
> Create a complete, playable browser game in a single HTML file with no external assets. The game: the player steers a paper boat down a river, avoiding rocks and collecting floating lanterns. Requirements: keyboard and touch controls; increasing difficulty over time; score and best score saved in localStorage; a start screen, a game-over screen and a restart button; sound effects generated with the Web Audio API. Output only the complete HTML file.

**Test 3: Landing page**
> Build a single-file, responsive HTML landing page for "Driftwood", a fictional subscription service that delivers one handmade ceramic mug per month. Include: a hero section with a headline and call-to-action, three benefit blocks, a three-tier pricing table ($19, $29, $49 per month), five FAQ items in an accordion, and a footer. The page must look polished at 390px and 1440px widths. Use no images; create all visuals with CSS or inline SVG. Output only the complete HTML file.

**Test 4: Constrained rewrite**
> Rewrite the announcement below for a company newsletter. Rules: between 120 and 150 words; no em dashes; no exclamation marks; do not use any of these words: "excited", "thrilled", "leverage", "journey", "game-changer", "innovative", "seamless"; keep every fact; end with one sentence telling employees exactly what to do next.
> Announcement: "Starting November 3, the office in Building B will be closed for renovation for six weeks. All Building B teams will move temporarily to the fourth floor of Building A. Desk booking for the fourth floor opens on October 27 through the internal portal. Parking permits remain valid. Questions go to facilities@company.example."

**Test 5: Document audit**
> *(Підготуйте самостійно: 100-сторінковий PDF, наприклад договір або звіт, у який ви вручну вставили 5 суперечностей, записані окремо як еталон.)*
> Read the attached document in full. List every internal contradiction you find, where two statements in the document cannot both be true. For each, quote both statements exactly and give their page numbers. Do not list anything that is merely unclear. If you find none, say so.

**Test 6: CSV to insight**
> *(Підготуйте самостійно: CSV на ~2 000 рядків продажів з навмисними проблемами: дублікати, порожні клітинки, різні формати дат. Еталонні відповіді порахуйте заздалегідь.)*
> The attached CSV contains raw sales records. Clean the data, explaining every cleaning step. Then report: total revenue by month, the top five products by revenue, and the single most important trend a store manager should know. Include one chart. State any assumptions you made.

**Test 7: Research brief**
> Write a 400-word briefing on the most significant AI model releases from OpenAI and Anthropic between September 1 and October 9, 2026. Every factual claim must have a linked source. Prefer official company pages. Do not include anything you cannot source.

**Test 8: Visual explainer**
> Create a visual that explains to a 12-year-old how a solar panel turns sunlight into electricity. It should be understandable without any additional text from me, accurate, and suitable for printing on a single A4 page.

## 3.5 X-пости для вставки (обов'язково перевірте вручну)

Я не зміг відкрити x.com із дослідницького середовища, тому всі описи взяті з пошукових фрагментів. Перед публікацією відкрийте кожне посилання і перевірте: чи пост існує, дату, точний текст, які саме моделі використано.

1. OpenDesign, 3D-місто (GPT-6 Sol vs Opus 5.5): https://x.com/OpenDesignHQ/status/2102700049885245874 → розділ 4, після обговорення тесту Gekkode.
2. Izzy, промпт для відео запуску: https://x.com/israelfemiojo/status/2102642002613481939 → розділ 3, поруч із правилами протоколу як приклад впливу налаштувань.
3. Julian Goldie, X Article про Ultrafast за $500: https://x.com/JulianGoldieSEO/article/2106221272376221809 → розділ 6, біля тарифу Pro $500.
4. UxUi Tega, Claude vs ChatGPT vs Figma Make: https://x.com/Tegadesigns/status/2091215120475004968 → розділ 2, підрозділ про візуал.
5. Chase Dimond, однаковий email-промпт: https://x.com/ecomchasedimond/status/2048975571640852989 → розділ 2, підрозділ «Writing».

## 3.6 Чого не вистачає: що маєте надати ви

1. Результати всіх 8 тестів (3 прогони × 2 моделі × 2 треки), включно з точною назвою моделі, як її показує інтерфейс, датою, тарифом, рівнем effort, часом і вартістю.
2. Скріншоти дашбордів витрат (Anthropic Console / Claude Code і OpenAI usage), щоб цифри вартості були підтвердженими.
3. Скріншоти тестів 3 (ширина 390px і 1440px) і 4 (з підсвіченими порушеннями правил).
4. Запис екрана тесту 1 та GIF тесту 2.
5. Еталонні файли для тестів 5 і 6 (PDF із суперечностями та CSV з відомими правильними відповідями).
6. Імена двох незалежних суддів для сліпого оцінювання та їхні таблиці балів.
7. Примітка: у цьому репозиторії вже є `index.html` з 3D-гоночним симулятором на Three.js. Якщо це результат однієї з моделей з одного промпта, збережіть точний промпт, модель і дату, і він може стати додатковим прикладом для розділу 4. Без цих даних не використовуйте його як доказ.

## 3.7 Куди саме вставляти кожен медіа-актив

Кожен маркер `[MEDIA TO ADD: ...]` у статті стоїть саме там, де має бути відповідний матеріал. Замініть маркер на зображення, відео або вбудований пост, а підпис до медіа беріть з тексту маркера. Після запуску тестів замініть усі «Pending» у таблиці розділу 9 і оновіть висновки в розділах 7, 9 та Conclusion лише на основі отриманих даних.

---
---

# PART 4: PROMOTIONAL CONTENT FOR X

**Main promotional post:**

> Every "Claude vs ChatGPT" test you've seen has a hidden third player: the human fixing the output.
>
> So we removed them.
>
> One prompt. Two AIs. Zero edits.
>
> What the evidence already shows: one model over-delivers, the other delivers exactly the brief, and in the best-documented 3D test, the cost gap was about 24x.
>
> Full breakdown, pricing, every source, and the 8 frozen prompts you can run yourself 👇

**Alternative hook (short):**

> Claude gives you more than you asked for. ChatGPT gives you exactly what you asked for, faster and cheaper. Which one you want depends on one question. One prompt, two AIs, zero edits 👇
