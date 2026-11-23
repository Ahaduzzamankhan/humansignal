# Linguistic Analysis Framework

Version 2.1.0 · Human Signal

This file describes how Human Signal conducts an analysis: the levels it examines, the evidence it accepts, the way it combines observations, and the limits of what a textual analysis can conclude. It is the methodological companion to the pattern encyclopedia.

Related: [ai-writing-patterns.md](ai-writing-patterns.md) · [natural-language-principles.md](natural-language-principles.md) · [sentence-structure.md](sentence-structure.md) · [paragraph-analysis.md](paragraph-analysis.md) · [vocabulary-analysis.md](vocabulary-analysis.md) · [detector-reliability.md](detector-reliability.md)

---

## 1. What an analysis is for

A linguistic analysis answers one of three questions:

1. **Comprehension:** what does this text mean, and where is that meaning unclear?
2. **Quality:** where does the text fail to serve its reader, and why?
3. **Consistency:** where does the text contradict itself, its genre, or its own terminology?

It does **not** answer "who wrote this." That question requires provenance evidence, not textual features. See [detector-reliability.md](detector-reliability.md).

Keep the question fixed. Analyses drift when the analyst starts describing everything instead of answering the question asked.

---

## 2. Levels of analysis

Text can be analyzed at five levels. Each has its own units, evidence, and failure modes. A complete analysis moves from the largest unit to the smallest, because higher-level problems invalidate lower-level polish.

### Level 1 — Pragmatic and contextual

**Unit:** the text as an act of communication.

**Questions:** Who is the reader? What is the text for? Does the genre fit? Is the register appropriate? Does the text assume the right background? Is the channel suited to the content?

**Evidence:** the document's stated purpose, its venue, its audience cues (headings, examples, terminology), comparison with competent texts in the same genre.

**Typical findings:** wrong audience, wrong genre, mismatched register, missing prerequisites, inappropriate length for channel.

**Why it comes first:** a perfectly edited text for the wrong reader is still a failure. Do not polish sentences in a document that should be restructured or rewritten for a different audience.

### Level 2 — Discourse and structure

**Unit:** sections, paragraphs, argument.

**Questions:** Does the document progress? Does each section have a job? Are claims and evidence adjacent? Are boundaries in the right places? Is anything redundant at the document level?

**Evidence:** outline of section functions, paragraph summaries, the claim–evidence–implication chain.

**Typical findings:** buried lede, circular structure, repeated sections, missing conclusion, orphan evidence, scope creep.

### Level 3 — Syntactic

**Unit:** sentences and clauses.

**Questions:** Is the main claim in the main clause? Is the subject close to the verb? Is subordination accurate? Is voice appropriate? Are lists parallel? Are fragments intentional?

**Evidence:** clause diagrams, sentence-length distribution, subject–verb distance, punctuation relationships.

**Typical findings:** main claim buried, ambiguous attachment, over-nesting, comma splices, faulty parallelism, passive with a relevant actor.

### Level 4 — Lexical

**Unit:** words and multi-word expressions.

**Questions:** Is the word precise? Does it fit the register? Is the collocation natural? Is terminology consistent? Is repetition functional? Is the modifier doing work?

**Evidence:** collocation checks, term frequency, synonym mapping, register markers, domain glossaries.

**Typical findings:** evaluative filler, nominalization, synonym drift, jargon mismatch, vague quantifiers, redundant modifiers.

### Level 5 — Orthographic and typographic

**Unit:** spelling, punctuation, capitalization, formatting.

**Questions:** Is spelling consistent with the declared variety? Is punctuation conventional and meaningful? Are headings hierarchical? Is emphasis functional? Are code and identifiers intact?

**Evidence:** style guide, project conventions, diff against identifiers in the source.

**Typical findings:** mixed US/UK spelling, decorative dashes, bold inflation, broken heading levels, altered identifiers.

**Rule:** never fix Level 5 before Levels 1–4. Correcting commas in a paragraph that should be deleted is wasted work.

---

## 3. Evidence standards

An observation is only usable if it is **located**, **described**, and **explained**.

| Standard | Requirement | Counter-example |
|---|---|---|
| **Located** | Name the sentence, paragraph, or section | "The writing is vague" |
| **Described** | Name the feature precisely | "It uses vague language" |
| **Explained** | State the effect on the reader | "It is bad" |

**Good observation:** "In paragraph 3, 'significantly improved' gives no baseline or measure, so the reader cannot tell whether the change matters."

**Bad observation:** "Paragraph 3 is AI-like."

The second is not an analysis; it is a label. Labels cannot be verified, taught, or acted on.

### Distinguish observation from inference

- **Observation:** the text contains four sentences beginning with "The system."
- **Inference:** the repetition makes the paragraph feel mechanical.
- **Judgment:** the paragraph should be revised.

Keep these separate. An observation can be true while the inference is wrong; an inference can be reasonable while the judgment is optional.

### Frequency and distribution

A single instance is rarely a finding. Record:
- how many times the feature occurs;
- where it occurs (clustered or spread);
- whether it correlates with a section's function.

A pattern that appears once in a conclusion may be a deliberate close. The same pattern ten times across a document is a habit.

### Baseline comparison

Compare with competent texts in the same genre. A legal contract's repetition is not a defect; a blog post's repetition may be. Without a baseline, "unusual" is just "different from what I would write."

---

## 4. Combining signals

Individual features are weak. Combinations are stronger, but they are still not proof of authorship. Use combinations to prioritize editing, not to classify.

### A worked combination

**Observations:**
- Every section begins with a definition.
- Every section ends with a one-sentence summary.
- Transition vocabulary is drawn from a set of six connectives.
- Evaluative adjectives appear at a rate of one per 40 words, none tied to a property.
- Sentence lengths cluster between 18 and 24 words.

**Inference:** the text is organized by a template rather than by its content.

**Editing implication:** restructure sections by function; keep the content; remove recaps and unsupported adjectives.

**What this does not show:** who wrote it, or whether a detector would flag it.

### Weighting signals

Give more weight to features that:
- affect comprehension;
- recur across the document;
- conflict with the genre;
- cannot be explained by the topic.

Give less weight to features that:
- are single instances;
- are conventional in the genre;
- are required by a style guide;
- are explained by the subject matter (e.g., repeated technical terms).

---

## 5. The diagnostic sequence

Use this sequence for any substantial text.

### Pass 1 — Global
1. Read once for meaning.
2. State the text's purpose and audience.
3. Classify the genre.
4. Outline the sections and their jobs.
5. Identify the author's voice features.

### Pass 2 — Structural
6. Check progression: does each section depend on the previous?
7. Check claim–evidence adjacency.
8. Check for missing or duplicated sections.
9. Check paragraph boundaries and lengths.
10. Check redundancy at the document level.

### Pass 3 — Sentence
11. Check main claims vs. subordinate clauses.
12. Check subject–verb distance and clause depth.
13. Check voice and agency.
14. Check parallelism and punctuation.
15. Check sentence-length distribution against information load.

### Pass 4 — Lexical
16. Check terminology consistency.
17. Check evaluative words for missing properties.
18. Check nominalizations and light verbs.
19. Check collocations.
20. Check register markers.
21. Check vague quantifiers and undefined terms.

### Pass 5 — Verification
22. Check facts, numbers, citations, identifiers.
23. Check meaning preservation against the original.
24. Read the revised text aloud.
25. Review the diff for new patterns.

---

## 6. Analysis of a short passage

A complete worked example, showing the levels in order.

**Original:**
> In today's rapidly evolving digital landscape, effective communication is more important than ever. Furthermore, clear writing is a crucial component of professional success. Moreover, it enables teams to collaborate seamlessly and achieve their goals. In conclusion, mastering the art of communication is essential for anyone who wants to thrive.

**Level 1 — Pragmatic.** No stated audience or purpose; the register is motivational and generic. The passage could open almost any professional communication guide.

**Level 2 — Discourse.** Four sentences: a landscape claim, two additive restatements, and a conclusion. Each sentence restates the same proposition at a higher level of abstraction. There is no evidence, example, or mechanism.

**Level 3 — Syntactic.** All four sentences are declarative and medium-long. The openings are formulaic ("In today's…", "Furthermore…", "Moreover…", "In conclusion…"). No sentence contains a concrete subject.

**Level 4 — Lexical.** "Rapidly evolving digital landscape," "crucial component," "seamlessly," "mastering the art," "thrive" are evaluative or metaphorical with no referent. "Effective," "clear," and "important" are undefined.

**Level 5 — Orthographic.** Nothing notable; standard punctuation.

**Diagnosis:** The passage asserts that communication matters without saying what makes writing clear, for whom, or in what situation. The problem is not the presence of transitions; it is that there is no content for them to connect.

**Revision (if the writer's point is that clarity is a professional skill):**
> Clear writing saves time: a message that states the request, the deadline, and the constraint can be answered in one reply instead of three.

**What changed:** A claim with a mechanism replaced four restatements. The revision is shorter, but the real change is that it now says something falsifiable.

**Meaning check:** The original's general claim ("communication matters") is narrowed to a specific benefit ("clarity saves time"). If the writer intended the broader claim, the revision would need to preserve it and add support. This is exactly the kind of change that must be flagged rather than made silently.

---

## 7. Common analysis errors

| Error | Description | Correction |
|---|---|---|
| **Pattern spotting** | Labeling features without explaining their effect | Require a located, described, explained observation |
| **Over-attribution** | Concluding authorship from style | Restrict conclusions to quality and comprehension |
| **Genre blindness** | Judging a contract by blog standards | Establish the genre baseline first |
| **Single-feature diagnosis** | Treating one em dash as a finding | Check frequency, distribution, and function |
| **Precision theater** | Quoting statistics without a baseline | State the comparison and the sample |
| **Ignoring content** | Polishing prose that says nothing | Check the claim before the sentence |
| **Voice erasure** | Editing toward a neutral ideal | Record and preserve voice features |
| **Level skipping** | Fixing commas in a document that needs restructuring | Work top-down |
| **Confirmation bias** | Finding what you expected to find | Analyze before labeling; check counter-evidence |
| **False precision** | Assigning numeric scores to unmeasured qualities | Use severity categories with stated reasons |

---

## 8. Reporting an analysis

A useful report has five parts:

1. **Scope and assumptions** — what was analyzed, for whom, under what genre assumption.
2. **Findings by level** — pragmatic, structural, syntactic, lexical, typographic. Each finding located and explained.
3. **Severity** — critical, high, medium, low, preserve.
4. **Recommended actions** — minimum effective edits, in order.
5. **Limits** — what could not be verified, what requires the author, what was left alone deliberately.

Do not include a list of 120 pattern IDs. Group by effect. A writer can act on "three sections restate the introduction; cut two" more easily than on "AWP-005, AWP-024, AWP-041."

---

## 9. What textual analysis cannot do

- It cannot establish authorship.
- It cannot verify facts without external sources.
- It cannot recover the writer's intent beyond what the text and context support.
- It cannot judge whether a claim is true from its style.
- It cannot measure quality on a universal scale.
- It cannot predict how a detector will score the text, or guarantee any score.

State these limits when they matter. An analysis that overclaims is worse than one that is modest and accurate.

---

## Appendix: engineering quality controls retained from Human Signal 2.0

Version 2.0 included 120 controls for AI-generated output across writing, research, documentation, and source code. The writing-related controls have been reorganized into the 120-entry pattern encyclopedia in [ai-writing-patterns.md](ai-writing-patterns.md). The engineering controls remain useful for code review and technical work, and are retained here in compact form.

They are not linguistic patterns and should not be applied to prose as style rules. Use them when the task includes source code or repository changes.

| ID | Control |
|---|---|
| P01 | Avoid buzzword overuse; use precise terminology. |
| P02 | Do not stack generic adjectives in place of capabilities. |
| P03 | Do not replace ordinary words with complicated ones to sound intelligent. |
| P04 | Limit repeated stock vocabulary (delve, furthermore, seamless). |
| P05 | Do not turn simple communication into bureaucratic prose. |
| P06 | Keep marketing vocabulary out of technical writing. |
| P07 | Remove empty intensifiers (extremely, incredibly, truly). |
| P08 | Do not rotate synonyms for a technical term that must stay consistent. |
| P09 | Replace vague action verbs (utilize, facilitate) with precise ones. |
| P10 | Do not mechanically open every paragraph with a transition. |
| P11 | Avoid repeated contrastive negation ("not X; Y"). |
| P12 | Do not force complex subjects into binary framing. |
| P13 | Do not default to three-item lists regardless of content. |
| P14 | Use em dashes only when they improve readability. |
| P15 | Do not join unrelated statements with semicolons. |
| P16 | Avoid consecutive sentences with identical openings. |
| P17 | Avoid uniform sentence lengths without artificially varying them. |
| P18 | Break overloaded sentences with excessive subordinate clauses. |
| P19 | Do not insert rhetorical questions for dramatic effect. |
| P20 | Avoid repetitive generic sentence endings. |
| P21 | Prefer active voice when the actor is known and relevant. |
| P22 | Prefer direct verbs over excessive nominalization. |
| P23 | Do not use fragments for artificial drama. |
| P24 | Do not repeatedly assert that something is important or critical. |
| P25 | Avoid long introductory clauses before the main point. |
| P26 | Avoid formulaic era/landscape introductions. |
| P27 | Do not mechanically summarize what was already explained. |
| P28 | Avoid identical paragraph lengths and structures. |
| P29 | Do not create a heading for every small idea. |
| P30 | Do not add executive summaries to short documents. |
| P31 | Let each section's structure fit its content. |
| P32 | Do not convert every paragraph into bullets. |
| P33 | Use numbering only for sequences, rankings, or references. |
| P34 | Do not introduce the same information multiple times. |
| P35 | Do not add paragraphs that only announce the next section. |
| P36 | Do not end every section with a miniature summary. |
| P37 | Do not repeatedly restate what the document will cover. |
| P38 | Avoid empty closing statements. |
| P39 | Do not force equal section sizes or subsection counts. |
| P40 | Do not turn a simple answer into a formal report. |
| P41 | Bold only information that benefits from emphasis. |
| P42 | Use heading capitalization consistent with the style guide. |
| P43 | Do not insert decorative separators without structural purpose. |
| P44 | Keep list nesting shallow. |
| P45 | Avoid repeating the same label-description pattern in prose. |
| P46 | Do not turn simple explanations into tables. |
| P47 | Use blockquotes for quotation or meaningful callouts. |
| P48 | Do not add emoji to technical or academic writing without reason. |
| P49 | Avoid artificial whitespace and fragmented paragraphs. |
| P50 | Maintain logical Markdown heading hierarchy. |
| P51 | Do not restate the entire question before answering. |
| P52 | Do not explain what the audience already knows. |
| P53 | Do not define a concept with the same concept. |
| P54 | Distinguish established facts from assumptions. |
| P55 | Do not stack hedges in one claim. |
| P56 | Do not weight positions equally when evidence favors one. |
| P57 | Do not manufacture opposing viewpoints. |
| P58 | Include only caveats that affect the answer. |
| P59 | Use analogies to aid understanding, not as decoration. |
| P60 | Do not repeat near-identical examples. |
| P61 | Do not confuse correlation, sequence, and causation. |
| P62 | Make important assumptions explicit. |
| P63 | Do not answer a narrow question with a broad lecture. |
| P64 | Do not make simple concepts sound complicated. |
| P65 | Establish facts before recommending a solution. |
| P66 | Never invent papers, authors, dates, DOIs, or URLs. |
| P67 | Do not add references to look academic. |
| P68 | Do not claim universal agreement without evidence. |
| P69 | Do not call ordinary findings groundbreaking. |
| P70 | Do not repeatedly summarize the same source. |
| P71 | Describe methods, datasets, and procedures precisely. |
| P72 | Distinguish observations from interpretations. |
| P73 | Document genuine methodological limitations. |
| P74 | Do not overstate results or misrepresent significance. |
| P75 | Do not report precision the evidence does not support. |
| P76 | Avoid generic statements about a topic's importance. |
| P77 | Use academic transitions only when the logic requires them. |
| P78 | Do not claim findings prove more than the design allows. |
| P79 | Represent cited sources accurately. |
| P80 | Attribute ideas, findings, and interpretations clearly. |
| P81 | Describe functionality rather than promoting it. |
| P82 | Never document unverified or unimplemented features. |
| P83 | Do not repeat the same functionality description across sections. |
| P84 | Document versions, limits, dependencies, and restrictions. |
| P85 | Use examples that match real APIs and usage. |
| P86 | Use one name for one concept throughout documentation. |
| P87 | Explain important configuration fields and their effects. |
| P88 | Document relevant errors and failure scenarios. |
| P89 | Do not add setup steps without a technical reason. |
| P90 | Keep documentation consistent with the implementation. |
| P91 | Do not introduce abstractions without a design benefit. |
| P92 | Do not build a framework for simple requirements. |
| P93 | Do not wrap existing functionality without a reason. |
| P94 | Avoid meaningless identifiers (handleData, processStuff). |
| P95 | Comments should explain intent, not restate code. |
| P96 | Do not add checks for impossible conditions without justification. |
| P97 | Never swallow errors without a deliberate recovery strategy. |
| P98 | Do not create one-off interfaces without an architectural reason. |
| P99 | Do not expose configuration users do not need. |
| P100 | Do not add dependencies for trivial functionality. |
| P101 | Remove unused functions, imports, variables, and branches. |
| P102 | Reuse existing project conventions and utilities. |
| P103 | Optimize measured bottlenecks, not imagined ones. |
| P104 | Do not introduce async where synchronous execution suffices. |
| P105 | Do not wrap errors repeatedly without adding context. |
| P106 | Follow the project's real architecture, not a universal pattern. |
| P107 | Test meaningful behavior, not duplicate assertions. |
| P108 | Do not present TODOs, mocks, or stubs as complete. |
| P109 | Do not preserve obsolete interfaces without a compatibility need. |
| P110 | Do not generate near-identical code where a shared implementation fits. |
| P111 | Avoid generic praise and exaggerated excitement. |
| P112 | Do not promise outcomes without evidence. |
| P113 | Apologize only for actual mistakes or inconvenience. |
| P114 | Do not bury the answer under formalities. |
| P115 | Avoid "Absolutely," "Certainly," and "Great question" openers. |
| P116 | Offer follow-up work only when it adds value. |
| P117 | Do not repeat limitations already explained. |
| P118 | Do not insert personal details unnecessarily. |
| P119 | Remove conversational filler that carries no information. |
| P120 | Do not end every answer with a question. |

Back to [SKILL.md](../SKILL.md).
