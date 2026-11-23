# Sentence Structure Analysis

Version 2.1.0 · Human Signal

This file explains how English sentences are built, what each structure is for, and how to recognize when a structure is helping or hurting comprehension. Grammatical correctness and preservation of meaning take priority over stylistic variation.

Related: [vocabulary-analysis.md](vocabulary-analysis.md) · [paragraph-analysis.md](paragraph-analysis.md) · [natural-language-principles.md](natural-language-principles.md) · [ai-writing-patterns.md](ai-writing-patterns.md)

**Convention used below:** *Original* examples show a problem; *Revised* examples show a possible fix. A revision is one valid option, not the only one.

---

## 1. Simple sentences

**Explanation.** A simple sentence contains one independent clause: one subject (which may be compound) and one finite verb. It can be long — "The team that owns billing rewrote the reconciliation job over the winter holidays" is still simple, because it has one independent clause.

**Linguistic purpose.** Simple sentences carry single propositions. They are the natural choice for definitions, instructions, conclusions, and any statement the reader must not misparse.

**Recognition criteria.** Count finite verbs that have their own subject. One such clause = simple sentence. Length is irrelevant.

**Correct usage.**
- "The migration is reversible." (single claim, high stakes)
- "Click **Save**, then restart the service." (two simple sentences in a sequence)

**Incorrect usage.**
- Using a simple sentence for a claim that needs a condition: "The cache is safe." (Safe when? Under what concurrency?)
- A string of simple sentences where the relations between them matter: "Latency rose. The cache expired. Requests hit the database." The reader must supply the causality.

**Original / Revised.**
- Original: "The parser rejects the file. The file has a BOM."
- Revised: "The parser rejects files that begin with a byte-order mark."

**Editing recommendations.**
- Keep simple sentences for rules, steps, and conclusions.
- If three consecutive simple sentences share a subject, consider combining them — not for variety, but because they describe one process.
- Never combine two independent claims with a comma (see §15).

---

## 2. Compound sentences

**Explanation.** A compound sentence joins two or more independent clauses with a coordinating conjunction (*and, but, or, nor, for, so, yet*) and usually a comma, or with a semicolon.

**Linguistic purpose.** Coordination places two ideas at the same grammatical level. It is right when the ideas are genuinely parallel in importance and when the reader needs to see them as a pair.

**Recognition criteria.** Two finite clauses, each able to stand alone, joined by a coordinator or semicolon.

**Correct usage.**
- "The write succeeds, but the index update is asynchronous." (two facts the reader must hold together)
- "Backups run nightly; restores are tested weekly." (paired operational facts)

**Incorrect usage.**
- Coordination of unequal ideas: "The datacenter flooded, and the team uses PostgreSQL." The two facts are not peers.
- Long chains of *and*: "The service reads the file, and it validates the schema, and it writes the rows, and it emits an event." This is a sequence, not a set of peers.

**Original / Revised.**
- Original: "The job retries failed uploads, and it logs each attempt, and it alerts after three failures."
- Revised: "The job retries failed uploads and logs each attempt; after three failures, it alerts."

**Editing recommendations.**
- Use *but* and *yet* only for real contrast, *so* only for real consequence.
- If a compound sentence has three or more clauses, check whether it is really a sequence or a list; restructure accordingly.
- Do not replace every *and* with a semicolon. The punctuation should reflect the relationship.

---

## 3. Complex sentences

**Explanation.** A complex sentence contains one independent clause and at least one dependent clause (relative, adverbial, or nominal).

**Linguistic purpose.** Subordination ranks information. It tells the reader which proposition is the main claim and which is background, condition, cause, or concession.

**Recognition criteria.** Look for a subordinator (*because, although, when, if, while, that, which, who*) attached to a clause that cannot stand alone.

**Correct usage.**
- "Because the token expires after 15 minutes, the client refreshes it before each batch." (cause → main clause)
- "The service, which runs in three regions, reconciles writes every 30 seconds." (nonrestrictive detail)

**Incorrect usage.**
- Subordinating the main point: "Although the migration succeeded, we found a data-loss bug." The reader expects the main clause to be the news; here the news is in the subordinate clause.
- Stacking three or more dependent clauses before the main clause: "When the job starts, if the queue is empty, and unless the lock exists, it exits." The reader must hold three conditions before learning the action.

**Original / Revised.**
- Original: "Although latency improved after the change, which was deployed on Tuesday, the error rate rose, which concerned the team."
- Revised: "The Tuesday change cut latency but raised the error rate, which concerned the team."

**Editing recommendations.**
- Put the main claim in the main clause.
- Limit preposed dependent clauses to one per sentence.
- Convert nominalizations inside dependent clauses to verbs where possible.

---

## 4. Compound-complex sentences

**Explanation.** A compound-complex sentence has at least two independent clauses and at least one dependent clause.

**Linguistic purpose.** It expresses a relationship among several propositions: for example, a condition, two consequences, and a contrast. Used well, it compresses a small argument into one sentence.

**Recognition criteria.** Two or more finite independent clauses plus at least one subordinate clause.

**Correct usage.**
- "If the write succeeds but the index update fails, the job retries the index step only, and the client sees success after both complete."

**Incorrect usage.**
- Overloading: "If the cache is cold and the database is under load, the request queues, but because the timeout is short, it fails, and the user retries, which adds more load." Four propositions and two causal chains in one sentence. Split it.
- Unclear attachment: "The service retries when the network fails and the queue is full, which alerts the operator." What does *which* refer to?

**Original / Revised.**
- Original: "When the queue fills, producers block, and consumers slow down, so latency rises, and the dashboard turns red, which pages the on-call engineer."
- Revised: "When the queue fills, producers block and consumers slow down, so latency rises. The dashboard pages the on-call engineer when p95 exceeds two seconds."

**Editing recommendations.**
- One causal chain per sentence.
- Keep each independent clause short enough to parse on first read.
- If a sentence needs a diagram to understand, split it.

---

## 5. Sentence-length variation

**Explanation.** Sentence length is the number of words (or clauses) between capital and period. Variation is the natural result of different information loads.

**Linguistic purpose.** Length controls pace and emphasis. A short sentence after a long one lands hard; a long sentence slows the reader down for a complex relationship.

**Recognition criteria.** Count words per sentence across a paragraph. Also note the *distribution*: many mid-length sentences with no short or long ones produces a flat rhythm.

**Correct usage.**
- Long sentence to establish a mechanism, short sentence to state the consequence.
- A short sentence for a decision, a long one for its justification.

**Incorrect usage.**
- Uniform length: nineteen sentences of 17–22 words. Reads as a list of equivalent facts.
- Mechanical alternation: every paragraph ends with a four-word sentence for "punch."
- Artificial choppiness: splitting a single idea into three fragments to create drama (see §12).

**Original / Revised.**
- Original: "The migration ran. It took six hours. It moved 4.2 million rows. It encountered no errors. It completed successfully."
- Revised: "The migration moved 4.2 million rows in six hours without errors."

**Editing recommendations.**
- Merge sentences that share a subject and describe one event.
- Split sentences that contain more than one main claim.
- Do not add short sentences for rhythm alone. Add them when a conclusion or decision deserves its own line.

---

## 6. Clause distribution

**Explanation.** Clause distribution describes where clauses sit in a sentence: before the main clause, after it, or nested inside it.

**Linguistic purpose.** Position signals information status. Initial position is natural for context and conditions; final position is natural for new information and emphasis; medial position is natural for identifying detail.

**Recognition criteria.** Mark each clause and its function. Then check whether its position matches its function.

**Correct usage.**
- Condition first: "If the lock is held, the worker exits."
- New information last: "The worker exits if another process holds the lock."
- Identifying detail adjacent to its noun: "The table that stores sessions is partitioned by month."

**Incorrect usage.**
- New information buried mid-sentence: "The worker, if another process holds the lock, which happens during deploys, exits."
- Conditions after the consequence when the consequence is uninterpretable without them: "The job stops after three failures unless retries are disabled." (Is the default retries enabled? The sentence is ambiguous.)

**Original / Revised.**
- Original: "The endpoint returns 429, when the bucket is empty, to the caller."
- Revised: "When the bucket is empty, the endpoint returns 429 to the caller."

**Editing recommendations.**
- Put conditions before the action they govern.
- Keep relative clauses next to the noun they modify.
- Avoid interrupting subject and verb with more than a short phrase.

---

## 7. Subject placement

**Explanation.** The grammatical subject is the entity the sentence says something about. Its position — first, delayed, or displaced by an expletive — shapes how quickly the reader finds the topic.

**Linguistic purpose.** Early subjects help the reader attach the sentence to what they already know. Delayed subjects create suspense or emphasis, but cost comprehension.

**Recognition criteria.** Underline the subject of each main clause. Check for expletives (*there is, it is*) and long pre-subject frames.

**Correct usage.**
- "The retry policy caps attempts at three." (subject first)
- "Only after the third failure does the circuit open." (fronted adverbial for emphasis; subject delayed deliberately)

**Incorrect usage.**
- Empty subjects: "There are several reasons why the build fails."
- Frame before subject: "When it comes to deployment frequency, the team ships daily."
- Subject separated from verb: "The service, after the migration and the configuration change and the restart, failed."

**Original / Revised.**
- Original: "There are three settings that control how the cache behaves."
- Revised: "Three settings control the cache: `ttl`, `max_bytes`, and `eviction_policy`."

**Editing recommendations.**
- Prefer the real topic as the subject.
- Delete expletive constructions unless they introduce genuinely new information.
- Keep subject and verb within a few words of each other.

---

## 8. Verb selection

**Explanation.** The verb carries the sentence's action and much of its precision. Strong verb choice reduces the need for adverbs, nominalizations, and supporting phrases.

**Linguistic purpose.** Verbs determine argument structure: who does what to whom. A precise verb encodes the relationship without extra words.

**Recognition criteria.** For each sentence, name the action. If the action is in a noun ("make a decision," "perform an analysis"), the verb is weak. If the verb is generic (*do, make, have, perform, utilize*), check whether a specific verb exists.

**Correct usage.**
- "The worker **drains** the queue before shutdown." (precise action)
- "The migration **rewrites** foreign keys in place." (specific mechanism)

**Incorrect usage.**
- Light verbs: "We **made** a **decision** to **perform** a **migration**."
- Nominalized actions: "The **implementation** of the **validation** occurs at startup."
- Vague verbs: "The system **handles** errors." (retries? logs? crashes? ignores?)

**Original / Revised.**
- Original: "The team carried out an evaluation of the proposal and came to the conclusion that it should be implemented."
- Revised: "The team evaluated the proposal and recommended implementing it."

**Editing recommendations.**
- Convert nominalizations to verbs.
- Replace *handle*, *manage*, *process*, *support* with the specific operation when the specific operation is known.
- Keep the verb's tense and aspect consistent with the timeline.

---

## 9. Active voice

**Explanation.** In active voice, the grammatical subject performs the action: "The scheduler **dispatches** the job."

**Linguistic purpose.** Active voice is direct, shorter, and identifies the actor. It is the default in instructions, explanations of mechanism, and most prose.

**Recognition criteria.** Ask "who does the action?" If the answer is the grammatical subject, the clause is active.

**Correct usage.**
- "The client **sends** a heartbeat every 30 seconds."
- "**Run** the migration before deploying." (imperative, inherently active)

**Incorrect usage.**
- Active voice with a vague actor: "The system **does** the validation." (Which component? When?)
- Active voice that invents an actor to satisfy a style rule: "The parser **decides** to reject the file" when the rejection is actually a configured policy.

**Original / Revised.**
- Original: "The validation is performed by the service."
- Revised: "The service validates the payload before writing it."

**Editing recommendations.**
- Prefer active when the actor is known and relevant.
- Do not convert to active if doing so requires inventing an actor.
- Keep the actor consistent across a procedure so the reader can track responsibility.

---

## 10. Passive voice

**Explanation.** In passive voice, the grammatical subject receives the action: "The job **was dispatched** by the scheduler."

**Linguistic purpose.** Passive voice is correct when:
- the actor is unknown or irrelevant ("The backup was deleted");
- the object is the topic and the actor is secondary ("The index is rebuilt nightly");
- the genre expects impersonal framing (lab reports, specifications);
- the actor is deliberately withheld for confidentiality.

**Recognition criteria.** A form of *be* or *get* plus a past participle, often with a *by* phrase.

**Correct usage.**
- "The table is partitioned by month." (the table is the topic; the partitioner is irrelevant)
- "Samples were stored at −80 °C." (standard methods register)

**Incorrect usage.**
- Hiding responsibility: "Mistakes were made."
- Long passive chains: "The configuration is loaded by the service, which is started by the supervisor, which is managed by systemd."
- Passive where the actor matters: "The flag was removed." (Who removed it? When? Why?)

**Original / Revised.**
- Original: "The cache is invalidated by the writer after each update."
- Revised: "The writer invalidates the cache after each update."

**Editing recommendations.**
- Keep passive when the actor is unknown, irrelevant, or already established.
- Convert to active when the reader needs to know who is responsible.
- Do not treat passive as an error by itself. It is a common, correct English structure.

---

## 11. Parallel construction

**Explanation.** Parallel construction gives items in a list or comparison the same grammatical form.

**Linguistic purpose.** Parallelism signals that items belong to one set and makes them easy to compare and scan.

**Recognition criteria.** Check the form of each item: all nouns, all gerunds, all infinitives, all clauses with the same shape. Check that the shared element actually applies to every item.

**Correct usage.**
- "The job validates input, writes rows, and emits events." (three verbs)
- "Choose a queue that is durable, that retries, and that supports priorities." (three relative clauses)

**Incorrect usage.**
- Mixed forms: "The job validates input, writes rows, and event emission."
- Faulty parallelism with a shared preposition: "We investigated the cause of the outage, the backup policy, and why restores were slow." (The preposition applies awkwardly to a clause.)
- False parallelism that implies equivalence: "The update improves speed, reliability, and user interface." (Two properties and one component.)

**Original / Revised.**
- Original: "The tool is fast, has good documentation, and people like using it."
- Revised: "The tool is fast, well documented, and pleasant to use."

**Editing recommendations.**
- Make list items the same part of speech.
- Ensure each item is logically on the same level.
- Parallelism is not required in every sentence; it is required when the reader is meant to compare items.

---

## 12. Sentence fragments

**Explanation.** A fragment lacks a subject, a finite verb, or an independent clause. In formal prose it is usually an error; in some genres it is a deliberate device.

**Linguistic purpose.** Intentional fragments create emphasis, mimic speech, or compress labels ("Faster. Cheaper. Simpler."). They work when the missing material is obvious and the rhythm supports the omission.

**Recognition criteria.** Can the group of words stand alone as a sentence? If not, is the omission intentional and controlled?

**Correct usage.**
- Advertising and headlines: "Smaller. Lighter. Faster."
- Narrative emphasis: "Then silence."
- Documentation labels: "**Required.**"

**Incorrect usage.**
- Accidental fragments in reports: "Because the cache expired. The request failed." (The first is a dependent clause punctuated as a sentence.)
- Fragment chains substituting for analysis: "The migration failed. Again." repeated as a stylistic tic.
- Fragments in formal academic prose where the genre expects full sentences.

**Original / Revised.**
- Original: "The team shipped on time. Despite the outage. And the missing tests."
- Revised: "The team shipped on time despite the outage and the missing tests."

**Editing recommendations.**
- Fix unintentional fragments by attaching them to the clause they depend on.
- Keep deliberate fragments only in genres that support them, and only when the emphasis is earned.
- Never use fragments to avoid stating a relationship.

---

## 13. Coordination

**Explanation.** Coordination joins elements of equal grammatical status using *and, but, or, nor, for, so, yet* (and correlatives *either…or, not only…but also*).

**Linguistic purpose.** Coordination says: these items are peers. It is the correct structure for parallel facts, alternatives, and joint conditions.

**Recognition criteria.** Identify the joined elements. Confirm they are the same category (clauses with clauses, nouns with nouns) and the same logical level.

**Correct usage.**
- "The endpoint accepts JSON or XML."
- "Either the lock is stale, or the worker crashed."

**Incorrect usage.**
- Coordinating a cause and an effect as peers: "The disk filled, and the job failed." The second is a consequence; subordination makes the relation clear: "The job failed because the disk filled."
- Correlative mismatch: "Not only did the build fail, but also the tests were slow." (The second element is not parallel to the first.)
- Ambiguous *or*: "Restart the service or contact support." (exclusive or inclusive? in what order?)

**Original / Revised.**
- Original: "The queue overflowed, and the producer blocked, and the client timed out."
- Revised: "When the queue overflowed, the producer blocked, and the client timed out."

**Editing recommendations.**
- Use coordination for peers, subordination for hierarchy.
- Keep correlative pairs grammatically parallel.
- Clarify *or* when the choice matters.

---

## 14. Subordination

**Explanation.** Subordination places one clause inside another's grammatical structure, marking it as background, cause, condition, concession, or complement.

**Linguistic purpose.** Subordination encodes logical hierarchy. It tells the reader which claim is primary and which qualifies it.

**Recognition criteria.** Look for subordinators: *because, since, although, while, if, unless, when, after, before, so that, which, who, that*.

**Correct usage.**
- Cause: "Because the token expired, the request returned 401."
- Concession: "Although the cache was warm, latency rose."
- Purpose: "The job backs off so that retries do not amplify load."

**Incorrect usage.**
- Main claim buried: "Although we fixed the leak, memory use still grows." (The news is the second clause; it should be main.)
- Ambiguous subordinator: "The job runs after the backup completes or fails." (Does it run in both cases? Only after success?)
- Over-subordination: four levels of nesting in one sentence.

**Original / Revised.**
- Original: "Since the service, which was deployed on Tuesday, had a bug that caused retries, which increased load, we rolled back."
- Revised: "We rolled back the Tuesday deploy because a retry bug increased load."

**Editing recommendations.**
- Put the primary claim in the main clause.
- Limit nesting to two levels.
- Replace vague subordinators (*as, while*) with precise ones when the relation matters.

---

## 15. Punctuation patterns

**Explanation.** Punctuation marks grammatical and rhetorical relationships. The marks most often involved in quality problems are the comma, semicolon, colon, dash, and parentheses.

**Linguistic purpose.**

| Mark | Primary job |
|---|---|
| Comma | Separates items, marks nonrestrictive material, joins clauses with a coordinator |
| Semicolon | Joins closely related independent clauses; separates complex list items |
| Colon | Introduces an explanation, list, or quotation; signals "namely" |
| Em dash | Marks an interruption or an emphatic aside |
| Parentheses | Marks material that is supplementary and can be skipped |
| Period | Ends a statement; the strongest separator |

**Recognition criteria.** For each mark, ask what relationship it encodes. If removing the mark leaves the relationship unchanged and the sentence still grammatical, the mark may be decorative.

**Correct usage.**
- "The retry failed; the circuit opened." (related independent clauses)
- "One setting matters: `max_retries`." (colon introduces the specification)
- "The service — a single binary — starts in 40 ms." (parenthetical aside)

**Incorrect usage.**
- Comma splice: "The cache expired, the request hit the database."
- Semicolon between unrelated statements: "The cache expired; the team uses PostgreSQL."
- Colon without an explanation following: "The results were: we shipped."
- Dash overload: three dashes in one paragraph, each introducing a different kind of aside.
- Parentheses nested inside parentheses.

**Original / Revised.**
- Original: "The migration is risky, it touches 40 tables, we tested it twice."
- Revised: "The migration is risky: it touches 40 tables, and we tested it twice."

**Editing recommendations.**
- Prefer the period when in doubt; short sentences are rarely wrong.
- Use a colon only when what follows explains or specifies what precedes.
- Keep one dash construction per paragraph at most.
- Match punctuation to the genre's style guide (serial comma, dash spacing).

---

## 16. Syntactic repetition

**Explanation.** Syntactic repetition is the reuse of a sentence pattern. It can be a deliberate rhetorical device (anaphora, parallelism) or an unintended habit.

**Linguistic purpose.** Deliberate repetition creates rhythm, emphasis, and memorability. Unintended repetition makes prose feel mechanical and can hide weak logic, because every idea is forced into the same frame.

**Recognition criteria.** Compare the skeletons of consecutive sentences, not their words. If three or more share the same opening, clause order, or closing pattern, examine whether the content justifies it.

**Correct usage.**
- Anaphora: "We tested the parser. We tested the scheduler. We tested the queue."
- Parallel definitions: "A token authenticates a request. A session persists one."
- Repeated frame for contrast: "The old job retried on failure. The new job retries on timeout."

**Incorrect usage.**
- Template prose: every paragraph built as "X is not Y; it is Z."
- Repeated openings: "The system… The system… The system…"
- Repeated closers: every paragraph ending with "…which is why this matters."

**Original / Revised.**
- Original: "The service is fast. The service is reliable. The service is secure."
- Revised: "The service answers in 40 ms, stays within its error budget, and encrypts data at rest."

**Editing recommendations.**
- Keep repetition when it marks a real parallel or builds deliberate emphasis.
- Break the frame when the content's relationships differ.
- Do not replace repetition with synonyms merely to avoid it; see [vocabulary-analysis.md](vocabulary-analysis.md).

---

## Diagnostic summary

| Symptom | Likely structural cause | First fix to try |
|---|---|---|
| Reader loses the main point | Main claim in a subordinate clause | Promote it to the main clause |
| Sentence feels endless | Three or more preposed clauses, or two causal chains | Split; keep one chain per sentence |
| Paragraph feels flat | Uniform sentence length and shape | Merge shared-subject sentences; split multi-claim ones |
| Text feels choppy | Fragment chains or very short sentences for effect | Restore full clauses; keep short sentences for real conclusions |
| Ambiguous responsibility | Passive voice with a relevant actor | Name the actor or keep passive deliberately |
| List is hard to scan | Mixed grammatical forms | Make items parallel |
| Punctuation feels busy | Dashes, semicolons, and colons used decoratively | Prefer periods; use marks for specific relations |
| Prose sounds templated | Repeated syntactic frame | Vary only where the content's logic differs |

Back to [SKILL.md](../SKILL.md).
