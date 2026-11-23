# Paragraph Analysis

Version 2.1.0 · Human Signal

A paragraph is a unit of thought with a boundary. This file explains how to judge whether that unit is doing its job: whether it has a topic, whether its support is relevant, whether its order helps the reader, and whether its boundaries fall in the right places.

Related: [sentence-structure.md](sentence-structure.md) · [natural-language-principles.md](natural-language-principles.md) · [vocabulary-analysis.md](vocabulary-analysis.md) · [ai-writing-patterns.md](ai-writing-patterns.md)

---

## 1. Topic sentence relevance

**Definition.** The topic sentence states what the paragraph is about and, usually, what it claims about that topic.

**What good looks like.** The topic sentence is specific enough to be arguable or informative, and the rest of the paragraph supports it. It often appears first in explanatory prose, but it can appear last in narrative or argumentative prose where the evidence leads to the claim.

**Recognition criteria.**
- Read only the first sentence. Can you predict what the paragraph will contain?
- Read only the rest. Can you infer the topic sentence?
- If both answers are yes and they match, the paragraph is well focused.

**Common problems.**
- **Topic-less paragraph:** a sequence of facts with no stated connection. The reader must infer the point.
- **Topic sentence that announces instead of claims:** "This section discusses performance." That names a topic but makes no assertion, so the paragraph has no direction.
- **Topic sentence that overpromises:** "Performance improved across every dimension," followed by evidence about one dimension.

**Editing action.** Write the claim the paragraph actually supports, then either use it as the topic sentence or revise the paragraph to support the claim you intended.

**Exceptions.** Narrative paragraphs often delay the topic sentence for effect. Reference entries may have no topic sentence at all, because the heading supplies the topic.

## 2. Supporting information

**Definition.** The evidence, explanation, example, or detail that justifies the paragraph's claim.

**What counts as support.**
- **Data:** measurements, counts, dates, versions.
- **Mechanism:** how something works, step by step.
- **Example:** a specific case that demonstrates the claim.
- **Authority:** a cited source, with the specific finding it supports.
- **Comparison:** a contrast that clarifies the claim.
- **Consequence:** what follows if the claim is true.

**Recognition criteria.** For each supporting sentence, ask: *what claim does this support, and how?* If the link requires a leap, the support is weak or the claim is too strong.

**Common problems.**
- **Assertion stacking:** several claims, no evidence.
- **Evidence without a claim:** data presented with no interpretation, so the reader does not know what to conclude.
- **Irrelevant support:** interesting detail that does not bear on the claim.
- **Circular support:** the evidence restates the claim.

**Editing action.** Add the missing link between claim and evidence. If the evidence does not support the claim, weaken the claim or find better evidence.

## 3. Evidence integration

**Definition.** The way evidence is introduced, attributed, interpreted, and connected to the argument.

**What good integration looks like.**
1. The evidence is introduced with enough context to interpret it.
2. The source and its limits are clear.
3. The writer says what the evidence shows.
4. The connection to the paragraph's claim is explicit.

**Weak integration patterns.**
- **Drop-in quote:** a quotation with no framing, leaving the reader to infer its relevance.
- **Citation as decoration:** a citation that does not support the specific sentence it follows.
- **Evidence dump:** several findings in a row with no synthesis.
- **Over-claiming:** "This proves…" where the evidence only suggests.

**Example.**
- Weak: "Response times increased. (Smith 2021)"
- Better: "Smith (2021) measured a 40% increase in response time after the cache was disabled, which suggests the cache was absorbing most read traffic in that deployment."

**Editing action.** For each piece of evidence, write one sentence stating what it shows. If you cannot, the evidence is not integrated.

## 4. Logical transitions

**Definition.** The words, phrases, and sentence structures that signal relationships between paragraphs.

**Types of relation.** Addition, contrast, cause, consequence, example, concession, sequence, specification, summary.

**What good transitions do.** They encode a real relation and can be removed without breaking the logic when the relation is already clear. They do not merely announce that a new paragraph has begun.

**Recognition criteria.**
- Name the relation between paragraph N and paragraph N+1.
- Check whether the transition names that relation.
- Check whether the relation is real (does the next paragraph actually contrast, or does it continue?).

**Common problems.**
- **Transition inflation:** every paragraph starts with a connector, including paragraphs that simply continue.
- **Wrong relation:** "However" where the next paragraph adds a supporting point.
- **Missing relation:** a sharp turn with no signal, leaving the reader to reconstruct the logic.

**Editing action.** Prefer content-based transitions (repeat a key term from the previous paragraph, state the consequence) over label-based ones. Use explicit connectors when the relation is easy to miss.

## 5. Paragraph boundaries

**Definition.** The points at which one paragraph ends and another begins.

**What a boundary signals.** A change of topic, a change of function (claim → evidence → implication), a change of time or place, or a deliberate pause for emphasis.

**Recognition criteria.** At each boundary, ask: *what changed?* If nothing changed, the boundary is arbitrary. If something changed but the boundary is missing, the paragraph is doing two jobs.

**Common problems.**
- **Boundary by length:** new paragraph every four sentences regardless of content.
- **Missing boundary:** a paragraph covering two distinct claims, so neither gets emphasis.
- **Boundary after a single sentence:** a one-line paragraph for drama, used repeatedly.
- **Boundary inside a list:** splitting a list across paragraphs without a reason.

**Editing action.** Place boundaries where the job changes. Then check that each resulting paragraph can be summarized in one sentence.

## 6. Paragraph length

**Definition.** The number of sentences or words between boundaries.

**What length communicates.** Length is a visual cue for weight and complexity. A long paragraph says "this is one sustained idea"; a short paragraph says "this is a distinct point" or "this is a pause."

**Guidance, not rules.**
- **Short paragraphs (1–3 sentences)** suit web content, instructions, and emphasis. Overused, they fragment the argument.
- **Medium paragraphs (4–7 sentences)** suit most explanatory and professional prose.
- **Long paragraphs (8+ sentences)** suit sustained analysis, legal reasoning, and literary prose. They require strong internal cohesion, or the reader loses the thread.

**Recognition criteria.** Compare paragraph length with the weight of the idea. If minor points get as much space as major ones, the lengths are not doing their job.

**Common problems.**
- **Uniform length:** every paragraph is five sentences, so nothing looks more important than anything else.
- **Wall of text:** a 300-word paragraph with three topics.
- **Confetti paragraphs:** every sentence its own paragraph, so nothing connects.

**Editing action.** Let the idea determine the length. Split when the topic changes; merge when several short paragraphs develop one point.

## 7. Information density

**Definition.** The amount of new, relevant information per sentence in a paragraph.

**Why it matters.** Low density means the paragraph takes more reading time than its content justifies. High density can be efficient, but if it exceeds the reader's processing capacity, comprehension drops.

**Signs of low density.**
- Frames and restatements ("In other words…", "As mentioned earlier…").
- Obvious consequences spelled out.
- Repeated claims in different words.
- Generic examples that add no new case.

**Signs of excessive density.**
- Multiple claims per sentence with unclear attachment.
- Unexplained abbreviations.
- Missing connectives between steps.
- Assumed background the audience does not have.

**Editing action.** Cut filler first. If the paragraph is still dense, split it and add the missing logical links — not more words, but the right ones.

## 8. Cohesion

**Definition.** The surface links that make sentences read as a unit (see [natural-language-principles.md](natural-language-principles.md) §4).

**Devices.**
- Pronoun and demonstrative reference.
- Lexical repetition of key terms.
- Synonymy and generalization.
- Connectors.
- Parallel structure.
- Given-new ordering.

**Recognition criteria.** Cover each sentence in turn and ask how it connects to the previous one. If the connection is only "it is also about the topic," cohesion is weak.

**Common problems.**
- **Ambiguous reference:** "This shows…" with no clear referent.
- **Synonym drift:** the same entity named three different ways, so the reader suspects three entities.
- **Connector dependence:** cohesion carried entirely by *however* and *therefore*, with no lexical links.
- **Over-cohesion:** every sentence explicitly linked, so the prose feels mechanical.

**Editing action.** Strengthen lexical links (repeat the key noun) before adding connectors. Remove connectors that duplicate a link already made by the content.

## 9. Coherence

**Definition.** Whether the paragraph's ideas belong together and form a coherent whole.

**Cohesion vs. coherence.** Cohesion is how sentences are linked. Coherence is whether they should be linked at all. A paragraph can be perfectly cohesive and still incoherent: "The build is reproducible. Reproducible builds require pinned dependencies. Pinned dependencies slow updates. Slow updates frustrate developers. Developers prefer faster tools." Each sentence links to the last, but the paragraph has no single point.

**Recognition criteria.** Summarize the paragraph in one sentence. If the summary requires "and also," the paragraph may be incoherent or may need splitting.

**Editing action.** Identify the one claim the paragraph supports. Move or delete material that supports a different claim. If both claims matter, split the paragraph and add a transition that states their relation.

## 10. Redundancy

**Definition.** Content that repeats information already present without adding function.

**Types.**
- **Verbal redundancy:** saying the same thing twice in different words.
- **Structural redundancy:** a summary that repeats the section, a heading that repeats the title.
- **Evidential redundancy:** the same evidence cited twice for the same claim.
- **Definitional redundancy:** defining a term and then explaining the definition.

**When repetition is functional.**
- A key term repeated to maintain topic tracking.
- A safety warning repeated at the point of use.
- A summary that serves readers who skip sections, when it adds a decision or implication.
- Deliberate rhetorical repetition.

**Recognition criteria.** Remove the candidate. Does the reader lose information, orientation, or safety? If not, it was redundant.

**Editing action.** Delete verbal and structural redundancy. Keep functional repetition and mark it as intentional.

## 11. Argument progression

**Definition.** The order in which claims, evidence, and conclusions are presented.

**Common progressions.**
- **Claim → evidence → implication** (most explanatory prose).
- **Problem → cause → options → recommendation** (technical and business writing).
- **Question → method → result → interpretation** (research).
- **Chronological** (narrative, procedures, incident reports).
- **General → specific → general** (essays and introductions).

**Recognition criteria.** Outline the paragraph (or section) by function. Does each step depend on the previous one? Does the conclusion follow from what precedes it?

**Common problems.**
- **Premature conclusion:** the recommendation appears before the evidence.
- **Buried lede:** the main finding appears at the end of a long setup.
- **Circular progression:** the argument returns to its starting point without advancing.
- **Orphan evidence:** data that never connects to a claim.

**Editing action.** Choose one progression and follow it. If the genre has a conventional order (IMRaD, incident timeline), follow it unless there is a reason not to.

## 12. Explanatory structure

**Definition.** The internal pattern used to explain a concept, mechanism, or procedure.

**Useful patterns.**
- **Definition → mechanism → example → boundary** (concepts).
- **Goal → steps → verification → failure modes** (procedures).
- **Observation → explanation → alternative explanations → conclusion** (analysis).
- **Principle → application → exception** (guidance).

**Recognition criteria.** Ask what the reader needs next. If the paragraph supplies it, the structure is working. If the pattern is the same in every section regardless of content, it is a template.

**Common problems.**
- **Definition-only:** explains what something is but never how it works.
- **Example-first:** uses an example before the reader knows what it illustrates.
- **Missing boundary:** explains when something works but not when it fails.
- **Template drift:** forcing a comparison section into a definition-example shape.

**Editing action.** Match the structure to the reader's next question. See AWP-110.

## 13. Contextual relevance

**Definition.** The degree to which a paragraph serves the document's stated purpose and audience.

**Recognition criteria.**
- Does the paragraph help the reader decide, do, verify, or understand something they came for?
- Would the document be worse without it? (If not, consider cutting.)
- Does it belong in this section, or in an appendix, a sidebar, or another document?

**Common problems.**
- **Interesting aside:** relevant to the writer's curiosity, not the reader's task.
- **Scope creep:** a paragraph that expands the document's subject without warning.
- **Audience mismatch:** detail for experts in a beginner guide, or background for beginners in a reference manual.

**Editing action.** Keep what serves the purpose. Move useful but secondary material to an appendix or a separate document. Cut what serves neither.

## 14. Reader expectations

**Definition.** The conventions and patterns a reader brings to a genre.

**What readers expect.**
- **Documentation:** prerequisites, steps, verification, errors.
- **Research:** question, method, result, limitation.
- **Business memos:** decision, rationale, cost, next step.
- **Narratives:** a situation, a complication, a resolution.
- **Reference entries:** parameters, returns, examples.

**Why it matters.** Violating expectations is not always wrong, but it costs the reader effort. A reference page written as an essay will be harder to use even if it is well written.

**Recognition criteria.** Compare the document with two competent examples in the same genre. Note the structural features they share. If the document omits one, decide whether the omission is deliberate.

**Editing action.** Meet the genre's expectations first, then improve the prose. Do not impose a universal structure on every genre.

---

## When to use short paragraphs, long paragraphs, lists, and headings

### Short paragraphs
**Use when:** each point is distinct; the reader is scanning; a decision or warning needs emphasis; the channel is a screen.
**Avoid when:** every sentence becomes a paragraph, so relationships disappear.

### Long paragraphs
**Use when:** one idea requires sustained development; the genre expects continuous argument (law, literary criticism, some academic prose); the evidence needs to be held together.
**Avoid when:** the paragraph contains more than one topic, or the reader is likely to be interrupted.

### Lists
**Use when:** items are parallel, independent, and meant to be scanned or checked; the order matters (numbered); each item is short enough to read as a unit.
**Avoid when:** items depend on each other for meaning; the list has one item; the items are long explanations; a table would compare attributes better.

### Headings
**Use when:** the document is long enough to need navigation; sections have distinct topics; readers will jump between sections.
**Avoid when:** the document is short; headings would outnumber paragraphs; the heading merely restates the title; a heading breaks a single argument into artificial pieces.

### Tables
**Use when:** several items share the same attributes and the reader needs to compare them.
**Avoid when:** the content is prose with one or two attributes; the table would have many empty cells; the relationships are causal rather than comparative.

---

## Paragraph diagnostic sequence

1. **Summarize** the paragraph in one sentence. If you cannot, it is doing too much.
2. **Locate the claim.** Is it stated, implied, or missing?
3. **Check the support.** Does each sentence support the claim? How?
4. **Check the order.** Does each sentence depend on the previous one?
5. **Check the links.** Are references clear? Are key terms repeated?
6. **Check the boundaries.** Does the paragraph start and end where the topic changes?
7. **Check the length.** Does the space match the weight?
8. **Check the genre.** Would a competent example in this genre look like this?

Back to [SKILL.md](../SKILL.md).
