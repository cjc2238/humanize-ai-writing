---
name: humanize-writing
description: Revise AI-generated prose so it reads like a human wrote it. Use when text feels like "AI slop" — over-explained, tidy, sensory-heavy, morally neat — or when someone asks to make writing sound more human, less like ChatGPT, or less detectable. Grounded in StoryScope (COLM 2026), which isolates the structural (not just stylistic) choices that separate human from AI writing.
---

# Humanize Writing

## What this skill does

Most "make it sound human" advice targets surface tells — em-dashes, "delve,"
"tapestry," "it's not just X, it's Y." Those matter, but they are the easy 20%,
and newer models and a quick find-and-replace already strip them.

This skill targets the harder, more durable layer: the **structural and
rhetorical choices** that separate human from AI writing even after you fix the
vocabulary. These come from StoryScope (Russell et al., COLM 2026), which
compared 10,272 human-written texts against five frontier models across 304
narrative features. The finding that matters: AI writing clusters in a narrow,
predictable region of "narrative space," and humans are both more varied and
measurably *rarer*. The gap survives surface editing — so you have to change the
decisions underneath, not just the words on top.

Use this skill to **revise** a draft, or to **generate** fresh text that avoids
the defaults from the start.

## How to use it

1. Read the draft (or the request) and diagnose which AI tells are present —
   work through `references/ai-tells-checklist.md`.
2. Apply the fixes below, prioritizing structure over vocabulary.
3. If the user names the model that wrote it, also apply the model-specific
   fingerprint from `references/model-fingerprints.md`.
4. Preserve the author's meaning and facts. Humanizing is not rewriting the
   content — it is changing *how* the content is constructed and delivered.
5. Don't overcorrect into a new monoculture. The goal is human *variety*, not a
   second formula. If every fix below is applied to every piece, you've just
   built a different tell.

> **Scope note.** This makes writing read as human-authored for quality and
> voice. Use it for your own drafts and honest editing. It is not for passing
> off AI work as human where disclosure is expected, or for defeating academic-
> integrity or detection systems you're obligated to respect.

## The seven shifts (structure first)

### 1. Stop over-explaining the point
AI states the moral or theme outright ~77% of the time; humans do ~52%. AI
spells out meaning rather than trusting the reader to infer it.
- **Cut the sentence that explains what the previous sentences meant.** The one
  starting "This shows that…", "The lesson here is…", "Ultimately, what matters…".
- Let an example or image carry the point without a gloss. Trust the reader.
- Remove the tidy summary that restates the intro. Not every piece needs to
  land its thesis twice.

### 2. Break the straight line
AI builds tidy, single-track plots and arguments: 79% of AI stories have no
subplots (vs. 57% for humans); AI favors clean causal chains and arrives at the
reveal in order. Humans use digression, time jumps, and loose ends.
- Allow a tangent that doesn't fully resolve. Open a thread, leave it.
- Don't present every cause before every effect. Start in the middle; circle back.
- Resist the urge to tie every thread off at the end. Ambiguity reads as human;
  AI prefers resolution and closure.
- In an argument: a real aside, a "but here's where it gets complicated,"
  a point you raise and then partly walk back.

### 3. Name feelings sometimes; stop over-rendering the body
AI conveys emotion through physical sensation and imagery far more than humans
(bodily metaphors 81% vs. 38%; smell-based imagery 82% vs. 57%), and uses
explicit emotion words far *less* (8% vs. 29%). The "show don't tell" rule,
over-applied, is itself an AI tell.
- Where AI writes "her chest tightened, her palms went cold," a human will often
  just write "she was scared" — and move on.
- Cut at least half the sensory inventory. You rarely need the light, the smell,
  *and* the temperature of a room.
- Delete the reflexive "the air was thick with…", "a knot formed in…".

### 4. Reference the real, specific world
Humans name real texts, brands, places, and people at nearly double the AI rate
(47% vs. 24%) and mix explicit and implicit reference more evenly. AI defaults to
vague allusion and generic stand-ins.
- Replace "a popular social media platform" with the actual one. "A classic
  novel" → the title. "A major city" → the city.
- Add a concrete, checkable detail only a person who was there would include —
  a specific date, a price, a street name, a product version.
- Specificity is one of the cheapest and strongest human signals.

### 5. Acknowledge the reader
Humans break the fourth wall and address the reader far more (direct address
28% vs. 7%; fourth-wall breaks 67% vs. 39%). AI writes "as though no one is
watching."
- An aside to the reader: "You've probably seen this." "Bear with me here."
- A real rhetorical question you then actually answer unexpectedly — not the
  AI-pattern question that sets up a tidy answer.
- First-person intrusion: a genuine opinion, a hedge, an admission of doubt.

### 6. Let it be uneven
AI output is uniform: consistent sentence rhythm, even paragraph lengths,
balanced structure, measured tone throughout. Humans are lumpy.
- Vary sentence length hard. A long, winding, subordinate-clause-heavy sentence
  that keeps going. Then a short one.
- Let one paragraph be three sentences and the next be one.
- Allow a fragment. An abrupt start. A section that runs hot while the rest is cool.

### 7. Prefer the morally ambiguous read
AI resolves toward neat understanding and acceptance; it moralizes and presents
tidy, well-behaved conclusions. Humans sit with unresolved tension and
morally mixed outcomes (ambivalent protagonists 59% vs. 38%).
- Don't make everyone reasonable and the ending reconciled.
- Leave a cost unpaid, a question open, a character partly wrong.
- Cut the "but ultimately there's hope" / "a reminder that…" bow on top.

## Surface pass (do this too, but last)

After the structural edits, clean the known lexical tells. These are necessary
but not sufficient — see `references/surface-tells.md` for the full list:
- Overused words: delve, tapestry, testament, realm, navigate, landscape,
  underscore, pivotal, crucial, vibrant, meticulous, boasts, nestled.
- The "not just X, but Y" / "it's not about X, it's about Y" construction.
- Triadic lists everywhere (always three parallel items).
- Em-dash overuse; uniform transitions (Moreover, Furthermore, In conclusion).
- Hedging throat-clearing: "It's important to note that," "In today's world."

## When generating from scratch

Write to a target instead of a formula. Before drafting, pick deliberate
deviations: one unresolved thread, one real-world specific, one direct address,
one place you'll name the feeling flatly instead of rendering it, one uneven
stretch. Then write. The checklist in `references/ai-tells-checklist.md` works as
a pre-flight for generation, not only as a diagnostic for revision.

## References
- `references/ai-tells-checklist.md` — diagnostic pass, grouped by severity.
- `references/surface-tells.md` — the full lexical/syntactic tell list.
- `references/model-fingerprints.md` — per-model quirks (Claude, GPT, Gemini,
  DeepSeek, Kimi) for model-specific cleanup.
- `references/the-research.md` — plain-language summary of StoryScope and the
  citation.
