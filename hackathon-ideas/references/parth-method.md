# Parth Mittal's Method - Full Breakdown

Source article: "How to find hackathon winning ideas", Parth Mittal (@mittalparth_), 19 Aug 2026.
https://x.com/mittalparth_/status/2090033629422604523
Author: MTS at Oracle, 35+ hackathons, 15 wins, incl. Anthropic, Google DeepMind, Sarvam AI, ETHIndia.

Framing from the article: finding the idea is the hardest part now that building is easy. The method helps find ideas in general, not just to win. Hackathons are about hacking something cool, learning under constraint, and having fun.

---

## Rule 1 - Don't ask AI
- Don't ask an AI assistant for ideas first. Everyone else does the same and gets the same generic results.
- But AI output is a good proxy for **what not to build**, because everyone else will build it.
- AI is fine for **expanding** an idea you already have and for **asking pointed questions** to check feasibility.

**How the skill uses it:** Step 1 writes the default AI ideas and bans them. Step 6 uses AI only to sharpen.

## Rule 2 - Gather inspiration casually, over time
- Treat X and Reddit as places to see interesting ideas before they go mainstream. Tune your feed to show new ideas, launches, and demos early.
- Don't copy. See, appreciate, bookmark, without thinking about building it. Mix fields: design, tech, art.
- Over time you build a muscle to spot good ideas and build something **tangential**.
- The winning mix: **a very recent idea + a forgotten one**, or **what was not possible before + a nostalgic twist**.
- Don't stress about the problem at hand; the links form on their own.

**Worked example - Claude City** (2nd place, $3000, Anthropic x Elevation Capital "Push to Prod", 8 Aug 2026, 5 hours):
- Spark A (Apr 2026): Flipbook by @zan2434. Every pixel on screen streamed live from a model, no HTML or layout engine. https://x.com/zan2434/status/2046982383430496444
- Spark B (Aug 2026): sf.isopolis.city by @nuwandavek. SimCity meets Ghibli pixel-art map of SF, built with a "ragtag team of coding agents". https://x.com/nuwandavek/status/2084069099412611156 · build blog https://sf.isopolis.city/dev.html
- Result: your repo becomes an isometric city. Files are buildings, you choose your crew (model), you watch agents construct buildings in real time, open PRs are ships you sail to a new island to review. Built on the Claude Agent SDK. Insight: engineering is shifting to managing many agents, not reading diffs. https://x.com/mittalparth_/status/2086438075652067553
- Why it clicked: the two sparks came from different times; models had just become good enough to build it in 4 hours; Claude was the heart of it.

## Rule 3 - The organiser's tech has to be the hero
- Companies run hackathons to see their new tech shine brightest. Best product or best architecture loses if the sponsor's product isn't the heart and soul.
- **Test: "Could I build my project without this?"** If yes, you're building the wrong thing.
- Simple but pushes the tech's limit, or shows something totally different = higher chance.
- Balance: forcing the tech, or stacking multiple sponsors to raise odds without adding value, is a red flag. **Simple is beautiful.**

**Worked example - Kahani** (1st place, $5000, Google DeepMind x Cerebral Valley, Bangalore, Jul 2026):
- Goal: push the limit of Nano Banana (new, fast, cheap image model). Games are a good way to push creative limits.
- An RPG generator: worlds and assets generated as you play, rooted in Indian culture (e.g. a world from the film Lagaan). Assets, dialogue, and clues change with the theme. Every asset generated on the fly, so the UI/UX depends on the model's quality and speed.
- https://x.com/mittalparth_/status/2076292927882682602 · https://playkahani.vercel.app/

## Rule 4 - It must be demo-able
- You get 3 minutes at best; judges are overwhelmed, so assume 1 minute.
- The idea must catch attention and be explainable in **one line**. If explaining the problem takes **over 30 seconds, drop it**. If the use case isn't visible, drop it. It must be showcase-worthy.

Not-so-good:
- **Aaroh** (PL_Genesis hackathon): agentic commerce. Agents find merchants via Google's UCP, shop, pay with crypto via x402, carry a trustless identity (ERC-8004). A mouthful; explaining the problem ate the time before the demo. https://x.com/ahmedfahim21_/status/2041754118923174265
- **Medha** (Lightspeed Warpspeed Agentic AI hackathon; did win Base track runner-up): a proactive, ambient Siri connected to Calendar, Gmail, Drive, with Sarvam audio. At the edge, but hard to demo. How do you show "proactive" in seconds? You have to live with it over time. https://devfolio.co/projects/aeva-58d2

Good:
- Claude City and Kahani (above).
- **ComicifyAI** (2023, Devfolio Warpspeed GenAI hackathon: 1st runner-up overall by Lightspeed of 107 hackers, top 3 on Replit, AWS runner-up): text to comics, when image models were still bad at text. Simple, easy to show, at the slight edge. https://x.com/mittalparth_/status/1658866506455977984

## Rule 5 - Be early
- Projects change with technical progress, with what's already been done, and with what's being looked for.
- A limitation a month ago can be mainstream now. Spot things before most of the world has.

**Worked example - Sarvam voice game** (Sarvam x GrowthX Epoch Buildathon, Jul 2026, 8 hours, 200 builders; judged on Technical Depth, Creativity, Impact, Delight; didn't make top 15):
- Spark: @mattshumer_'s "Claude of Duty", a game one-shotted by Claude Opus 5 with zero external assets, trending that week. https://x.com/mattshumer_/status/2081054356405731740
- Twist: same energy, Indian context, built around Sarvam's stack. A voice-first 3D game where you learn an Indic language through everyday conversations. Insight: most people don't need to master a language, just a few useful sentences. Pick a region (e.g. Bengaluru) and difficulty; it guides what to say (e.g. booking an auto) and grades how you spoke. https://x.com/mittalparth_/status/2081961512415936697
- First attempt (@marcdhi): an open-world, GTA-style Bengaluru where conversations happen in place (flower stall, auto rickshaw), with every asset generated in JavaScript and nothing downloaded. Too slow, so they shipped the simpler, finished version. https://x.com/marcdhi/status/2081976006643273867 · http://playsadak.vercel.app
- Lesson: they cut the gameplay but kept the Sarvam STT-TTS stack at the heart, because showing that off mattered most.
- Event brief: https://x.com/udayan_w/status/2079070819444298059

## Rule 6 - Use your domain knowledge
- Prior experience is the only thing you bring to the table beforehand. Good at design? Design something wild. Did a project at work in a field? Borrow that knowledge.
- Think in directions others can't, because they lack your knowledge.
- **Two kinds of projects win:** the idea itself is exceptional, OR it's executed so well, with domain knowledge, that it stands out.
- Don't pick something totally outside your knowledge. For his team that's hardware: no experience and no time to learn.

## Rule 7 - Align with the theme
- Organisers have a theme; stick to it. A great off-theme idea may not make it. The theme also gives you a direction to think in.
- Push to Prod theme "Build the Next Audacious" (Devfolio, https://x.com/devfolio/status/2076996065837117840) was defined as:
  - Next frontier capability: something that doesn't exist yet, not a repackaging of existing tools
  - Next billion dollar idea: a believable path to massive scale, not a feature bolted onto a workflow
  - Product that redefines a category: makes today's default look outdated; not 20% better, a different way entirely
  - Interface that doesn't exist yet: voice, agents acting for you, new input/output modes; not another app on a screen
  - Infrastructure everyone else builds on: the layer others depend on in 5 years, not a one-off tool
- Claude City fit "a new interface that makes today's way look outdated". The mix of Claude Code + SimCity + game didn't exist as an interface. Demo-able, early, functional.

**Ideas his team rejected for Push to Prod, and why:**
- AI on-call engineer: strong domain knowledge and demo-able, but **not early anymore**, so not audacious. **It's a workflow.**
- Educational tool generating 3D models for explanations: **no domain knowledge**; felt like just writing three.js code.
- Marketing campaigns localized per geography (pop culture, memes): **a workflow again**, and the demo depended on **taste** they didn't have.

## Rule 8 - Don't be afraid
- His team isn't game devs. They're optimists with a little taste, building games because models got exceptionally good. Hours of coding and rendering now take minutes.
- A blurred vision, a rough plan, and strong motivation are enough. Don't overthink; hackathons are for experimenting.

## Closing
Hackathons aren't only about winning: hack something cool, learn under constraints, have fun. The joy of building is what lets you keep doing it for years.
