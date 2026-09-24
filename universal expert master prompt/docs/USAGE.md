# Usage Guide

## 1. Full vs. Quick Template

Use `prompts/UNIVERSAL_EXPERT_MASTER_PROMPT.md` when the task is complex, high-stakes, research-heavy, or requires strong control over quality and output structure.

Use `prompts/PROMPT_QUICK_TEMPLATE.md` for routine tasks where the full specification would add unnecessary overhead.

## 2. How to Personalize

At minimum, fill in:

- Field / Discipline
- Degree / Role
- Technical Background
- Technical Depth
- Main Goal
- Current Task
- Context
- Constraints
- Required Output Format

For technical research, also provide:

- Known parameters
- Units
- Operating conditions
- Relevant references
- Experimental limitations
- Acceptance criteria

## 3. How to Improve Results

A prompt becomes more effective when vague requirements are converted into measurable requirements.

Instead of:

```text
Make it very accurate.
```

Prefer:

```text
Use verified sources for technical claims, preserve SI units, define assumptions explicitly, and perform an independent check of important calculations.
```

Instead of:

```text
Design a fast system.
```

Prefer:

```text
Target sampling rate >= 1 MHz, define required analog bandwidth, state synchronization constraints, and verify the architecture against those requirements.
```

## 4. Recommended Workflow

1. Fill the personalization fields.
2. Define the objective in one or two precise sentences.
3. Provide all known inputs.
4. State constraints and acceptance criteria.
5. Specify the exact deliverable.
6. Run the prompt.
7. Review the English output first.
8. Use the Persian output as a faithful translation/reference.

## 5. Important Principle

Longer does not automatically mean better. The objective is to reduce ambiguity and make quality testable.

A useful mental model is:

```text
Intent + Context + Inputs + Assumptions + Constraints
+ Requirements + Output Format + Evidence + Validation
```
