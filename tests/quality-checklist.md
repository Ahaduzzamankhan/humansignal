# Quality Checklist

Version 2.1.0 · Human Signal

A practical review sheet for any text edited with Human Signal. Use it after editing, not instead of the editing workflow in [../references/editing-guidelines.md](../references/editing-guidelines.md).

**How to score:** each item is marked **Pass**, **Fail**, or **N/A**. A fail requires either a fix or a recorded reason for leaving the text as it is. Do not mark an item pass without checking the specific evidence named in the "Check" column.

---

## A. Natural expression

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| A1 | Sentences read without stumbling | Read aloud; note every place you re-read | |
| A2 | Word order follows given-new information | Topics connect to the previous sentence | |
| A3 | No template-like frames remain | No repeated "In today's…", "It is important to note…" | |
| A4 | Rhythm follows information load | Short sentences carry conclusions or decisions | |
| A5 | No artificial variation | Length and structure were not alternated mechanically | |
| A6 | Idiom and collocation are correct | No "make a conclusion," "dependent of" | |
| A7 | Figurative language maps to the subject | Each metaphor names a property it transfers | |

**Failure examples:** a paragraph of nineteen 20-word sentences; a thesaurus swap that changes meaning; a metaphor that implies a false mechanism.

---

## B. Clear communication

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| B1 | Main claim is identifiable | Can state it in one sentence | |
| B2 | Main claim is in the main clause | Not buried after "although" or "while" | |
| B3 | No ambiguous pronouns | Every "it," "this," "they" has one referent | |
| B4 | No ambiguous attachment | Modifiers sit next to what they modify | |
| B5 | Conditions precede consequences | "If X, then Y" rather than the reverse | |
| B6 | Quantifiers are precise | "Most," "some," "several" are defined or replaced | |
| B7 | Instructions have observable success criteria | Reader can tell whether the step worked | |

**Failure examples:** "The service calls the API, then it retries if it fails"; a step that says "verify it works" with no expected output.

---

## C. Contextual vocabulary

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| C1 | Terminology is consistent | One term per concept throughout | |
| C2 | Register matches the genre | No chat idioms in a report, no ceremony in chat | |
| C3 | Jargon matches the audience | Terms defined or standard for the reader | |
| C4 | Evaluative adjectives are supported | Each has a property or measure nearby | |
| C5 | No synonym drift | Key referents are not renamed for variety | |
| C6 | Technical terms preserved | Identifiers, API names, units unchanged | |
| C7 | No invented jargon | No "solutioning," "future-proofed" without definition | |

**Failure examples:** tenant/customer/account/organization used for one entity; "robust" with no failure mode; `timeout` renamed to `timeLimit` in prose but not in code.

---

## D. Logical sentence construction

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| D1 | Grammatical sentences | Subject–verb agreement, complete clauses | |
| D2 | No comma splices | Independent clauses joined correctly | |
| D3 | Subordination matches importance | Main claim in main clause | |
| D4 | Voice matches agency | Actor named when responsibility matters | |
| D5 | Parallel items are parallel | Same grammatical form in lists | |
| D6 | Fragments are intentional | Fragments only where the genre supports them | |
| D7 | Punctuation encodes real relations | Colons introduce, semicolons join related clauses | |

**Failure examples:** "The migration is risky, it touches 40 tables"; a list mixing gerunds, infinitives, and nouns.

---

## E. Paragraph cohesion

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| E1 | One claim per paragraph | Paragraph can be summarized in one sentence | |
| E2 | Support is adjacent to claim | Evidence within a sentence or two | |
| E3 | Topic sentence is present or inferable | First or last sentence states the point | |
| E4 | Boundaries fall at changes of job | New paragraph when the function changes | |
| E5 | Links are explicit where needed | Key term repeated or relation stated | |
| E6 | No over-signposting | Connectors only where the relation is unclear | |
| E7 | Length reflects weight | Major claims get more space than caveats | |

**Failure examples:** a paragraph covering two unrelated claims; every paragraph ending with a recap; a connector at the start of every sentence.

---

## F. Appropriate formality

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| F1 | Register is consistent within sections | No formal opening and casual body | |
| F2 | Formality matches the relationship | Peer messages are not ceremonial | |
| F3 | Consequence-appropriate precision | High-stakes text has explicit conditions | |
| F4 | No euphemism for material facts | Layoffs, failures, risks stated plainly | |
| F5 | Politeness is proportionate | One marker per request, not four | |
| F6 | No forced personality | No jokes or asides the author did not use | |

**Failure examples:** "Please be advised" in a two-line chat; "right-sized" for layoffs in an internal memo.

---

## G. Author voice consistency

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| G1 | Voice features identified before editing | Recorded list of register, rhythm, vocabulary | |
| G2 | Distinctive choices preserved | Unusual but clear phrasing retained | |
| G3 | No invented personality | No added humor, rhetorical questions, or asides | |
| G4 | Formality level preserved | Unless the genre requires a change | |
| G5 | Stance preserved | Confidence or skepticism unchanged | |
| G6 | No flattening | Text does not read like generic professional prose | |

**Note:** voice preservation is judged against the original, not against a preference for how the text "should" sound.

---

## H. Factual accuracy

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| H1 | Numbers, units, dates unchanged or corrected | Diff against source | |
| H2 | Identifiers match implementation | Code, API, config checked | |
| H3 | Citations verified | Each source exists and supports the claim | |
| H4 | No fabricated examples | Illustrations labeled as illustrative | |
| H5 | No unsupported causal claims | Verb matches design | |
| H6 | No invented specificity | No precise figure without a source | |
| H7 | Time-sensitive claims dated | "Currently" replaced by a date or version | |

**A fail here is critical.** Do not deliver a text with an unverified factual claim presented as fact.

---

## I. Grammatical correctness

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| I1 | Agreement | Subject and verb, pronoun and antecedent | |
| I2 | Tense consistency | Timeline is coherent | |
| I3 | Article and preposition use | No "dependent of," "in the Monday" | |
| I4 | Complete clauses | No accidental fragments | |
| I5 | Correct punctuation | No comma splices, no dangling modifiers | |
| I6 | Consistent spelling variety | US or UK, not mixed | |
| I7 | Consistent style mechanics | Serial comma, dash spacing, capitalization | |

---

## J. No unnecessary repetition

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| J1 | No repeated claims | Each claim appears once | |
| J2 | No repeated evidence | Each source used once per claim | |
| J3 | No repeated caveats | Scope stated once, where it applies | |
| J4 | No echoed intro/conclusion | Conclusion adds consequence or limit | |
| J5 | Repetition of terminology is intentional | Topic terms repeat correctly | |
| J6 | Functional repetition preserved | Safety warnings, legal terms, key definitions | |
| J7 | No duplicated headings or captions | Heading does not restate title; caption adds analysis | |

---

## K. Structure and genre fit

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| K1 | Genre conventions met | Compare with two competent examples | |
| K2 | Sections have distinct jobs | No two sections do the same work | |
| K3 | Navigation aids are accurate | Headings, TOC, links match content | |
| K4 | Length matches purpose | No padding, no missing prerequisites | |
| K5 | Formatting is functional | Lists, tables, and bold used for a reason | |
| K6 | Channel-appropriate | Chat is not a report; report is not a chat | |

---

## L. Detector independence

| # | Check | Evidence to look for | Result |
|---|---|---|---|
| L1 | No detector score used as a quality criterion | Scores absent from the rationale | |
| L2 | No manipulation for detection | No paraphrase done solely to lower a score | |
| L3 | Quality judged by reader effect | Findings explained in terms of comprehension | |
| L4 | Uncertainty stated where relevant | No authorship claims from style | |

See [../references/detector-reliability.md](../references/detector-reliability.md).

---

## Scoring summary

| Section | Items | Pass | Fail | N/A |
|---|---:|---:|---:|---:|
| A. Natural expression | 7 | | | |
| B. Clear communication | 7 | | | |
| C. Contextual vocabulary | 7 | | | |
| D. Logical sentence construction | 7 | | | |
| E. Paragraph cohesion | 7 | | | |
| F. Appropriate formality | 6 | | | |
| G. Author voice consistency | 6 | | | |
| H. Factual accuracy | 7 | | | |
| I. Grammatical correctness | 7 | | | |
| J. No unnecessary repetition | 7 | | | |
| K. Structure and genre fit | 6 | | | |
| L. Detector independence | 4 | | | |
| **Total** | **78** | | | |

### Release thresholds

- **Critical fail (H):** do not deliver. Fix or flag every item.
- **More than two fails in A–E:** revise before delivery.
- **Any fail in G:** re-check whether the edit flattened the voice.
- **Fails in L:** remove detector-based reasoning from the edit rationale.

---

## Reviewer sign-off

```
Text: ______________________________
Genre / mode: ______________________
Audience: __________________________
Reviewer: __________________________
Date: ______________________________

Critical findings: __________________
Fixes applied: _____________________
Items left as-is (reason): __________
Meaning check: pass / pass with notes / fail
Voice check: pass / fail
Link check: pass / n/a

Signature: _________________________
```

---

## Ten-minute quick pass

When a full checklist is impractical, run these ten checks in order:

1. Can I state the main claim in one sentence?
2. Is the claim in the main clause, near the front?
3. Does every paragraph do one job?
4. Is every number, name, and identifier verified?
5. Is any claim stronger than its evidence?
6. Is any term renamed for variety?
7. Is the register consistent?
8. Does the conclusion add something?
9. Did I preserve the author's voice?
10. Did I introduce a new pattern while removing one?

If any answer is "no" or "unsure," do not deliver yet.

Back to [SKILL.md](../SKILL.md).
