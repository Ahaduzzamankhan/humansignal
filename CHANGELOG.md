# Changelog

All notable changes to Human Signal are documented here. Version numbers follow a simple major.minor.patch scheme.

---

# Human Signal 2.1.0

**Release type:** Major documentation and capability expansion.
**Language:** English only.

## Summary

Version 2.1.0 refocuses Human Signal on linguistic analysis and natural-writing refinement. The previous single-file skill is preserved in substance — the 120 engineering controls remain available as an appendix — and expanded into a structured reference system with modes, worked examples, and quality tests.

## Added

### Writing-pattern encyclopedia
- `references/ai-writing-patterns.md` with **120 documented writing-pattern observations** across **30 categories**.
- Every entry includes: pattern ID, name, category, description, linguistic characteristics, why it can weaken writing, recognition criteria, original example, improved example, explanation of the improvement, and appropriate exceptions.
- A closing section explains responsible use: frequency over presence, genre over fashion, meaning over style, and detectors as non-arbiters.

### Natural language principles
- `references/natural-language-principles.md` covering natural vocabulary selection, context-sensitive phrasing, sentence rhythm, paragraph cohesion, natural information ordering, conciseness, appropriate specificity, logical progression, semantic consistency, audience awareness, register consistency, author voice preservation, clear explanations, appropriate formality, information density, natural emphasis, and contextual relevance.
- A dedicated comparison of **natural variation versus artificial variation**, with a worked contrast and a diagnostic sequence.

### Sentence structure analysis
- `references/sentence-structure.md` covering simple, compound, complex, and compound-complex sentences; sentence-length variation; clause distribution; subject placement; verb selection; active and passive voice; parallel construction; fragments; coordination; subordination; punctuation patterns; and syntactic repetition.
- Each major topic includes explanation, purpose, recognition criteria, correct and incorrect usage, original and revised examples, and editing recommendations.

### Paragraph analysis
- `references/paragraph-analysis.md` covering topic sentences, supporting information, evidence integration, logical transitions, boundaries, length, information density, cohesion, coherence, redundancy, argument progression, explanatory structure, contextual relevance, and reader expectations.
- Guidance on when short paragraphs, long paragraphs, lists, headings, and tables are appropriate.

### Vocabulary and lexical analysis
- `references/vocabulary-analysis.md` covering word frequency, lexical diversity, contextual selection, collocations, synonym appropriateness, repeated expressions, redundant modifiers, domain terminology, register consistency, semantic precision, vocabulary complexity, jargon, generic expressions, word-choice ambiguity, and repeated transitions.
- Rules for editors, including the prohibition on automatic synonym replacement.

### Linguistic analysis framework
- `references/linguistic-analysis.md` describing five levels of analysis, evidence standards, signal combination, a diagnostic sequence, a worked passage analysis, common analysis errors, and the limits of textual analysis.
- An appendix retaining the 120 engineering quality controls from version 2.0 in compact form.

### Detector reliability
- `references/detector-reliability.md` explaining perplexity, burstiness, token distributions, n-gram analysis, lexical diversity, linguistic feature extraction, transformer classifiers, embedding-based classification, statistical classification, dataset bias, training-data limitations, false positives, false negatives, calibration, cross-domain generalization, multilingual limitations, detection uncertainty, and evaluation metrics.
- Definitions and formulas for precision, recall, F1, accuracy, false-positive rate, false-negative rate, and calibration, including a base-rate worked example.
- An explicit argument for why detector output cannot independently establish authorship.

### Academic writing
- `references/academic-writing.md` with guidance for essays, research papers, literature reviews, scientific explanations, arguments, comparative analysis, reports, critical analysis, evidence-based claims, citations, research summaries, methodology, discussion, and conclusions.
- Non-negotiable integrity rules and a pre-submission checklist.

### Technical documentation
- `references/technical-documentation.md` covering READMEs, API documentation, installation guides, architecture documentation, tutorials, changelogs, release notes, error messages, code comments, configuration guides, developer guides, troubleshooting, migration guides, and security documentation.
- An overriding rule that technical accuracy outranks stylistic preference, with a list of protected technical elements.

### Context awareness
- `references/context-awareness.md` covering the six contextual variables, purpose, audience, genre, channel, relationship, consequence, register, culture, temporal context, multimodal context, an adaptation matrix, and context failures.

### Editing guidelines and naturalness engine
- `references/editing-guidelines.md` with the full 16-step naturalness engine, 16 mandatory constraints, a five-level severity model, minimum-effective-edit rules, preservation rules, a report format, and common editing failures.

### Writing modes
- `modes/academic.md`
- `modes/technical.md`
- `modes/conversational.md`
- `modes/professional.md`
- `modes/creative.md`

Each mode specifies intended use, tone, vocabulary, sentence characteristics, paragraph structure, common mistakes, editing rules, examples, and a checklist.

### Example library
- `examples/english-examples.md` — **40** general English cases.
- `examples/academic-examples.md` — **10** academic cases.
- `examples/technical-examples.md` — **10** technical cases.
- `examples/conversational-examples.md` — **10** conversational cases.
- **70 total**, each with original text, identified issues, linguistic analysis, explanation, revised version, explanation of improvements, and meaning-preservation assessment.

### Quality assurance
- `tests/quality-checklist.md` — 78 checks across 12 areas, with evidence requirements, scoring, release thresholds, sign-off, and a ten-minute quick pass.
- `tests/meaning-preservation.md` — preservation categories, a seven-step protocol, failure modes, worked checks, a preservation matrix, and change documentation.
- `tests/regression-cases.md` — 12 tests for over-editing, technical meaning changes, removal of necessary repetition, unnecessary transitions, register drift in both directions, generic replacement, unsupported claims, voice flattening, editing good prose, list normalization, and invented conclusions.

### Project documentation
- `README.md` with overview, scope, structure, installation, usage, mode table, pattern summary, quality assurance, design principles, and contribution guidance.
- This `CHANGELOG.md`.

## Changed

- `SKILL.md` rewritten and expanded for version 2.1.0.
  - Project identity and version updated.
  - Purpose, scope, and English-only policy stated explicitly.
  - Supported writing categories mapped to modes and references.
  - Core operating principles reduced to operational statements.
  - Five-level pattern-analysis workflow added.
  - Naturalness engine summarized with a pointer to the full sequence.
  - Context-aware mode selection and hybrid rules added.
  - Editing workflow, minimum-effective-edit rules, and preservation rules added.
  - Quality assurance, academic integrity, and detector limitations given dedicated sections.
  - Full reference map added.
  - Priority order for conflicting instructions added.
- Detector language tightened: the skill no longer presents detection reduction as an objective and explicitly declines detector-evasion requests.
- Technical scope clarified: writing quality is primary; the engineering controls are retained as a secondary appendix rather than presented as writing patterns.

## Preserved

- The 120 engineering quality controls from version 2.0 (P01–P120), retained in `references/linguistic-analysis.md`.
- The 2.0 commitments to accuracy, specificity, contextual fit, and authorial voice.
- The prohibition on fabricated content and unsupported claims.
- The rule that no isolated stylistic feature proves AI authorship.

## Fixed

- Removed the implication that a fixed set of 120 patterns should be applied uniformly to every text.
- Removed detector-score optimization from the operating instructions.
- Resolved the tension between "avoid repetition" and "preserve terminology" by making functional repetition an explicit exception.
- Corrected guidance that could encourage artificial sentence-length variation.
- Clarified that the engineering controls are not prose-style rules.
- Added a reverse-direction check for claims introduced during editing.
- Added register-preservation rules for high-consequence text.

## Known limitations

- The regression cases are specification walkthroughs, not an empirical benchmark of any model or detector.
- The skill cannot verify facts without external sources.
- The skill cannot establish authorship and does not attempt to.
- No automated link checker or test runner is included; link validation was performed manually during release.
- No license file is included.

---

# Human Signal 2.0.0

The prior release was a single-file skill (`SKILL.md`, 751 lines) organized around 120 pattern controls in 12 categories:

- Vocabulary inflation
- Sentence construction
- Paragraph and structural patterns
- Formatting and typography
- Reasoning and explanation
- Research and academic writing
- Technical documentation
- Programming and source code
- Communication

It included a three-dimension detection engine, a rewrite engine with examples, discipline-specific quality profiles, repository-aware code review guidance, a research integrity protocol, a six-stage self-audit pipeline, six operating modes (AUTO, STRICT, RESEARCH, DOCUMENTATION, CODE, EDIT), and rules for agents using the skill.

Version 2.1.0 preserves the useful parts of that release while shifting the primary focus to linguistic analysis and natural-writing refinement.
