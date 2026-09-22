# humanize-writing

A [Claude Skill](https://support.claude.com/en/articles/12512176-what-are-skills) that helps Claude diagnose and fix AI-sounding prose — and write more naturally human prose from the start. It works on text you give Claude, and on Claude's own output.

## Why

Most popular advice about "sounding less like AI" ("avoid em dashes," "never say delve") is folklore. This skill is built instead from six corpus-linguistics studies that actually measured human vs. AI writing with real statistical methodology — engagement-strategy analysis of academic essays, formal-grammar diversity metrics, Biber's 66-feature linguistic tagset, stylometric clustering, and two discourse/semantic studies. Full citations are in [`humanize-writing/references/bibliography.md`](humanize-writing/references/bibliography.md).

The two strongest, most independently-confirmed findings:

- **AI-generated text dramatically underuses epistemic hedges and connective language** — words like *possibly, arguably, nonetheless, by contrast, admittedly*. One study found an 8–11x gap between human and AI writing on this category alone.
- **Newer, more heavily instruction-tuned models are *more* uniform and formulaic than older ones, not less** — three independent methodologies converge on this. Polish and humanness are not the same axis.

## What's inside

```
humanize-writing/
├── SKILL.md                          # the skill itself — triggers and core guidance
└── references/
    ├── diagnostic-checklist.md       # checklist for fixing existing AI-sounding text
    ├── writing-habits.md             # the same patterns, for drafting from scratch
    ├── word-and-construction-lists.md  # specific vocabulary/grammar with source numbers
    └── bibliography.md               # full citations for all six sources
```

## Install

1. Download this repository, or just the `humanize-writing/` folder, and zip it (the ZIP must contain `SKILL.md` at the top level once extracted).
2. In Claude, go to **Settings → Capabilities** and make sure **Code execution and file creation** is turned on.
3. Go to **Customize → Skills**.
4. Click **"+"** → **"+ Create skill"** → **"Upload a skill"**, and select the ZIP.
5. Toggle the skill on.

Claude will use it automatically when you ask it to make text sound more human, check writing for AI "tells," or when it's about to draft substantial analytical/academic/professional prose. You can also invoke it explicitly: *"Use the humanize-writing skill on this draft."*

Full official instructions: [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

## A caution

This is a genuine writing-quality tool, not a way to defeat plagiarism/AI-detection software for dishonest purposes — see the note in `SKILL.md` itself. AI-detection tools are also known to be unreliable and biased against non-native English writers; nothing here is a guarantee against any specific detector.

## License

The contents of this repository (the skill's instructions, checklists, and synthesis) are original writing. See `humanize-writing/references/bibliography.md` for the licensing status of the six source papers it cites. Consider adding a license for this repository itself (e.g. MIT) if you want to make reuse terms explicit — GitHub repos without one default to no reuse rights beyond viewing.
