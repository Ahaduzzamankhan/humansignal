# Context Awareness

Version 2.1.0 · Human Signal

Writing quality is not a property of sentences in isolation. The same sentence can be excellent in one setting and wrong in another. This file explains the contextual variables Human Signal evaluates before editing, and how to adapt without imposing a single style.

Related: [natural-language-principles.md](natural-language-principles.md) · [../modes/academic.md](../modes/academic.md) · [../modes/technical.md](../modes/technical.md) · [../modes/conversational.md](../modes/conversational.md) · [../modes/professional.md](../modes/professional.md) · [../modes/creative.md](../modes/creative.md)

---

## 1. The six contextual variables

Every editing decision depends on six variables. Establish them before changing a sentence.

| Variable | Question | What it changes |
|---|---|---|
| **Purpose** | What must the reader be able to do or believe after reading? | Structure, detail, directness |
| **Audience** | Who is reading, and what do they already know? | Explanation depth, terminology, register |
| **Genre** | What conventions does this kind of document follow? | Organization, citation, formatting |
| **Channel** | Where will this appear? | Length, formatting, formality |
| **Relationship** | What is the social distance between writer and reader? | Politeness, directness, pronouns |
| **Consequence** | What happens if the reader misreads it? | Redundancy, precision, hedging |

If the writer has not supplied these, infer them from the text and say so when the inference matters. Do not silently impose a default.

---

## 2. Purpose

Purpose determines what counts as relevant.

- **To inform:** accuracy and completeness dominate; style should be invisible.
- **To instruct:** order and testability dominate; prose should be minimal.
- **To persuade:** evidence and framing dominate; repetition can be functional.
- **To record:** precision, dates, and attribution dominate; narrative is secondary.
- **To entertain:** voice, rhythm, and surprise dominate; information density can be low.
- **To request:** clarity of the ask and the deadline dominate; context is secondary.

An edit that improves elegance but weakens the purpose is a regression. See [../tests/regression-cases.md](../tests/regression-cases.md).

---

## 3. Audience

### Knowledge level
- **Novice:** define terms, give examples, avoid unexplained abbreviations.
- **Practitioner:** use standard terminology, skip basics, give edge cases.
- **Expert:** assume the field, focus on what is new or contested.
- **Mixed:** separate layers explicitly (summary, detail, appendix) rather than averaging.

### Role
A decision-maker reads for consequences and options. An operator reads for steps and failure modes. A reviewer reads for evidence and gaps. A learner reads for sequence and explanation. The same document can serve several roles only if the sections are visibly distinct.

### Reading conditions
A reader on a phone, in an interrupted session, or under time pressure needs shorter sections, clearer headings, and more repetition of key terms. A reader studying a text closely can handle longer paragraphs and more complex syntax.

### What not to assume
Do not assume the audience shares the writer's context, tools, or vocabulary. Do not assume they are hostile, either; defensive prose is its own failure.

---

## 4. Genre

Genre is a contract with the reader. It sets expectations about structure, evidence, length, and tone.

| Genre | Expected structure | Evidence norm | Register |
|---|---|---|---|
| Research article | IMRaD | Citations, statistics | Formal |
| Technical reference | Task- or object-oriented | Verified behavior | Neutral, precise |
| Tutorial | Sequential steps | Working examples | Direct, second person |
| Business memo | Decision, rationale, action | Internal data | Professional |
| News report | Inverted pyramid | Attribution | Neutral |
| Personal essay | Narrative or reflective | Experience | Variable |
| Legal contract | Defined terms, clauses | Statutory language | Highly formal |
| Chat message | Fragments acceptable | Shared context | Informal |

Deviating from genre conventions is allowed, but it costs the reader effort. Deviate deliberately, and signal it.

---

## 5. Channel

Channel constrains form more than most writers admit.

- **Print report:** headings, page numbers, captions, formal apparatus.
- **Web documentation:** scannable headings, short paragraphs, links, code blocks.
- **Email:** a subject line that states the action, a first sentence that states the purpose.
- **Chat:** short turns, minimal formatting, shared context assumed.
- **Slides:** one idea per slide, sparse text, speaker notes for detail.
- **Commit message:** imperative subject line, body explaining why.
- **Error message:** what failed, why, what to do.

A paragraph that works in a report may be unreadable in a chat window. Adapt length and formatting to the channel, not just the words.

---

## 6. Relationship and politeness

Social distance affects directness. The same request can be:

- **Peer to peer:** "Can you review this by Thursday?"
- **Subordinate to manager:** "Could you review this by Thursday, if you have time?"
- **Manager to subordinate:** "Please review this by Thursday."
- **External client:** "I would be grateful for your comments by Thursday."

None is more "natural" in general. Each fits a relationship. Editing toward a single directness level damages the ones it does not fit.

**Power and face.** A request imposes on the reader. Politeness markers acknowledge the imposition. Removing all of them can read as rude; adding too many can read as anxious or manipulative. Match the norm of the relationship.

---

## 7. Consequence and risk

The higher the cost of misreading, the more redundancy and precision are justified.

- **Low consequence (a blog post):** a slightly ambiguous sentence is tolerable.
- **Medium consequence (internal documentation):** ambiguity should be fixed, but some shorthand is acceptable.
- **High consequence (medical, legal, security, financial):** explicit conditions, defined terms, repeated warnings, and no stylistic experimentation.

In high-consequence writing, repetition is often a feature. A warning repeated at each point of use prevents harm. Do not "improve" it by consolidating.

---

## 8. Register

Register is the configuration of formality in a text. It is not a single scale from bad to good; it is a fit between text and situation.

**Formal register markers:** full forms, Latinate vocabulary, impersonal constructions, complex syntax, explicit structure.
**Informal register markers:** contractions, phrasal verbs, direct address, short sentences, shared references.

**Consistency rules.**
- Keep one register per section.
- Mark deliberate shifts ("In plain terms…").
- Do not mix ceremonial and casual language in the same paragraph unless the contrast is the point.

**Adaptation, not elevation.** A conversational message does not become better by becoming formal. A formal document does not become better by becoming chatty. Each becomes better by becoming clearer within its register.

---

## 9. Culture and convention

Writing conventions vary across communities and regions.

- **Directness:** some academic and professional cultures expect a thesis in the first paragraph; others build toward it.
- **Citation style:** APA, MLA, Chicago, IEEE, Vancouver, and house styles differ.
- **Spelling:** US, UK, Australian, and Canadian conventions differ (organize/organise, color/colour).
- **Date formats:** 03/04/2025 is ambiguous across regions; write the month or use ISO 8601.
- **Names and titles:** order, honorifics, and romanization vary.
- **Numbers:** decimal separators and digit grouping vary.

Do not "correct" a consistent regional convention into another. Match the document's declared style or the venue's.

---

## 10. Temporal context

Language changes, and so do facts.

- **Dated claims:** "currently," "recently," "soon," and "the latest version" decay. Prefer explicit dates and version numbers.
- **Model and tool references:** name versions where behavior differs.
- **Deprecated conventions:** what was standard five years ago may now be misleading.
- **Historical writing:** preserve period language when quoting; do not modernize a source silently.

When editing an older document, check whether its facts are still true before polishing its prose.

---

## 11. Multimodal context

Text rarely stands alone.

- **Code blocks:** must match the surrounding explanation and run as shown.
- **Tables:** captions and column headers carry meaning; do not edit cells into inconsistency.
- **Figures:** alt text and captions should state what to notice, not just what is shown.
- **Slides:** text supports speech; it should not duplicate the speaker's script.
- **Forms and UI:** labels, help text, and error messages form one system; terminology must match across them.

Editing one element without checking the others can create a contradiction that no sentence-level review will catch.

---

## 12. The adaptation matrix

Use this to decide how much to change when moving text between contexts.

| Change | Keep | Adjust |
|---|---|---|
| Report → executive summary | Findings, numbers, caveats | Length, structure, jargon |
| Documentation → tutorial | Facts, commands | Order, explanation depth, examples |
| Academic → general article | Evidence, attribution | Terminology, sentence length, hedging |
| Chat → email | The request, the facts | Greeting, context, formatting |
| Email → chat | The ask | Formality, salutation, sign-off |
| Blog → documentation | Explanation | Structure, precision, testability |

**Rule:** adapt the form, preserve the facts. When compression forces a choice, keep the qualifications and cut the framing.

---

## 13. Context failures and their symptoms

| Failure | Symptom | Repair |
|---|---|---|
| Wrong audience | Unexplained terms, or condescending basics | Rewrite for one audience; link for the other |
| Wrong genre | Missing expected sections; reader cannot navigate | Follow the genre template |
| Wrong channel | Long blocks in chat; fragments in a report | Reformat for the medium |
| Wrong register | Ceremonial email; casual contract | Choose one register and apply it |
| Wrong relationship | Over-familiar or distant tone | Match the social distance |
| Ignored consequence | Ambiguity in a high-stakes instruction | Add conditions and explicit warnings |
| Mixed audiences | Sections that serve no one | Separate layers explicitly |

---

## 14. Questions to ask before editing

1. Who is the reader, and what do they already know?
2. What must the reader do after reading?
3. What genre is this, and which conventions are non-negotiable?
4. Where will it be read, and on what device?
5. What happens if a sentence is misread?
6. What is the relationship between writer and reader?
7. Which register does the situation call for?
8. Which regional or institutional conventions apply?
9. Is any factual content time-sensitive?
10. Does the text coordinate with code, figures, or UI strings?

If the answer to any of these is unknown and material, ask the writer or state the assumption in the edit note. Do not guess silently.

Back to [SKILL.md](../SKILL.md).
