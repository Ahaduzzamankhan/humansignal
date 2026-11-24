# Human Signal 2.1.0

A linguistic analysis and natural-writing refinement skill for English prose.

Human Signal helps an editor or an AI agent improve writing quality: clarity, specificity, cohesion, register fit, and structural logic. It also helps identify the habits that make prose feel formulaic — generic openings, stacked adjectives, redundant transitions, over-signposting, vague claims, and mechanical symmetry — without treating those features as proof of machine authorship.

**Version:** 2.1.0
**Language:** English only
**Format:** Markdown skill with references, modes, examples, and tests

---

## What it does

- Diagnoses a text at five levels: pragmatic, discourse, syntactic, lexical, typographic.
- Documents 120 recurring writing-pattern observations across 30 categories.
- Provides a 16-step editing workflow with explicit preservation constraints.
- Supplies five context-aware modes: academic, technical, conversational, professional, creative.
- Contains 70 worked examples with meaning-preservation assessments.
- Includes a 78-item quality checklist, a meaning-preservation protocol, and 12 regression tests.

## What it does not do

- It does not evade AI detectors, and it does not promise lower detection scores.
- It does not treat a detector score as evidence of authorship.
- It does not fabricate sources, data, examples, or experience.
- It does not rewrite everything. Most edits are deletions, reordering, and precision.
- It does not replace domain expertise. It can improve the clarity of a legal or medical text; it cannot certify its correctness.
- It does not support languages other than English.

For the reasoning behind the detector stance, see [references/detector-reliability.md](references/detector-reliability.md).

---

## Repository structure

```
humansignal/
├── SKILL.md                          # Main skill instructions (v2.1.0)
├── README.md                         # This file
├── CHANGELOG.md                      # Release history
├── index.html                        # Single-file showcase
├── agent.md                          # Agent installation contract
├── vercel.json                       # Vercel static config
├── references/
│   ├── ai-writing-patterns.md        # 120 patterns, 30 categories
│   ├── natural-language-principles.md
│   ├── sentence-structure.md
│   ├── paragraph-analysis.md
│   ├── vocabulary-analysis.md
│   ├── linguistic-analysis.md
│   ├── detector-reliability.md
│   ├── academic-writing.md
│   ├── technical-documentation.md
│   ├── context-awareness.md
│   └── editing-guidelines.md
├── modes/
│   ├── academic.md
│   ├── technical.md
│   ├── conversational.md
│   ├── professional.md
│   └── creative.md
├── examples/
│   ├── english-examples.md           # 40 cases
│   ├── academic-examples.md          # 10 cases
│   ├── technical-examples.md         # 10 cases
│   └── conversational-examples.md    # 10 cases
└── tests/
    ├── quality-checklist.md
    ├── meaning-preservation.md
    └── regression-cases.md
```

---

## Installation

Human Signal is a set of Markdown files. There is no build step and no dependency.

### As an agent skill

1. Copy the repository into your skills directory, keeping the internal structure:

   ```
   <skills-dir>/humansignal/
   ```

2. Ensure `SKILL.md` is at the root of that directory. Its frontmatter declares the skill name and version:

   ```yaml
   ---
   name: humansignal
   version: 2.1.0
   ---
   ```

3. If your platform requires a single-file skill, use `SKILL.md` and copy the `references/`, `modes/`, `examples/`, and `tests/` directories alongside it so the relative links resolve.

### As a writing reference

Read [SKILL.md](SKILL.md) first. It is the operational summary. Use the reference files when you need the reasoning behind a rule.

### Requirements

- A Markdown reader or an agent runtime that loads Markdown skills.
- No external services, packages, or network access.

### From a URL (agent install)

If you want an agent to install the skill itself, give it the deployment URL followed by `/agent.md`:

```
https://v2humansignalliard.vercel.app/agent.md
```

That file contains the git and tarball install commands, verification checks, activation steps, and a context-only fallback. See [agent.md](agent.md).

---

## Deployment

The repository is also a static site. `index.html` is the showcase, `agent.md` is the install contract, and `vercel.json` supplies headers and a `/agent` redirect.

### Vercel

1. Import the repository at [vercel.com/new](https://vercel.com/new).
2. Use the **Other** preset. Leave the build command and output directory empty.
3. Deploy. `index.html` is served at `/`, and the contract at `/agent.md`.

With the CLI:

```bash
npm i -g vercel
vercel --prod
```

No environment variables, serverless functions, or external services are required. The site has no trackers and no runtime dependencies.

### Other static hosts

Upload the repository root as-is. Keep `index.html`, `agent.md`, and the Markdown directories together so the relative links resolve. GitHub Pages serves the same files; the Vercel headers are optional.

---

## Usage

### Basic edit

Provide the text, the intended reader, and the purpose. Human Signal selects a mode, runs the analysis, and returns the revised text.

```
Edit this README section for backend developers evaluating the library.
Preserve the technical terms and the measured numbers.

[paste text]
```

### With explicit mode

```
Use technical mode. Check every command and default value.
Do not add features that are not implemented.

[paste text]
```

### Audit instead of edit

```
Audit this paragraph. Identify the problems by level, assign severity,
and explain the effect on the reader. Do not rewrite it yet.

[paste text]
```

### Academic integrity check

```
Review this literature review for unsupported consensus claims,
citation slippage, and causal overreach. Do not invent sources.

[paste text]
```

### What a good response looks like

For a small edit, the response is the revised text, optionally with one or two sentences about material changes. For an audit, it follows the report format in [references/editing-guidelines.md](references/editing-guidelines.md) Part VI:

```
Scope: ...
Assumptions: ...
Critical findings: ...
Changes made: ...
Preserved deliberately: ...
Unresolved: ...
Meaning check: ...
```

---

## The five modes

| Mode | Use for | Key constraint |
|---|---|---|
| [Academic](modes/academic.md) | Essays, papers, reviews, analysis | Evidence and attribution outrank elegance |
| [Technical](modes/technical.md) | READMEs, APIs, guides, changelogs | Accuracy and testability outrank style |
| [Conversational](modes/conversational.md) | Chat, short email, support | Clarity and register fit outrank completeness |
| [Professional](modes/professional.md) | Memos, proposals, updates | Decisions and ownership outrank ceremony |
| [Creative](modes/creative.md) | Fiction, narrative, personal essays | Voice and effect outrank information density |

Choose by primary purpose. When two modes apply, satisfy the stricter constraint.

---

## The pattern encyclopedia

[references/ai-writing-patterns.md](references/ai-writing-patterns.md) documents 120 observations, four in each of 30 categories:

1. Formulaic introductions
2. Formulaic conclusions
3. Repetitive transitions
4. Overused vocabulary
5. Generic descriptions
6. Excessive adjectives
7. Unnecessary adverbs
8. Repetitive sentence structures
9. Artificial paragraph symmetry
10. Redundant explanations
11. Excessive summarization
12. Generic examples
13. Empty motivational statements
14. Unnecessary disclaimers
15. Repetitive headings
16. Excessive bullet-list usage
17. Artificially balanced arguments
18. Unnecessary rhetorical questions
19. Vague claims
20. Contextually inappropriate formality
21. Overexplaining obvious concepts
22. Repetitive opening phrases
23. Predictable paragraph endings
24. Unnecessary restatements
25. Artificially polished phrasing
26. Excessive hedging
27. Unnatural word substitutions
28. Repetitive explanatory structures
29. Unnecessary meta-commentary
30. Generic comparisons

Each entry has a pattern ID, name, category, description, linguistic characteristics, an explanation of why it can weaken writing, recognition criteria, an original example, an improved example, an explanation of the improvement, and appropriate exceptions.

**None of these patterns proves AI authorship.** They are editing prompts. See the caution at the top of the encyclopedia and the analysis in [references/detector-reliability.md](references/detector-reliability.md).

---

## Quality assurance

- [tests/quality-checklist.md](tests/quality-checklist.md) — 78 checks in 12 areas, with evidence requirements and release thresholds.
- [tests/meaning-preservation.md](tests/meaning-preservation.md) — a claim-by-claim protocol, a preservation matrix, and worked failure cases.
- [tests/regression-cases.md](tests/regression-cases.md) — 12 tests for over-editing, terminology damage, register drift, synonym inflation, invented specificity, and unsupported conclusions.

The regression cases are specification walkthroughs, not an empirical benchmark of any model. They record the behavior the instructions require and the wording changes made to close gaps.

---

## Design principles

1. Meaning is the invariant; style is the variable.
2. Find the problem before changing the sentence.
3. Prefer deletion to replacement.
4. Precision outranks variety.
5. Never invent specificity.
6. Let form follow content.
7. Preserve voice.
8. Respect genre.
9. Protect technical terminology.
10. Judge quality by readers, not detectors.

The full list and priority order are in [SKILL.md](SKILL.md) §6 and §15.

---

## Version history

See [CHANGELOG.md](CHANGELOG.md). Current version: **2.1.0**.

---

## Contributing

When adding a pattern, example, or rule:

1. Place it in the existing structure; do not create a parallel system.
2. Follow the field structure used by neighboring entries.
3. Use original examples with a meaning-preservation assessment.
4. Do not invent citations, data, or sources.
5. Add the file to the reference map in `SKILL.md` §14 if it is new.
6. Verify that every relative link resolves.
7. Add a CHANGELOG entry for user-visible changes.

## License

No license file is included in this repository. Add one before redistributing or publishing.
