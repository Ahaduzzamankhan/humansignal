# Vocabulary and Lexical Analysis

Version 2.1.0 · Human Signal

Word choice is where most judgments of "natural" writing are made, and where most bad edits happen. This file explains how to analyze vocabulary without damaging precision.

Related: [sentence-structure.md](sentence-structure.md) · [natural-language-principles.md](natural-language-principles.md) · [ai-writing-patterns.md](ai-writing-patterns.md) · [context-awareness.md](context-awareness.md)

---

## 1. Word frequency

**What it measures.** How often a word appears in a text, and how that rate compares with the word's rate in the genre.

**Why it matters.** Function words (*the, of, and*) are frequent in all English. Content words are more informative: an unusually high rate of *robust, comprehensive, crucial*, or *seamless* suggests evaluative filler. An unusually low rate of pronouns and conjunctions can suggest choppy, disconnected prose.

**How to analyze.**
- Count content-word frequency, not just raw tokens.
- Compare against the document's own length: three uses in 400 words is different from three uses in 4,000.
- Separate **topic repetition** (necessary) from **evaluative repetition** (often removable).

**What not to conclude.** Frequency alone does not indicate authorship or quality. A document about caching will use "cache" often and correctly.

**Editing action.** Treat high frequency as a prompt: for each repeated content word, ask whether the repetition is the topic, a deliberate refrain, or a habit.

## 2. Lexical diversity

**What it measures.** The ratio of distinct words to total words (type–token ratio), often adjusted for length (e.g., MTLD, moving-average type–token ratio).

**Why it matters.** Very low diversity can indicate repetition; very high diversity can indicate thesaurus-driven synonym rotation that damages terminology.

**How to analyze.**
- Do not rely on raw type–token ratio: it falls automatically as texts get longer.
- Compute diversity within windows (e.g., 100-word moving windows) to see local repetition.
- Inspect the *reason* for low diversity before acting.

**Interpretation pitfalls.**
- Technical vocabulary is legitimately repetitive. A legal contract may repeat "Party" hundreds of times by design.
- High diversity is not a virtue. Replacing "tenant" with "customer," "account," and "organization" across a paragraph creates ambiguity.
- Short texts produce unstable ratios.

**Editing action.** Use diversity as a locator, not a score. Open the window with low diversity and read it.

## 3. Contextual word selection

**Principle.** A word is well chosen when it fits the referent, the register, the audience, and the surrounding collocations.

**Diagnostic questions.**
1. Does the word name the thing precisely?
2. Would the intended reader use this word in this situation?
3. Does it carry connotations the writer did not intend?
4. Does it collide with a nearby word (repetition, rhyme, ambiguity)?
5. Is it consistent with how the text names the same thing elsewhere?

**Example.**

| Weak | Why | Better |
|---|---|---|
| "utilize a mechanism" | vague noun + inflated verb | "use a retry queue" |
| "significant uplift" | two evaluative abstractions | "12% more sign-ups" |
| "leverage the API" | jargon verb with unclear object | "call the `/v2/events` endpoint" |

**Rule.** Precision beats elegance. If the precise word is plain, use the plain word.

## 4. Collocations

**What they are.** Words that habitually occur together: *make a decision* (not *do a decision*), *heavy rain* (not *strong rain*), *commit a change* (in version control).

**Why they matter.** Unnatural collocations are one of the clearest signals of text assembled word by word rather than written from familiarity with the language. They also slow reading, because the reader's prediction is violated.

**Common problem types.**
- **Verb–noun mismatch:** "perform a conclusion," "conduct an improvement."
- **Adjective–noun mismatch:** "a strong argument" vs. "a powerful argument" (both exist, different force), "high latency" (correct) vs. "tall latency" (wrong).
- **Preposition mismatch:** "dependent of" (should be *on*), "responsible of" (should be *for*).
- **Technical collocations:** "raise an exception" (Python), "throw an exception" (C++/Java), "open a pull request" (not "make a pull request" in most teams).

**How to check.** Read the phrase aloud; ask whether you have seen it in published prose of this kind. For technical terms, check the project's own usage.

**Editing action.** Fix clear mismatches. Do not "improve" a correct but plain collocation into a rarer one.

## 5. Synonym appropriateness

**Principle.** Synonyms overlap in some senses and diverge in others. Substitution is safe only when the relevant sense, connotation, and grammar match.

**Dimensions of difference.**
- **Register:** *ask / request / petition*.
- **Intensity:** *warm / hot / scorching*.
- **Evaluation:** *thrifty / stingy / economical*.
- **Grammar:** *allow someone to do* vs. *permit someone to do* (similar); *suggest* takes a clause, *recommend* can take a gerund.
- **Domain:** *client* (business), *patient* (medicine), *user* (software).

**The synonym trap.** Replacing a repeated word to "improve variety" often produces a near-miss: "The tenant's data is isolated. The customer's records are separated. The account's information is partitioned." The reader now wonders whether tenant, customer, and account are the same entity.

**Rule.** Repeat the term when the referent is the same. Vary when the referent or the level of abstraction changes.

## 6. Repeated expressions

**What counts.** Multi-word strings repeated across the document: "in order to," "it is important to note," "plays a key role," "at the end of the day."

**Why they matter.** Repeated expressions are more noticeable than repeated single words and often mark filler.

**Analysis method.**
- Extract 3- to 5-word n-grams and sort by count.
- Filter out necessary technical phrases ("content security policy").
- Read the remaining high-frequency phrases in context.

**Editing action.**
- Delete filler expressions outright.
- If the expression carries meaning, keep one instance and rewrite the others.
- Do not replace a meaningful phrase with a synonym phrase just to reduce the count.

## 7. Redundant modifiers

**Definition.** A modifier that repeats information already present in the head word or in another modifier.

**Types.**
- **Semantic redundancy:** *free gift*, *past history*, *final outcome*, *advance planning*.
- **Category redundancy:** *ATM machine*, *PIN number*, *LCD display*.
- **Adjective stacking:** *large big house*.
- **Adverb–verb redundancy:** *shout loudly*, *whisper quietly*, *completely destroy*.

**Exceptions.** Some redundant-looking phrases are fixed terms (*null and void*, *cease and desist*) or carry a legal/technical function. Do not edit terms of art.

**Editing action.** Remove the redundant element, then verify that no nuance was lost. *Complete destruction* differs from *damage*; the redundancy may be doing work.

## 8. Domain-specific terminology

**Principle.** Technical terms are not decoration. They are compressed, precise references to concepts the audience shares.

**Rules.**
1. **Never rename a term for variety.** If the code calls it `tenant_id`, the documentation calls it `tenant_id`.
2. **Define on first use only if the audience may not know it.** Otherwise, use it.
3. **Preserve capitalization, hyphenation, and spelling** established by the project or standard.
4. **Distinguish near-terms carefully:** *authentication* vs. *authorization*, *latency* vs. *response time*, *concurrency* vs. *parallelism*.
5. **Do not replace a term with a plain-language gloss in the same sentence** unless the gloss is marked as such; it reads as hesitation.

**Editing action.** Treat terminology as data. Check the glossary, the codebase, or the standard before changing a term.

## 9. Register consistency

**Definition.** Register is the configuration of formality, technicality, and social distance in a text.

**Markers of register.**
- Contractions (*don't* vs. *do not*)
- Pronoun use (*you* vs. *the user* vs. *one*)
- Phrasal verbs vs. Latinate verbs (*set up* vs. *configure*)
- Sentence complexity
- Directness of directives (*Run this* vs. *This should be run*)
- Humor, asides, emoji

**Analysis.** Sample the opening, middle, and end of the document. If the register shifts without a reason, flag it.

**Common mismatch.** A README that opens with a formal abstract and then says "just run `make` and you're good to go." Both registers are fine; the transition is not signposted, so the reader is unsure who the document is for.

**Editing action.** Choose one register per section, or mark deliberate shifts ("For a plain-language overview, see…").

## 10. Semantic precision

**Definition.** A word is semantically precise when its boundaries are clear enough that the reader can tell what it includes and excludes.

**Imprecise words and their costs.**
- *Fast* — relative to what?
- *Secure* — against which threat model?
- *Scalable* — in which dimension, to what load?
- *Improved* — measured how?
- *Several* — how many?
- *Often* — at what rate?

**Precision tests.**
1. **Substitution test:** replace the word with a more specific one. If the sentence becomes clearer and no meaning is lost, the original was vague.
2. **Falsification test:** what observation would make the claim false? If none, the word is empty.
3. **Boundary test:** where does the word stop applying? If the text cannot say, the concept is underspecified.

**Caution.** Precision is not the same as numbers. "The service is unavailable during the migration window" is precise without a figure.

## 11. Vocabulary complexity

**Definition.** Complexity combines word length, morphological complexity, and abstraction.

**Why it matters.** Complexity imposes reading cost. It is justified when it buys precision (a technical term, a legal distinction), not when it buys an impression of seriousness.

**Signs of unjustified complexity.**
- Latinate abstractions where a verb exists: *endeavor, commence, utilize, facilitate*.
- Nominalizations: *the utilization of*, *the implementation of*.
- Multiple abstractions in one clause: *the optimization of resource allocation efficiency*.
- Rare words used with imprecise meaning.

**Signs of justified complexity.** A term of art that has no plain equivalent without losing precision; a standard phrase from the field; a word whose connotation is exactly the intended one.

**Editing action.** Simplify until precision would be lost, then stop.

## 12. Unnecessary jargon

**Definition.** Jargon is vocabulary specific to a group. It is unnecessary when the audience is outside the group, or when a common word is available and equally precise.

**Types.**
- **Corporate jargon:** *synergy, alignment, optics, bandwidth* (as attention), *circle back*.
- **Technical jargon used outside its domain:** *orthogonal* for "unrelated," *idempotent* for "safe to repeat."
- **Invented jargon:** *learnings, solutioning, deliverable-oriented*.
- **Abbreviations** introduced without definition.

**Distinguish from necessary terminology.** A Kubernetes operator manual must use *pod*, *kubelet*, and *admission controller*. A general introduction should not.

**Editing action.** Replace jargon with plain language when the audience is general. Keep it when the audience is specialist and the term is standard.

## 13. Generic expressions

**Definition.** Phrases that could appear in almost any document on almost any topic.

**Examples.**
- "In today's fast-paced world…"
- "plays a crucial role"
- "a wide range of"
- "various factors"
- "it is important to note"
- "the key takeaway is"
- "on the other hand" (when there is no real contrast)

**Why they weaken.** They carry no specific information, and they signal that the writer has not yet found the concrete claim.

**Recognition.** Ask: could this sentence appear unchanged in a different document about a different subject? If yes, it is generic.

**Editing action.** Delete, or replace with the specific fact the generic phrase was standing in for. Do not replace one generic phrase with another.

## 14. Word-choice ambiguity

**Definition.** A word or phrase admits more than one reading, and the difference matters.

**Sources.**
- **Polysemy:** *bank*, *table*, *host*, *run*.
- **Pronoun ambiguity:** "The service calls the API, then it retries." (What is *it*?)
- **Attachment ambiguity:** "the log of the failed job with retries" (which noun does *with retries* modify?)
- **Scope ambiguity:** "All users can view reports and export data." (Can all users export?)
- **Quantifier ambiguity:** "Most failures occur after three retries." (Most of what?)
- **Modality ambiguity:** "The client may retry." (permission or possibility?)

**Detection.** Read the sentence as if you were a hostile reader looking for a different interpretation. If you find one, fix it.

**Editing action.** Prefer explicit reference, clear attachment, and unambiguous quantifiers. Do not add words that remove ambiguity only by making the sentence unreadable; restructure instead.

## 15. Repeated transition vocabulary

**Definition.** The overuse of a small set of connectives to mark relationships.

**Common set.** *Furthermore, moreover, additionally, however, therefore, thus, consequently, nevertheless, in addition, on the other hand, ultimately.*

**Why it matters.** Transitions should encode logical relations. When they are used as paragraph decoration, the reader learns to ignore them, and the real logical signals lose force.

**Analysis.**
- List every sentence-initial connective.
- For each, name the relation it encodes (addition, contrast, cause, consequence, example, concession).
- Check whether the relation is real.

**Repair strategies.**
- Delete the connective when the relation is clear from the content.
- Replace with a precise connective when the relation is specific (*because*, *so*, *by contrast*, *for example*).
- Restructure so the relation is carried by the sentence order rather than a label.

**Example.**
- Original: "Furthermore, the cache reduces load. Moreover, it lowers latency. Additionally, it simplifies retries."
- Revised: "The cache reduces database load and lowers latency; it also makes retries cheaper, because a failed request can often be served from memory."

The revision keeps one additive signal and adds the mechanism that connects the three claims.

---

## Diagnostic checklist

For any passage, answer these in order:

1. **Topic terms:** Which words name the central concepts? Are they used consistently?
2. **Evaluative words:** Which words rank or praise? What property do they refer to?
3. **Repeated phrases:** Which multi-word strings recur? Which carry meaning?
4. **Collocations:** Which verb–noun or adjective–noun pairs feel off?
5. **Register:** Are contractions, pronouns, and complexity consistent?
6. **Precision:** Which claims cannot be falsified because a word is too vague?
7. **Ambiguity:** Where could a careful reader take a different meaning?
8. **Terminology:** Has any technical term been renamed, abbreviated, or paraphrased?

---

## Rules for editors

1. **Do not replace a repeated technical term with a synonym.**
2. **Do not simplify a term of art into a vague paraphrase.**
3. **Do not add evaluative adjectives to make a sentence sound stronger.**
4. **Do not replace a plain word with a rare one to avoid repetition.**
5. **Do not introduce jargon the audience does not share.**
6. **Do simplify nominalizations, light verbs, and empty modifiers.**
7. **Do preserve the author's register unless the genre requires otherwise.**
8. **Do check the project's own vocabulary before changing names.**
9. **Do prefer one precise word over two approximate ones.**
10. **Do stop simplifying when the next step would lose meaning.**

Back to [SKILL.md](../SKILL.md).
