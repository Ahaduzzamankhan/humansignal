# Editing Guidelines and the Naturalness Engine

Version 2.1.0 · Human Signal

This file defines how Human Signal edits. It is the operational core: the sequence, the constraints, the severity model, and the verification steps. The reference files explain *what* to look for; this file governs *whether and how* to change anything.

Related: [natural-language-principles.md](natural-language-principles.md) · [ai-writing-patterns.md](ai-writing-patterns.md) · [context-awareness.md](context-awareness.md) · [../tests/meaning-preservation.md](../tests/meaning-preservation.md) · [../tests/regression-cases.md](../tests/regression-cases.md)

---

## Part I — The Naturalness Engine

The engine is a fixed sequence. Do not skip steps, and do not begin rewriting before step 13.

### Step 1 — Read the original text

Read the whole text once without editing. Note its genre, length, structure, and apparent purpose. Do not form conclusions about quality yet; first impressions are biased toward surface features.

If the text is long, read it in sections but keep the whole in view. Local improvements can damage global coherence.

### Step 2 — Understand the intended meaning

State the text's main claim or function in one sentence of your own. For each section, state its job in a phrase. If you cannot, the text is ambiguous, and the ambiguity must be resolved before style is touched.

Distinguish:
- what the text says;
- what it implies;
- what it assumes;
- what it leaves out.

### Step 3 — Identify the audience

Determine the reader's knowledge, role, and reading conditions (see [context-awareness.md](context-awareness.md)). If the audience is mixed, identify which parts serve which reader. Record the assumption.

### Step 4 — Determine the writing category

Classify the text: general prose, academic, technical, conversational, professional, creative, legal, journalistic, or a hybrid. The category selects the mode file and the relevant reference sections.

Category determines which patterns matter. A rhetorical question in an essay is normal; in an API reference it is a defect.

### Step 5 — Identify the existing author voice

List the voice's observable features:
- typical sentence length and shape;
- level of formality;
- use of first person, contractions, humor, asides;
- preferred punctuation;
- characteristic vocabulary;
- degree of directness;
- use of examples and evidence.

This list is a constraint. Edits must preserve it unless it conflicts with the genre or the reader's needs.

### Step 6 — Analyze vocabulary

Apply the vocabulary checks:
- repeated content words and whether they are topical;
- evaluative adjectives without properties;
- nominalizations and light verbs;
- collocation errors;
- synonym drift around a single referent;
- register inconsistency;
- vague quantifiers;
- jargon mismatched to the audience;
- terminology that conflicts with the project or field.

Record findings as locations plus a proposed action. Do not edit yet.

### Step 7 — Analyze sentence structure

Check:
- sentence length distribution and whether it tracks information load;
- subject–verb distance;
- main claim in main clause;
- clause nesting depth;
- passive voice where the actor matters;
- fragments;
- parallelism in lists;
- punctuation relationships;
- repeated syntactic frames.

See [sentence-structure.md](sentence-structure.md).

### Step 8 — Analyze paragraph organization

Check:
- one claim per paragraph;
- topic sentence present or inferable;
- support adjacent to claim;
- boundaries at changes of job;
- cohesion and coherence;
- paragraph length relative to importance;
- transitions that encode real relations;
- redundancy across paragraphs.

See [paragraph-analysis.md](paragraph-analysis.md).

### Step 9 — Detect unnecessary repetition

Search for:
- repeated claims in different words;
- repeated evidence;
- repeated caveats;
- repeated headings or labels;
- echoed introductions and conclusions;
- repeated sentence frames;
- redundant modifiers;
- duplicated captions.

Distinguish functional repetition (terminology, safety, topic tracking) from redundant repetition.

### Step 10 — Identify vague or unsupported claims

For each claim, ask:
- What would make this false?
- What is the source?
- What is the comparison baseline?
- What is the scope?

Flag claims that cannot be evaluated. Do not invent support. Either the writer supplies it, the claim is softened to what the text supports, or the claim is removed with a note.

### Step 11 — Identify unnatural phrasing

Look for:
- collocation errors;
- thesaurus substitutions that change meaning;
- register clashes;
- metaphors that do not map;
- over-polished or template-like constructions;
- translated syntax that does not fit English;
- idiom errors;
- over-signposting.

### Step 12 — Identify redundant explanations

Look for:
- definitions immediately restated;
- obvious consequences spelled out;
- pre-emptive justifications;
- beginner tangents in advanced text;
- section recaps that add nothing;
- meta-commentary about the writing process.

### Step 13 — Make targeted improvements

Now edit. Apply the smallest change that fixes the identified problem. Prefer deletion over replacement, and replacement over addition.

Order of operations:
1. Remove filler and redundancy.
2. Fix factual and terminological errors (or flag them).
3. Repair sentence structure where meaning was obscured.
4. Repair paragraph boundaries and progression.
5. Adjust vocabulary for precision and register.
6. Only then consider rhythm and emphasis.

Do not perform a global rewrite unless the text is incoherent or the writer asked for one. Preserve as much original wording as the problems allow.

### Step 14 — Verify semantic preservation

Compare original and revised text claim by claim. Use the protocol in [../tests/meaning-preservation.md](../tests/meaning-preservation.md). Check:
- claims and their strength;
- conditions and exceptions;
- quantities, units, dates;
- attribution and citations;
- technical terms;
- scope and generalization;
- tone and stance.

If any item changed, either restore it or record the change as intentional.

### Step 15 — Verify factual accuracy

Check every verifiable statement:
- names, numbers, versions, dates;
- commands and identifiers;
- citations and quotations;
- descriptions of behavior;
- claims about causes.

If verification is impossible, mark the claim as unverified rather than asserting it. Never add a fact to make a sentence read better.

### Step 16 — Review the final text

Read the revised text as a whole, without reference to the original. Check:
- Does it read coherently?
- Does it keep the author's voice?
- Is anything missing that the reader needs?
- Is anything present that the reader does not need?
- Does the register hold?
- Do the transitions work?
- Are there new problems introduced by the edits?

Then read the original and revised side by side one last time.

---

## Part II — Mandatory editing principles

These are constraints, not preferences. Violating one is a defect in the edit.

1. **Do not rewrite everything unnecessarily.** Preserve wording that works. The diff should be proportional to the problems.
2. **Do not introduce intentional grammatical errors.** Natural writing is not ungrammatical writing.
3. **Do not manufacture personal experience.** No invented anecdotes, credentials, or memories.
4. **Do not invent anecdotes or examples presented as real.** Illustrative examples must be labeled as illustrative.
5. **Do not artificially vary sentence lengths.** Length follows information load.
6. **Do not remove useful terminology.** Technical terms, defined terms, and standard phrases stay.
7. **Do not replace every repeated word with synonyms.** Repetition of the topic term is correct.
8. **Do not change the author's intended argument.** You may clarify it; you may not redirect it.
9. **Do not add unsupported details.** No numbers, names, dates, or causes that the source does not provide.
10. **Do not sacrifice clarity for stylistic novelty.** A plain sentence that works beats an interesting one that confuses.
11. **Do not impose an artificial personality.** No jokes, asides, or rhetorical questions the author did not use.
12. **Do not optimize for detector scores.** Quality is judged by readers, not by classifiers. See [detector-reliability.md](detector-reliability.md).
13. **Do not flatten a distinctive voice into neutral prose.** Preserve idiosyncrasy that is clear and appropriate.
14. **Do not "fix" a regional or house convention into another.** Match the declared style.
15. **Do not remove qualifications to make a claim sound stronger.** Qualifications are meaning.
16. **Do not add transitions merely to smooth the surface.** Add them only when the logical relation is unclear.

---

## Part III — Severity model

Every finding gets a severity. Severity determines whether the edit is mandatory, recommended, or optional.

| Severity | Definition | Action | Examples |
|---|---|---|---|
| **Critical** | Factually wrong, fabricated, unsafe, or legally/medically misleading | Must fix or flag; never leave unmarked | Invented citation, wrong dosage, false security claim |
| **High** | Obscures meaning, contradicts itself, or misleads the reader about scope | Rewrite the affected passage | Ambiguous instruction, unsupported causal claim, missing condition |
| **Medium** | Reduces clarity, efficiency, or credibility without changing meaning | Improve if it does not risk meaning | Formulaic opening, redundant recap, adjective stacking |
| **Low** | Stylistic preference with no clear cost | Optional; respect author voice | One em dash, a single rhetorical question, a three-item list |
| **Preserve** | A feature that looks like a pattern but is correct here | Do not change | Repeated technical term, passive voice with unknown actor, formal register in a legal text |

**Rule:** severity is assigned by effect on the reader, not by how recognizable the pattern is.

A pattern can be high-frequency and low-severity. Ten em dashes in a personal essay may be a voice choice. One wrong version number in an installation guide is critical.

---

## Part IV — Scope discipline

### Minimum effective edit

The minimum effective edit is the smallest change that removes the problem without changing anything else. It has three properties:

1. **Local:** it touches the smallest unit that contains the problem (phrase, sentence, paragraph).
2. **Sufficient:** it removes the cause, not just the symptom.
3. **Non-invasive:** it does not create a new problem elsewhere.

**Example.**
- Original: "In today's rapidly evolving landscape, teams must leverage robust solutions."
- Over-edit: a full rewrite of the paragraph in a new voice.
- Minimum effective edit: "Teams need tools that work under load." (If the original claim was that vague, the edit must also flag that no specific claim was made.)

### When a larger rewrite is justified

- The text is incoherent at the paragraph level.
- The genre is wrong for the audience.
- The structure prevents the reader from finding the answer.
- The author explicitly asks for a rewrite.
- The text contains fabricated content that cannot be isolated.

Even then, preserve the author's claims, terminology, and voice where possible.

### Diff discipline

After editing, review the diff. Ask of each change:
- What problem did this fix?
- Could a smaller change have fixed it?
- Did this change introduce a new pattern?
- Did this change alter meaning?

Revert changes that cannot answer the first question.

---

## Part V — Preservation rules

### Meaning
- Preserve the truth conditions of every claim.
- Preserve the strength of modality (*may*, *must*, *typically*).
- Preserve scope (*all*, *most*, *some*, *in this sample*).
- Preserve conditions and exceptions.
- Preserve causal vs. correlational language.
- Preserve the difference between observation and interpretation.

### Facts
- Preserve numbers, units, dates, names, versions, and identifiers exactly, unless correcting a verified error.
- Preserve quotations verbatim; mark ellipses and insertions.
- Preserve citations and their attachment to claims.
- Preserve legal and safety language.

### Voice
- Preserve register, directness, and characteristic vocabulary.
- Preserve the author's stance (confidence, skepticism, enthusiasm) where appropriate to the genre.
- Preserve deliberate stylistic devices, even unusual ones, when they are clear and consistent.

### Structure
- Preserve section order unless it obstructs the reader.
- Preserve headings that function as navigation, even if they could be more elegant.
- Preserve document conventions required by a template or venue.

### Formatting
- Preserve code blocks, tables, and figure references.
- Preserve link targets.
- Preserve required metadata.

---

## Part VI — Editing report

By default, Human Signal operates silently: the output is the revised text, not a commentary on it. Produce an editing report only when the user asks for an audit, when the text contains critical issues that the writer must know about, or when a change could not be made without altering meaning.

### Report format

```
Scope: [what was edited]
Assumptions: [audience, genre, purpose, if inferred]
Critical findings: [none, or list with locations]
Changes made: [grouped by type, with one example each]
Preserved deliberately: [patterns left alone and why]
Unresolved: [claims that need verification, ambiguities that need the author]
Meaning check: [pass / pass with noted changes / fail]
```

### What not to do in a report

- Do not list every pattern by ID; group by effect.
- Do not claim an audit that was not performed.
- Do not present stylistic preferences as errors.
- Do not include a detector score as evidence.

---

## Part VII — Common editing failures

| Failure | What it looks like | Correction |
|---|---|---|
| **Over-editing** | Every sentence reworded; voice replaced | Revert to minimum effective edits |
| **Under-editing** | Critical ambiguity left because the prose "reads fine" | Re-check claims and conditions |
| **Synonym drift** | One referent named four ways | Restore the term |
| **Flattening** | Distinctive voice replaced by neutral professional prose | Restore voice features |
| **Register clash** | Formal opening, casual body | Choose one register |
| **Transition inflation** | A connector before every sentence | Delete unnecessary connectors |
| **Artificial variation** | Length and structure alternated mechanically | Let content drive form |
| **Precision loss** | "May" became "does"; "associated" became "causes" | Restore modality and causality |
| **Fabricated support** | A number or citation added to fill a gap | Remove; flag the gap |
| **New patterns** | The edit introduces its own formula | Review the diff for repetition |
| **Genre mismatch** | Academic text made chatty, or chat made academic | Apply the mode file |
| **Terminology rewrite** | Code identifiers or API names "cleaned up" | Restore exactly |

---

## Part VIII — Quick reference

**Before editing:** purpose, audience, genre, channel, relationship, consequence, voice.

**While editing:** smallest change, preserve meaning, preserve terminology, preserve voice, no invention.

**After editing:** meaning check, fact check, voice check, diff review, read-aloud check, link check.

**Never:** fabricate, flatten, inflate, optimize for detectors, introduce errors, remove qualifications, rename technical terms.

**Always:** verify, bound claims, state uncertainty, respect genre, keep the reader's task in view.

Back to [SKILL.md](../SKILL.md).
