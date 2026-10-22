---
name: hackathon-ideas
description: Use when the user shares a hackathon, buildathon, or sponsor challenge (link, announcement, theme, sponsor list, or pasted details) and wants to know what to build, needs project ideas, or asks for creative, unique, non-generic ideas for an event.
---

# Hackathon Ideas

## Overview

Finds hackathon ideas that nobody else in the room will have. It follows the method of Parth Mittal (15 wins from 35+ hackathons, incl. Anthropic, Google DeepMind, Sarvam, ETHIndia), backed by advice from other winners and judges.

**Core principle:** the first ideas an AI gives are the ideas every other team will build, so they are banned. Your job is research, mixing, and filtering. Every idea must trace back to real, cited, recent sparks, and the sponsor's tech must be the hero.

Read `profile.md` (the user's settings) and `inspiration.md` (the user's own bookmarks) before starting. Deep background, with every example and source, is in `references/`.

## The Run (do every step, in order)

### Step 0 - Understand the event
If given a link, fetch it (for X links use `curl -s https://api.fxtwitter.com/i/status/<id>`, since x.com blocks fetches). Write down:
- **Sponsor tech** (exact products, models, APIs, and what is NEW in them)
- **Theme** and its sub-lines, word for word
- **Judging criteria**
- **Time box**, team size, tracks and prizes, location and culture, rules

Search for anything missing. Ask the user only if the sponsor tech or theme is still unknown.

### Step 1 - Write the banned list (Rule 1: don't ask AI)
Before any research, write the 8-12 ideas you would give by default for this event. These are what every other team's AI will say. Every one of them, and anything close to it, is banned for the rest of the run. Keep the list; it goes in the output.

### Step 2 - Collect sparks (Rules 2 and 5: gather inspiration, be early)
Use web search. Follow `references/where-to-look.md`. Collect **at least 12 sparks**, each with a link and a date:
- **Sponsor-new**: what the sponsor shipped or announced in the last ~60 days. What does it do that was impossible or too slow/expensive before? This is the "early" edge.
- **Culture-new**: striking demos, launches, and weird projects from the last ~60 days on X, Reddit, HN, Product Hunt, GitHub, and HF Spaces. Include ones **outside tech** (design, art, games, music, film).
- **Forgotten/nostalgic**: an old format, game, toy, or interface to twist. `references/remix-bank.md` has seeds; prefer ones tied to the event's culture or place.
- **Past winners** of this event, series, or sponsor: learn what got rewarded, and add them to the banned list (no repeats).
- **User bookmarks** from `inspiration.md`: always include these first.

**Cite the primary source**: the maker's own post, repo, demo, or the sponsor's own page. Use roundup or SEO blogs ("10 wildest projects...") only to find the original link; they don't count as a spark. Any claim about what the sponsor tech can do must come from a page you actually fetched.

### Step 3 - Collide (Rule 2)
Make at least 15 raw candidates. Each one is **one recent spark + one different spark (old, cross-field, or local culture) + the sponsor's new capability at the center**. Pattern from Claude City: Flipbook (Apr) + isometric SF map (Aug) + Claude Agent SDK = "your repo as a live city where agents build". Keep collisions unexpected. Two sparks from the same field rarely surprise anyone. The second spark must be **load-bearing**: it changes what the judge sees or does (the city IS the repo view). If it's only a name or a skin ("arcade-style leaderboard"), drop it and find a real one.

### Step 4 - Kill (Rules 3, 4, 5, 6, 7)
Run every candidate through the gate. **One fail = dead.** No rescue edits that just paper over the fail.

| # | Gate | Kill if |
|---|------|---------|
| 1 | Hero | You could build it without the sponsor's tech |
| 2 | Forced | The sponsor tech is bolted on, or several sponsors are stacked just to raise the odds |
| 3 | One line | The pitch needs more than 1 sentence, or the problem takes more than 30s to explain (Aaroh failed this) |
| 4 | Visible | A judge can't SEE the wow within 60 seconds; things that are proactive or pay off over time fail here (Medha failed this) |
| 5 | Early | It was already doable or common months ago ("AI on-call engineer": not early anymore) |
| 6 | Workflow | It's just a workflow/automation and the theme asks for bold (Parth rejected 2 ideas for this) |
| 7 | Theme | It doesn't map to a specific line of the theme |
| 8 | Banned | It resembles anything on the Step 1 list or a past winner |
| 9 | Doable | It can't reach a demo-able core in the time box with AI coding help, or it's in the profile's no-go list, or it needs skills nobody on the team has (e.g. hardware) |
| 10 | Taste | The demo only lands with taste or domain feel the team lacks (the multilingual-memes marketing idea died here) |
| 11 | Sponsor pride | The sponsor wouldn't be proud to repost the demo video |

Use `profile.md` strengths only to **boost** a survivor's rank, never to kill an idea.

### Step 5 - Rank and pick
Score survivors 1-5 on: sponsor-as-hero, wow in 60s, earliness, theme fit, buildability, and surprise (how unlikely another team builds it). Pick the top N (`profile.md`, default 5). Rule 8 (don't be afraid): an unfamiliar format (a game, a city, a comic) is fine if AI coding makes it doable in the time box. If several survivors are near-copies of each other, keep the best one and replace the rest with the next-best distinct ideas.

### Step 6 - Use AI only to sharpen (Rule 1, allowed use)
For each pick, stress-test feasibility with pointed questions: What breaks at hour 3? What gets mocked? What is the one moment the demo is built around? Tighten the pitch.

## Output (exact shape, simple English)

Start with one line: the event, the sponsor tech, and the theme as you understood them.

Then, for each idea:

```
## <n>. <Name> - <one-line pitch a 12-year-old gets>
**What it is:** 2-3 plain sentences.
**Why <sponsor tech> is the hero:** "Without it, this can't exist because ..."
**Why now:** the recent capability/launch it rides on (link, date).
**Built from:** spark A (link) + spark B (link) [+ user bookmark if used]
**The 60-second demo:** what the judge sees, step by step, and the "wow" moment.
**Theme fit:** which theme line, quoted.
**Build plan for <time box>:** the core to build, what to fake/mock, what to cut.
**Biggest risk -> fallback:** one line.
**Scores:** Hero x/5 · Wow x/5 · Early x/5 · Theme x/5 · Buildable x/5 · Surprise x/5
```

Then:

```
### Obvious AI ideas (banned - other teams will build these)
- <idea>: one line
```

End with `Sources:` listing every link used. **Every idea must cite at least 2 real links.** An idea you can't source is a generic idea: kill it.

Write in simple English: short sentences, no jargon without a plain explanation, no em dashes.

## Red Flags - you are generating, not researching

- An idea has no linked spark, or only cites the sponsor's homepage
- Ideas sound like "AI-powered X assistant", "agent that automates Y", "RAG over Z docs", "copilot for W"
- Ideas match the shapes a plain model produced in a no-skill baseline test: "ask your codebase why this exists", "type one sentence, get an app", "agent watches you once and repeats the task", "shared memory bus for agents", "voice incident war room / AI on-call engineer"
- All sparks are from the last 2 days of one feed, or all from tech
- You skipped Step 1 because "I'll avoid generic ideas anyway"
- The same idea shows up twice with different names
- The sponsor could be swapped for a competitor with one line of code
- A "Built from" link is a roundup blog, or the old format is only a skin

**Any of these: go back to Step 2.**

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Best product, sponsor on the side | Rule 3: without the sponsor tech the project must not exist |
| Mouthful pitch ("agents find merchants via UCP, pay with x402, carry ERC-8004 identity") | One sentence, then show it |
| Great idea, off-theme | Quote the theme line it serves or kill it |
| Over-scoped demo (open-world GTA Bengaluru) | Ship the simpler version with the sponsor tech still the hero (what Parth's team did) |
| Idea needs weeks of use to show value | Pick something whose value shows up on screen instantly |
