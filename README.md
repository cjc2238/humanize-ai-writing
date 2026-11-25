# humanize-writing

A portable **Claude skill** that revises AI-generated prose so it reads like a
human wrote it — targeting the structural choices that mark text as machine-
written, not just the surface vocabulary.

Most "make it sound human" tricks go after em-dashes and words like *delve* and
*tapestry*. Those are the easy tells, and newer models and a find-and-replace
already defeat them. This skill goes after the harder layer: **how the text is
built** — whether it over-explains its point, resolves too tidily, over-renders
the senses, avoids the reader, and converges on the same safe, central choices
every model makes.

It's grounded in one specific study rather than folk wisdom — see
[the research](#the-research).

---

## What's inside

```
humanize-writing/
├── SKILL.md                         # the skill: seven structural shifts + a surface pass
└── references/
    ├── ai-tells-checklist.md        # diagnostic pass, grouped by severity
    ├── surface-tells.md             # the full lexical / syntactic tell list
    ├── model-fingerprints.md        # per-model quirks (Claude, GPT, Gemini, DeepSeek, Kimi)
    └── the-research.md              # plain-language summary + citation
```

## What it does

It applies **seven shifts**, structure first:

1. **Stop over-explaining the point** — cut the sentence that states the moral.
   (AI states the theme outright 77% of the time; humans 52%.)
2. **Break the straight line** — allow digression, time jumps, unresolved threads.
   (79% of AI texts have no subplots vs. 57% for humans.)
3. **Name feelings sometimes; stop over-rendering the body** — "show don't tell,"
   over-applied, is itself a tell. (AI uses bodily metaphor 81% vs. 38%; explicit
   emotion words only 8% vs. 29%.)
4. **Reference the real, specific world** — actual names, dates, places, prices.
   (Humans name real things 47% vs. 24%.)
5. **Acknowledge the reader** — a genuine aside, a real opinion.
   (Direct address 28% vs. 7%.)
6. **Let it be uneven** — lumpy sentence and paragraph rhythm.
7. **Prefer the morally ambiguous read** — leave a cost unpaid, a question open.

…then a **surface pass** for the lexical tells everyone already knows.

## How to use it

### With Claude Code
Drop the `humanize-writing/` folder into your skills directory:

```bash
# project-level
mkdir -p .claude/skills && cp -r humanize-writing .claude/skills/

# or user-level (available in every project)
mkdir -p ~/.claude/skills && cp -r humanize-writing ~/.claude/skills/
```

Then just ask, in natural language:
> "This draft sounds like ChatGPT. Make it read like a person wrote it."

Claude will invoke the skill, diagnose the tells, and revise. If you tell it which
model wrote the draft, it also applies that model's fingerprint.

### With Claude.ai, the API, or another assistant
You don't need Claude Code. Paste the contents of `SKILL.md` (and any reference
file you want) into your chat or system prompt, then give it the text to revise.
The skill is plain Markdown and model-agnostic — the instructions work anywhere.

### As a human editor's checklist
`references/ai-tells-checklist.md` works on its own as a manual editing pass —
no tooling required.

## The research

This isn't vibes. It's built on:

> **StoryScope: Investigating idiosyncrasies in AI fiction.** Jenna Russell,
> Rishanth Rajendhran, Chau Minh Pham, Mohit Iyyer, John Wieting. COLM 2026.
> arXiv:2604.03136 · [code & data](https://github.com/jenna-russell/storyscope)

The authors compared 10,272 human-written texts against five frontier models
across 304 narrative-structure features. The key result: **structure alone
identifies AI writing at 93% accuracy, and it stays that detectable even after
the surface style is edited away.** Humans write in a more varied, rarer region of
"narrative space"; AI models converge on the same safe center. That's the whole
reason this skill leads with structure. Full summary and all the statistics are in
[`references/the-research.md`](humanize-writing/references/the-research.md).

## Scope and honest use

This is for improving the quality and voice of your own writing, and for honest
editing. It is **not** intended for passing AI work off as human where disclosure
is expected, or for defeating academic-integrity or detection systems you're
obligated to respect. The study's own point cuts both ways: the structural tells
are durable, so "humanizing" is better understood as *writing better* than as
*hiding the source*.

The percentages describe populations of **fiction**, so they're directional for a
single essay or post — use the checklist to diagnose the actual draft in front of
you, and don't turn the seven shifts into a new formula. The goal is human
*variety*, not a second monoculture.

## License

MIT — see [LICENSE](LICENSE).

## Credit

Skill by [Chad Coleman, Ph.D.](https://www.chadcoleman.net) Built on the
StoryScope research by Russell et al. (COLM 2026); all credit for the underlying
findings is theirs.
