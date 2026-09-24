# Universal Expert Master Prompt

[![Repository Check](https://github.com/your-username/universal-expert-master-prompt/actions/workflows/repository-check.yml/badge.svg)](https://github.com/your-username/universal-expert-master-prompt/actions/workflows/repository-check.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A reusable, customizable master prompt for producing accurate, structured, evidence-aware, technically rigorous, and bilingual AI outputs.

The framework is designed for research, academic writing, engineering, programming, technical analysis, literature review, decision support, data analysis, and other complex tasks.

## Key Features

- **Personalization layer** for user background, expertise, goals, and preferences
- **Context-first task specification** to reduce ambiguity
- Explicit **scope, assumptions, constraints, requirements, and priorities**
- Domain-aware reasoning guidance for **science and engineering**
- **Evidence and sourcing rules** with anti-hallucination safeguards
- **Numerical, mathematical, and dimensional checks**
- **Five-pass internal quality-control loop** before the final answer
- **English primary output**
- **Faithful Persian translation** as a second output
- Consistent technical terminology, notation, units, and formatting
- Support for **research, thesis work, engineering design, coding, and decision support**
- Clear rules for uncertainty, missing information, edge cases, and limitations

## Repository Structure

```text
universal-expert-master-prompt/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
├── .gitignore
├── prompts/
│   ├── UNIVERSAL_EXPERT_MASTER_PROMPT.md
│   └── PROMPT_QUICK_TEMPLATE.md
├── examples/
│   └── thesis-research-example.md
└── docs/
    └── USAGE.md
```

## Quick Start

For GitHub publishing instructions, see [`docs/GITHUB_PUBLISH.md`](docs/GITHUB_PUBLISH.md).

1. Open [`prompts/UNIVERSAL_EXPERT_MASTER_PROMPT.md`](prompts/UNIVERSAL_EXPERT_MASTER_PROMPT.md).
2. Fill in the bracketed fields such as `[FIELD]`, `[OBJECTIVE]`, and `[CONSTRAINTS]`.
3. Add your task-specific context and inputs.
4. Paste the completed prompt into your preferred AI assistant.
5. Review the generated English output and its Persian translation.

For a lighter workflow, use [`prompts/PROMPT_QUICK_TEMPLATE.md`](prompts/PROMPT_QUICK_TEMPLATE.md).

## Recommended Personalization

The master prompt supports fields such as:

- Academic or professional role
- Degree and technical background
- Research area
- Programming level
- Preferred technical depth
- Communication style
- Current project or thesis
- Long-term goal
- Geographic or institutional context
- Special preferences

### Example

```text
Field / Discipline: Nuclear Fusion Engineering
Degree / Education Level: Master's
Technical Background: Plasma physics, diagnostics, electronics, data acquisition
Research Topic: High-speed Langmuir probe diagnostics
Preferred Technical Depth: Advanced
Communication Style: Academic and engineering-oriented
```

## Five-Pass Quality Loop

Before returning the final answer, the prompt asks the model to perform five internal review passes:

1. **Requirement Check** — verifies the task, requested format, and constraints.
2. **Factual & Technical Check** — checks claims, equations, units, calculations, and unsupported information.
3. **Logical & Consistency Check** — checks contradictions, assumptions, causality, and conclusions.
4. **Quality & Practicality Check** — checks usefulness, depth, trade-offs, limitations, and applicability.
5. **Final Polish & Compliance Check** — checks language, terminology, formatting, citations, personalization, and bilingual fidelity.

The process is used for quality control; private chain-of-thought is not requested or exposed.

## Bilingual Output Policy

The default final response contains exactly two main outputs:

### Output 1 — English

A polished, technically accurate English answer.

### Output 2 — Persian

A faithful Persian translation of Output 1, preserving the same structure, meaning, equations, numbers, tables, and technical notation where practical.

## Design Philosophy

The goal is not to make prompts merely longer. The goal is to make them **less ambiguous, more testable, and more useful**.

A strong prompt specifies:

> **Intent + Context + Inputs + Assumptions + Constraints + Requirements + Output Format + Quality Criteria + Validation**

## Use Cases

This framework can be adapted for:

- Thesis and dissertation work
- Journal papers and literature reviews
- Scientific research
- Plasma and fusion engineering
- Experimental planning
- Engineering system design
- Data analysis
- Software development
- Technical documentation
- Comparison and trade-off analysis
- Decision-support tasks
- Professional writing and editing

## Suggested GitHub Repository Metadata

**Repository name:** `universal-expert-master-prompt`  
**Short description:** `A reusable expert master prompt for accurate, structured, personalized, and bilingual AI outputs.`  
**Suggested topics:** `prompt-engineering`, `master-prompt`, `generative-ai`, `research`, `engineering`, `academic-writing`, `bilingual`, `persian`

## Contribution

Contributions are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

This project is released under the MIT License. See [`LICENSE`](LICENSE).

## Author

Created as a reusable open prompt framework for advanced research, engineering, and technical workflows.
