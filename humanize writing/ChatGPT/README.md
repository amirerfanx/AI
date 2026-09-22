# Humanize Writing for ChatGPT

A ChatGPT-native version of the `humanize-writing` methodology.

## What is included

- `INSTRUCTIONS.md` — the main instruction set. This is the file to paste into a Custom GPT's Instructions field or use as project-level instructions.
- `PATTERNS.md` — optional reference material with pattern families, phrase examples, and editorial transformations.
- `TESTS.md` — a small test suite for checking whether the instructions work as intended.

## Design goals

This version is intentionally more than a list of “AI words to avoid.” It treats machine-like prose as a combination of:

- predictable structure;
- repetitive rhetorical moves;
- generic importance claims;
- over-explicit signposting;
- vague attribution;
- uniform sentence rhythm;
- inflated vocabulary;
- unnecessary closure;
- and excessive lexical or punctuation fingerprints.

It also contains explicit preservation rules for academic and scientific writing, plus a dedicated Persian-writing mode.

## Recommended ChatGPT setup

### Project instructions

Put the complete contents of `INSTRUCTIONS.md` into the project's instructions. Keep `PATTERNS.md` as optional project knowledge when you want the model to have the longer reference table available.

### Custom GPT

Use the complete contents of `INSTRUCTIONS.md` in the GPT's main Instructions field. Add `PATTERNS.md` as a knowledge/reference file when supported by your configuration.

## Suggested test prompts

English:

> Humanize this paragraph. Preserve every factual claim, citation, number, and technical term. Do not make it casual. First diagnose the strongest machine-like patterns internally, then rewrite it.

Persian:

> این متن را طبیعی‌تر و انسانی‌تر کن، اما معنی علمی، اعداد، ارجاعات و اصطلاحات تخصصی آن را تغییر نده. متن را محاوره‌ای نکن و از جمله‌های کلیشه‌ای هم استفاده نکن.

Academic:

> Rewrite this thesis paragraph in natural academic English. Keep the uncertainty exactly calibrated and do not replace technical terminology with generic synonyms.

Diagnosis:

> فقط الگوهای ماشینی و کلیشه‌ای این متن را شناسایی کن. آن را بازنویسی نکن و برای هر مورد مثال کوتاه بده.

## Expected behavior

A successful rewrite should usually show structural improvement before lexical variation. It should not contain fake mistakes, forced slang, unnecessary “personality,” or a recognizable stock humanizer style.

## Important limitation

This is a writing-quality framework. It does not guarantee detector outcomes and should not be used to misrepresent authorship where disclosure or attribution is required.

## Repository placement

Recommended path:

`humanize-writing/chatgpt/`
