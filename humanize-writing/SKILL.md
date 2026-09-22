---
name: humanize-writing
description: Make AI-generated or AI-influenced prose read as naturally human-written, and diagnose AI-sounding text supplied by the user. Use whenever the user asks to make text "sound more human," "less AI," "less like ChatGPT," to check writing for AI "tells," to edit/rewrite a draft (their own or Claude's own prior output) to read as human-written, or to review a document for AI-detection risk before submission. Also trigger proactively whenever Claude is about to produce substantial prose in an analytical, academic, journalistic, or professional register (essay, article, report, review, long explanation) — apply these habits while drafting, not only when fixing text afterward. Grounded in six corpus-linguistics studies comparing human and AI writing (Appraisal Theory engagement analysis, HPSG/ERG grammar diversity metrics, Biber's 66-feature tagset, Burrows' Delta stylometry, plus two semantic/discourse studies), not folk claims about em dashes.
---

# Humanizing AI-influenced writing

## Why this skill exists, and what it is actually based on

Popular advice about "sounding less like AI" is mostly folklore — "avoid em dashes," "don't use the word 'delve.'" Some of that folklore is roughly right but for the wrong reasons, and most of it misses the load-bearing patterns entirely. This skill is built from six sources that actually measured human vs. AI text with real methodology: engagement-strategy analysis of 80 academic essays (Alghazo et al. 2025), formal-grammar diversity metrics on news writing across two LLM generations (Gude et al. 2026), Biber's 66-feature tagset applied to six genres with statistical testing (Reinhart et al. 2025, PNAS), stylometric clustering of creative fiction (O'Sullivan 2025), a discourse-analytic framework applied to academic writing (Andoniou 2026), and a semantic/embedding-based study of German academic introductions (Wegerhoff 2025). Where their findings converge independently — different languages, different genres, different statistical methods — that convergence is the strongest evidence here, and it's flagged below. Where a single source claims something, treat it as a lead worth trying, not gospel.

The single most consistent, most robust, most repeatedly-confirmed finding across every source that measured it: **AI-generated text is dramatically less likely to use epistemically cautious, connective, and critical language** — words like *possibly, presumably, admittedly, nonetheless, by contrast, arguably, at least, by no means, on the other hand, ultimately, merely, questionable, inconsistent*. One study found humans use this class of word 8–11 times more often than AI. If you fix nothing else, fix this.

The second most consistent finding: **newer, more heavily instruction-tuned models are *more* uniform and formulaic than older ones, not less** — three completely independent methodologies (formal grammar diversity, Biber features, stylometric clustering) converge on this. "Sounding polished" and "sounding human" are not the same axis, and optimizing for the former can actively work against the latter. Don't mistake fluency for humanness while editing.

## How to use this skill

This skill works two ways, and both matter for what the user asked:

1. **Diagnosing text you're given** (the user's draft, or Claude's own earlier output in the conversation). Read it against the checklist in `references/diagnostic-checklist.md`, mark what's actually present, and rewrite. Don't apply every fix mechanically to every sentence — a text that's already varied and hedged doesn't need more hedging bolted on. Diagnose first, then treat only what's actually broken.
2. **Writing prose from scratch** so it doesn't need fixing afterward. If you're about to draft something substantial and analytical, build the habits in `references/writing-habits.md` in as you go, rather than writing in default style and patching it after.

Before rewriting anything, skim `references/word-and-construction-lists.md` — it has the specific vocabulary and grammatical constructions with the numbers behind them, which is more useful to have open while editing than to hold in memory.

## The core moves, briefly

These are the patterns worth internalizing even without opening the reference files:

- **Take a side.** AI-generated argumentative writing tends to acknowledge an opposing view and then soften into both-sides balance rather than actually refuting it. Human writers use flat negation ("there is no evidence that...", "X is not Y") and genuine rebuttal far more. If the content supports a conclusion, land on it — don't hedge into permanent neutrality out of politeness.
- **Let some claims be common ground.** AI text almost never uses words like "of course," "naturally," or "obviously" to signal that something is shared, uncontroversial knowledge. Real writers do this constantly. If a point genuinely is uncontroversial, say so plainly instead of re-litigating it.
- **Stop narrating your own rigor.** "Through careful analysis," "using a systematic methodology," "this comprehensive approach reveals" — AI text performs analytical-sounding-ness by *talking about* being analytical rather than *being* analytical through the actual content. Cut the meta-commentary about your own method and just do the thing.
- **Commit to a real claim, not just a topic.** AI text often talks *about* an idea (frames an "analysis of X," gestures at a "hypothesis") without ever stating what it actually concludes. State the conclusion.
- **Don't inflate importance.** AI text has a measurable habit of calling whatever it's discussing "central," "crucial," or "a key issue in the field" — often when the thing is genuinely a minor or peripheral point. Only claim centrality when it's actually warranted.
- **Vary the rhythm.** Sentence length, paragraph shape, and internal structure in AI text tend to be unusually even — this is measurable and is called "low burstiness" in the literature. Real human writing mixes short blunt sentences with longer ones, and doesn't run every paragraph through the same define→elaborate→conclude template.
- **Don't over-tidy the ending.** AI text resolves almost every paragraph with an explicit "In conclusion," "Therefore," "As a result" — closing every loop. Let some paragraphs end on a genuinely open note, a transition, or an unresolved tension, the way people actually write.
- **Cut the padding clauses.** Stacked participial phrases ("X, leaning on Y, doing Z, evading W..."), "That [clause] [verb]s..." subject fronting, and nominalizations (turning "underscores" into "provides an underscoring of") inflate apparent density without adding real content. These are measured at 2–5x human rate in instruction-tuned models. Say it more directly.
- **Get specific.** AI text drifts toward abstraction — "job creation," "economic growth," "concerns" — rather than concrete grounding: real numbers, named entities used referentially, direct quotation. This is partly the model hedging against getting a specific fact wrong, but it reads as vague. Where you actually have or can verify a specific detail, use it.
- **Avoid the tell-vocabulary in non-fiction registers.** *Tapestry, camaraderie, palpable, intricate, underscore(s), unspoken, amidst, testament, bittersweet, poignant, delve, boasts, elevate, unleash, unlock, a game-changer, in today's world/fast-paced world/digital age, it's important to note, navigate the complexities of, plays a crucial/vital/pivotal role, stands as a, seamlessly, robust, holistic, multifaceted, tapestry of, weaving together.* These words aren't inherently bad — some belong naturally in fiction or casual speech — but instruction-tuned models use them at 80–170x the human rate in genres like journalism and academic writing, where they read as conspicuously overwrought. See the full annotated list in `references/word-and-construction-lists.md` for genre-specific guidance, since a few of these are fine in the right context.

## A caution about "humanizer" tools and naive fixes

One source in this skill's basis specifically tested what happens when AI output is run through synonym-swapping "humanizer" tools, and found the result is *still* detectably artificial — and sometimes worse, because forced uncommon synonyms read as "lexical over-compensation," a distinct and recognizable tell of its own. Swapping "important" for "salient" doesn't fix anything if the underlying paragraph still has the tidy define-example-conclude shape, the flat positive tone, and the total absence of hedging. Fix structure and stance first; word choice is the smallest lever here, not the biggest one, whatever the popular advice about "avoid the word delve" might suggest.

Also worth being honest about: this is pattern-matching against *statistical averages* from specific studies (news leads, academic introductions, short fiction, argumentative essays), not a guaranteed detector-proof recipe, and AI detection tools themselves are known to be unreliable and biased against non-native English writers — treat this skill as a genuine writing-quality tool, not a way to defeat academic-integrity software. If the goal is passing off AI-written work as entirely one's own for an assignment or publication where that would be dishonest, that's a call for the user to make, not something this skill is designed to help launder.

## Files in this skill

- `references/diagnostic-checklist.md` — the checklist to run existing text against before rewriting. Organized by how confident the evidence is (cross-source-confirmed patterns first).
- `references/writing-habits.md` — the same patterns, reframed as generation-time habits for drafting prose that won't need this kind of fix afterward.
- `references/word-and-construction-lists.md` — the actual vocabulary and grammatical-construction lists with their source numbers, genre caveats, and what to use instead.
