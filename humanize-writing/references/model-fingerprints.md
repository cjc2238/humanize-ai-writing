# Model Fingerprints

StoryScope found that the five frontier models don't just differ from humans —
they differ from *each other* in predictable ways, enough to attribute a text to
its model from narrative structure alone (68.4% six-way macro-F1). If you know
which model produced a draft, target its specific defaults in addition to the
general shifts in SKILL.md.

These are tendencies, not laws, and they reflect the model versions studied
(Claude Sonnet 4.6, GPT-5.4, Gemini 3 Flash, DeepSeek V3.2, Kimi K2.5). Treat
them as "where this model is most likely to be boring," not as fixed rules.

## Claude — restrained and reverent
Claude has the most distinctive profile of the five. Its writing is defined by
restraint: event intensity escalates *less* than any other source, the voice is
the most uniform, and it treats conventions reverently — honoring and extending
tradition rather than subverting it (62% of Claude texts, vs. 39–56% elsewhere).
It favors quiet, careful, consistent endings and avoids dream sequences.
- **Push against:** flatness of escalation. Let stakes actually spike.
- Introduce a genuine subversion or rule-break instead of the tasteful,
  tradition-honoring move.
- Allow a messier, less composed ending; break the even voice somewhere.

## GPT — social and gossipy
GPT centers socially-oriented storytelling: gossip and rumor as a plot mechanism
(64% vs. 44–55%), framing things as reflections on events from years or decades
ago, and ensemble-heavy social networks. It subverts expectations more than other
AIs (41%) and leaves reconciliations ambiguous.
- **Push against:** the reflexive "looking back on it now…" retrospective frame.
- Cut reliance on who-said-what-about-whom as the engine.
- It already does ambiguity relatively well — keep that, trim the social clutter.

## Gemini — tidy and bleak
Gemini produces the tidiest endings and extended denouements, and the bleakest
settings (88% tagged bleak/oppressive). It over-resolves while over-darkening the
backdrop.
- **Push against:** the neat, drawn-out wrap-up. End sooner and messier.
- Lighten or vary the default grim atmosphere; not everything needs to be
  oppressive.

## DeepSeek — front-loads context
DeepSeek front-loads crucial context that other sources reveal later. It tells
you what you need up front instead of withholding.
- **Push against:** the information dump at the start. Hold something back; let
  it surface later.

## Kimi — generic
Kimi has the fewest distinctive fingerprints and sits at the generic center of
the AI distribution, with the least separable style.
- **Push against:** blandness itself. It needs the *most* deliberate
  specificity, voice, and risk — apply all seven shifts from SKILL.md hard,
  because there's little character to preserve.

## Note on detection
All five AI models cluster together in a region of narrative space that is
distinct from, and less varied than, human writing — and human texts are
measurably *rarer* (they sit in sparser parts of the space). The practical
upshot: the strongest single move toward "human" is unpredictability and
specificity, because the shared AI failure mode is converging on the safe,
common, central choice.
