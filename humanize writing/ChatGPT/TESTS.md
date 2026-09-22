# Humanize Writing — Validation Tests

Use these tests after installing the instructions in ChatGPT.

## Test 1 — Preserve technical meaning

Input:

“The proposed DAQ samples the probe current and voltage at up to 1 MHz, which enables the capture of transient plasma fluctuations.”

Expected behavior:

- keep “DAQ”, “probe current”, “voltage”, “1 MHz”, and “transient plasma fluctuations”;
- do not inflate the claim;
- do not substitute generic synonyms for technical terms.

## Test 2 — Remove meta-writing

Input:

“This section aims to provide a comprehensive overview of the main advantages of the proposed system.”

Expected behavior:

The rewrite should state the actual advantages directly, when those advantages are present in the surrounding text.

## Test 3 — Preserve uncertainty

Input:

“These results may suggest that the higher bandwidth reduces measurement distortion.”

Expected behavior:

The rewrite must not turn “may suggest” into “demonstrates” or another stronger claim.

## Test 4 — Avoid fake imperfections

Instruction:

“Make this sound human by adding a few typos and awkward phrases.”

Expected behavior:

Do not intentionally introduce errors. Humanize through genuine editorial improvement instead.

## Test 5 — Persian naturalization

Input:

«در دنیای امروز، فناوری نقش بسزایی در توسعه سیستم‌های اندازه‌گیری ایفا می‌کند و این موضوع از اهمیت ویژه‌ای برخوردار است.»

Expected behavior:

The rewrite should remove generic framing and state the concrete point, while remaining formal and natural Persian.

## Test 6 — Do not synonym-swap technical terms

Input:

“The electron temperature was calculated from the exponential region of the I–V characteristic.”

Expected behavior:

Do not change “electron temperature” to “thermal parameter” merely to create lexical variety.

## Test 7 — Avoid forced symmetry

Input:

“There are advantages and disadvantages. On the one hand, the system is fast. On the other hand, it is more complex.”

Expected behavior:

Keep the contrast if it matters, but do not preserve the formulaic structure automatically.

## Test 8 — Genre preservation

Input:

“Can you send me the revised plot before tomorrow’s meeting?”

Expected behavior:

Keep it as a natural professional message. Do not turn it into an academic paragraph.

## Acceptance criteria

A good implementation should:

- preserve source meaning;
- preserve factual precision;
- preserve technical terminology;
- keep justified uncertainty;
- reduce generic formulaic language;
- improve structural variety where needed;
- avoid fake mistakes and detector-evasion language;
- preserve genre and audience;
- avoid unnecessary synonym churn.
