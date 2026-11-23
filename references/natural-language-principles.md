# Natural Language Principles

Version 2.1.0 · Human Signal

Natural writing is not a style. It is writing in which every choice — word, clause, order, length, level of detail — is explained by the situation. This file sets out the principles that guide those choices, and the difference between variation that serves meaning and variation that only looks like it.

Related: [ai-writing-patterns.md](ai-writing-patterns.md) · [sentence-structure.md](sentence-structure.md) · [vocabulary-analysis.md](vocabulary-analysis.md) · [paragraph-analysis.md](paragraph-analysis.md) · [context-awareness.md](context-awareness.md)

---

## 1. Natural vocabulary selection

Word choice is natural when it matches three things at once: the referent (what is being named), the register (how formal the situation is), and the reader's expected vocabulary.

A natural word is usually the most **specific** word the audience will recognize. "Tool" is natural when the kind of tool does not matter. "Static analyzer" is natural when it does. Precision is not the same as rarity: "use" is more precise than "utilize" in most sentences because "utilize" adds a claim about productive use that the writer usually does not mean.

Judgments of naturalness should be based on the sentence's job, not on a list of banned words. A word is a problem when:

- it names the thing less accurately than an available alternative;
- it belongs to a different register than the surrounding text;
- it repeats a nearby word with no gain in meaning;
- it signals a claim the sentence does not support ("robust" without a failure mode).

See [vocabulary-analysis.md](vocabulary-analysis.md) for diagnostic tests.

## 2. Context-sensitive phrasing

The same proposition has many correct phrasings. Which one is natural depends on:

| Factor | Question it answers |
|---|---|
| Audience | What does the reader already know and expect? |
| Purpose | Is the reader deciding, learning, verifying, or being persuaded? |
| Channel | Is this a report, a chat message, a commit message, a label? |
| Consequence | What happens if the reader misreads it? |
| Relationship | How much shared context exists between writer and reader? |
| Genre | What conventions does the reader's community enforce? |

A phrase that is natural in one cell of that table can be wrong in another. "Ship it" is natural in a team chat and wrong in a release note. "The system shall…" is natural in a specification and wrong in a tutorial.

Context sensitivity is not license for vagueness. It means choosing the form that the situation makes readable. See [context-awareness.md](context-awareness.md).

## 3. Sentence rhythm

Rhythm in prose is the pattern of stressed and unstressed information, carried by sentence length, clause order, and the position of the main verb.

Three observations matter more than any rule:

1. **Rhythm follows content.** A short sentence after a long one creates emphasis because the short sentence carries a conclusion. If it carries no conclusion, the rhythm is empty.
2. **Monotony is a symptom, not a cause.** Sentences of identical length usually mean the writer treated every idea as equally important. Fix the thinking, and the rhythm often fixes itself.
3. **Rhythm is heard, not counted.** Reading aloud reveals collisions — repeated sounds, accidental rhymes, three clauses that all end the same way — that a word count will not.

Do not "vary sentence length" as a mechanical operation. Vary the amount of information per sentence according to its role, and length variation follows.

## 4. Paragraph cohesion

Cohesion is the set of links that make consecutive sentences read as one unit. English offers several kinds:

- **Reference:** pronouns and demonstratives ("this limit," "that failure") pointing to earlier content.
- **Lexical repetition:** repeating a key term so the reader knows the topic has not changed.
- **Synonyms and generalizations:** "the parser… the component…" — useful only when the reader can tell they refer to the same thing.
- **Connectors:** *because*, *but*, *so*, *for example* — explicit logical links.
- **Parallel structure:** sentences with the same shape signalling that they belong to a list.
- **Given-new ordering:** starting with information the reader already has, ending with the new information.

Cohesion fails in two ways. Too little, and the reader cannot tell how sentences relate. Too much, and the text is over-signposted, with every sentence announcing its relation to the last. Both are quality problems; the second is more common in heavily templated text.

Coherence is different from cohesion. Cohesion is the surface linking; coherence is whether the paragraph's ideas actually belong together. A paragraph can be flawlessly cohesive and still incoherent.

## 5. Natural information ordering

Readers process a sentence by attaching new information to old. The most natural order therefore usually runs:

**known → new**, and **cause → effect**, and **condition → consequence**, and **general → specific** (or specific → general, if the specific case is the point).

Three practical consequences:

- **Put the topic first.** The grammatical subject should be the thing the sentence is about, not an empty frame ("There are…", "It is important to note that…").
- **Keep the main verb close to the subject.** Long insertions between subject and verb force the reader to hold the subject in memory.
- **End with the information that matters.** The end of a sentence is the natural stress position. Do not waste it on a qualifier or a citation marker.

Information order is not fixed. Inverted order can create suspense or emphasis, and in some genres (news, abstracts) the conclusion comes first by convention. The test is whether the order helps the intended reader do the intended job.

## 6. Conciseness

Concise writing removes words that do not change the reader's understanding, decision, or action. It does not remove information.

Common sources of avoidable length:

- **Frames:** "When it comes to X," "In order to," "The fact that."
- **Nominalizations:** "the implementation of" → "implementing."
- **Doubled modifiers:** "basic fundamentals," "future plans."
- **Redundant pairs:** "each and every," "first and foremost."
- **Restatement:** defining a term, then redefining it.
- **Meta-commentary:** telling the reader what the text will do.
- **Over-explanation:** teaching what the audience already knows.

Conciseness has a floor. Removing a qualification, a scope statement, or a definition can make a sentence shorter and less true. The test is **information per unit of reader effort**, not words per sentence.

## 7. Appropriate specificity

Specificity is the degree to which a statement constrains what could count as evidence against it.

- Vague: "Performance improved."
- Specific: "The p95 response time fell from 800 ms to 200 ms after the index change."

Specificity is appropriate when the reader needs the detail to act, verify, or compare. It is excessive when the detail does not change any decision and costs reading effort (a p-value quoted for a design choice, a version number in a conceptual overview).

Two rules:

1. **Prefer the specific over the general when both are available and the specific matters.**
2. **Never invent specificity.** A precise-looking number without a source is worse than an honest range.

## 8. Logical progression

An argument progresses when each step depends on the previous one and adds something the conclusion needs.

Signs of weak progression:

- The same point appears in two sections with different wording.
- A conclusion appears before its evidence and is then never supported.
- A section answers a question the previous section did not raise.
- Examples illustrate a claim made three paragraphs later.
- The text moves between levels (principle, implementation, anecdote) without signalling the shift.

Signs of strong progression:

- Each paragraph's first sentence connects to the previous paragraph's last idea.
- Claims and evidence stay adjacent.
- Exceptions follow the rule they limit.
- The conclusion depends on the body rather than repeating it.

Outlining by **claim, evidence, implication** is a reliable check. If a paragraph cannot be summarized in that form, it may be doing two jobs at once.

## 9. Semantic consistency

A text is semantically consistent when a term means the same thing throughout, and when statements do not contradict each other.

Technical writing depends on this more than literary writing. If "job" means a unit of work in one section and a scheduled task in another, the reader will misread one of them. If "fast" means under 100 ms in the introduction and under one second in the results, the claim has quietly changed.

Consistency checks:

- Build a short glossary of recurring terms and their definitions.
- Search for synonyms of key terms; confirm each substitution is intentional.
- Check numbers, units, and dates across sections.
- Check that scope statements in the introduction match the analysis.

## 10. Audience awareness

Audience awareness is the practice of writing for the knowledge, goals, and constraints of the actual reader — not an imagined average.

Questions to answer before editing:

- What does the reader already know? (Determines how much to explain.)
- What are they trying to do? (Determines order and detail.)
- What will they do with the text? (Read once? Follow as instructions? Cite? Skim?)
- What will they get wrong if a sentence is ambiguous? (Determines how much redundancy is warranted.)
- What register do they expect? (Determines formality.)

A common failure is writing for two audiences at once without signposting which parts serve which. A README can serve both evaluators and operators, but the quick start and the architecture notes should be visibly separate.

## 11. Register consistency

Register is the level of formality and the set of conventions a text uses. It includes contractions, pronoun choice, terminology, sentence complexity, and directness.

Register should be **consistent within a document** except where a deliberate shift serves a purpose (a plain-language summary after a technical section, a quoted colloquial source in a formal paper).

Inconsistent register shows up as:

- A formal introduction followed by chatty bullets.
- Technical terms mixed with vague marketing language.
- Contractions in one paragraph and "shall" constructions in the next.
- Jokes in a risk assessment.

Consistency does not mean monotony. It means the reader always knows what kind of text they are reading.

## 12. Author voice preservation

Voice is the pattern of choices that makes a writer recognizable: preferred sentence shapes, degree of directness, use of examples, humor, hedging, punctuation habits.

When editing someone else's text, preserve voice unless the voice itself is the problem (for example, a voice that is inappropriate for the genre). Practical rules:

- Keep distinctive word choices that are accurate, even if you would not choose them.
- Keep the writer's level of formality.
- Keep idiosyncratic but clear punctuation if it is consistent.
- Do not add personality markers — jokes, asides, rhetorical questions — that the writer did not use.
- Do not flatten a distinctive style into neutral professional prose.

The goal is the writer's clearest version of their own text, not a version that sounds like the editor.

## 13. Clear explanations

A clear explanation does four things:

1. **Names the thing** being explained.
2. **States why it matters** in the reader's terms.
3. **Gives the mechanism** — how it works, in the order it happens.
4. **Bounds it** — when it applies, when it fails, what it costs.

Explanations fail when they:

- define a term with a synonym the reader also does not know;
- give an example before the reader knows what it exemplifies;
- explain the mechanism but never the purpose;
- state the purpose but never the mechanism;
- omit the failure condition, leaving the reader to discover it in production.

Analogies can help, but only when the mapping is tight and the text marks where it breaks. See AWP-119.

## 14. Appropriate formality

Formality is a cost the writer imposes on the reader in exchange for distance, precision, or ceremony. It is appropriate when the situation requires that distance: legal documents, regulatory submissions, formal correspondence with unfamiliar parties, certain academic genres.

It is inappropriate when it is borrowed from another genre without need. A two-line status update does not need "Please be advised." A tutorial does not need "the user shall."

A useful test: would a knowledgeable member of the target audience find the formality normal for this genre? If not, the formality is costume.

## 15. Information density

Information density is the amount of new, relevant content per sentence. Dense writing is not the same as difficult writing.

Ways to raise density without raising difficulty:

- Replace vague verbs with specific ones.
- Replace evaluative adjectives with properties or numbers.
- Cut frames and restatements.
- Put the condition next to the consequence.
- Use a table when several items share the same attributes.

Ways density becomes harmful:

- Packing three claims into one sentence with ambiguous attachment.
- Using abbreviations before defining them.
- Omitting the connective logic that lets the reader follow the inference.
- Assuming knowledge the audience does not have.

The target is the highest density the intended reader can process comfortably — not the highest density possible.

## 16. Natural emphasis

Emphasis should come from **position, structure, and evidence**, not from typography or intensifiers.

Natural emphasis techniques:

- Put the important information at the end of the sentence.
- Give the important point its own short sentence.
- Use a paragraph break before a key claim.
- Repeat a key term deliberately at the point where it matters.
- Provide the number or consequence that makes the point land.

Unnatural emphasis:

- Bold on every third phrase.
- "Crucially," "importantly," "it is essential to note" before ordinary statements.
- Stacked intensifiers.
- Exclamation marks in formal prose.
- Dramatic one-line paragraphs used repeatedly.

If everything is emphasized, nothing is.

## 17. Contextual relevance

Every sentence should earn its place by serving the reader's task. Contextual relevance is the test of whether it does.

Questions:

- Does this sentence help the reader decide, do, verify, or understand something they came for?
- Does it repeat something already established?
- Does it introduce a topic the document never returns to?
- Does it answer a question no one asked?
- Does it belong in this section, or in an appendix, or nowhere?

Relevance is judged against the document's stated purpose, not against the writer's interest. An interesting aside is still an aside.

---

## Natural variation versus artificial variation

This distinction is central to Human Signal. Both produce surface difference; only one improves the text.

| | Natural variation | Artificial variation |
|---|---|---|
| **Source** | Changes in what the sentence needs to do | A rule that consecutive sentences must differ |
| **Sentence length** | Follows information load | Alternates on a schedule |
| **Vocabulary** | Follows precision and audience | Replaces words to avoid repetition |
| **Structure** | Follows logical relations | Rotates syntactic templates |
| **Effect** | Invisible; the reader follows the content | Visible; the reader notices the style |
| **Failure mode** | None, if meaning is preserved | Distortion, vagueness, and loss of terminology |

### Why random restructuring fails

1. **It breaks terminology.** Replacing "cache" with "buffer," "store," and "memory layer" across a paragraph makes the reader wonder whether these are different things.
2. **It damages given-new order.** Moving the subject to the end to "vary the opening" can separate the topic from what the sentence says about it.
3. **It creates false emphasis.** A short sentence in a new position looks important even when it is not.
4. **It can change meaning.** Passive-to-active conversion requires knowing the actor; if the actor is unknown, the conversion invents one.
5. **It is detectable as a pattern in itself.** Mechanical variation is just a different template.

### What to vary, and why

Vary a feature only when the content gives a reason:

- **Length:** because one idea is a conclusion and another is a qualification.
- **Opening:** because the topic changed, or because the previous sentence ended on the new topic.
- **Voice:** because the actor matters in one sentence and does not in another.
- **Structure:** because one relationship is causal, another contrastive, another sequential.
- **Vocabulary:** because a general term is needed after specific ones, or because a technical term must be introduced.

When no such reason exists, leave the sentence alone. Consistency is not a flaw.

### A worked contrast

**Mechanical variation (bad):**

> The cache stores hot rows. Frequently accessed records are kept in memory by the system. Data that is read often resides in a fast-access layer.

Three sentences, three synonyms, one fact. The variation makes the reader search for a distinction that does not exist.

**Natural variation (good):**

> The cache stores hot rows in memory. Reads for those rows skip the database. When a row changes, the cache entry is invalidated, so the next read pays the full query cost.

Same opening subject, but the sentences differ because each adds a new mechanism: storage, effect, invalidation. The repetition of "cache" and "row" is correct — it is the topic.

---

## A short diagnostic sequence

Use this when a passage feels unnatural but the problem is not obvious:

1. **Read it aloud.** Note where you stumble. Stumbles usually mark a broken given-new link or a clause that arrived too late.
2. **Underline the topic of each sentence.** If the topics jump without reason, the paragraph lacks a through-line.
3. **Circle the main verb in each sentence.** If verbs are far from subjects, or nominalized, rewrite.
4. **Mark every evaluative word.** Ask what property it refers to.
5. **Find the claim and its evidence.** If they are more than two sentences apart, bring them together.
6. **Delete the first and last sentence of each paragraph.** If nothing is lost, they were frames.
7. **Check the genre.** Compare with two good examples in the same genre.

---

## Principles in one page

1. Every choice should have a reason grounded in meaning, audience, or genre.
2. Specific beats general when the specific is available and relevant.
3. Repeat terms when repetition aids clarity; vary them when it does not.
4. Put known information before new information.
5. Let sentence length follow information load.
6. Keep claims next to their evidence.
7. Preserve qualifications; they are part of the meaning.
8. Match register to genre and relationship.
9. Preserve the author's voice unless it conflicts with the genre.
10. Never manufacture specificity, experience, or certainty.
11. Prefer clarity over stylistic novelty.
12. Judge naturalness by whether the reader can follow the text, not by whether it resembles a human sample.

Back to [SKILL.md](../SKILL.md).
