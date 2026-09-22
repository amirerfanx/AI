# Humanize Writing for ChatGPT

This folder adapts the repository's **humanize-writing** methodology for use with ChatGPT.

The Claude implementation is packaged as a Claude Skill. ChatGPT does not use that same skill package format, so this version is provided as a reusable instruction set that can be placed into a Custom GPT's **Instructions** field or used as project-level instructions.

## Files

- `INSTRUCTIONS.md` — the ChatGPT-ready instruction set.
- `README.md` — setup and usage notes.

## Setup in ChatGPT

### Custom GPT

1. Create or edit a Custom GPT.
2. Open its configuration/instructions.
3. Copy the complete contents of `INSTRUCTIONS.md` into the GPT's **Instructions** field.
4. Save the GPT.
5. Test it with both academic and general-purpose prose.

### ChatGPT Project

The same instruction set can be used as project instructions where that feature is available.

## Example prompts

### Persian

- «این متن را طبیعی‌تر و انسانی‌تر کن، بدون اینکه معنی علمی آن تغییر کند.»
- «این متن را از نظر الگوهای ماشینی بررسی کن و بعد بازنویسی کن.»
- «این پاراگراف را برای یک مقاله علمی روان‌تر کن، ولی اصطلاحات تخصصی و ارجاعات را حفظ کن.»

### English

- "Use the humanize-writing instructions on this draft."
- "Rewrite this academic paragraph so it reads naturally while preserving the technical meaning and citations."
- "Diagnose the formulaic patterns in this text, then revise it."

## Important limitation

This is a writing-quality framework. It does not guarantee that text will evade AI detectors, and it should not be used to misrepresent AI-generated work where disclosure or attribution is required.

The original evidence base and citations remain in the parent `humanize-writing` directory.

## Relationship to the Claude version

The ChatGPT version preserves the core methodology of the original Claude Skill but translates its operating instructions into a format suitable for ChatGPT. It is not intended to be a byte-for-byte copy of the Claude Skill package.
