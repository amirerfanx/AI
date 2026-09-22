# AI

A practical collection of AI skills, prompts, agents, and workflows for developers. Includes templates, examples, and best practices for LLMs, RAG, and automation. Open source and contribution-friendly.

## Contents

| Path | Description |
|---|---|
| [`humanize writing`](./humanize%20writing) | Claude Skill that detects and removes signs of AI-generated writing, based on [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) and six academic papers comparing human- and AI-written text. |
| [`humanize-writing/chatgpt`](./humanize-writing/chatgpt) | ChatGPT-native version of the same methodology — a self-contained instruction set for Custom GPTs or project-level instructions, with a reference pattern library and a validation test suite. |
| `LICENSE` | MIT license |

## Humanize Writing — Claude Skill

Reviews text for common AI-writing tells — promotional tone, template-shaped paragraphs, rule-of-three lists, em-dash overuse, passive voice, filler phrases — and rewrites it to read naturally, without adding or removing any fact, number, date, or quotation from the source.

Load `SKILL.md` (inside `humanize writing`) as a Skill in Claude. It supports three invocation modes:

- **Pasted text** — the user gives text in chat; output includes a draft, an audit, and a final rewrite.
- **File mode** — a file is targeted directly and rewritten in place.
- **Embedded mode** — used as one step inside a larger agent or workflow, returning only the final text.

## Humanize Writing — ChatGPT

A parallel implementation of the same approach, designed to be dropped into ChatGPT rather than run as a Claude Skill.

- **`INSTRUCTIONS.md`** — the main instruction set. Paste this into a Custom GPT's Instructions field, or use it as project-level instructions.
- **`PATTERNS.md`** — optional reference material: pattern families, stock phrases (English and Persian), and worked sentence-level transformations. Add it as project knowledge when you want the model to have the longer reference table available.
- **`TESTS.md`** — a small validation suite covering technical-meaning preservation, uncertainty calibration, and resistance to fake imperfections or synonym churn.

Unlike a simple "avoid these AI words" list, this instruction set treats machine-like prose as a *combination* of signals — predictable structure, generic importance claims, uniform sentence rhythm, vague attribution, over-explicit meta-writing — and edits only where several of these actually stack up. It includes explicit preservation rules for academic, scientific, and technical writing, and a dedicated Persian-writing mode.

**Setup:** put the full contents of `INSTRUCTIONS.md` into the GPT's or project's instructions; keep `PATTERNS.md` as optional reference knowledge.

**Limitation:** this is a writing-quality framework, not a detector-evasion tool. It does not guarantee any particular AI-detector outcome and should not be used to misrepresent authorship where disclosure is required.

## License

Released under the [MIT license](./LICENSE).

## Contributing

Contributions are welcome. Open a pull request to add a new skill, prompt, or workflow.

---

## نسخه‌ی فارسی

مجموعه‌ای کاربردی از Skillها، پرامپت‌ها، ایجنت‌ها و ورک‌فلوهای هوش مصنوعی برای توسعه‌دهندگان. شامل قالب‌ها، مثال‌ها و بهترین شیوه‌ها برای کار با LLMها، RAG و اتوماسیون. متن‌باز و پذیرای مشارکت.

### محتوای مخزن

| مسیر | توضیح |
|---|---|
| [`humanize writing`](./humanize%20writing) | یک Claude Skill برای شناسایی و حذف نشانه‌های متن تولیدشده توسط هوش مصنوعی، بر پایه‌ی راهنمای Wikipedia:Signs of AI writing و شش مقاله‌ی علمی مقایسه‌ی سبک نوشتار انسان و AI. |
| [`humanize-writing/chatgpt`](./humanize-writing/chatgpt) | نسخه‌ی بومی ChatGPT از همان روش — مجموعه‌دستورالعملی مستقل برای Custom GPT یا دستورالعمل سطح پروژه، همراه با یک کتابخانه‌ی الگوی مرجع و یک مجموعه تست اعتبارسنجی. |
| `LICENSE` | مجوز MIT |

### Humanize Writing — نسخه‌ی Claude

متن را از نظر نشانه‌های رایج نوشتار AI بررسی می‌کند — لحن تبلیغاتی، پاراگراف‌های الگو-محور، فهرست‌های سه‌تایی، استفاده‌ی افراطی از em dash، جملات منفعل، عبارات پرکننده — و آن را بدون افزودن یا حذف هیچ واقعیت، عدد، تاریخ یا نقل‌قولی نسبت به متن اصلی، طبیعی‌تر بازنویسی می‌کند.

فایل `SKILL.md` (داخل پوشه‌ی `humanize writing`) را به‌عنوان یک Skill در Claude بارگذاری کنید. سه حالت فراخوانی پشتیبانی می‌شود:

- **متن مستقیم** — متن در گفتگو داده می‌شود؛ خروجی شامل پیش‌نویس، بررسی و نسخه‌ی نهایی است.
- **حالت فایل** — یک فایل مشخص می‌شود و در همان مسیر بازنویسی می‌شود.
- **حالت تعبیه‌شده** — به‌عنوان یک مرحله در یک ایجنت یا ورک‌فلوی بزرگ‌تر استفاده می‌شود و فقط متن نهایی را برمی‌گرداند.

### Humanize Writing — نسخه‌ی ChatGPT

پیاده‌سازی موازی همان روش، برای استفاده در ChatGPT به‌جای اجرا به‌عنوان Claude Skill.

- **`INSTRUCTIONS.md`** — مجموعه‌دستورالعمل اصلی. این فایل را در فیلد Instructions یک Custom GPT یا به‌عنوان دستورالعمل سطح پروژه قرار دهید.
- **`PATTERNS.md`** — مرجع اختیاری: خانواده‌های الگو، عبارات کلیشه‌ای (انگلیسی و فارسی) و نمونه‌های بازنویسی در سطح جمله. آن را به‌عنوان دانش پروژه اضافه کنید تا مدل به جدول مرجع طولانی‌تر دسترسی داشته باشد.
- **`TESTS.md`** — مجموعه‌تست کوچکی که حفظ معنای فنی، کالیبراسیون عدم‌قطعیت و مقاومت در برابر خطاهای ساختگی یا تعویض بی‌مورد مترادف‌ها را می‌سنجد.

برخلاف یک فهرست ساده‌ی «کلمات ممنوعه‌ی AI»، این مجموعه‌دستورالعمل نثر ماشین‌گونه را ترکیبی از چند نشانه می‌داند — ساختار قابل‌پیش‌بینی، ادعاهای اهمیت کلی‌گویانه، ریتم یکنواخت جملات، ارجاع مبهم، فرانوشتار (meta-writing) بیش‌ازحد صریح — و فقط زمانی ویرایش می‌کند که چند مورد از این‌ها واقعاً روی هم انباشته شده باشند. قواعد صریحی برای حفظ نوشتار آکادمیک، علمی و فنی، و یک حالت مخصوص نوشتار فارسی نیز دارد.

**راه‌اندازی:** کل محتوای `INSTRUCTIONS.md` را در دستورالعمل GPT یا پروژه قرار دهید؛ `PATTERNS.md` را به‌عنوان دانش مرجع اختیاری نگه دارید.

**محدودیت:** این یک چارچوب برای کیفیت نوشتار است، نه ابزار دور زدن ابزارهای تشخیص AI. هیچ تضمینی برای نتیجه‌ی خاص در ابزارهای تشخیص AI نمی‌دهد و نباید برای پنهان‌کردن نویسندگی در جایی که افشا لازم است استفاده شود.

### مجوز

این پروژه تحت مجوز [MIT](./LICENSE) منتشر شده است.

### مشارکت

مشارکت‌ها خوش‌آمدند. برای افزودن Skill، پرامپت یا ورک‌فلوی جدید، یک Pull Request باز کنید.
