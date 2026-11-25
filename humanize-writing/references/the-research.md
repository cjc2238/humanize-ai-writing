# The Research Behind This Skill

This skill is grounded in a single, specific study rather than folk wisdom about
"AI voice." Everything in the shifts and checklists traces back to measured
differences in it.

## The paper

**StoryScope: Investigating idiosyncrasies in AI fiction**
Jenna Russell, Rishanth Rajendhran, Chau Minh Pham, Mohit Iyyer, John Wieting.
University of Maryland (CLIP Lab) and Google DeepMind.
Published as a conference paper at **COLM 2026**. arXiv:2604.03136.
Code and data: https://github.com/jenna-russell/storyscope

## What they did

The team built a parallel corpus: 10,272 writing prompts, each answered by a
human author and by five frontier LLMs (Claude Sonnet 4.6, GPT-5.4, Gemini 3
Flash, DeepSeek V3.2, Kimi K2.5) — 61,608 stories averaging ~4,750 words each.

Instead of looking at surface style (word choice, sentence shape), they built a
pipeline that extracts **304 discourse-level narrative features** — decisions
about plot, character agency, how and when information is revealed, temporal
structure, moral framing, and so on — grounded in narrative theory (the
NarraBench taxonomy).

## What they found

1. **Structure alone gives away AI.** Using *only* narrative-structure features
   and withholding all stylistic signals, a classifier separates human from AI
   writing at 93.2% macro-F1 — retaining over 97% of the performance of a model
   that also sees style. The tell isn't just the words; it's the construction.

2. **It survives editing.** When AI text is stylistically rewritten to remove
   surface artifacts (cliché, purple prose), narrative-structure detection barely
   moves (95.5% → 93.9%). Fixing vocabulary doesn't fix the underlying choices.
   This is *why* this skill prioritizes structure over surface.

3. **AI occupies a narrow, shared region.** All five models cluster together in
   "narrative space," well-separated from human writing, which is more dispersed.
   Human texts are measurably *rarer* — they sit in sparser parts of the space
   (mean rarity percentile 0.71 vs. 0.49 for AI).

4. **The specific differences** (human vs. AI, from §4.1) — these drive the
   seven shifts:
   - Explicitly states the theme: **52% human / 77% AI** (AI over-explains).
   - "No subplots": **57% human / 79% AI** (AI is more linear).
   - Emotion via bodily metaphor: **38% human / 81% AI**.
   - Smell-based imagery: **57% human / 82% AI**.
   - Explicit emotion words: **29% human / 8% AI** (AI shows, rarely tells).
   - References real texts/brands/places: **47% human / 24% AI**.
   - Directly addresses the reader: **28% human / 7% AI**.
   - Breaks the fourth wall: **67% human / 39% AI**.
   - Morally ambivalent protagonists: **59% human / 38% AI**.

5. **Each model has a fingerprint** (six-way attribution from structure alone,
   68.4% macro-F1) — summarized in `model-fingerprints.md`.

## Important scope caveats

- The study is about **fiction / narrative writing**. The structural findings
  generalize well to essays, posts, and other prose (over-explaining, linearity,
  uniformity, vague reference, no reader address all show up far beyond fiction),
  but the exact percentages are measured on stories.
- Percentages describe populations, not any single text. A given AI draft may not
  show every tell; a human draft may show some. Use the checklist to diagnose the
  specific draft in front of you.
- The numbers reflect the model *versions* studied. Surface tells in particular
  shift fast between releases; the structural tells are more stable, which is the
  whole point of the paper.

## How to cite

> Russell, J., Rajendhran, R., Pham, C. M., Iyyer, M., & Wieting, J. (2026).
> *StoryScope: Investigating idiosyncrasies in AI fiction.* Conference on
> Language Modeling (COLM) 2026. arXiv:2604.03136.
